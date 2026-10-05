# Full Independent Study Template

Use this page as the main project protocol. Details are filled in using the specialized templates, while this page records brief decisions, links, and checkpoints.

## 0. Document card

- ★ Title: [short, specific]
- ★ Version and date: [v0.1, YYYY-MM-DD]
- ★ Author/team and roles: [name — role]
- ★ Decision owner: [who makes the go/no-go decision or approves publication]
- ★ Status: [idea / protocol / data collection / analysis / manuscript / completed]
- Repository/storage link: [URL or reason for restriction]
- Planned output: [publication / technical report / prototype / dataset / decision]
- Type of work: [basic / applied / experimental development / mixed]

## 1. Study summary

Fill in after the design stage but before the main experiment.

> We are studying **[object]** because **[gap or problem]**. The main question is **[question]**. We will test it using **[design and data]**, measuring **[primary metric/outcome]** against **[control/baseline]**. We define in advance as practically significant **[threshold or interval]**. The result will be used for **[decision/contribution]**.

## 2. Problem and scope

- ★ Observed problem: [what is happening; without explaining the causes]
- ★ Why this is a research problem rather than a routine engineering task: [what substantial uncertainty is not resolved by known practice]
- ★ What is already known: [3–7 key points with references]
- ★ What is unknown: [specific gap]
- ★ In scope: [objects, populations, environments, periods]
- ★ Out of scope: [explicit non-goals]
- Decision that will change after the study: [who will choose what]
- Cost of a false-positive and a false-negative conclusion: [consequences]

Details: [Research brief](research-brief.md).

## 3. Questions and success criteria

| ID | Question | Type | Unit of analysis | Required evidence | Answer criterion |
|---|---|---|---|---|---|
| RQ1 | [main question] | [descriptive/causal/comparative/predictive/design] | [unit] | [data and analysis] | [what will allow an answer] |
| RQ2 | [secondary question] | [type] | [unit] | [evidence] | [criterion] |

- ★ Practically significant effect/quality: [magnitude and units]
- ★ Conditions under which the answer is considered inconclusive: [for example, a wide interval or conflicting checks]
- Conditions for transferring the conclusion to other environments: [boundary conditions]

Details: [Research questions](questions.md).

## 4. Grounding in the literature

- ★ Review type: [orienting / scoping / systematic / meta-analysis]
- ★ Search end date: [YYYY-MM-DD]
- ★ Sources and full protocol: [link]
- ★ Key gap: [what existing work does not allow us to conclude]
- Main competing explanations/methods: [list]
- Assessment of quality and risk of bias: [method]

Details: [Literature review](literature-review.md).

## 5. Hypotheses and predictions

| ID | Hypothesis or claim | Mechanism | Observable prediction | What would refute it | Alternative |
|---|---|---|---|---|---|
| H1 | [statement] | [why it is expected] | [measurable consequence] | [result] | [explanation] |

- ★ Status of each hypothesis: [confirmatory, fixed before the result / exploratory, formed afterward]
- ★ Priority: [information value × decision significance ÷ cost]
- ◇ Prior degree of confidence and its basis: [low/medium/high; why]

Details: [Hypotheses](hypotheses.md).

## 6. Testing protocol

- ★ Design: [controlled experiment / quasi-experiment / observational study / simulation / benchmark / qualitative]
- ★ Experimental unit: [what independently receives the condition]
- ★ Intervention/factors and levels: [description]
- ★ Control and baselines: [minimal, strong, current practice]
- ★ Randomization, blocking, blinding: [how, or why not applicable]
- ★ Sample size/number of replicates and justification: [power, required precision, resources]
- ★ Primary outcome and time of measurement: [one or a small number]
- ★ Rules for inclusion, exclusion, missing data, and stopping: [before launch]
- Pilot procedure: [what may and may not be changed after the pilot]
- Deviation plan: [where to record deviations]

Details: [Experimental protocol](experiment.md).

