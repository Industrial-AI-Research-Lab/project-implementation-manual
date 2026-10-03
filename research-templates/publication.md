# Publication or R&D Report Template

A publication is neither a chronological diary nor promotional copy. It connects a limited set of claims to sufficient evidence, methods, and uncertainty. Use the IMRaD structure as a reasonable default for empirical work, but adapt it for theoretical, qualitative, dataset, and systems publications.

## 0. Output strategy

- ★ Type: [journal article / conference paper / technical report / research note / dataset paper / replication / negative result / thesis]
- ★ Primary audience: [ ]
- ★ Venue/series and scope fit: [ ]
- ★ Requirements for format, length, open access, and data/code: [link and date checked]
- ★ Applicable reporting guideline: [EQUATOR/PRISMA/CONSORT/STROBE/SRQR/NeurIPS/industry-specific]
- ★ Main contribution in one sentence: [ ]
- Preprint/embargo/IP constraints: [ ]

## 1. Claim-to-evidence map

| Claim ID | Statement | Type | Data/analysis | Figure/table | Assumptions | Limitation | Confidence |
|---|---|---|---|---|---|---|---|
| C1 | [ ] | [empirical/theoretical/methodological] | [ ] | [ ] | [ ] | [ ] | [ ] |

Remove a claim if it has no independent evidence and is not honestly labeled as a hypothesis or opinion. Do not stretch a single benchmark into a claim of universal superiority.

## 2. Title

> **[Object/method]** for **[task]**: **[design/context]**

Check:

- the specific object and the type of study are visible;
- no "revolutionary", "proven", or "universal" without sufficient grounds;
- the title does not hide an important design limitation;
- for a systematic/scoping review, the review type is stated.

## 3. Abstract

### Structured outline

- **Context:** [1–2 sentences: the problem and the gap]
- **Objective:** [RQ/contribution]
- **Method:** [design, data/n, comparator, main analysis]
- **Result:** [numerical estimate + uncertainty; not just "significant"]
- **Limitation:** [the main boundary]
- **Conclusion:** [an answer that does not exceed the evidence]
- **Artifacts/registration:** [link, if the format allows]

Do not include in the abstract any result that is absent from the main text and tables.

## 4. Introduction

1. Context and importance of the problem.
2. What is reliably known.
3. What specific gap remains.
4. Why existing methods/work do not close it.
5. RQs/hypotheses.
6. Contribution and a brief outline of the paper.

### Contribution

> This work contributes: (1) **[new knowledge/method]**; (2) **[empirical evidence/dataset]**; (3) **[artifact/replication]**. Unlike **[closest prior work]**, we **[specific difference]**.

Do not present the volume of engineering implementation as scientific novelty if it produces no new knowledge.

## 5. Related work

Organize the section by questions, approaches, or limitations rather than as a sequence of "Author A did…, author B did…".

| Cluster | What is known | Strongest evidence | Contradiction/limitation | Relation to this work |
|---|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] |

- Describe the review strategy or link to it.
- Include the closest negative and contradictory results.
- Cite primary works, data, and software, not only reviews.
- Do not treat lack of peer review as an automatic ban; label the status and assess the quality.

## 6. Methods

Minimum required for replication:

- design, dates, and setting;
- population/sample, inclusion/exclusion, and flow;
- experimental unit, assignment, control, blinding;
- data: source, version, license, preprocessing, splits;
- method/algorithm: inputs, outputs, parameters, pseudocode/implementation;
- outcomes/metrics and time of measurement;
- sample size/number of runs and its justification;
- frozen analysis plan, missing data/outliers/multiplicity;
- software/hardware/versions/seeds/compute;
- ethics approval/consent;
- deviations from protocol.

An essential detail must not be available only "upon request to the author" if it can be documented safely.

## 7. Results

Order:

1. Flow of data/participants/runs and exclusions.
2. Descriptive characteristics of the data and QC.
3. The main result for each RQ/H.
4. Secondary results.
5. Robustness/sensitivity and diagnostics.
6. Exploratory findings, explicitly labeled.
7. Negative/inconclusive results.

### Results table

| RQ/H | n | Estimate/effect | Uncertainty | Practical threshold | Robustness | Status |
|---|---:|---:|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [supported/not/uncertain] |

Do not repeat every number from the table in the text. The text reports the pattern and what it means for the question.

## 8. Discussion

### Structure

