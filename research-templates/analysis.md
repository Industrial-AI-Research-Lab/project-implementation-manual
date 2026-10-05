# Analysis Plan, Metrics, and Uncertainty Template

Fix the primary analysis before looking at the final data. The plan does not have to forbid investigating unexpected patterns; it must clearly separate pre-specified conclusions from subsequent exploratory findings.

## 0. Analysis card

- ★ Version/date/author: [ ]
- ★ Related RQ/H/protocol: [links]
- ★ Data version/split manifest: [ ]
- ★ Status: [draft / frozen / amended / executed]
- ★ What was known at the time of freezing: [aggregates, pilot, labels]
- Code/repository/commit: [ ]

## 1. Inference chain

| RQ/H | Estimand/target quantity | Data | Contrast | Method | Permissible conclusion |
|---|---|---|---|---|---|
| RQ1/H1 | [what is being estimated] | [ ] | [A−B/other] | [ ] | [exact wording] |

### Defining the estimand

- Population: [ ]
- Variable/outcome: [ ]
- Conditions/intervention: [ ]
- Contrast: [ ]
- Handling of intercurrent events/missing data: [ ]
- Time horizon: [ ]

Without an estimand, the same "effect" can refer to different quantities.

## 2. Outcomes and metrics

| Metric/outcome | Role | Formula | Units | Direction | Aggregation | Practical threshold |
|---|---|---|---|---|---|---|
| [ ] | [primary/secondary/exploratory] | [ ] | [ ] | [↑/↓] | [ ] | [ ] |

- ★ One primary outcome or a justified small family: [ ]
- ★ Why the metric is valid for the construct: [ ]
- ★ Minimally important difference: [domain rationale]
- Ceiling/floor/saturation of the metric: [ ]
- Trade-offs between metrics: [how they are resolved]

## 3. Descriptive analysis

Before drawing conclusions, show the data:

- the flow of observations and the reasons for exclusions;
- group/cluster sizes and exposure;
- distributions, missing values, and extreme values;
- baseline characteristics and possible imbalance;
- quality of measurements and labels;
- plots of individual values/distributions, not only means.

Table 1 must not be used as an automatic battery of tests for "baseline equality" without a substantive reason.

## 4. Primary model/procedure

- ★ Method: [name + formula/algorithm]
- ★ Outcome distribution/link/loss: [ ]
- ★ Predictors/factors/covariates: [complete list and coding]
- ★ Interactions/nonlinearity: [pre-specified]
- ★ Clustering/repeated measures: [levels and model]
- ★ Weights/offsets/exposure: [ ]
- ★ Estimation/inference: [frequentist/Bayesian/randomization-based/other]
- ★ Software/package/version and key parameters: [ ]
- Reason for the choice: [fit with the design and the estimand]

## 5. Uncertainty and decision criteria

- ★ Point estimate/distribution: [ ]
- ★ Interval and level/credible interval: [ ]
- ★ Source of uncertainty: [sampling, seeds, measurement, model]
- ★ Practical threshold: [ ]
- ★ "Supported" decision: [joint rule for the effect, interval, and robustness]
- ★ "Not supported" decision: [ ]
- ★ "Inconclusive" decision: [ ]
- Equivalence/non-inferiority, if the goal is to show the absence of an important difference: [margin and rationale]

A p-value is not the probability that a hypothesis is true and does not measure the size or importance of an effect. Report the estimate, uncertainty, assumptions, and decision context.

## 6. Sample size/number of repetitions

- Purpose of the calculation: [power / interval width / probability of a correct decision / saturation]
- Assumed effect/variance and its source: [ ]
- Alpha/Type I error, if used: [ ]
- Power/Type II error, if used: [ ]
- Clustering/design effect: [ ]
- Multiplicity/interim adjustment: [ ]
- Required and available n: [ ]
- What will remain indistinguishable with the available n: [ ]

For a computational benchmark, account for variance across seeds/tasks/datasets, not only the number of rows in the test set.

