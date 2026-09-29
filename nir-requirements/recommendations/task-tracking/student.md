# Task Tracking — Student Guide

A task board is kept where the code is and shows the supervisor how the work is going without separate status messages. Set it up in the first week of the semester and keep it until the defence.

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| Board (GitHub Project), card | A board is a project in GitHub Projects: a table and Kanban board of issues, PRs and drafts. Each row of the board is a card. In this guide "project" means only the board, not your research project. | One board per semester, in the same account as the repository. |
| Draft issue | A card that exists only on the board: it has no repository, labels or number. | Fine for a quick note. Before starting work, convert the draft into an issue (Convert to issue); otherwise no PR can close it. |
| View | A saved look of the board: layout (board, table, roadmap), filter and grouping. | The supervisor opens ready views and never builds filters. |
| Built-in automation (workflow) | A board rule that fires by itself: for example, when an issue closes or a PR merges, the card moves to Done. | In the first week check that the rules are on, and do not move such cards by hand. |
| Sub-issue | An issue nested in another issue. The parent shows how many nested issues are closed. | The parent is a checkpoint; the nested issues are its experiments and tasks. |
| Issue form | An issue template as a form with fields, a file in `.github/ISSUE_TEMPLATE/`. | Open all experiments from one and the same form: then neither the hypothesis nor the outcome gets lost. |
| Definition of Done | The condition under which a card may move to Done. | Here: the result is already there and linked to the card. "I worked on it" is not a result. |
| Close reason: completed, not planned | When closing an issue, GitHub asks why: done (completed) or no longer planned (not planned). | Close an experiment with a negative result as completed: it is a result too. Not planned is only for work dropped before any result. |
| Evidence chain, Step field | The logic of a strong project from the [general requirements](../../general/student.md#core-principle): problem, relevance, existing solutions, gap, contribution, method, experiment, metrics, comparison, analysis, conclusion. The Step field marks which link a card closes. | The field shows which links are still empty. If a link is empty, a formal grade cap applies. |
| Closing keyword | A line such as `Closes #N` in a PR description: after the merge into the default branch the issue closes by itself. | How to use it is in the [repository guide](../repository/student.md#pull-request). |

## The board in the first week

1. Copy the lab's board template: open the template in the lab organisation, click Make a copy and save the copy in your account. Fields, views and automations are copied except auto-add; cards and collaborators are not. Our lab has such a template; if you do not have one, build the board yourself from "Fields and views".
2. Link the board to the repository in the Projects tab. The tab lists only boards of the repository owner, so the board and the repository must belong to the same account.
3. Add the supervisor to the board members with the Admin role: Settings → Manage access. Board access and repository access are granted separately; both invitations are needed.
4. Set the board's visibility yourself: Settings → Danger zone → Visibility. Keep boards of industrial projects and projects under NDA private; never post partner data, screenshots or logs in cards.
5. Open Workflows and check that closing an issue and merging a PR move the card to Done. The free plan allows only one auto-add rule (Auto-add to project): turn it on for your repository.

## Fields and views

| Field | Values | Purpose |
|---|---|---|
| Status | Backlog, In Progress, Blocked, Review, Done | Where the card is now. Blocked: the card waits for the supervisor, data or a cluster job. Review: a PR is open for the card. |
| Iteration | two-week iterations, a break for the exam session | How often you plan work and write reports. |
| Kind | experiment, code, reading, writing | The type of work. Issue types are unavailable in personal repositories, so the type lives in a field. |
| Step | problem and relevance; related work and gap; method and implementation; experiment and metrics; analysis and conclusions | The link of the evidence chain. The five groups are a shortened version of the chain from the general requirements and the [task template](../../llm-assistant/project-context.md#tasks). |
| Target date | a date | The card's deadline. |

Views:

- **Board**: Board layout by Status, filter `iteration:@current`.
- **Plan**: Roadmap layout by iteration, with milestones.
- **Overdue**: a table filtered by `iteration:<@current is:open`, that is, the open cards of past iterations.

## Cards and done

- A card is one step that ends in a PR or a written outcome in the issue description. If a card stays in In Progress for a week, split it.
- There is no limit on cards in progress. Keep two or three in In Progress: they are easier to finish. Everything waiting on others goes to Blocked.
- A card moves to Done when it has a result and the result is linked to the card:
  - a merged PR with `Closes #N`;
  - an entry in the [reading log](../papers/student.md#reading-and-notes) for a reading card;
  - the outcome and interpretation in the description of an experiment issue;
  - a text section in the repository for a writing card.

## Experiments as issues

- Open a parent issue for each checkpoint and nest sub-issues in it: one experiment, one issue.
- Open experiments from the form `.github/ISSUE_TEMPLATE/experiment.yml`. Turn off creating blank issues with `blank_issues_enabled: false` in `.github/ISSUE_TEMPLATE/config.yml`. GitHub enforces required form fields only in public repositories.

```yaml
name: Experiment
description: One hypothesis, one issue
title: "exp: "
projects: ["<owner>/<board number>"]
body:
  - type: textarea
    id: hypothesis
    attributes:
      label: Hypothesis
    validations:
      required: true
  - type: textarea
    id: setup
    attributes:
      label: Setup
      description: Data, baseline, metric
  - type: textarea
    id: expected
    attributes:
      label: Expected result
  - type: textarea
    id: result
    attributes:
      label: Outcome and interpretation
      description: Filled in at closing
```

- Put the issue number in the PR description (`Closes #N`) and in the MLflow run note, so that result, code and discussion will be connected.
- Close a negative result as completed and describe in the issue the outcome and what it means for the work. Close as not planned only work dropped before any result.
- If a result breaks the rest of the plan, ask the LLM assistant to draft an ADR with the new plan, discuss it with the supervisor, and update cards and milestones.

## Semester plan

1. First enter the dates you do not control: report submission, pre-defence, originality check, defence. Make the three checkpoints from the [supervisor guide](../../general/supervisor.md#supervisor-checkpoints) (start of the project, before the midpoint, before the defence) repository milestones: give each milestone a date and list the expected artifacts in its description. Check the exact dates in your programme's schedule.
2. Split the semester into two-week iterations with a break for the exam session. Plan the whole semester to the iteration level and the next iteration to the card level: a detailed plan a month ahead breaks at the first surprise.
3. Plan the core scope so that it fits roughly half of the semester. New ideas, models and datasets go to Backlog; they enter the plan only after the supervisor's written agreement in the issue.
4. At the end of an iteration, move unfinished cards to the next one (Move items to…) and say in the report why they stayed open.

## Reports and meetings

**Report on the board.** Agree with the supervisor at the start of the semester how often you report; at least once per iteration. Send the report even when the supervisor did not ask and there are no results yet: it shows where the work is stuck. Write it as a board status update: choose the status On track, At risk or Off track and fill in three items:

- what was done against the previous plan, with links to closed issues and PRs;
- the plan for the next iteration: items whose completion can be checked;
- what you need from the supervisor: a decision, advice or feedback.

**Meetings.** For example, in our lab meetings take place in Talk (itmo.ktalk.ru). Remember to start the recording when the meeting begins; better, schedule the meeting in advance and turn on auto-record while scheduling, so the recording starts by itself. Tell the participants that the meeting is recorded. After the meeting Talk produces a transcript with speaker names and time codes and a meeting summary; they appear under "Artefacts → Video recordings → Overview".

1. Ask the LLM assistant to write `docs/meetings/YYYY-MM-DD.md` from the summary: participants by role, a link to the recording, decisions with time codes, actions with owner, issue link and date, open questions, the next meeting date.
2. Check decisions, numbers and names against the transcript: clicking a line makes Talk play that fragment. A neural network writes the summary, and it makes mistakes.
3. Talk creates neither ADRs nor tasks; that is your job: ask the assistant to draft an ADR from the meeting file (see the [repository guide](../repository/student.md#decisions)) and to turn the meeting's actions into issues and add them to the board with `gh`. Once, allow `gh` to work with boards: `gh auth refresh -s project`.

   ```bash
   gh issue create --title "..." --body "..." --project "<board title>"
   ```

4. Add the meeting file through a PR: the supervisor confirms the record by approving the PR. Commit the summary only. A full transcript may be added only after sanitization, that is, removing personal and confidential data; how to sanitize, how to transcribe a recording without Talk and which prompts to use are in the [meeting records reference](meeting-records.md).

**Falling behind.** If you fall behind, set the status to At risk at once, without waiting for the checkpoint. Agree with the supervisor by which date the problem must be solved and how you will know it is. If the delay persists, write down the new plan: an ADR and new milestone dates.

**The supervisor does not open the board.** Send the report link with its three items where you agreed with the supervisor: most often Telegram or e-mail. The message holds only the link; the information itself stays on the board.

## End of the semester

- Close every card: finished ones through a PR or an outcome in the issue, the rest as not planned with a reason.
- Write the final report on the board with links to the practice report, the release and the ADRs.
- Archive the cards in Done (Archive): field values are kept, and archiving can be undone.
- Build the list of completed work for the practice report from the closed issues of each milestone. Formal documents are still submitted through the university.

## Minimum expected result

By each checkpoint, show the supervisor:

1. The board with the fields Status, Iteration, Kind, Step and three views; the supervisor is its Admin.
2. A board report for every iteration of the period.
3. An issue for every experiment of the period with outcome and interpretation.
4. Meeting files in `docs/meetings/` with links to issues and ADRs.
5. Milestones with dates and a current completion percentage.

## Further reading

- [Best practices for Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/best-practices-for-projects), GitHub Docs — fields instead of duplicate labels, the board as the main record of the work.
- [About iteration fields](https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-iteration-fields), GitHub Docs — iterations, breaks, `@current` filters.
- [Syntax for issue forms](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms), GitHub Docs — form fields and linking to a board.
- [Personal Kanban](https://personalkanban.com/learn/personal-kanban/), Jim Benson and Tonianne DeMaria Barry — the two rules of a personal Kanban board.
- [Project proposal](https://www.cst.cam.ac.uk/teaching/part-ii/projects/project-proposal), University of Cambridge — work packages of at most two weeks with a checkable result.
- [Writing a progress report](https://homes.cs.washington.edu/~mernst/advice/progress-report.html), Michael Ernst, University of Washington — what to put in a report to the supervisor.
- [Научно-исследовательская работа (рекомендации)](http://www.machinelearning.ru/wiki/index.php?title=%D0%9D%D0%B0%D1%83%D1%87%D0%BD%D0%BE-%D0%B8%D1%81%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%B0%D1%8F_%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0_%28%D1%80%D0%B5%D0%BA%D0%BE%D0%BC%D0%B5%D0%BD%D0%B4%D0%B0%D1%86%D0%B8%D0%B8%29), MachineLearning.ru — a regular written report even when nobody asks.
