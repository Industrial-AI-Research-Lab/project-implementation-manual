# Template for Generating and Testing Hypotheses

A hypothesis is a testable claim, not merely an interesting idea. A strong hypothesis links a proposed mechanism to an observable prediction, allows for refutation in advance, and competes with alternative explanations.

## 1. Source of hypotheses

- ★ Related RQ: [ID and link]
- ★ Observation/anomaly: [what needs to be explained]
- ★ Theory or mechanism: [why this might be happening]
- Basis: [literature, data, expert knowledge, analogy]
- Source status: [reliable evidence / preliminary / conjecture]

## 2. Divergent generation

Before ranking, generate several explanations of different types:

- a mechanism that directly produces the effect;
- an alternative mechanism with the same observable result;
- a confounding factor or selection effect;
- an error in measurement, labeling, or analysis;
- an artifact of the data, preprocessing, or leakage;
- the absence of a stable effect/random variation;
- a boundary condition: the effect exists only in some contexts;
- for an engineering problem, a simpler baseline that could explain the gain.

Do not filter ideas by how desirable the conclusion is. Ask separately: "What would the data look like if our favorite hypothesis were wrong?"

## 3. Hypothesis card

### H[number]: [short name]

- ★ Statement: [X leads to / is associated with / predicts Y under conditions C]
- ★ Type: [descriptive / associative / causal / mechanistic / predictive / engineering]
- ★ Mechanism: [chain of causes or operations]
- ★ Population and conditions: [where it is expected]
- ★ Observable prediction: [direction, magnitude/pattern, timing]
- ★ Comparator: [what it is compared with]
- ★ Result that contradicts the hypothesis: [what would reduce confidence]
- ★ Result that does not distinguish the hypotheses: [what would be ambiguous]
- ★ Key assumptions: [list]
- ★ Alternative explanations: [Halt1, Halt2]
- ◇ Boundary conditions: [where the effect disappears/changes sign]
- ◇ Prior confidence: [low/medium/high + basis]
- ◇ Potential harm from wrongly accepting/rejecting it: [consequences]

### Logical chain

`If mechanism M holds under C → intermediate state Z arises → we observe Y on metric K relative to B.`

Check every arrow: is there a step that admits another explanation?

## 4. Matrix for distinguishing alternatives

| Possible result | H1 | H2 | H3 | Error/artifact | How to measure |
|---|---|---|---|---|---|
| R1: [pattern] | [expected] | [not expected] | [partially] | [possible] | [test] |
| R2: [pattern] | [ ] | [ ] | [ ] | [ ] | [ ] |

Choose an experiment whose results are expected to differ under competing hypotheses. Confirming a pattern shared by all of them provides little information.

## 5. Operationalizing the prediction

| Element | Definition before the experiment |
|---|---|
| Independent variable/condition | [ ] |
| Dependent variable/outcome | [ ] |
| Primary metric | [formula, units, direction] |
| Practically important magnitude | [threshold + basis] |
| Time window | [ ] |
| Population/subgroup | [ ] |
| Control/baseline | [ ] |
| Supporting evidence | [ ] |
| Refuting evidence | [ ] |
| Uncertainty | [when the data are insufficient] |

## 6. Prioritizing hypotheses

| H | Importance for the decision | Distinguishability | Information value | Cost | Risk | Priority and rationale |
|---|---|---|---|---|---|---|
| H1 | [1–5] | [1–5] | [1–5] | [1–5] | [1–5] | [text] |

Recommendation: first test inexpensive hypotheses that can refute a key assumption or distinguish between several alternatives. The numerical scale is a tool for discussion, not an objective scientific score.

## 7. Confirmatory and exploratory

### Before viewing the main results

- ★ Fixed primary hypotheses: [IDs]
- ★ Date fixed: [date/link to registration]
- ★ Analysis plan and decision criteria: [link]
- ★ What was already known about the data: [list]

### After viewing the data

- New hypotheses: [IDs marked as exploratory]
- The observation that generated them: [what was seen]
- Plan for independent testing: [new data/holdout/replication]

A new hypothesis may be valuable, but a result on the same data is hypothesis generation, not an independent test.

## 8. Test result

| H | Predicted result | Observed result | Size/uncertainty | Alternatives | Status |
|---|---|---|---|---|---|
| H1 | [ ] | [ ] | [ ] | [which remain] | [supported / weakened / indistinguishable / not tested] |