## 7. Data

- ★ Sources and versions: [links/identifiers/access dates]
- ★ Right of use: [license, consent, agreement, restrictions]
- ★ Provenance and transformation chain: [raw → intermediate → analysis]
- ★ Quality and fitness criteria: [completeness, correctness, representativeness, timeliness]
- ★ Train/validation/test or discovery/confirmation split: [how leakage is prevented]
- Personal/sensitive data: [categories and measures]
- Storage, access, backup, and deletion scheme: [DMP]

Details: [Data and datasets](data.md).

## 8. Method or algorithm

- ★ Purpose: [what operation it performs]
- ★ Inputs/outputs and units: [contract]
- ★ Preconditions and assumptions: [when it is applicable]
- ★ Unambiguous steps or pseudocode: [link]
- ★ Parameters and how they are chosen: [without peeking at the test set]
- ★ Randomness and seeds: [sources and control]
- ★ Complexity/resources: [time, memory, compute]
- ★ Baselines, ablations, and failure modes: [list]
- Implementation and test cases: [link]

Details: [Method or algorithm](method-algorithm.md).

## 9. Analysis plan

- ★ Target quantity (estimand): [what exactly is being estimated]
- ★ Primary metric/outcome: [definition and direction of improvement]
- ★ Model/statistical method: [formula or link]
- ★ Effect size and uncertainty: [interval/distribution/error]
- ★ Assumption checks: [diagnostics]
- ★ Multiple comparisons: [family of tests and control]
- ★ Missing data/outliers/exclusions: [rules]
- ★ Sensitivity/robustness analyses: [variants capable of changing the conclusion]
- Exploratory analysis: [will be labeled separately]

Details: [Analysis plan](analysis.md).

## 10. Ethics, safety, and risks

| Risk | Harm to whom/what | Likelihood | Severity | Measure | Residual risk | Owner |
|---|---|---|---|---|---|---|
| [risk] | [group/system] | [estimate] | [estimate] | [control] | [estimate] | [name] |

- ★ Required approval: [ethics committee / data owner / security / legal / not required, with justification]
- ★ Conflicts of interest and funding: [disclosure]
- ★ Incident/stopping procedure: [who decides and how]
- Use of generative AI: [tasks, tool/version, human verification, confidentiality]

Details: [Ethics, safety, and privacy](ethics.md).

## 11. Reproducibility

- ★ Repository and pinned version: [URL + commit/tag/DOI]
- ★ "From a clean environment to the main result" instructions: [link]
- ★ Environment and dependency versions: [lockfile/container/spec]
- ★ Available data, code, materials, and restrictions: [manifest]
- ★ Expected result and acceptable numerical deviation: [value/interval]
- ★ Computational resources and time: [hardware, memory, runtime, cost]
- Independent verification: [who, date, result]

Details: [Reproducibility and artifacts](reproducibility.md).

## 12. Results

Filled in after the protocol is locked.

| Question/hypothesis ID | Estimate | Uncertainty | Robustness checks | Status | Artifact link |
|---|---|---|---|---|---|
| [RQ1/H1] | [effect] | [interval] | [result] | [supported/not supported/inconclusive] | [URL] |

- Unexpected observations: [do not mix with confirmatory results]
- Negative results: [what did not work]
- Protocol deviations: [what, when, why, impact]
- Limitations: [sources of bias, external validity, precision]

## 13. Conclusion and decision

- ★ Answer to each RQ: [one cautious statement]
- ★ Which claims are supported: [with degree of confidence]
- ★ Which are not supported or remain inconclusive: [list]
- ★ Decision: [go / revise / stop / replicate / collect more data]
- ★ What the conclusion does **not** extend to: [boundaries]
- Next most valuable study: [what uncertainty remains]

## 14. Publication package

