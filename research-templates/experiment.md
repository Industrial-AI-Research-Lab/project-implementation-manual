# Experimental Protocol Template

Complete and fix the protocol before the main data collection or benchmark run. A pilot should test the procedure rather than quietly turning into the main experiment. Substantive changes made after viewing the results are recorded in the deviation log.

## 0. Protocol card

- ★ Title and ID: [EXP-001]
- ★ Version, date, author: [ ]
- ★ Related RQs/Hs: [links]
- ★ Status: [draft / approved / running / completed / stopped]
- ★ Type: [randomized / quasi-experiment / observational / simulation / benchmark / qualitative / mixed]
- Preregistration: [link/not applicable, with an explanation]
- Required approvals: [ethics/data/security/environment owner]

## 1. Objective and logic

- ★ Objective: [what uncertainty it resolves]
- ★ Experimental unit: [the unit independently assigned to a condition]
- ★ Observational unit: [may differ]
- ★ Inference population: [whom/what the conclusions are about]
- ★ Intervention/factor: [exact description]
- ★ Comparator/control: [current practice, placebo, no-treatment, strong baseline]
- ★ Primary outcome: [definition, units, timing]
- ★ Expected pattern under H1 and the alternatives: [link to the matrix]

## 2. Design

| Element | Decision | Rationale |
|---|---|---|
| Groups/conditions | [ ] | [ ] |
| Factors and levels | [ ] | [ ] |
| Between/within/mixed | [ ] | [ ] |
| Presentation order | [ ] | [ ] |
| Randomization | [unit, algorithm, seed, concealment] | [ ] |
| Blocking/stratification | [variables] | [ ] |
| Blinding | [who is blinded to what] | [ ] |
| Confounding control | [design/analysis] | [ ] |
| Replicates | [biological/technical/independent seeds] | [ ] |

Do not call repeated measurements of the same experimental unit independent replications.

## 3. Sample and power/precision

- ★ Recruitment/selection method: [sampling frame and procedure]
- ★ Inclusion criteria: [before access to the outcome]
- ★ Exclusion criteria: [before access to the outcome]
- ★ Planned n per group/number of runs: [ ]
- ★ Justification of n: [minimal important effect, variance, power/precision, simulation, saturation, or resource constraint]
- ★ Level of clustering/dependence: [and how it is accounted for in the calculation]
- Expected attrition/failures: [magnitude and reserve]
- Interim analyses: [none / schedule and error control]

If the sample size is determined by resources, state what precision it actually provides and which effects will remain indistinguishable.

## 4. Variables and measurements

| Variable | Role | Operationalization | Instrument/version | Units | Timing | QC |
|---|---|---|---|---|---|---|
| [ ] | [primary/secondary/covariate] | [ ] | [ ] | [ ] | [ ] | [ ] |

- ★ Primary outcome: [one or a small, predefined number]
- Secondary outcomes: [list]
- Exploratory outcomes: [explicit labeling]
- Measurement validity and reliability: [evidence]
- Minimal important change: [value and basis]

## 5. Materials and environment

- Equipment/software/model: [name, version, identifier]
- Configuration: [full file/link]
- Stimuli/questionnaires/instructions: [link and license]
- Data: [version, checksum, split]
- Hardware and system environment: [CPU/GPU/RAM/OS/runtime]
- External services: [version/API/date; risk of change]
- Calibration/authentication of resources: [procedure]

## 6. Step-by-step procedure

| Step | Performer | Input | Action | Output | Check | Time |
|---|---|---|---|---|---|---|
| 1 | [role/script] | [ ] | [unambiguous command/procedure] | [ ] | [criterion] | [ ] |

Include:

1. preparing and checking the environment;
2. obtaining/assigning units;
3. delivering the intervention or executing the run;
4. collecting raw data without manual "cleaning";
5. QC and documenting exclusions;
6. freezing the data/version;
7. handing off to analysis without changing the primary plan.

## 7. Pilot plan

- Pilot objective: [feasibility, variance, time, understanding of instructions — not confirmation of H]
- Size and source of data: [ ]
- Which parts may be changed after the pilot: [ ]
- Which pilot results will not be included in the main analysis: [ ]
- Criterion for proceeding to the main experiment: [ ]
- How changes will be incorporated into a new protocol version: [ ]

