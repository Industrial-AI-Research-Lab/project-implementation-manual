# Repository and Code Work — Student Guide

This guide sets up a repository the supervisor can run from a fresh clone, pull requests as the record of your work, a decision log, and experiments recorded in MLflow. Apply it from the first week; the list at the end is what the supervisor checks at each checkpoint.

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| Pull request (PR), Draft, Ready for review | A PR proposes a change from a branch into `main`, with a description and a review thread. Draft marks it unfinished; Ready for review requests the reviewer. | A draft cannot be merged and requests no review. Remove Draft only when the work is done. |
| CODEOWNERS | The file `.github/CODEOWNERS` maps paths to reviewers; GitHub requests them when a PR becomes Ready for review. | One line `* @<supervisor>` makes the supervisor the reviewer of every PR. It works only after the file is merged into `main`. |
| Ruleset, branch protection | Repository settings that block direct pushes to `main` and require a PR, an approval, resolved threads, or green checks. | Free on a public repository; on a private one only on a paid plan. Without it the rules hold by agreement. |
| ADR, decision log, statuses | An architecture decision record is one file per decision: context, options, decision, consequences. The folder is the decision log. Statuses: proposed, accepted, rejected, superseded. | An accepted record is never edited; a change is a new record that supersedes the old one. |
| Tracking server, backend store, artifact store | MLflow parts: the server receives runs; the backend store keeps params, metrics and tags in a database; the artifact store keeps files, models, plots and configs, for example in an S3-compatible storage such as MinIO. | Locally the file `mlflow.db` is the backend store and artifacts land in a folder; a shared server of the lab has all three set up. |
| Experiment, run, param, metric, artifact, tag | MLflow vocabulary: an experiment groups runs; a run is one execution with params (inputs), metrics (numbers over time), artifacts (files) and tags (labels, including the commit). | Every number in your results table must name the run that produced it. |
| `.env`, `.env.example`, environment variable | Configuration that differs between machines (paths, endpoints, keys) lives in environment variables. `.env` holds them locally and is ignored; `.env.example` lists the keys with placeholders and is committed. | The supervisor copies `.env.example` to `.env`, fills it in and runs the project. |
| Repository secret, environment secret | Encrypted values for GitHub Actions. Repository secrets can be created by a collaborator; environment secrets only by the owner. | Credentials that CI needs go there, never into a workflow file or a PR. |
| pre-commit hook, VCS hook, agent hook | Three mechanisms share the word: pre-commit runs checks before a commit, configured in `.pre-commit-config.yaml`; a bare VCS hook is a script in `.git/hooks`; an agent hook runs a command at a step of an LLM assistant's work. | This guide uses pre-commit and the agent hook; both run the same `make check`. |
| Lock file (`uv.lock`) | The exact version of every dependency resolved for the project. | Commit it. CI installs from it with `uv sync --locked`, so a run tied to a commit can be re-run. |
| Harness, LLM harness | The environment an LLM assistant works in: its instruction files, permissions, hooks and the checks they run. | The harness runs `make check` after edits, so the assistant cannot leave the repository red. A separate guide on agent artifacts covers it. |

## Repository and access

- The repository lives in your personal account. Transfer it to the lab organisation only when the code is needed in a lab project.
- The supervisor is a collaborator with write access and an Admin of your GitHub Project. A personal repository has no other roles, so the owner-only actions stay with you and you do them on request: visibility, rulesets, merging CODEOWNERS and the PR template, environment secrets, transfer.
- Visibility is your choice. Recommended: public, unless the data or intellectual property forbids it. Visibility decides what the platform can enforce:

| Enforced by the platform | Public, Free | Private, Free |
|---|---|---|
| Rulesets: PR required, approval, resolved threads, green checks | yes | no |
| Review from code owners | yes | no |
| Secret scanning and push protection | yes | no |
| Draft PRs, review requests via CODEOWNERS, Actions minutes | yes | yes, 2 000 minutes a month |

- On a private repository the same rules hold by agreement; CI is the only automatic gate there.
- Keep a full local clone and a second remote, an institutional GitLab or another forge: access to the platform can be intermittent, and the supervisor runs exactly a fresh clone.

## Layout and what never enters the repository