## 7. Missing data, exclusions, and outliers

| Situation | Diagnostics | Primary analysis | Sensitivity analysis | Reporting |
|---|---|---|---|---|
| Missing outcome | [ ] | [ ] | [ ] | [n/%] |
| Missing covariate | [ ] | [ ] | [ ] | [ ] |
| Outlier | [pre-specified rule] | [ ] | [with/without] | [ ] |
| Protocol violation | [ ] | [ITT/per-protocol/other] | [ ] | [ ] |
| Failed run | [technical criterion] | [ ] | [ ] | [ ] |

Do not use outcome-dependent exclusions without explicit labeling and a sensitivity analysis.

## 8. Multiple comparisons

- Family of confirmatory claims: [ ]
- Number of outcomes/contrasts/subgroups: [ ]
- Control method: [FWER/FDR/hierarchical/not required, with justification]
- Order/hierarchy: [ ]
- Exploratory comparisons: [labeled, without confirmatory language]

## 9. Checking assumptions

| Assumption | Diagnostics | Threshold/criterion | Plan if violated |
|---|---|---|---|
| Independence/clustering | [ ] | [ ] | [ ] |
| Functional form | [ ] | [ ] | [ ] |
| Distribution/variance | [ ] | [ ] | [ ] |
| Measurement validity | [ ] | [ ] | [ ] |
| Exchangeability/no confounding | [ ] | [ ] | [ ] |
| Positivity/overlap | [ ] | [ ] | [ ] |
| Missingness | [ ] | [ ] | [ ] |

Do not switch to whichever model produces the desired result. Specify alternatives as sensitivity analyses and show all relevant variants.

## 10. Robustness and sensitivity

| Check | Threat addressed | Variant | What would change the conclusion |
|---|---|---|---|
| Alternative specification | Model dependence | [ ] | [ ] |
| Alternative metric | Construct choice | [ ] | [ ] |
| With/without disputed observations | Influence | [ ] | [ ] |
| By subgroup/environment | Heterogeneity | [ ] | [ ] |
| Placebo/negative control | Confounding/leakage | [ ] | [ ] |
| Temporal/external validation | Generalization | [ ] | [ ] |

Robustness is not the number of additional tables but the stability of the substantive conclusion under plausible analytical choices.

## 11. Subgroups and heterogeneity

- Pre-specified subgroups and rationale: [ ]
- Interaction test/model: [not separate "significant/non-significant" results within groups]
- Minimum size/precision: [ ]
- Exploratory subgroups: [labeling and confirmation plan]
- Fairness/harm for affected groups: [ ]

## 12. Qualitative analysis

If applicable:

- Epistemological position/approach: [ ]
- Sampling and sufficiency/saturation criterion: [ ]
- Coding scheme: [inductive/deductive, versions]
- Number of coders and resolution of disagreements: [ ]
- Researcher reflexivity: [position and influence]
- Negative/deviant cases: [how they are sought]
- Audit trail and linking of themes to data excerpts: [ ]
- Member checking/triangulation: [if appropriate, not as a mechanical requirement]

## 13. Visualizations and tables

| ID | Purpose | Data | Geometry/statistic | Uncertainty | Hidden/shown points |
|---|---|---|---|---|---|
| Fig1 | [ ] | [ ] | [ ] | [ ] | [ ] |

Define the main figures in advance, but allow exploratory visualizations with explicit labeling. Axes, aggregation, and color must not exaggerate the effect.

## 14. Reproducible execution

- Entry point: [command/notebook/script]
- Frozen environment: [lock/container]
- Data checksum: [ ]
- Seed/config: [ ]
- Automatically generated tables/figures: [ ]
- Expected outputs/tolerances: [ ]
- Blind/double programming or code review: [ ]

## 15. Deviations and exploratory analysis

| ID | Date | Pre-specified plan | Change | Reason | Data already seen? | Labeling in the report |
|---|---|---|---|---|---|---|
| ADEV-01 | [ ] | [ ] | [ ] | [ ] | [yes/no] | [ ] |

