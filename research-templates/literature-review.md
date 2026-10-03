# Literature Review Template

This template supports a rapid orienting review, a scoping review, a systematic review, and a meta-analysis. The depth differs, but even a rapid review must preserve the queries, dates, and reasons for selection. PRISMA is primarily a standard for transparent reporting; following its checklist does not automatically prove the quality of the design.

## 0. Review card

- ★ Title: [title]
- ★ Protocol version and date: [version]
- ★ Author(s) of the search/screening: [names]
- ★ Date of the latest search: [YYYY-MM-DD]
- ★ Type: [orienting / narrative / scoping / systematic / meta-analysis]
- ★ Related RQ: [link]
- Protocol registration: [OSF/PROSPERO/other/not registered, with an explanation]

## 1. Choosing the depth

| Type | When it fits | Minimum |
|---|---|---|
| Orienting | To quickly understand the terms, key works, and feasibility | Several sources, a query log, limitations |
| Narrative | To synthesize concepts and schools of thought | A clear selection principle, critical comparison, the author's position |
| Scoping | To map the volume, types, and gaps of the literature | A protocol, a broad search, transparent screening, charting |
| Systematic | To answer a narrow question with a reproducible method | Predefined criteria, a comprehensive search, screening, risk of bias, synthesis |
| Meta-analysis | To quantitatively pool comparable effects | Everything above, plus an estimand, a pooling model, heterogeneity, and sensitivity |

Do not call a review systematic if the process cannot be repeated from a saved protocol.

## 2. Question and protocol

- ★ Review objective: [what it should clarify]
- ★ Question: [PICO/PICOS, PCC, SPIDER, or a custom structure]
- ★ Population/object: [definition]
- ★ Concept/intervention/exposure: [definition]
- ★ Comparator: [if applicable]
- ★ Outcomes/themes: [primary and secondary]
- ★ Context and period: [boundaries]
- ★ Unit of inclusion: [article, report, dataset, preprint, patent, system]
- How protocol changes will be recorded: [log]

## 3. Inclusion and exclusion criteria

| Criterion | Include | Exclude | Rationale |
|---|---|---|---|
| Population/domain | [ ] | [ ] | [ ] |
| Study design | [ ] | [ ] | [ ] |
| Outcomes | [ ] | [ ] | [ ] |
| Period | [ ] | [ ] | [ ] |
| Language | [ ] | [ ] | [ ] |
| Publication status | [ ] | [ ] | [ ] |
| Full-text availability | [ ] | [ ] | [ ] |

Justify restrictions on language, date, and publication type by the question, not by convenience. Consider grey literature, preprints, and negative results as ways to reduce publication bias.

## 4. Information sources

| Source/database | Platform | Coverage | Search date | Reason for selection |
|---|---|---|---|---|
| [for example, ACM DL] | [platform] | [field] | [date] | [rationale] |

Check, where necessary:

- bibliographic databases from different disciplines;
- registries of studies and protocols;
- preprints, dissertations, technical reports, and patents;
- backward citation search through reference lists;
- forward citation search through citing works;
- hand searching of key conferences/journals;
- requests to authors or experts;
- previously published reviews and their updates.

## 5. Search strategy

### Concept map

| Concept | Keywords | Synonyms/variants | Controlled vocabulary | Exclusions |
|---|---|---|---|---|
| C1 | [ ] | [ ] | [MeSH/thesaurus/none] | [ ] |

### Query log

| ID | Source | Full query string | Filters | Date/time | Results | Export |
|---|---|---|---|---|---|---|
| S1 | [database] | `[full query without abbreviations]` | [filters] | [ISO 8601] | [n] | [file/URL] |

- ★ Save the query for **each** database: platform syntax differs.
- ★ Record all restrictions and coverage dates.
- ◇ Test the search against a set of known relevant works (benchmark set).
- ◇ For a systematic review, submit the strategy for PRESS-style peer review by a search specialist.
- Use of ML/LLM in the search: [tool, version, prompt/parameters, stage, human verification]. Do not use it as a substitute for a verifiable search log.

## 6. Record management

- Tool/export format: [RIS/BibTeX/CSV]
- Deduplication rule: [fields, order, manual check]
- Library version after dedup: [file + checksum]
- Linking multiple publications of the same study: [rule]
- Corrections/retractions checked: [how]

## 7. Screening

| Stage | Reviewers | Mode | Disagreement resolution | Artifact |
|---|---|---|---|---|
| Title/abstract | [ ] | [single/two independently] | [ ] | [file] |
| Full text | [ ] | [single/two independently] | [ ] | [file] |

