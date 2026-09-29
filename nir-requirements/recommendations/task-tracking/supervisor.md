# Task Tracking — Supervisor Guide

What this gives you: the student board shows in five minutes how the work is going; meeting records are kept in the repository; material for the checkpoint is already collected. The rules for the student are in the [student guide](student.md).

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| Board (GitHub Project), card | A project in GitHub Projects: a table and Kanban board of issues and PRs. Each row is a card. | The board is in the student's account; you have the Admin role in it. |
| View | A saved look of the board: layout, filter, grouping. | Two views are enough for you: "Overdue" and "Plan". |
| Sub-issue | An issue nested in another issue. | The parent is a checkpoint; the nested issues are its experiments. |
| Close reason: completed, not planned | Done, or no longer planned. | An issue with a negative result is closed as completed; not planned is only for dropped work. |
| Evidence chain, Step field | The links that make up a strong project under the general requirements, grouped here into five. | Filtering by this field shows which links are still empty before the checkpoint. |

## First week

This is a reminder list; decide yourself what a particular student needs from it:

- store a board template in the lab organisation: the fields Status, Iteration, Kind, Step, Target date and three views. The student copies it with Make a copy; auto-add, cards and collaborators are not copied;
- accept the invitation to the student's board with the Admin role;
- discuss with the student how often they report on the board (at least once per iteration) and agree on meeting times; schedule meetings in Talk with auto-record;
- agree where the student will duplicate the report link so that you do not miss it even if you have not opened the board for a while: Telegram or e-mail;
- in the student's repository choose Watch → Custom → Pull requests: you will then get notifications about both code PRs and meeting-file PRs.

## Weekly look

Five minutes per student:

- the latest report on the board;
- the "Overdue" view: open cards of past iterations;
- cards in Review and Blocked that wait for you: a PR to review, a decision, an access.

Do not audit card moves.

## Meetings

- At the meeting, take decisions: the student has already written about the progress in the report.
- Put a question to the student on every agenda: what should I as the supervisor do differently?
- If there are no results, do not cancel the meeting: help the student put into words what they learned.
- Confirm the meeting file by approving its PR (Approve); mark inaccuracies with a comment on the line.

## Re-planning and scope

- If the core scope changes, agree it with the student in writing in the issue; until then, a new idea stays in Backlog.
- A negative result counts as a result. After one, choose with the student one of three paths: move to a fallback contribution, change the objective, or make the negative result the finding of the work. The student records the decision in an ADR.
- If the student falls behind, ask them to set the status to At risk at once and agree by which date the problem must be solved.

## From the board to the checkpoint and the grade

- For each milestone ask the student for a note of at most one page: what was done against the plan (with links to results); results; the plan to the end of the semester with dates; risks and what to do about them; how many weeks behind the student is. Judge the quality of the plan as well as the progress.
- Filter the board by the Step field: empty links of the chain show which [formal cap](../../general/student.md#formal-caps) applies now. For example, if no card with the step "experiment and metrics" and a quantitative comparison is closed, the grade cannot be higher than **4C**.
- Tell the student which cap applies and which issue removes it when closed.

## Checkpoint checklist

- [ ] There is a board report for every iteration of the period.
- [ ] The "Overdue" view has no cards older than one iteration without an explanation.
- [ ] Every experiment of the period has an issue with outcome and interpretation.
- [ ] Negative results are closed as completed, dropped work as not planned.
- [ ] Meeting files of the period are confirmed; their decisions are in ADRs, their actions are on the board.
- [ ] The Step field shows no empty links, or you have told the student which issues will close them.
- [ ] The checkpoint milestone is closed or moved, and the reason for moving it is recorded.

## Further reading

- [Part IIB projects: notes for supervisors](https://teaching.eng.cam.ac.uk/content/part-iib-projects-notes-supervisors-0), University of Cambridge — weekly meetings based on a written log.
- [Effective PhD supervision meeting agendas](https://www.imperial.ac.uk/media/imperial-college/administration-and-support-services/staff-development/public/pfdc/Download-C.4.9---Advice-sheet---Effective-PhD-supervision-meeting-agendas.pdf), Imperial College London — an agenda for supervision meetings.
- [Ten simple rules for early-career researchers supervising short-term student projects](https://pmc.ncbi.nlm.nih.gov/articles/PMC12626309/), PLOS Computational Biology, 2025 — scope and planning of a short student project.
- [The Kanban Guide](https://kanbanguides.org/the-kanban-guide/) — work item age and work in progress.
- [Sharing project updates](https://docs.github.com/en/issues/planning-and-tracking-with-projects/sharing-project-updates), GitHub Docs — status reports on the board.