## Results table

| RQ/H | n | Estimate | Interval/uncertainty | Practical threshold | Robustness | Conclusion |
|---|---:|---:|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

## Quality check

- [ ] The estimand and primary outcome were defined before the result.
- [ ] The metric is valid, and the practically important threshold has a domain rationale.
- [ ] The model fits the design, dependence structure, and data type.
- [ ] Effect size and uncertainty are reported.
- [ ] Missing data, exclusions, outliers, and multiplicity have pre-specified rules.
- [ ] Sensitivity checks address real threats to the conclusion.
- [ ] Test/confirmation data were not used to choose the analysis.
- [ ] Confirmatory, secondary, and exploratory results are kept separate.
- [ ] The code and environment reproduce tables and figures automatically.
- [ ] "Inconclusive" remains a permissible and honest conclusion.

Methodological basis: [ASA Statement on Statistical Significance and P-Values](https://www.amstat.org/asa/files/pdfs/p-valuestatement.pdf), [National Academies on reproducibility](https://www.nationalacademies.org/read/25303/chapter/2), [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist), [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Uncertainty** — the range of plausible values for an estimate, usually expressed as an interval, a standard error, or the spread across repeated runs. Without it, a single number cannot be interpreted properly.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Estimand** — a precise definition of what is being estimated: the population, outcome, conditions compared, summary measure, and handling of intercurrent events. Without it, the same "effect" can mean different quantities.
- **Intercurrent events** — events after the start of an intervention that affect the measurement or interpretation of the outcome, such as dropout, switching conditions, or a failed run. How they are handled is part of the estimand definition.
- **Primary outcome** — the main measure, chosen in advance, on which the main conclusion is based; secondary outcomes complement it. Changing the primary outcome after seeing the results without disclosure is a serious violation.
- **Smallest effect size of interest (SESOI)** — the smallest effect size that matters in practice for the decision. It is set in advance on domain grounds and serves as the threshold of practical significance.
- **Ceiling and floor effects** — a situation in which metric values hit the top or bottom of the scale, so the metric can no longer distinguish improvements or declines.
- **Baseline characteristics** — a description of the groups before the intervention, usually in "Table 1". It is used to judge whether the groups are comparable, not for formal statistical testing of their "equality".
- **Outcome distribution and link function** — in generalized linear models, the assumed distribution of the outcome (for example, normal, binomial, or Poisson) and the function linking its mean to a linear combination of predictors.
- **Covariate** — a variable that is not the focus of the study but may affect the outcome; it is accounted for in the design or model to improve precision or control confounding.
- **Interaction** — a situation in which the effect of one factor depends on the value of another. Differences in an effect between subgroups are tested through an interaction, not by comparing "significant/non-significant" within groups.
- **Clustering** — a situation in which observations are grouped (students in classes, queries from one user, repeated measurements of one unit) and therefore not independent. Ignoring it understates uncertainty.
- **Frequentist and Bayesian inference** — the frequentist approach describes the properties of a procedure under repeated sampling (p-values, confidence intervals); the Bayesian approach updates a prior distribution with data to obtain a posterior distribution of the parameter.
- **Point estimate** — a single best value of the quantity being estimated. Without an uncertainty interval it is not enough for a conclusion.
- **Confidence interval and credible interval** — a confidence interval is built by a frequentist procedure that, under repeated sampling, covers the true value at a given rate (for example, 95%); a credible interval is a Bayesian interval that contains the parameter with a given posterior probability.
- **Equivalence testing** — testing whether a difference lies within preset margins of practical irrelevance. Only this, not the absence of a significant result, can justify a conclusion that there is no important difference.
- **Non-inferiority** — testing that a new method is worse than the comparator by no more than a preset acceptable amount (margin).
- **P-value** — the probability of obtaining data at least as extreme as those observed if the null hypothesis and all model assumptions are true. It is not the probability that a hypothesis is true, nor a measure of an effect's size or importance.
- **Effect size** — the quantitative magnitude of a difference or association, such as a difference in means, an odds ratio, or a metric gain. Unlike a p-value, it shows how large and practically important an effect is.
- **Statistical power** — the probability of detecting an effect of a given size if it truly exists. Power analysis is used to justify the sample size.
- **Type I and Type II errors (alpha)** — a Type I error is a false positive, and its acceptable probability is denoted alpha; a Type II error is a false negative, and its probability equals 1 − power.
- **Design effect** — the factor by which the variance of an estimate under cluster or complex sampling exceeds that under simple random sampling of the same size. It is used to adjust the sample size.
- **Multiple comparisons (multiplicity)** — a situation in which many hypotheses, metrics, or subgroups are tested. The probability of at least one false positive grows, so a predefined control method is needed.
- **Sensitivity analysis** — assessing how much the result changes when assumptions or debatable analytic choices change, for example the handling of missing data or outliers.
- **ITT and per-protocol (intention-to-treat, per-protocol analysis)** — ITT analyzes all units in the groups to which they were assigned, regardless of what actually happened; per-protocol analyzes only units that followed the protocol. ITT preserves the benefits of randomization.
- **Outcome-dependent exclusions** — excluding observations by a rule related to the outcome value. This easily creates a spurious effect, so it requires explicit labeling and sensitivity analysis.
- **FWER and FDR (family-wise error rate, false discovery rate)** — two error measures controlled in multiple comparisons: FWER is the probability of at least one false positive in a family of tests (for example, Bonferroni or Holm corrections); FDR is the expected share of false findings among all reported findings (for example, the Benjamini–Hochberg procedure).
- **Exchangeability (no unmeasured confounding)** — a causal inference assumption that, after accounting for measured covariates, the groups compared are comparable and there are no unmeasured confounders.
- **Positivity (overlap)** — the assumption that for every combination of the characteristics considered there are units in all conditions compared. Otherwise, the effect for part of the population is estimated only by extrapolation.
- **Robustness checks** — repeating the analysis under other plausible choices (model specification, metric, exclusion rules, subsets) to confirm that the substantive conclusion does not depend on them.
- **Heterogeneity** — differences in an effect across studies, subgroups, or settings beyond random variation, for example due to different populations, methods, or conditions. It should be assessed and explained, not simply averaged out.
- **Placebo and negative control checks** — checks on an outcome or exposure where there should be no effect. A detected "effect" points to confounding, leakage, or an analysis error.
- **Saturation** — in qualitative research, the point at which new observations or interviews yield hardly any new themes; it is used as a criterion of sample sufficiency.
- **Inductive and deductive coding** — in qualitative analysis, deriving categories from the data themselves (inductive) or applying a predefined category scheme (deductive).
- **Reflexivity** — in qualitative research, systematic reflection on how the researcher's position, experience, and expectations influence data collection and interpretation.
- **Negative/deviant cases** — observations that do not fit the identified themes or explanation. Searching for them deliberately tests and refines the interpretation.
- **Audit trail** — a documented sequence of decisions and materials that makes it possible to trace the path from raw data to themes and conclusions.
- **Member checking and triangulation** — member checking means verifying interpretations with the participants themselves; triangulation means comparing different data sources, methods, or researchers to check a conclusion.
- **Double and blind programming** — an independent implementation of the same analysis by another person, sometimes without knowledge of the expected results, to catch errors in the code.
- **ASA Statement on Statistical Significance and P-Values** — a 2016 statement by the American Statistical Association on the correct interpretation of p-values, stressing that scientific conclusions should not rest solely on whether a significance threshold is passed.
- **National Academies** — the U.S. National Academies of Sciences, Engineering, and Medicine. Their report "Reproducibility and Replicability in Science" (2019) provides widely used definitions of reproducibility and replicability and recommendations for achieving them.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
