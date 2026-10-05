# Checklists for Self-Review, Reviewers, and Supervisors

Review is carried out stage by stage. A total "score" does not compensate for a critical defect: an unknown license, test leakage, a missing link between the RQ and the method, or an undisclosed change to the primary outcome must be fixed regardless of the total.

## Review decisions

- **Approve** — the stage criteria are met; residual limitations are explicitly accepted.
- **Revise** — the defect can be fixed before the next gate.
- **Repeat/collect** — the current data do not support a reliable conclusion.
- **Stop** — the question has lost its value, the risk is unacceptable, or the study is infeasible.
- **Escalate** — ethics, data, security, legal, or subject-matter expertise is required.

For each comment, specify: `ID → requirement → evidence → defect → required change → owner → deadline`.

## G0. Problem statement review

### Critical questions

- [ ] The observed problem is separated from the presumed solution.
- [ ] There is substantial uncertainty, so the task is genuinely a research task.
- [ ] The decision owner is identified, along with what will change once the question is answered.
- [ ] The objective allows for a negative/null/inconclusive result.
- [ ] Boundaries, non-goals, population, and unit of analysis are clear.
- [ ] Novelty has been checked against the external literature, not only within the team.
- [ ] The practical criterion has a domain-based justification.
- [ ] Stop criteria and a resource ceiling are stated.

### G0 decision

- Outcome: [approve/revise/stop]
- Main gap: [ ]
- Conditions for proceeding: [ ]
- Reviewer/date: [ ]

## G1. Protocol review before data collection

### Questions and hypotheses

- [ ] The main RQ is specific, testable, and linked to a decision.
- [ ] Constructs are operationalized with valid metrics.
- [ ] A causal claim has an identification strategy.
- [ ] A predictive claim has an honest out-of-sample test.
- [ ] Hypotheses include a mechanism, a prediction, alternatives, and a falsification condition.
- [ ] Confirmatory and exploratory parts are separated.

### Design

- [ ] The experimental unit and independent replicates are correctly defined.
- [ ] Controls/baselines correspond to the real alternative.
- [ ] Randomization, blocking, and blinding are described or justifiably not applicable.
- [ ] n/the number of runs is justified by precision, power, saturation, or an honest resource limit.
- [ ] The primary outcome, inclusion/exclusion, missing data/outliers, and stop rules are prespecified.
- [ ] The analysis plan is linked to the estimand and accounts for dependence/multiplicity.
- [ ] The pilot is not mixed with confirmation.

### Risks

- [ ] Data rights, ethics, privacy, security, and dual use have been considered.
- [ ] All approvals have been obtained, or there is a blocking plan.
- [ ] Residual risks have owners and a stop/escalation rule.

### G1 decision

- Outcome: [approve/revise/escalate]
- Frozen protocol version: [ ]
- Open conditions: [ ]
- Reviewer/date: [ ]

## G2. Data readiness review

- [ ] Version, provenance, license, and access date are traceable.
- [ ] The datasheet and data dictionary are completed.
- [ ] The sample matches the population, or limits on transferability are explicit.
- [ ] Schema, missing-value, duplicate, label, and subgroup quality checks have been performed.
- [ ] Splits are made at the correct entity/time level.
- [ ] Leakage, overlap, and benchmark contamination have been checked.
- [ ] The test/confirmation snapshot is frozen and access to it is restricted.
- [ ] Raw data are immutable; preprocessing is reproducible from code/the log.
- [ ] Personal data are minimized; retention/access rules are defined.
- [ ] Quality failures were not covertly "fixed" after the outcome was seen.

### G2 decision

- Outcome: [approve/revise/stop]
- Frozen data ID/hash: [ ]
- Remaining limitations: [ ]
- Reviewer/date: [ ]

## G3. Analysis and results review

### Analysis integrity

- [ ] The code was run on frozen data in a versioned environment.
- [ ] Exclusions and failed runs comply with the protocol.
- [ ] Deviations are listed with dates and with whether the result was known at the time.
- [ ] The primary analysis is shown regardless of whether the result looks good.
- [ ] Effect size and uncertainty are reported; the p-value is not used as a measure of importance.
- [ ] Assumption diagnostics and sensitivity analyses address real threats.
- [ ] Multiplicity and exploratory comparisons are disclosed.
- [ ] Subgroup differences are assessed with an interaction term/an appropriate model.
- [ ] "No significant difference" is not turned into proof of equivalence without precision/an equivalence analysis.

### Alignment of conclusions

- [ ] Each RQ is answered as supported/not supported/uncertain.
- [ ] No claim is broader than the data, design, and population.
- [ ] Alternative explanations and contradictory results are discussed.
- [ ] Negative and ambiguous results are retained.
- [ ] Each exploratory finding has a plan for independent verification.

### G3 decision

- Outcome: [conclude/repeat/collect/stop]
- Permitted claims: [ ]
- Prohibited claims: [ ]
- Reviewer/date: [ ]

## G4. Artifact review