- [ ] The manuscript/report follows the appropriate disciplinary guideline.
- [ ] There is a "claim → data/analysis/figure" map.
- [ ] The methods allow the work to be repeated.
- [ ] Exploratory and confirmatory results are separated.
- [ ] Effect sizes and uncertainty are reported.
- [ ] Limitations and negative results are visible.
- [ ] There are statements on data, code, ethics, funding, and conflicts of interest.
- [ ] Author contributions are stated according to CRediT or an equivalent scheme.
- [ ] Artifacts have passed an independent smoke test.

Details: [Publication or R&D report](publication.md) and [Review checklists](review.md).

## 15. Checkpoints

| Gate | When | Decision | Minimum evidence |
|---|---|---|---|
| G0 | After problem formulation | Investigate / narrow / stop | A significant gap and a decision owner |
| G1 | Before the main data | Launch / revise the protocol | RQs, hypotheses, design, analysis, risks |
| G2 | After data preparation | Analyze / fix the data | Datasheet, quality report, frozen split/version |
| G3 | After analysis | Conclude / repeat / acknowledge uncertainty | Complete results and robustness checks |
| G4 | Before publication | Publish / revise | Manuscript, artifacts, independent verification |

## Protocol version log

| Version | Date | What changed | Why | Were results already visible | Impact on interpretation |
|---|---|---|---|---|---|
| v0.1 | [date] | [change] | [reason] | [yes/no] | [impact] |

