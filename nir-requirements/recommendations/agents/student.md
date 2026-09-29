# Agent Artifacts — Student Guide

An agent works more precisely when the project's rules live in files it reads by itself and the checks run without you. This guide describes what to put in the repository, how to move shared rules into an overlay repository, and how to connect the agent with CI.

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| Agent, harness | An agent is an LLM assistant that reads files, runs commands and edits code by itself. The harness is the environment it works in: instruction files, permissions, hooks and checks. | The more rules the harness holds, the less often you repeat them in requests. |
| Instruction file | A file the agent reads at start-up: AGENTS.md, CLAUDE.md, `.github/copilot-instructions.md`. | The main file is AGENTS.md: almost every agent reads it. |
| Rule, skill | A rule is a short instruction in a separate file, for example about code style or working with data. A skill is a set of instructions for a typical task that the agent loads when the task fits. | Rules and skills are the natural things to move into an overlay and reuse across projects. |
| Agent hook | A command the agent runs by itself at a given step of its work, for example before it finishes a reply. | A hook always fires; a request in text the agent may skip. |
| Overlay repository | A separate repository with the agent's rules, skills, hooks and settings, connected to a project. The term has no established meaning; in this guide it means exactly this. | Your agent know-how lives in one place and connects to any project. |
| Submodule, pinning a version | A submodule is a repository nested in another one at a specific commit. Pinning a version means naming a tag or a commit instead of a branch. | The project does not change by itself when the overlay changes: you connect a new version explicitly. |
| Workspace trust | The question an agent asks when it first opens a folder: whether you trust its contents. | Hooks from committed settings run with your permissions; agree only after reading them. |
| Prompt injection | An instruction for the agent hidden in a file or page it reads. The agent may carry it out as if it were yours. | Read someone else's rules and hooks before connecting them. |
| Permissions deny | A rule in the agent's settings that forbids an action, for example reading a file. | Denying reads of `.env` keeps your keys away from the agent. |
| MIT licence | A short permissive licence: code and texts may be taken, changed and redistributed if the licence text is kept. | Without a licence, only the author may legally use the rules. |

## Instruction files