- [ ] There is a manifest of data, code, config, environment, results, and licenses.
- [ ] A single set of instructions leads from a clean environment to the main result.
- [ ] Versions are pinned by commit/tag/DOI/hash.
- [ ] Expected outputs and numerical tolerances are specified.
- [ ] Hardware, runtime, and cost are realistic.
- [ ] No secrets or sensitive data are present.
- [ ] Restricted items have a clear reason and an access procedure.
- [ ] An independent tester has executed the runbook.
- [ ] Defects found by the tester have been fixed or disclosed.
- [ ] The archived copy is linked to the publication.

### G4 decision

- Functional: [yes/no]
- Reusable: [yes/no/not checked]
- Available: [yes/no/restricted]
- Independently reproduced: [yes/no]
- Reviewer/date: [ ]

## G5. Manuscript/report review

### Logic

- [ ] The title and abstract accurately convey the design, result, and limitation.
- [ ] The introduction ends with an explicit RQ/contribution.
- [ ] Related work is critically synthesized and includes contradictions.
- [ ] The methods are detailed enough for replication.
- [ ] The results follow the RQs and contain no hidden interpretation.
- [ ] The discussion distinguishes between result, mechanism, and speculation.
- [ ] The conclusion does not overstate causality/generality.

### Transparency

- [ ] An appropriate reporting guideline has been selected and its checklist attached.
- [ ] There is a claim-to-evidence map.
- [ ] Protocol/registration and deviations are stated.
- [ ] Data/code/materials availability statements are specific.
- [ ] Ethics, funding, conflicts, authorship, and AI use are disclosed.
- [ ] Limitations explain their direction/impact on the conclusion.
- [ ] Citations lead to primary sources that genuinely support the claim.
- [ ] Figures/tables are self-contained and do not distort scale.

### G5 decision

- Outcome: [submit/revise/do not submit]
- Target venue/guideline: [ ]
- Blocking issues: [ ]
- Reviewer/date: [ ]

## Rubric for student work

Rate each area as `0 — absent`, `1 — partial/unjustified`, `2 — complete and verifiable`. The score supports learning, but critical defects are checked separately.

| Area | 0 | 1 | 2 | Score/comment |
|---|---|---|---|---|
| Problem and RQ | No clear question | A question exists, but boundaries/the decision are unclear | Testable RQ, boundaries, and value | [ ] |
| Literature | Random list | Search partially described | Reproducible search and critical synthesis | [ ] |
| Hypotheses/logic | Desired answer | Prediction without alternatives | Mechanism, falsification, and alternatives | [ ] |
| Design | Does not answer the RQ | Substantial threats without mitigation | Design, control, sampling, and risks are justified | [ ] |
| Data | Unclear provenance | Data incompletely described | Provenance, quality, rights, and splits are transparent | [ ] |
| Method | Impossible to replicate | General steps | Contract, algorithm, parameters, failure modes | [ ] |
| Analysis | Overfitting/p-values only | Partial plan | Estimand, effect, uncertainty, sensitivity | [ ] |
| Conclusion | Stronger than the data | Limitations mentioned | Claims precisely match the evidence | [ ] |
| Reproducibility | No artifacts | Code/data without instructions | Independently verified package | [ ] |
| Ethics/integrity | Not considered | Generic statements | Specific risks, measures, and disclosures | [ ] |

### Critical defects regardless of score

- fabrication, falsification, plagiarism, or concealed selective reporting;
- research involving humans/sensitive data without the required approval;
- unknown right to use the data;
- test leakage or tuning on the final set without disclosure;
- a post hoc hypothesis presented as prespecified;
- a changed primary outcome/observations excluded after the result was known, without a log;
- a causal conclusion drawn from a design that does not identify it;
- missing data/code/methods with no explanation of the restriction.

## Reviewer comment template

### REV-[number]: [short title]

- Priority: [blocking/major/minor/question]
- Criterion: [which requirement is not met]
- Evidence: [page/line/artifact]
- Problem: [why it affects validity/reproducibility/clarity]
- Required change: [a verifiable outcome, not a means of implementation]
- Acceptable alternative: [if any]
- Owner/deadline: [ ]
- Author response and new evidence: [ ]
- Status: [open/resolved/accepted risk]

## Common red flags

- The result is described before the question and the protocol.
- "Better than SOTA" without an equal tuning budget and a strong baseline.
- Many metrics, but none declared primary.
- Erroneous/inconvenient observations removed without a blind rule.
- An unstable result reported from a single seed.
- A claim about mechanism based solely on correlation.
- Limitations hidden in the appendix while the abstract sounds universal.
- The code link points to a mutable branch without a tag/commit.
- The dataset is "public", but its license, consent, and provenance are unknown.
- "The LLM checked it" is used in place of human verification of references/code/analysis.

