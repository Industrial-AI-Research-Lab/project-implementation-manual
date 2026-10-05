# Research Questions and Success Criteria Template

A good research question links a knowledge gap to observable data and a permissible conclusion. It does not have to be a hypothesis: descriptive, qualitative, and design studies may begin with an open question.

## 1. From problem to question

- ★ Problem: [brief reference to the research brief]
- ★ Known: [what is already reliably established]
- ★ Unknown: [one specific gap in knowledge]
- ★ Decision/contribution: [what will change after the answer]

> In **[population/system/context]**, how/to what extent/why is **[phenomenon or intervention]** associated with **[outcome]** compared with **[control/alternative]** over **[period]**?

Use only the elements that fit. PICO/PICOS is useful for comparative questions; PCC for a scoping review; for qualitative work, explicitly state the phenomenon, participants, and context.

## 2. Question classification

| Type | Typical form | What is required to answer |
|---|---|---|
| Descriptive | What, how many, how is it distributed? | A defined population, measurement, and sample |
| Comparative | How does A differ from B? | Comparable conditions, a baseline, the magnitude of the difference |
| Causal | What is the effect of X on Y? | An identification strategy and control of confounding |
| Predictive | How accurately does X predict Y? | Held-out validation, calibration, absence of leakage |
| Explanatory | What mechanism links X and Y? | Distinguishable mechanistic predictions |
| Design/optimization | Which method achieves the goal under the constraints? | An objective function, constraints, baselines, robustness |
| Qualitative | How do participants understand or experience the phenomenon? | A justified sample, a data collection procedure, and reflexive analysis |
| Theoretical | Does the claim follow from the assumptions? | Complete assumptions, definitions, a proof/counterexample |

## 3. Question register

| ID | Priority | Question | Type | Unit of analysis | Context/scope | Decision |
|---|---|---|---|---|---|---|
| RQ1 | primary | [statement] | [type] | [unit] | [conditions] | [what will change] |
| RQ2 | secondary | [statement] | [type] | [unit] | [conditions] | [what will change] |
| RQX1 | exploratory | [statement] | [type] | [unit] | [conditions] | [generating a future hypothesis] |

Limit the number of primary questions. If every outcome is declared primary, there are effectively no priorities.

## 4. Operationalizing concepts

| Construct | Conceptual definition | Observable variable/metric | Units | Validity | Limitation |
|---|---|---|---|---|---|
| [for example, quality] | [what it means] | [how it is measured] | [units] | [why it reflects the construct] | [what it does not reflect] |

- ★ Experimental/observational unit: [definition]
- ★ Inference population: [whom/what we want to draw conclusions about]
- ★ Sample: [what we actually observe]
- ★ Exposure/intervention: [precise definition]
- ★ Comparator/baseline: [precise definition]
- ★ Outcome and time of measurement: [precise definition]
- Potential proxies and construct validity risk: [description]

## 5. The "question → evidence → conclusion" chain

For each primary question, fill in:

### RQ[number]: [question]

- ★ Data: [what observations are needed]
- ★ Contrast: [what is compared with what]
- ★ Method: [how the answer is extracted]
- ★ Primary estimate: [estimand/metric]
- ★ Uncertainty: [interval, distribution, qualitative saturation, etc.]
- ★ Assumptions: [what must be true]
- ★ Supporting result: [not only the direction, but the magnitude/pattern]
- ★ Refuting result: [what contradicts the expectation]
- ★ Inconclusive result: [what does not allow choosing between explanations]
- ★ Permissible conclusion: [exact wording]
- Impermissible broader conclusion: [extrapolation that the data do not support]

## 6. Success criteria

Distinguish four kinds of criteria:

| Kind | Statement | Threshold/rule | Basis |
|---|---|---|---|
| Scientific | [to what extent the question is resolved] | [precision/distinguishability of alternatives] | [why] |
| Practical | [an effect that changes the decision] | [magnitude and units] | [cost/value] |
| Methodological | [quality of the measurement/procedure] | [reliability, coverage, error] | [standard] |
| Operational | [deadline/resource] | [constraint] | [context] |

Statistical significance by itself is not a practical criterion. The threshold should follow from the cost of errors, the minimal important effect, or the required precision.

## 7. Validity boundaries

- Internal validity: [which alternative causes are ruled out and how]
- External validity: [to which populations/conditions the conclusion can be transferred]
- Construct validity: [how well the measurements correspond to the concepts]
- Statistical conclusion validity: [what precision and robustness are required]
- Temporal validity: [how quickly the conclusion may become outdated]

## 8. Prioritization

Assess not "interestingness" but the expected value of the answer:

| RQ | Impact on the decision | Current uncertainty | Distinguishability of answers | Cost/time | Priority |
|---|---|---|---|---|---|
| RQ1 | [1–5] | [1–5] | [1–5] | [1–5] | [justification] |

Numbers help the discussion, but they do not turn subjective assessments into objective truth. Keep the written justification.

## Quality check

- [ ] The question cannot be replaced by an answer already built into its wording.
- [ ] The inference population and the actual sample are defined.
- [ ] Concepts are operationalized; the metric does not substitute for the construct without discussion.
- [ ] For a causal question, the identification strategy is described.
- [ ] For a predictive question, an honest out-of-sample validation is planned.
- [ ] Supporting, refuting, and inconclusive outcomes are defined in advance.
- [ ] The practical significance criterion has a domain-specific basis.
- [ ] The conclusion is limited to the conditions under which the evidence was obtained.