- A brief answer to the RQ without new analysis.
- Comparison with predictions and the literature.
- Which mechanisms are consistent with the results and which alternatives remain.
- Practical/theoretical meaning of the effect size.
- Unexpected results and their exploratory status.
- Limitations and the direction of possible bias.
- What is required for replication/transfer.
- The next most informative piece of work.

### Limitations

| Limitation | How it affects the result | Direction/unknown direction of bias | Mitigation | What is needed next |
|---|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] |

The phrase "further research is needed" is insufficient: name the specific uncertainty and the design that would reduce it.

## 9. Conclusion

> Under **[boundaries]**, we observed/estimated **[effect + uncertainty]** relative to **[baseline]**. This **[supports/does not support/does not allow us to distinguish]** **[claim]** and implies **[consequence]** for **[decision]**. The conclusion does not extend to **[boundaries]**.

Do not add to the conclusion a causal, universal, or product claim stronger than the design permits.

## 10. Statements and transparency

### Registration and protocol

- Registration/version/date: [ ]
- Deviations: [link/table]

### Data availability

> The data are **[available in a repository / available upon reasonable request / not available]** at **[persistent link]**. Restriction: **[privacy/license/security]**. Available metadata/code/synthetic example: **[link]**.

### Code/materials availability

> Code and materials, version **[tag/DOI]**, are available at **[URL]** under the **[ ]** license. Reproduction instructions: **[ ]**.

### Ethics

> Approval **[body, ID, date]**; consent **[how obtained]**; or justification of non-applicability **[ ]**.

### Funding/conflicts

- Funding and the sponsor's role: [ ]
- Conflicts of interest: [ ]

### Use of AI

- Tools/versions, tasks, and human verification: [ ]
- Follow the venue's specific rules.

## 11. Author contributions (CRediT)

| Role | Contributor(s) | Specific contribution |
|---|---|---|
| Conceptualization | [ ] | [ ] |
| Methodology | [ ] | [ ] |
| Software | [ ] | [ ] |
| Data curation | [ ] | [ ] |
| Formal analysis | [ ] | [ ] |
| Investigation | [ ] | [ ] |
| Validation | [ ] | [ ] |
| Visualization | [ ] | [ ] |
| Writing — original draft | [ ] | [ ] |
| Writing — review & editing | [ ] | [ ] |
| Supervision/administration/funding/resources | [ ] | [ ] |

A role does not automatically equal authorship; apply the venue's rules and agree on author order in advance.

## 12. Figures and tables

- Each item answers one question.
- The caption is self-contained and defines the data, n, units, aggregation, and uncertainty.
- Individual data points/distributions are shown where possible.
- Color is accessible and does not encode a value judgment without explanation.
- Axes and truncation do not exaggerate the effect.
- Main results are not hidden only in the appendix.
- Tables/figures are generated by the analysis pipeline.

## 13. Appendix and supplementary material

- full search strings/flow;
- extended methods and proofs;
- additional diagnostics/robustness;
- datasheet/model/method card;
- full protocol and deviation log;
- artifact manifest and runbook;
- additional negative results.

The appendix extends the main text, but it does not fix an incomplete main claim.

## 14. R&D decision memo — short version

For an internal decision, add a one-page summary:

- Decision: [go / revise / stop / replicate]
- What we learned: [3 points]
- Strength of evidence: [why]
- What we did not learn: [ ]
- Practical effect and cost: [ ]
- Risks/limitations: [ ]
- Next experiment and maximum budget: [ ]
- Artifacts/knowledge owner: [ ]

## Pre-submission check

- [ ] An appropriate reporting guideline has been selected and its checklist completed.
- [ ] Every main claim has direct evidence.
- [ ] The abstract and conclusion are no stronger than the results.
- [ ] The methods are sufficient for replication.
- [ ] Effect sizes/uncertainty and negative results are reported.
- [ ] Confirmatory and exploratory analyses are separated.
- [ ] The limitations state their impact on the conclusion rather than forming a ritual list.
- [ ] Data/code/materials statements are specific and include persistent links.
- [ ] Ethics, funding, conflicts, authorship, and AI use are disclosed.
- [ ] All references have been checked, and each citation supports the specific adjacent claim.
- [ ] An independent reader and an artifact tester have completed a check.