```
README.md  .env.example  pyproject.toml  uv.lock  Makefile
.github/          pull_request_template.md, CODEOWNERS, workflows/
src/<package>/    code that is imported and tested
notebooks/        exploration; outputs may stay as a report of a result
docs/adr/         decision log
configs/          experiment configs
data/             ignored; at most a tiny labelled sample
results/          tables and figures exported from code
```

- README is the entry point: purpose, `cp .env.example .env`, `uv sync`, `make check`, the command that runs one experiment, where the data lives, links to the decision log and the Project. It must work from a fresh clone.
- Commit `uv.lock`; CI installs with `uv sync --locked`; run `uv lock --check` before opening a PR.
- Never commit secrets and `.env`, raw data, model weights, files over a few tens of MB, generated logs. Data and artifacts live in MLflow and MinIO or on the cluster storage; README states how to fetch them. GitHub warns at 50 MB and blocks a file at 100 MB.
- Configuration lives in environment variables: `.env` locally and ignored; `.env.example` committed with every key, a placeholder and a one-line comment; loaded with python-dotenv or a typed settings class that fails fast on a missing key.
- Pre-commit hooks from day one: gitleaks and detect-private-key against secrets, check-added-large-files against data, plus `make check`. Every clone runs `pre-commit install`; README says so.
- A key that reached the history is compromised: rotate it first, then decide with the supervisor whether to rewrite the history. Deleting the file in a new commit removes nothing.
- One seed read from the environment, applied to `random`, NumPy and the framework, logged as a run parameter. Bit-exact reproduction across library versions and devices is not guaranteed; the seed and the lock file are what you can promise.
- Notebooks stay in `notebooks/`; their outputs may stay as a report of a result; code that will be reused moves into `src/`.

## Branches and commits

- Branch name: `<type>/<short-description>` in lowercase with hyphens. Types: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, plus `exp` for an experiment series. The same type opens the PR title: `feat: ...`.
- One branch per change; it lives days, not weeks. Commit and push at the end of every working session, so the semester's history shows work spread over the weeks.
- Never rewrite pushed history on `main`. Merge PRs with squash and merge; the PR title then becomes the commit message on `main`.
- Small fixes may go to `main` directly by agreement with the supervisor; the pre-commit hooks run on them too.
- Commit message wording is optional but useful: see [Commit messages](commit-messages.md).

## Pull request

All work goes through a pull request: it is the record of what was done and why. One branch per change, one PR per branch.

PR fields:

- title in the branch style: `feat: short description`;
- **Plan**: three to five lines written by hand when you open the PR, what you intend to do;
- **Done**: before removing Draft, have an LLM assistant generate a concise description of the work from the diff; the Plan and the `Closes #N` line stay untouched;
- **How to reproduce**: what the reviewer runs to see the result: the command with its config, where the data comes from, the MLflow run with the numbers;
- assignee: you; reviewer: the supervisor, requested by CODEOWNERS when Draft is removed;
- label `enhancement` for new functionality;
- Draft until the work is ready. A draft cannot be merged and requests no review.

A template with these fields lives in `.github/pull_request_template.md`, so a PR never opens empty.

Review loop:

1. The supervisor reads and leaves comments as one batch.
2. You fix in separate commits, no squash or rebase during review, and reply under each thread: what changed and in which commit.
3. You re-request review with the Re-request review button.
4. The supervisor resolves the threads. GitHub also lets the author resolve them, so the rule rests on the agreement.

Response time: as agreed with the supervisor. While waiting, start the next branch from the current one; a semester must never pile up in one PR.

Disagreeing with a comment: first check that you understood it; argue with facts and trade-offs, taste is no argument; offer two or three options; an architectural decision goes into an ADR.

## Decisions

Decisions live in `docs/adr/`, one file per decision: `NNNN-short-title.md`, a four-digit consecutive number that is never reused, a title that names the problem and the chosen solution. The file follows the MADR minimal template with front matter:

```
---
status: proposed | accepted | rejected | superseded by ADR-NNNN
date: 2026-09-24
decision-makers: <student>
consulted: <supervisor>
---
# <Problem and chosen solution>
## Context and problem statement
## Considered options
## Decision outcome
### Consequences
## Pros and cons of the options    <- required when an option the supervisor suggested is rejected
```