## 8. Handling problematic observations

- Missing data: [prevention, flagging, analysis]
- Outliers: [definition without looking at the group/outcome, main and sensitivity analysis]
- Protocol violations: [categories and actions]
- Failed runs: [technical criterion set before the result]
- Duplicates/contamination/leakage: [detection]
- Manual decisions: [who, whether blinded, log]

Never remove an observation solely because it weakens the expected effect.

## 9. Stopping rules and monitoring

| Signal | Threshold | Action | Who decides | Is unblinding/blinding break required |
|---|---|---|---|---|
| Safety | [ ] | [stop/pause] | [ ] | [ ] |
| Data quality | [ ] | [ ] | [ ] | [ ] |
| Feasibility/resources | [ ] | [ ] | [ ] | [ ] |
| Futility/efficacy | [only with a proper plan] | [ ] | [ ] | [ ] |

Stopping "once the result becomes significant" without a sequential plan and error control is not acceptable.

## 10. Analysis plan and decision criteria

- ★ Frozen analysis plan: [link and hash/version]
- ★ Primary contrast/estimand: [ ]
- ★ Effect and uncertainty: [ ]
- ★ Assumption checks: [ ]
- ★ Multiplicity: [ ]
- ★ Robustness/sensitivity checks: [ ]
- ★ Criteria for supported/not supported/inconclusive: [ ]
- Analysis code tested on simulated/toy data: [link]

## 11. Risks, ethics, and privacy

- Potential harm to participants/systems: [ ]
- Consent and the option to withdraw: [ ]
- Personal data minimization: [ ]
- Access, encryption, retention/deletion period: [ ]
- Dual-use/security: [ ]
- Residual risk and owner: [ ]

## 12. Run log

| Run ID | Date | Protocol/commit | Data version | Seed | Condition | Status | Exclusion/incident | Artifacts |
|---|---|---|---|---|---|---|---|---|
| RUN-001 | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

## 13. Deviations

| ID | Date | Plan | Actual | Reason | Results already visible? | Impact | Decision |
|---|---|---|---|---|---|---|---|
| DEV-001 | [ ] | [ ] | [ ] | [ ] | [yes/no] | [ ] | [ ] |

## Pre-launch check

- [ ] The RQs, hypotheses, and primary outcome are consistent with one another.
- [ ] The experimental unit and independent replicates are defined correctly.
- [ ] The control and strong baselines are implemented fairly.
- [ ] Randomization/blocking/blinding are described reproducibly.
- [ ] n is justified by the required precision or honestly limited by resources.
- [ ] Exclusion, missing data, outliers, and stop rules are set before the result.
- [ ] The pilot is separated from the main confirmatory set.
- [ ] The analysis code has been tested on toy/simulated data.
- [ ] Risks and approvals are resolved.
- [ ] The environment, versions, and seeds will be recorded for each run.

