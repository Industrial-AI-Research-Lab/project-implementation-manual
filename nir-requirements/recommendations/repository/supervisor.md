# Repository and Code Work — Supervisor Guide

What you get: a repository you can run from a fresh clone, a review loop that leaves a record, and a checkpoint list that maps repository state to the grade. The [student guide](student.md) holds the conventions; this one holds your side of them.

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| Pull request (PR), Draft, Ready for review | A PR proposes a change from a branch into `main`, with a description and a review thread. Draft marks it unfinished; Ready for review requests the reviewer. | You review PRs that are Ready; a draft is the student's work in progress. |
| CODEOWNERS | The file `.github/CODEOWNERS` maps paths to reviewers; GitHub requests them when a PR becomes Ready for review. | One line with your handle makes you the reviewer of every PR, once the file is merged into `main`. |
| Ruleset, branch protection | Repository settings that block direct pushes to `main` and require a PR, an approval, resolved threads, or green checks. | Free on a public repository; on a private one the same rules hold only by agreement. |
| ADR, decision log, statuses | An architecture decision record is one file per decision: context, options, decision, consequences. Statuses: proposed, accepted, rejected, superseded. | You review records in the PR like code; a rejected alternative of yours must appear with the reason. |
| Experiment, run, tag | MLflow vocabulary: an experiment groups runs; a run is one execution with params, metrics, artifacts and tags, including the commit. | A result without a run id on a PR commit is unverified. |
| `.env.example` | The committed list of configuration keys with placeholders; the real `.env` is ignored. | The filled keys show which accesses the student has; you copy it to `.env` to run the project. |

## First week

Agree the arrangement with the student and have it written into the repository README or the PR template: everything through PRs, or small fixes to `main` allowed; response time; who resolves threads.

A reminder so that nothing is forgotten; what is needed in each case, you decide:

- accept the invitations: collaborator on the repository, Admin on the student's GitHub Project;
- ask the student to merge `.github/CODEOWNERS` with your handle and the PR template, and, on a public repository, to set a ruleset on `main`: PR required, one approval, resolved threads, green checks;
- accesses: the lab LLM gateway, VPN, the cluster; say whether a shared MLflow server and artifact storage exist and hand over their addresses and credentials, otherwise the student records runs in a local database; the filled `.env.example` in the repository shows what the student has;
- a test stand, when the project needs one: help to deploy it or point to the lab's;
- the mandatory MLflow tags and the format of a results row, agreed once.

## Review

- Read the PR description first: Plan against Done, How to reproduce, `Closes #N`. If Done is missing or no run id is given, send the PR back before reading the code.
- Comment as one batch through Start a review. First round on design and decomposition; naming and style later or labelled as non-blocking.
- Label every comment: blocking or non-blocking, `nit:` for taste. Pair an issue with a suggestion. Approve with comments when only minor items remain.
- Ask for clearer code instead of an explanation in the thread; the explanation belongs in the code or in a decision record.
- Resolve the threads yourself after checking the fixing commit; GitHub lets the author resolve them too, so say once that you do it.
- In every PR that touches modelling code check: an MLflow run whose commit is on the PR branch and whose experiment is named in the description; a decision record when a library, a baseline, a metric or a dataset changed; no data, weights or secrets in the diff; CI green.
- Once per checkpoint, run the README commands yourself from a fresh clone.
- Do not paste the student's unpublished code into an external LLM service without their agreement.

## Assessment

The repository criteria and the formal caps are in the [general requirements](../../general/student.md): a result that cannot be verified from the repository caps the grade at 4C, a missing mandatory artifact at 4B, no working result at 3E. Say at the midpoint which cap currently applies and what removes it.

## After the defence

- Stay a collaborator; the history is the evidence.
- Ask for a final tag on `main`, `mlflow gc` on the experiments, and the paths to data and artifacts in README.
- Transfer to the lab organisation only when the code is needed in a lab project: the student initiates it from the repository settings after joining the organisation; issues, PRs, secrets and redirects move with it; the Project stays with the student and is copied.

## Checkpoint checklist

- [ ] The README commands work from a fresh clone.
- [ ] The merged PRs of the period have Plan, Done, How to reproduce, `Closes #N`.
- [ ] Each modelling PR has an MLflow run on its branch commit with the mandatory tags.
- [ ] `docs/adr/` has a record for every decision of the period; statuses are current.
- [ ] `make check` passes locally and CI is green on `main`.
- [ ] No secrets, data or weights in the history; `.env.example` is current.
- [ ] The applicable grade cap has been stated to the student.

## Further reading

- [How to do a code review](https://google.github.io/eng-practices/review/reviewer/), Google — the standard of approval, speed, comment etiquette.
- [Conventional Comments](https://conventionalcomments.org/) — a label vocabulary for review comments.
- [Code Review Guidelines](https://docs.gitlab.com/development/code_review/), GitLab — author and reviewer duties, resolving threads.
- [Checklist for code review process](https://book.the-turing-way.org/reproducible-research/reviewing/reviewing-checklist/), The Turing Way — a research-flavoured review checklist.
- [Managing access to your projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-your-project/managing-access-to-your-projects), GitHub Docs — the Admin role on a student's Project.