- ★ Run a pilot on a small shared sample and refine the criteria before full screening.
- ★ The reason for exclusion at the full-text stage must correspond to a predefined category.
- ◇ Assess inter-reviewer agreement, but do not let a number replace discussion of ambiguous rules.

### PRISMA flow

| Stage | Count |
|---|---:|
| Identified in databases/registries | [n] |
| Identified by other methods | [n] |
| After deduplication | [n] |
| Screened by title/abstract | [n] |
| Excluded | [n] |
| Full texts retrieved | [n] |
| Excluded at full text, with reasons | [n] |
| Included in qualitative synthesis | [n] |
| Included in quantitative synthesis | [n] |

## 8. Data extraction

### Extraction schema

| Field | Definition | Format/units | Ambiguity rule |
|---|---|---|---|
| Study ID | [stable ID] | [string] | [ ] |
| Design | [taxonomy] | [category] | [ ] |
| Population/data | [description] | [ ] | [ ] |
| Intervention/method | [ ] | [ ] | [ ] |
| Comparator | [ ] | [ ] | [ ] |
| Outcome/effect | [ ] | [units] | [ ] |
| Uncertainty | [SE/CI/SD/other] | [ ] | [ ] |
| Funding/conflict of interest | [ ] | [ ] | [ ] |

- Extraction form pilot: [n works, changes]
- Double extraction of critical fields: [yes/no; why]
- Handling missing data: [contacting authors, calculation, flagging]

## 9. Critical appraisal

- ★ Risk-of-bias/quality appraisal tool: [appropriate to the design]
- ★ Level of appraisal: [study / outcome / claim]
- ★ Who performed the appraisal and how disagreements were resolved: [process]
- Do not reduce different sources of bias to a single opaque sum without justification.

| Study ID | Risk domain 1 | Risk domain 2 | Risk domain 3 | Overall judgment | Rationale |
|---|---|---|---|---|---|
| [ID] | [low/unclear/high] | [ ] | [ ] | [ ] | [brief quote/page] |

## 10. Synthesis

- Method for grouping studies: [population, method, outcome]
- Narrative synthesis: [how results and quality are compared]
- Evidence tables: [link]
- If a meta-analysis: [common estimand, model, transformations, weights, heterogeneity, dependent effects]
- Sensitivity analyses: [excluding high risk, alternative models, influence of individual works]
- Publication bias/small-study effects: [method and limitations]
- Contradictions: [do not average them without explaining possible moderators]

## 11. Map of knowledge and gaps

| Claim | Supporting works | Contradicting works | Quality/risk | Confidence | Gap |
|---|---|---|---|---|---|
| [claim] | [IDs] | [IDs] | [judgment] | [low/medium/high] | [what is unknown] |

- What is firmly established: [list]
- What is likely but not reliable: [list]
- What is contradictory: [list]
- What has not been studied: [list]
- How the gap gives rise to the project's RQ/hypothesis: [connection]

## 12. Report on limitations

- Incomplete source coverage: [impact]
- Language/time restrictions: [impact]
- Unavailable full texts: [n and impact]
- Selection/extraction bias: [measures and residual risk]
- Heterogeneity of studies: [impact]
- Automation/LLM: [errors and human validation]
- Review expiry date/update plan: [date or trigger]

## Quality check

- [ ] The review type matches the question and the claimed rigor.
- [ ] The protocol and criteria were fixed before full screening.
- [ ] The exact string, platform, and date are saved for each database.
- [ ] The search is not limited to a convenient database and is not restricted without justification.
- [ ] Deduplication and reasons for exclusion are reproducible.
- [ ] The critical appraisal matches the study designs.
- [ ] The synthesis accounts for quality and contradictions rather than counting publication votes.
- [ ] The conclusions are no broader than the available evidence.