- AGENTS.md at the repository root is the main file. List in it the install and run commands, the check command `make check`, the branch and PR conventions (see the [repository guide](../repository/student.md#pull-request)), and the rule "never commit with `--no-verify`". Keep it short, under 200 lines; leave out what the code already shows.
- If you work in Claude Code, create CLAUDE.md with `@AGENTS.md` as its first line and add below it only what concerns Claude Code. Without that line Claude Code does not read AGENTS.md when a CLAUDE.md is present.

Which files the agents read, as of September 2026:

| Agent | Instruction files |
|---|---|
| Claude Code | CLAUDE.md, `.claude/rules/`, `.claude/skills/`; AGENTS.md when there is no CLAUDE.md, otherwise through the `@AGENTS.md` import |
| Codex | AGENTS.md |
| Cursor | AGENTS.md, `.cursor/rules/` |
| GitHub Copilot | AGENTS.md, CLAUDE.md, `.github/copilot-instructions.md` |

Each agent has its own settings for hooks; the examples below are for Claude Code.

## What to commit

Put shared files into the project repository or the overlay:

- AGENTS.md and CLAUDE.md;
- rules and skills: `.claude/rules/`, `.claude/skills/`;
- the agent's shared settings with hooks and denials: `.claude/settings.json`;
- service folders where tools keep the work plan, for example `.agent/`.

Add personal files to `.gitignore`:

```gitignore
# personal agent settings
*.local.*
CLAUDE.local.md
.claude/settings.local.json
```

Before committing, check that the shared files contain no tokens and no absolute paths to your machine. Gitleaks in pre-commit catches keys; look for paths yourself.

## One check for the agent, pre-commit and CI

The `make check` target from the [repository guide](../repository/student.md#automatic-checks) runs from three places: the agent hook, pre-commit and CI. The agent's edits, your commits and your PRs pass the same checks.

**Agent settings**, `.claude/settings.json`:

```json
{
  "permissions": {
    "deny": ["Read(./.env)", "Read(./.env.*)"]
  },
  "hooks": {
    "Stop": [
      {
        "hooks": [
          { "type": "command", "command": "make check >&2 || exit 2" }
        ]
      }
    ]
  }
}
```

The Stop hook runs the check before the agent finishes its reply. If the check fails, exit code 2 keeps the agent from stopping, and the agent receives the check output as the reason to continue and fixes what it broke. If it cannot fix it, the agent keeps trying; interrupt it and sort the problem out yourself.

**Pre-commit**, `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: local
    hooks:
      - id: make-check
        name: make check
        entry: make check
        language: unsupported
        pass_filenames: false
```

The value `unsupported` appeared in pre-commit 4.4; in older versions write `system`.

**CI**, `.github/workflows/check.yml`:

```yaml
name: check
on: pull_request
jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v7
      - uses: astral-sh/setup-uv@v9
      - run: uv sync --locked
      - run: make check
```

**AGENTS.md**:

```markdown
## Checks
Before finishing a task, run `make check` and make it pass. Never commit with `--no-verify`.
```

## Overlay repository

Shared rules, skills and hooks are easiest to keep in one overlay repository: a rule fixed there reaches every project that connects the overlay as soon as you update the version there.

**Connecting.** Add the overlay to the project as a submodule, pin the version, and create a symbolic link to the rules in the folder the agent reads:

```bash
git submodule add https://github.com/<group>/<overlay>.git .agents/overlay
git -C .agents/overlay checkout v0.3.0
mkdir -p .claude/rules
ln -s ../../.agents/overlay/rules .claude/rules/overlay
git add .gitmodules .agents/overlay .claude/rules/overlay
git commit -m "chore: connect agent overlay v0.3.0"
```

- Import the overlay's shared instructions into CLAUDE.md with the line `@.agents/overlay/AGENTS.md`.
- Clone the project with `--recurse-submodules`, otherwise the overlay folder stays empty. Say so in the README: the supervisor clones the project the same way.
- Connect a new overlay version through a PR: switch the submodule to the new tag and commit that on a `chore/...` branch. The history then shows when the agent's rules changed.

**Sharing.** Suggest to your study group one shared overlay, or team up in smaller groups with "friendly" overlays and help each other. Give classmates the link to this guide so that everyone connects the overlay the same way. Change a shared overlay through PRs, so the others see what changed.

**Licence.** Put a LICENSE file with the MIT licence at the root of the overlay. Without a licence, only the author may legally use the rules.

## Someone else's overlay: checks before connecting

- Read every hook, rule and settings file. Hooks run with your permissions, and the agent follows the rules as your instructions.
- Look at the raw text of the files, not only at how GitHub renders them: HTML comments and invisible characters can hold instructions the agent reads and you do not notice.
- Connect the overlay at a tag or a commit; connected at a branch, someone else's change reaches you unchecked.
- Deny the agent reading `.env`, as in the settings example above.
- Never put secrets, tokens or internal addresses into an overlay: everyone who connects it sees them.

## Disclosing agent use

Add a section "LLM assistants" to the project README: which agents you use and for what, with links to AGENTS.md and the overlay. You are responsible for code written with an agent, as the [general requirements](../../general/student.md#use-of-generative-ai) state. In a paper or thesis, describe the use as the publisher or programme requires: IEEE, ACM and Elsevier require disclosing the use of generative AI, and IEEE explicitly extends this to code.

## Minimum expected result

By the checkpoint, show the supervisor:

1. AGENTS.md at the root with the `make check` command; if there is a CLAUDE.md, it imports AGENTS.md.
2. The shared agent artifacts in the repository, the personal ones in `.gitignore`.
3. A `make check` that runs from the agent hook, pre-commit and CI.
4. An "LLM assistants" section in the README.
5. If you connected an overlay: a submodule pinned at a tag or commit, and a LICENSE file at the overlay's root.

## Further reading

- [AGENTS.md](https://agents.md/) — the open instruction-file format and the list of agents that read it.
- [How Claude remembers your project](https://code.claude.com/docs/en/memory), Claude Code documentation — CLAUDE.md, rules, imports and the link to AGENTS.md.
- [Hooks reference](https://code.claude.com/docs/en/hooks), Claude Code documentation — hook events and exit codes.
- [Adding repository custom instructions for GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-repository-instructions), GitHub Docs — which instruction files Copilot reads.
- [pre-commit](https://pre-commit.com/) — local hooks and running them in CI.
- [LLM01:2025 Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/), OWASP — indirect injection through files and ways to defend against it.
- [Licenses for non-software](https://choosealicense.com/non-software/), choosealicense.com — how to license texts and configuration.