Methodological basis: [OSF Registrations](https://help.osf.io/article/330-welcome-to-registrations), [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines), [NIH Rigor and Reproducibility](https://www.grants.nih.gov/policy-and-compliance/policy-topics/reproducibility), [National Academies](https://www.nationalacademies.org/read/25303/chapter/2).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Go/no-go** — a decision at a project checkpoint on whether to continue, revise, or stop the work based on the evidence obtained.
- **Baseline** — the reference point for comparison: current practice, or a simple or strong existing method. A new method's gain is meaningful only relative to a fairly tuned, strong baseline.
- **Practical significance** — whether an effect is large enough to change a decision in practice; the threshold is set in advance on domain grounds. It is not the same as statistical significance.
- **Non-goals** — an explicit list of what a study or method deliberately does not address. It helps keep the scope of the work in check and prevents overreaching conclusions.
- **Unit of analysis** — the entity on which results are computed and interpreted: a person, query, model, organization, or run. Its choice determines sampling, data splits, and the statistical model.
- **Boundary conditions** — the conditions beyond which an effect disappears or reverses and the conclusion no longer applies.
- **Scoping review** — a review that maps the extent, types, and gaps of the literature on a broad topic, usually without pooling results quantitatively.
- **Systematic review** — a review that answers a narrow question following a predefined protocol: comprehensive search, explicit selection criteria, risk-of-bias assessment, and synthesis. The process must be repeatable from the saved protocol.
- **Meta-analysis** — statistical pooling of comparable quantitative results from several studies into an overall effect estimate that accounts for their precision and the differences between them.
- **Risk of bias** — an assessment of how much features of a study's design or conduct could systematically distort its result. In reviews it is judged domain by domain using dedicated tools.
- **Confirmatory analysis** — analysis whose hypotheses and rules were fixed before the results were seen. Only such analysis supports a claim that a hypothesis was tested.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Prior belief** — the degree of confidence in a hypothesis before testing, based on literature and preliminary data. Writing it down helps assess honestly how much the result changed understanding.
- **Quasi-experiment** — a study of an intervention without random assignment of conditions. It requires additional measures against confounding, so its causal conclusions are weaker than those of a randomized experiment.
- **Benchmark** — a standardized set of tasks, data, and metrics for comparing methods under identical conditions. Success on one benchmark does not prove general superiority.
- **Experimental unit** — the smallest entity that independently receives an experimental condition. Repeated measurements of one unit are not independent replicates.
- **Randomization** — random assignment of units to experimental conditions. On average it balances known and unknown factors and thus protects against confounding.
- **Blocking** — grouping similar units (for example, by day, equipment, or dataset) and assigning all conditions within each group. It reduces noise from known sources of variation.
- **Blinding** — withholding from participants, staff, or analysts which condition a unit received, so that expectations do not influence measurements and decisions.
- **Statistical power** — the probability of detecting an effect of a given size if it truly exists. Power analysis is used to justify the sample size.
- **Train/validation/test split** — dividing data into a part for training, a part for tuning and model selection, and a held-out part for the final evaluation. For studies without model training, the analogue is discovery/confirmation: data for finding hypotheses and separate data for testing them.
- **Data leakage** — information from test or confirmation data reaching training, tuning, or analysis choices. It inflates performance estimates and leads to false conclusions.
- **DMP (Data Management Plan)** — a document describing how data will be collected, documented, stored, protected, shared, and deleted during and after a project.
- **Seed (random seed)** — the initial value of a pseudorandom number generator. Fixing the seed makes random steps repeatable, and running with several seeds shows how much the result varies.
- **Ablation (ablation study)** — an experiment in which a component of a method is removed or replaced to test its contribution to the overall gain.
- **Failure modes** — the conditions under which a method performs poorly or breaks, and how this shows up. Describing them explicitly shows the limits of applicability.
- **Estimand** — a precise definition of what is being estimated: the population, outcome, conditions compared, summary measure, and handling of intercurrent events. Without it, the same "effect" can mean different quantities.
- **Multiple comparisons (multiplicity)** — a situation in which many hypotheses, metrics, or subgroups are tested. The probability of at least one false positive grows, so a predefined control method is needed.
- **Sensitivity analysis** — assessing how much the result changes when assumptions or debatable analytic choices change, for example the handling of missing data or outliers.
- **Robustness checks** — repeating the analysis under other plausible choices (model specification, metric, exclusion rules, subsets) to confirm that the substantive conclusion does not depend on them.
- **Lockfile and container** — a lockfile pins the exact versions of all dependencies; a container (for example, a Docker image) packages the entire software environment, and the image digest uniquely identifies its version. Both make it possible to run the code in the same environment later or on another machine.
- **Manifest** — a list of files or artifacts with their purpose, version or checksum, license, and access conditions. It makes it possible to verify that a package is complete and unchanged.
- **Freezing (frozen)** — locking a version of the protocol, analysis plan, data, or split, after which changes are allowed only through the deviation log. It protects against fitting the analysis to the result.
- **External validity** — the extent to which a conclusion carries over to populations, settings, and conditions other than those studied.
- **Reporting guideline** — a checklist of what a publication must describe for a given study design, for example CONSORT for randomized trials or PRISMA for systematic reviews. It helps avoid omitting essential details of methods and results.
- **CRediT (Contributor Roles Taxonomy)** — a standard taxonomy of 14 contributor roles in research (for example, Conceptualization, Methodology, Software, Formal analysis) that makes each author's contribution explicit.
- **Smoke test** — a quick basic check that a package installs and its main workflow runs without errors. It does not replace full verification of the results.
- **Gate (checkpoint)** — a predefined project stage at which a decision to continue, revise, or stop the work is made based on a minimum set of evidence.
- **Datasheet** — a standardized description of a dataset: purpose, composition, provenance, collection, labeling, limitations, and recommended uses. It is based on the Datasheets for Datasets approach.
- **OSF (Open Science Framework)** — a free platform from the Center for Open Science for storing project materials and registering them, including study preregistrations and review protocols.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
- **NIH Rigor and Reproducibility** — requirements and guidance of the U.S. National Institutes of Health (NIH) on scientific rigor: a sound premise, rigorous design, consideration of relevant biological variables, and authentication of key resources.
- **National Academies** — the U.S. National Academies of Sciences, Engineering, and Medicine. Their report "Reproducibility and Replicability in Science" (2019) provides widely used definitions of reproducibility and replicability and recommendations for achieving them.