Methodological basis: [PRISMA 2020](https://www.prisma-statement.org/prisma-2020), [PRISMA-S](https://pmc.ncbi.nlm.nih.gov/articles/PMC8270366/), [Cochrane Handbook — Searching and selecting studies](https://www.cochrane.org/authors/handbooks-and-manuals/handbook/current/chapter-04), [OSF Generalized Systematic Review registration](https://help.osf.io/article/330-welcome-to-registrations), [EQUATOR guideline selector](https://www.equator-network.org/toolkits/selecting-the-appropriate-reporting-guideline/).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Scoping review** — a review that maps the extent, types, and gaps of the literature on a broad topic, usually without pooling results quantitatively.
- **Systematic review** — a review that answers a narrow question following a predefined protocol: comprehensive search, explicit selection criteria, risk-of-bias assessment, and synthesis. The process must be repeatable from the saved protocol.
- **Meta-analysis** — statistical pooling of comparable quantitative results from several studies into an overall effect estimate that accounts for their precision and the differences between them.
- **PRISMA (Preferred Reporting Items for Systematic Reviews and Meta-Analyses)** — a reporting guideline for systematic reviews and meta-analyses: a checklist and a diagram of the study selection flow (PRISMA flow diagram). PRISMA-S is an extension for reporting literature searches. Following the checklist makes a review transparent but does not by itself guarantee the quality of its design.
- **Narrative review** — a review that synthesizes concepts and schools of thought from the author's perspective, without a fully formalized search protocol. It requires a clear principle for selecting sources and critical comparison.
- **OSF (Open Science Framework)** — a free platform from the Center for Open Science for storing project materials and registering them, including study preregistrations and review protocols.
- **PROSPERO** — an international registry of systematic review protocols, primarily in health. Registration records the review plan before the review is carried out.
- **Screening** — selecting retrieved records against the inclusion criteria: first by title and abstract, then by full text.
- **Charting** — in a scoping review, systematically extracting the characteristics of included studies into a common table to describe the literature.
- **Risk of bias** — an assessment of how much features of a study's design or conduct could systematically distort its result. In reviews it is judged domain by domain using dedicated tools.
- **Estimand** — a precise definition of what is being estimated: the population, outcome, conditions compared, summary measure, and handling of intercurrent events. Without it, the same "effect" can mean different quantities.
- **Heterogeneity** — differences in an effect across studies, subgroups, or settings beyond random variation, for example due to different populations, methods, or conditions. It should be assessed and explained, not simply averaged out.
- **Sensitivity analysis** — assessing how much the result changes when assumptions or debatable analytic choices change, for example the handling of missing data or outliers.
- **PICO/PICOS** — a framework for formulating a comparative question: Population, Intervention, Comparator, Outcome; PICOS adds Study design.
- **PCC (Population, Concept, Context)** — a framework for formulating a scoping review question: the population, the concept studied, and the context.
- **SPIDER (Sample, Phenomenon of Interest, Design, Evaluation, Research type)** — a framework for formulating questions and searches for qualitative and mixed-methods research.
- **Grey literature** — material outside traditional peer-reviewed publishing: reports, theses, preprints, conference materials, and organizational documents. Including it reduces publication bias.
- **Publication bias** — the tendency to publish mainly positive and statistically significant results. Because of it, the literature overstates effects and negative results get lost.
- **Backward and forward citation search** — checking the reference lists of found studies (backward) and the studies that cite them (forward). It helps find sources missed by database searches.
- **Controlled vocabulary, MeSH (Medical Subject Headings)** — a standardized set of subject terms a database uses to index publications; MeSH is such a vocabulary for biomedical literature (PubMed/MEDLINE). Searching with it finds studies regardless of the authors' wording.
- **Benchmark set** — a set of known relevant studies used to check whether a search strategy finds what it should.
- **PRESS (Peer Review of Electronic Search Strategies)** — a guideline and checklist for having a search strategy peer-reviewed by an information specialist before it is run.
- **Checksum (hash)** — a short string computed from a file's contents. Any change to the file changes it, so it confirms that exactly the intended version is being used.
- **Retraction** — the official withdrawal of a published article because of serious errors or misconduct. Retracted studies must not be relied on as evidence.
- **Inter-rater agreement** — the degree to which independent raters reach the same decisions, often measured with Cohen's kappa. It shows how unambiguous the criteria are.
- **SE, CI, SD** — the standard error (SE) describes the precision of an estimate; the confidence interval (CI) is a range of parameter values compatible with the data, constructed at a given level such as 95%; the standard deviation (SD) describes the spread of individual observations.
- **Narrative synthesis** — a systematic textual comparison of study results and quality when quantitative pooling is impossible or inappropriate.
- **Small-study effects** — the tendency of small studies to show stronger effects than large ones. It may indicate publication bias or differences in quality.
- **Moderator** — a factor on which the size or direction of an effect depends, such as population, design, or conditions. Identifying moderators helps explain contradictions between studies.
- **Cochrane Handbook** — Cochrane's guide to conducting systematic reviews of interventions, including searching for and selecting studies and assessing risk of bias.
- **EQUATOR Network** — an international initiative to improve the quality and transparency of research reporting (primarily in health research). It maintains a database of reporting guidelines and helps choose the right one for a given design.