Methodological basis: [OSF Registrations](https://help.osf.io/article/330-welcome-to-registrations), [NIH Rigor and Reproducibility](https://www.grants.nih.gov/policy-and-compliance/policy-topics/reproducibility), [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines), [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Benchmark** — a standardized set of tasks, data, and metrics for comparing methods under identical conditions. Success on one benchmark does not prove general superiority.
- **Pilot study** — a small preliminary run to check the procedure, instruments, and feasibility. Its results should not be used to confirm hypotheses.
- **Deviation log** — a dated list of changes to the frozen protocol or analysis plan: what changed, why, whether results were already visible, and how this affects interpretation. It lets readers tell what was planned from what changed along the way.
- **Quasi-experiment** — a study of an intervention without random assignment of conditions. It requires additional measures against confounding, so its causal conclusions are weaker than those of a randomized experiment.
- **Preregistration** — a time-stamped record of hypotheses, design, and analysis plan made before data are collected or examined, usually in a public registry. It makes it possible to separate confirmatory from exploratory analysis.
- **Experimental unit** — the smallest entity that independently receives an experimental condition. Repeated measurements of one unit are not independent replicates.
- **Observational unit** — the entity on which a measurement is actually taken. It may differ from the experimental unit: for example, a condition is assigned to a class, but students are measured.
- **Baseline** — the reference point for comparison: current practice, or a simple or strong existing method. A new method's gain is meaningful only relative to a fairly tuned, strong baseline.
- **Between-subjects, within-subjects, and mixed design** — in a between-subjects design each unit receives one condition; in a within-subjects design it receives all conditions in turn; a mixed design combines both. A within-subjects design requires control of presentation order.
- **Randomization** — random assignment of units to experimental conditions. On average it balances known and unknown factors and thus protects against confounding.
- **Seed (random seed)** — the initial value of a pseudorandom number generator. Fixing the seed makes random steps repeatable, and running with several seeds shows how much the result varies.
- **Allocation concealment** — measures that prevent anyone from knowing in advance or influencing which condition the next unit will receive. It protects randomization from deliberate or unconscious selection.
- **Blocking** — grouping similar units (for example, by day, equipment, or dataset) and assigning all conditions within each group. It reduces noise from known sources of variation.
- **Stratification** — dividing a sample into subgroups (strata) by important characteristics and randomizing or sampling within each, so that groups are balanced on those characteristics.
- **Blinding** — withholding from participants, staff, or analysts which condition a unit received, so that expectations do not influence measurements and decisions.
- **Confounding (confounder)** — a third variable that affects both the exposure and the outcome, so that the association between them can look causal when it is not.
- **Replicates** — repetitions of a measurement or experiment. Technical replicates measure the same unit several times and show measurement noise; independent replicates (new units, biological samples, seeds) show variation in the effect itself.
- **Sampling frame** — the list or mechanism from which sample units are actually drawn. A mismatch between it and the target population creates coverage bias.
- **Smallest effect size of interest (SESOI)** — the smallest effect size that matters in practice for the decision. It is set in advance on domain grounds and serves as the threshold of practical significance.
- **Statistical power** — the probability of detecting an effect of a given size if it truly exists. Power analysis is used to justify the sample size.
- **Clustering** — a situation in which observations are grouped (students in classes, queries from one user, repeated measurements of one unit) and therefore not independent. Ignoring it understates uncertainty.
- **Interim analysis** — analysis of accumulated data before an experiment is complete. It is acceptable only under a predefined plan with error control; otherwise it raises the risk of a false positive.
- **Covariate** — a variable that is not the focus of the study but may affect the outcome; it is accounted for in the design or model to improve precision or control confounding.
- **Freezing (frozen)** — locking a version of the protocol, analysis plan, data, or split, after which changes are allowed only through the deviation log. It protects against fitting the analysis to the result.
- **Outliers** — observations that differ sharply from the rest. The rule for handling them is set before the results are seen: removing "inconvenient" points distorts the conclusion.
- **Data leakage** — information from test or confirmation data reaching training, tuning, or analysis choices. It inflates performance estimates and leads to false conclusions.
- **Stopping for futility or efficacy** — ending an experiment early when an effect is almost certainly not going to be detected (futility) or has already been convincingly shown (efficacy). It is valid only under a sequential design with error control.
- **Estimand** — a precise definition of what is being estimated: the population, outcome, conditions compared, summary measure, and handling of intercurrent events. Without it, the same "effect" can mean different quantities.
- **Multiple comparisons (multiplicity)** — a situation in which many hypotheses, metrics, or subgroups are tested. The probability of at least one false positive grows, so a predefined control method is needed.
- **Robustness checks** — repeating the analysis under other plausible choices (model specification, metric, exclusion rules, subsets) to confirm that the substantive conclusion does not depend on them.
- **Sensitivity analysis** — assessing how much the result changes when assumptions or debatable analytic choices change, for example the handling of missing data or outliers.
- **Dual-use** — knowledge, technology, or artifacts created for beneficial purposes that can also be used to cause harm, for example for attacks or circumventing safeguards.
- **OSF (Open Science Framework)** — a free platform from the Center for Open Science for storing project materials and registering them, including study preregistrations and review protocols.
- **NIH Rigor and Reproducibility** — requirements and guidance of the U.S. National Institutes of Health (NIH) on scientific rigor: a sound premise, rigorous design, consideration of relevant biological variables, and authentication of key resources.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