Methodological basis: [EQUATOR reporting guidelines](https://www.equator-network.org/about-us/what-is-a-reporting-guideline/), [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist), [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current), [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines), [COPE Ethical Guidelines for Peer Reviewers](https://doi.org/10.24318/cope.2019.1.9).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Data leakage** — information from test or confirmation data reaching training, tuning, or analysis choices. It inflates performance estimates and leads to false conclusions.
- **Primary outcome** — the main measure, chosen in advance, on which the main conclusion is based; secondary outcomes complement it. Changing the primary outcome after seeing the results without disclosure is a serious violation.
- **Gate (checkpoint)** — a predefined project stage at which a decision to continue, revise, or stop the work is made based on a minimum set of evidence.
- **Non-goals** — an explicit list of what a study or method deliberately does not address. It helps keep the scope of the work in check and prevents overreaching conclusions.
- **Stop criteria (stopping criteria)** — conditions, set in advance, under which a study is stopped or paused: data cannot be obtained, risk becomes unacceptable, the budget is exceeded, or the work proves futile. They are set before the main resources are spent.
- **Identification strategy** — the justification for why an observed difference can be interpreted as a causal effect rather than a result of confounding or selection, for example through randomization or a natural experiment.
- **Out-of-sample (hold-out) validation** — evaluating a model or conclusion on data that were not used to build, tune, or select the model. Only such validation honestly shows predictive performance.
- **Falsifiability** — the property of a hypothesis for which an observation that would refute it can be named in advance. A hypothesis compatible with any result tests nothing.
- **Confirmatory analysis** — analysis whose hypotheses and rules were fixed before the results were seen. Only such analysis supports a claim that a hypothesis was tested.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Experimental unit** — the smallest entity that independently receives an experimental condition. Repeated measurements of one unit are not independent replicates.
- **Baseline** — the reference point for comparison: current practice, or a simple or strong existing method. A new method's gain is meaningful only relative to a fairly tuned, strong baseline.
- **Randomization** — random assignment of units to experimental conditions. On average it balances known and unknown factors and thus protects against confounding.
- **Blinding** — withholding from participants, staff, or analysts which condition a unit received, so that expectations do not influence measurements and decisions.
- **Statistical power** — the probability of detecting an effect of a given size if it truly exists. Power analysis is used to justify the sample size.
- **Estimand** — a precise definition of what is being estimated: the population, outcome, conditions compared, summary measure, and handling of intercurrent events. Without it, the same "effect" can mean different quantities.
- **Multiple comparisons (multiplicity)** — a situation in which many hypotheses, metrics, or subgroups are tested. The probability of at least one false positive grows, so a predefined control method is needed.
- **Freezing (frozen)** — locking a version of the protocol, analysis plan, data, or split, after which changes are allowed only through the deviation log. It protects against fitting the analysis to the result.
- **Benchmark contamination** — benchmark test examples ending up in a model's training data, for example through training on web data. Results on such a benchmark are inflated.
- **Effect size** — the quantitative magnitude of a difference or association, such as a difference in means, an odds ratio, or a metric gain. Unlike a p-value, it shows how large and practically important an effect is.
- **P-value** — the probability of obtaining data at least as extreme as those observed if the null hypothesis and all model assumptions are true. It is not the probability that a hypothesis is true, nor a measure of an effect's size or importance.
- **Equivalence testing** — testing whether a difference lies within preset margins of practical irrelevance. Only this, not the absence of a significant result, can justify a conclusion that there is no important difference.
- **Manifest** — a list of files or artifacts with their purpose, version or checksum, license, and access conditions. It makes it possible to verify that a package is complete and unchanged.
- **ACM Artifact Review and Badging** — the Association for Computing Machinery policy for reviewing research artifacts of papers and awarding badges: Artifacts Available, Artifacts Evaluated (Functional, Reusable), and Results Validated (Reproduced, Replicated).
- **Reporting guideline** — a checklist of what a publication must describe for a given study design, for example CONSORT for randomized trials or PRISMA for systematic reviews. It helps avoid omitting essential details of methods and results.
- **Claim–evidence map** — a table linking each claim of the work to specific data, analysis, figure or table, assumptions, and limitations. It helps remove unsupported claims.
- **Fabrication, falsification, plagiarism** — the three main forms of research misconduct: making up data or results; manipulating data, procedures, or results; and using others' ideas, text, or results without attribution.
- **Selective reporting** — reporting only the "successful" results, metrics, or analyses while hiding the rest. It distorts the overall body of evidence.
- **Post hoc explanation** — an explanation devised after the result is known. If any outcome can be explained this way, the hypothesis is effectively unfalsifiable; presenting such hypotheses as if they were predefined is called HARKing (hypothesizing after the results are known).
- **SOTA (state of the art)** — the best currently known result or method for a task. A claim of beating SOTA requires strong baselines and an equal tuning budget.
- **Tuning budget** — the amount of compute, time, or number of trials spent on hyperparameter search. A comparison is fair only if the new method and the baselines get a comparable budget.
- **EQUATOR Network** — an international initiative to improve the quality and transparency of research reporting (primarily in health research). It maintains a database of reporting guidelines and helps choose the right one for a given design.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
- **COPE (Committee on Publication Ethics)** — an international organization that publishes standards of publication ethics (Core Practices) and guidance for editors, authors, and reviewers, including on authorship, conflicts of interest, and corrections to the published record.
