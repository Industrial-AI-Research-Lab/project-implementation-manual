# Research Log and Decision Log Template

The log is a chronology of what the researcher knew, did, and decided at a specific moment. It must not be rewritten retroactively. A correction is added as a new entry that references the erroneous one.

## Logging rules

1. Make an entry after any significant action or decision, not only at the end of the week.
2. Separate **observation**, **interpretation**, and **decision**.
3. Reference immutable versions: commit, config, data hash, run ID, document.
4. Record negative results, failed runs, and dead ends.
5. Every deviation from the frozen protocol/analysis plan receives its own ID.
6. Do not put tokens, passwords, identifying participant data, or restricted raw data in the log.

## 1. Regular entry

### LOG-[YYYYMMDD]-[number]: [short title]

- ★ Date/time and time zone: [ISO 8601]
- ★ Author: [ ]
- ★ Stage/RQ/H: [ ]
- ★ Context: [what was known and what the task was]
- ★ Action: [what exactly was done]
- ★ Inputs and versions: [data/config/code/environment]
- ★ Observation: [what was directly seen; values/facts]
- Interpretation: [possible explanation; do not present it as fact]
- Alternative explanations: [ ]
- ★ Decision: [continue/change/stop/escalate]
- ★ Rationale for the decision: [why]
- Impact on protocol/analysis/risks: [none or link to deviation]
- Next step and owner: [ ]
- Artifacts: [links]

## 2. Run log

| Run ID | Date | Goal | Protocol/commit | Data version | Config/seed | Environment | Status | Main output | Problem | Artifacts |
|---|---|---|---|---|---|---|---|---|---|---|
| RUN-001 | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ok/failed/partial] | [ ] | [ ] | [ ] |

For a failed run, record the technical failure criterion. Do not rerun a "bad" statistical result as if it were a technical error.

## 3. Decision record

### DEC-[number]: [decision]

- Date and decision-maker: [ ]
- Question: [what needs to be chosen]
- Options: [A/B/C]
- Criteria: [quality, risk, cost, scientific value]
- Evidence at the time of the decision: [links]
- Chosen option: [ ]
- Reason: [ ]
- Uncertainties accepted: [ ]
- Conditions for revisiting: [trigger/date]
- Consequences for other documents: [ ]

## 4. Protocol deviation

### DEV-[number]: [short title]

- ★ Date of detection/decision: [ ]
- ★ Planned: [exact reference and text of the decision]
- ★ What happened/changed: [ ]
- ★ Reason: [error, feasibility, new information, external factor]
- ★ Were outcome/test results visible: [yes/no; which]
- ★ Who approved: [ ]
- ★ Impact on bias/validity/interpretation: [ ]
- ★ Action: [amend protocol / exploratory label / sensitivity / repeat]
- Where disclosed in the report: [section/link]

## 5. Negative result/dead end

### NEG-[number]: [what did not work]

- Expectation: [ ]
- What was tested: [method and versions]
- What was observed: [ ]
- Is the test sufficient to draw a conclusion: [precision/limitations]
- Possible causes: [ ]
- Which repetition would be pointless: [ ]
- What knowledge was retained: [ ]
- Reusable artifacts: [ ]

## 6. Quality/ethics/safety incident

### INC-[number]: [title]

- Date and who detected it: [ ]
- Affected data/people/systems: [no sensitive details in an open log]
- What is known and unknown: [ ]
- Immediate measure: [pause/isolate/notify]
- Escalated to: [ ]
- Decision and residual risk: [ ]
- Root cause and preventive action: [after investigation]
- Related notifications/tickets: [restricted access]

## 7. Weekly summary

- Period: [ ]
- Completed: [ ]
- Main new knowledge: [ ]
- What has become less certain: [ ]
- Open blockers/risks: [ ]
- Protocol changes: [IDs]
- Negative results: [IDs]
- Decisions for next week: [ ]
- State of artifacts and reproducibility: [ ]

## Quality check

- [ ] Entries are dated and attributed to an author.
- [ ] Observation, interpretation, and decision are separated.
- [ ] Each run is linked to versions of the code, data, config, seed, and environment.
- [ ] Negative results and failed runs have not been deleted.
- [ ] Deviations state whether the results were already visible.
- [ ] Decisions include alternatives and conditions for revisiting.
- [ ] Links point to immutable or versioned artifacts.
- [ ] Secrets and sensitive data have not entered the log.

Methodological basis: [National Academies on reproducibility and recordkeeping](https://www.nationalacademies.org/read/25303), [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines), [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Commit and tag** — in a version control system (for example, Git), a commit is a recorded state of the code with a unique identifier, and a tag is a permanent name for a specific commit. Referring to them, rather than to a changing branch, pins the exact version.
- **Checksum (hash)** — a short string computed from a file's contents. Any change to the file changes it, so it confirms that exactly the intended version is being used.
- **Null and negative results** — results that show no expected effect or no advantage of a method. With sufficient precision they are valid knowledge and should be reported.
- **Freezing (frozen)** — locking a version of the protocol, analysis plan, data, or split, after which changes are allowed only through the deviation log. It protects against fitting the analysis to the result.
- **ISO 8601** — the international standard for writing dates and times (for example, 2026-08-25T14:30+03:00). It is unambiguous, can include the time zone, and sorts conveniently.
- **Deviation log** — a dated list of changes to the frozen protocol or analysis plan: what changed, why, whether results were already visible, and how this affects interpretation. It lets readers tell what was planned from what changed along the way.
- **Seed (random seed)** — the initial value of a pseudorandom number generator. Fixing the seed makes random steps repeatable, and running with several seeds shows how much the result varies.
- **Failed run** — a run that failed according to a predefined technical criterion: an error, running out of memory, or corrupted data. An unwelcome statistical result is not a technical failure.
- **Decision record** — a structured record of a decision: the question, options, criteria, evidence, chosen option, accepted uncertainties, and conditions for revisiting it.
- **Feasibility** — the practical achievability of a study or procedure given the available data, time, resources, and constraints.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Sensitivity analysis** — assessing how much the result changes when assumptions or debatable analytic choices change, for example the handling of missing data or outliers.
- **Root cause and preventive action** — after an incident, the underlying cause whose removal prevents the problem from recurring, and the measure that ensures this.
- **National Academies** — the U.S. National Academies of Sciences, Engineering, and Medicine. Their report "Reproducibility and Replicability in Science" (2019) provides widely used definitions of reproducibility and replicability and recommendations for achieving them.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
- **ACM Artifact Review and Badging** — the Association for Computing Machinery policy for reviewing research artifacts of papers and awarding badges: Artifacts Available, Artifacts Evaluated (Functional, Reusable), and Results Validated (Reproduced, Replicated).