Methodological basis: [EQUATOR guideline selector](https://www.equator-network.org/toolkits/selecting-the-appropriate-reporting-guideline/), [PRISMA 2020](https://www.prisma-statement.org/prisma-2020), [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist), [CRediT](https://credit.niso.org/), [COPE Core Practices](https://publicationethics.org/core-practices).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Uncertainty** — the range of plausible values for an estimate, usually expressed as an interval, a standard error, or the spread across repeated runs. Without it, a single number cannot be interpreted properly.
- **IMRaD (Introduction, Methods, Results, and Discussion)** — the standard structure of an empirical paper: introduction, methods, results, and discussion.
- **Open access** — free public online access to a publication. Venues may require a specific license or a publication fee.
- **Reporting guideline** — a checklist of what a publication must describe for a given study design, for example CONSORT for randomized trials or PRISMA for systematic reviews. It helps avoid omitting essential details of methods and results.
- **EQUATOR Network** — an international initiative to improve the quality and transparency of research reporting (primarily in health research). It maintains a database of reporting guidelines and helps choose the right one for a given design.
- **PRISMA (Preferred Reporting Items for Systematic Reviews and Meta-Analyses)** — a reporting guideline for systematic reviews and meta-analyses: a checklist and a diagram of the study selection flow (PRISMA flow diagram). PRISMA-S is an extension for reporting literature searches. Following the checklist makes a review transparent but does not by itself guarantee the quality of its design.
- **CONSORT (Consolidated Standards of Reporting Trials)** — the reporting guideline for randomized controlled trials.
- **STROBE (Strengthening the Reporting of Observational Studies in Epidemiology)** — the reporting guideline for observational studies in epidemiology.
- **SRQR (Standards for Reporting Qualitative Research)** — a reporting guideline for qualitative research.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
- **Preprint** — a version of a paper made publicly available before peer review. It allows results to be shared quickly but has not been checked by reviewers.
- **Embargo** — a period during which data or a publication have been deposited but are not yet publicly available.
- **Claim–evidence map** — a table linking each claim of the work to specific data, analysis, figure or table, assumptions, and limitations. It helps remove unsupported claims.
- **Benchmark** — a standardized set of tasks, data, and metrics for comparing methods under identical conditions. Success on one benchmark does not prove general superiority.
- **Systematic review** — a review that answers a narrow question following a predefined protocol: comprehensive search, explicit selection criteria, risk-of-bias assessment, and synthesis. The process must be repeatable from the saved protocol.
- **Scoping review** — a review that maps the extent, types, and gaps of the literature on a broad topic, usually without pooling results quantitatively.
- **Multiple comparisons (multiplicity)** — a situation in which many hypotheses, metrics, or subgroups are tested. The probability of at least one false positive grows, so a predefined control method is needed.
- **Deviation log** — a dated list of changes to the frozen protocol or analysis plan: what changed, why, whether results were already visible, and how this affects interpretation. It lets readers tell what was planned from what changed along the way.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Effect size** — the quantitative magnitude of a difference or association, such as a difference in means, an odds ratio, or a metric gain. Unlike a p-value, it shows how large and practically important an effect is.
- **DOI, persistent identifier (Digital Object Identifier)** — a stable reference to a digital object (an article, dataset, or code archive) that keeps working when the storage location changes. DOI is the most common kind of such identifier.
- **CRediT (Contributor Roles Taxonomy)** — a standard taxonomy of 14 contributor roles in research (for example, Conceptualization, Methodology, Software, Formal analysis) that makes each author's contribution explicit.
- **Datasheet** — a standardized description of a dataset: purpose, composition, provenance, collection, labeling, limitations, and recommended uses. It is based on the Datasheets for Datasets approach.
- **Model card, method card** — a short standardized document describing a model's or method's purpose, data, metrics, limitations, risks, and recommended conditions of use.
- **Manifest** — a list of files or artifacts with their purpose, version or checksum, license, and access conditions. It makes it possible to verify that a package is complete and unchanged.
- **Runbook** — step-by-step instructions that let an outsider obtain the data, set up the environment, run the pipeline, and check the result.
- **Decision memo** — a short document for the decision-maker: what was learned, how reliable the evidence is, which decision is recommended, and what it costs and risks.
- **Confirmatory analysis** — analysis whose hypotheses and rules were fixed before the results were seen. Only such analysis supports a claim that a hypothesis was tested.
- **COPE (Committee on Publication Ethics)** — an international organization that publishes standards of publication ethics (Core Practices) and guidance for editors, authors, and reviewers, including on authorship, conflicts of interest, and corrections to the published record.