- The record is written by your LLM assistant, never by hand: at the moment of the decision, ask the assistant to draft it from the discussion, the PR thread and the code, then review it as you review code.
- What deserves a record: repository structure and data flow; a library, framework or tool such as the tracker, the storage or the LLM gateway; an interface or data contract; the baseline, the primary metric, the dataset and its split; a direction closed by a negative result. A single hyperparameter run is an MLflow run and needs no record.
- The record is born in the feature branch with status proposed, is reviewed in the PR like code, and becomes accepted in the same PR before merge. A rejected record is merged too, with the reason for the rejection. An accepted record is never edited; a change is a new record that supersedes the old one, linked both ways.
- The record links the MLflow experiment or run that motivated it.

## Experiments and reproducibility

- Every experiment is recorded in MLflow. Default: a local database, `MLFLOW_TRACKING_URI=sqlite:///mlflow.db` in `.env`, with `mlruns/` and `mlartifacts/` ignored. If `mlflow.db` is committed so that the supervisor can open it with `mlflow ui --backend-store-uri sqlite:///mlflow.db`: one author only, `mlflow gc` before the commit, the file under 50 MB, committed on the PR branch that produced the runs, a merge conflict resolved by keeping one side and re-running. MLflow documentation does not describe this practice.
- In the first week ask the supervisor whether the lab has a shared tracking server. If it does, switch the client to it: `MLFLOW_TRACKING_URI=https://<server>`, `MLFLOW_EXPERIMENT_NAME`, and for an S3-compatible artifact store `MLFLOW_S3_ENDPOINT_URL`, `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY` in `.env`; `.env.example` lists them empty. Lab example: the server and MinIO on the cluster.
- Naming: experiment `<repository>` or `<repository>/<task>`; run name `<branch>-<short-description>`; always call `mlflow.set_experiment`.
- Mandatory tags, agreed with the supervisor once: `stage` (baseline, ablation, final), `dataset`, `model_family`, `pr` (number). One paragraph in the run notes.
- Run experiments as scripts from inside the checkout, `uv run python -m <package>.train`, after committing: MLflow then records the commit itself. Runs from notebooks get no commit tag.
- Minimum logging: `mlflow.autolog()` before training, the config as an artifact, the final metrics table explicitly.
- A results row is commit, config path, seed, run id, metrics. The table lives in `results/` or in the PR; the thesis cites it.

## Automatic checks

- One target `make check` runs everything: ruff lint and format, pytest with at least one smoke test that runs the main pipeline on a tiny input in seconds.
- Three callers, the same target: pre-commit on your machine, CI on every PR, the agent hook after the assistant edits files. Add the command to the instruction file the assistant reads.
- CI on a PR adds what a machine checks better than a person: branch name and PR title against the type list, gitleaks, large files, `uv sync --locked`. Jobs that need lab credentials are optional and skipped when the secret is absent.
- Never commit with `--no-verify`; a red check gets fixed.

## Minimum expected result

By each checkpoint, show the supervisor:

1. The repository runs from a fresh clone with the README commands.
2. The merged PRs of the period, each with Plan, Done and How to reproduce.
3. Records in `docs/adr/` for the decisions taken.
4. MLflow runs on the commits of those PRs, with the mandatory tags.
5. CI green on `main`; no secrets or data in the history.

## Further reading

- [Helping others review your changes](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/helping-others-review-your-changes), GitHub Docs — self-review and the PR description.
- [Permission levels for a personal account repository](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/permission-levels-for-a-personal-account-repository), GitHub Docs — what a collaborator can and cannot do.
- [MADR](https://adr.github.io/madr/) — the decision record template.
- [MLflow Tracking](https://mlflow.org/docs/latest/ml/tracking/) — experiments, runs, tags, deployment options.
- [The Twelve-Factor App: Config](https://12factor.net/config) — why configuration lives in the environment.
- [Good enough practices in scientific computing](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510), Wilson et al., 2017 — layout, small commits, what never goes into version control.
- [The CL author's guide to getting through code review](https://google.github.io/eng-practices/review/developer/), Google — small changes, descriptions, handling comments.