Avoid the wording "the hypothesis is proven". A single test usually changes the degree of confidence and the set of plausible explanations.

## Quality check

- [ ] The hypothesis admits an observation that would reduce confidence in it.
- [ ] The mechanism is linked to a measurable prediction.
- [ ] The conditions of applicability and the comparator are specified.
- [ ] At least two plausible alternatives are considered, or their absence is justified.
- [ ] The experiment distinguishes between hypotheses rather than only showing the expected pattern.
- [ ] The practical threshold is defined before the result.
- [ ] Confirmatory and exploratory hypotheses are labeled honestly.
- [ ] A null/negative result can be published and interpreted.

## Common mistakes

- "H1: method A is better" without a metric, magnitude, conditions, or baseline.
- A statistical null hypothesis is passed off as a substantive theory.
- A post hoc explanation is invented for any result, so the hypothesis is effectively unfalsifiable.
- Only the favorite hypothesis is tested, while measurement error and leakage are not considered.
- The absence of a significant result is treated as proof of equality without an analysis of precision/equivalence.

Methodological basis: [OSF Registrations](https://help.osf.io/article/330-welcome-to-registrations), [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines), [NIH Rigor and Reproducibility](https://www.grants.nih.gov/policy-and-compliance/policy-topics/reproducibility).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Falsifiability** — the property of a hypothesis for which an observation that would refute it can be named in advance. A hypothesis compatible with any result tests nothing.
- **Confounding (confounder)** — a third variable that affects both the exposure and the outcome, so that the association between them can look causal when it is not.
- **Selection effect** — a distortion that arises when the way units enter a sample or group is related to the outcome. The observed effect may reflect who was selected rather than the intervention.
- **Preprocessing** — transformations applied to data before analysis or training: cleaning, normalization, filtering, and encoding. Errors or use of test data at this stage can create a spurious effect.
- **Data leakage** — information from test or confirmation data reaching training, tuning, or analysis choices. It inflates performance estimates and leads to false conclusions.
- **Baseline** — the reference point for comparison: current practice, or a simple or strong existing method. A new method's gain is meaningful only relative to a fairly tuned, strong baseline.
- **Comparator** — what an intervention or method is compared against: a control group, current practice, a placebo, or a baseline.
- **Boundary conditions** — the conditions beyond which an effect disappears or reverses and the conclusion no longer applies.
- **Prior belief** — the degree of confidence in a hypothesis before testing, based on literature and preliminary data. Writing it down helps assess honestly how much the result changed understanding.
- **Independent and dependent variable** — the independent variable is the condition or factor the researcher varies or compares; the dependent variable is the outcome measured in response.
- **Confirmatory analysis** — analysis whose hypotheses and rules were fixed before the results were seen. Only such analysis supports a claim that a hypothesis was tested.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Preregistration** — a time-stamped record of hypotheses, design, and analysis plan made before data are collected or examined, usually in a public registry. It makes it possible to separate confirmatory from exploratory analysis.
- **Out-of-sample (hold-out) validation** — evaluating a model or conclusion on data that were not used to build, tune, or select the model. Only such validation honestly shows predictive performance.
- **Replication (replicability)** — testing the same scientific question with new data, often by another team, in another setting, or with another implementation. Consistent results increase confidence in the conclusion.
- **Null hypothesis** — a statistical statement of no effect or no difference against which a p-value is computed. It is a technical part of a statistical test, not a substantive scientific theory.
- **Post hoc explanation** — an explanation devised after the result is known. If any outcome can be explained this way, the hypothesis is effectively unfalsifiable; presenting such hypotheses as if they were predefined is called HARKing (hypothesizing after the results are known).
- **Measurement error** — the difference between a measured and a true value. Systematic measurement error can mimic or mask an effect.
- **Equivalence testing** — testing whether a difference lies within preset margins of practical irrelevance. Only this, not the absence of a significant result, can justify a conclusion that there is no important difference.
- **OSF (Open Science Framework)** — a free platform from the Center for Open Science for storing project materials and registering them, including study preregistrations and review protocols.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
- **NIH Rigor and Reproducibility** — requirements and guidance of the U.S. National Institutes of Health (NIH) on scientific rigor: a sound premise, rigorous design, consideration of relevant biological variables, and authentication of key resources.