## Common mistakes

- "Does X affect Y?" with purely observational data and no causal inference strategy.
- The metric is convenient but has not been validated as a measure of the intended concept.
- The inference population is broader than the sample without an argument for transferability.
- The question is rewritten after the result as if it had been posed in advance.
- Success is defined as "p < 0.05" without an effect size, uncertainty, or the cost of the decision.

Methodological basis: [NIH Rigor and Reproducibility](https://www.grants.nih.gov/policy-and-compliance/policy-topics/reproducibility), [ASA Statement on Statistical Significance and P-Values](https://www.amstat.org/asa/files/pdfs/p-valuestatement.pdf), [JBI Manual for Evidence Synthesis](https://jbi-global-wiki.refined.site/download/attachments/355599504/JBI%20Manual%20for%20Evidence%20Synthesis%202024.pdf).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **PICO/PICOS** — a framework for formulating a comparative question: Population, Intervention, Comparator, Outcome; PICOS adds Study design.
- **PCC (Population, Concept, Context)** — a framework for formulating a scoping review question: the population, the concept studied, and the context.
- **Scoping review** — a review that maps the extent, types, and gaps of the literature on a broad topic, usually without pooling results quantitatively.
- **Baseline** — the reference point for comparison: current practice, or a simple or strong existing method. A new method's gain is meaningful only relative to a fairly tuned, strong baseline.
- **Identification strategy** — the justification for why an observed difference can be interpreted as a causal effect rather than a result of confounding or selection, for example through randomization or a natural experiment.
- **Confounding (confounder)** — a third variable that affects both the exposure and the outcome, so that the association between them can look causal when it is not.
- **Out-of-sample (hold-out) validation** — evaluating a model or conclusion on data that were not used to build, tune, or select the model. Only such validation honestly shows predictive performance.
- **Calibration** — the agreement between predicted probabilities and observed frequencies: among cases with a 70% forecast, the event should occur in about 70% of them.
- **Data leakage** — information from test or confirmation data reaching training, tuning, or analysis choices. It inflates performance estimates and leads to false conclusions.
- **Robustness checks** — repeating the analysis under other plausible choices (model specification, metric, exclusion rules, subsets) to confirm that the substantive conclusion does not depend on them.
- **Reflexivity** — in qualitative research, systematic reflection on how the researcher's position, experience, and expectations influence data collection and interpretation.
- **Unit of analysis** — the entity on which results are computed and interpreted: a person, query, model, organization, or run. Its choice determines sampling, data splits, and the statistical model.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Operationalization** — translating an abstract concept into a specific measurable variable or metric with a described measurement procedure.
- **Construct** — an abstract concept that cannot be observed directly (for example, "quality", "satisfaction", or "understanding"), so it is measured through observable indicators.
- **Target population** — the set of people, objects, or situations to which a conclusion is meant to apply. It may be broader than the actual sample, in which case generalizing the conclusion needs separate justification.
- **Comparator** — what an intervention or method is compared against: a control group, current practice, a placebo, or a baseline.
- **Proxy** — an indirect indicator used in place of an unavailable direct measurement. It is useful only if its link to the target concept is justified.
- **Construct validity** — the extent to which a metric or measurement actually reflects the concept under study rather than something else.
- **Estimand** — a precise definition of what is being estimated: the population, outcome, conditions compared, summary measure, and handling of intercurrent events. Without it, the same "effect" can mean different quantities.
- **Saturation** — in qualitative research, the point at which new observations or interviews yield hardly any new themes; it is used as a criterion of sample sufficiency.
- **Practical significance** — whether an effect is large enough to change a decision in practice; the threshold is set in advance on domain grounds. It is not the same as statistical significance.
- **Statistical significance** — the conventional conclusion that a p-value is below a preselected threshold (for example, 0.05). It says nothing about the size or practical importance of an effect.
- **Smallest effect size of interest (SESOI)** — the smallest effect size that matters in practice for the decision. It is set in advance on domain grounds and serves as the threshold of practical significance.
- **Internal validity** — the extent to which an observed effect is actually caused by the factor under study rather than by confounding, selection, or measurement error.
- **External validity** — the extent to which a conclusion carries over to populations, settings, and conditions other than those studied.
- **Statistical conclusion validity** — the correctness of statistical inferences: sufficient precision, methods appropriate to the data, and control for multiple comparisons.
- **P-value** — the probability of obtaining data at least as extreme as those observed if the null hypothesis and all model assumptions are true. It is not the probability that a hypothesis is true, nor a measure of an effect's size or importance.
- **NIH Rigor and Reproducibility** — requirements and guidance of the U.S. National Institutes of Health (NIH) on scientific rigor: a sound premise, rigorous design, consideration of relevant biological variables, and authentication of key resources.
- **ASA Statement on Statistical Significance and P-Values** — a 2016 statement by the American Statistical Association on the correct interpretation of p-values, stressing that scientific conclusions should not rest solely on whether a significance threshold is passed.
- **JBI Manual for Evidence Synthesis** — a guide by JBI (formerly the Joanna Briggs Institute) on evidence synthesis methods, including scoping reviews and systematic reviews.
