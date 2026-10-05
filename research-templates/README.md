# Research Templates

This set is intended for independent research, student projects, and applied R&D tasks. It does not replace the requirements of a specific discipline, supervisor, ethics committee, or publication venue. The purpose of the templates is to make the course of a study visible: from the initial uncertainty to a verifiable conclusion and reproducible artifacts.

For NIR projects, use the templates together with the [NIR requirements](../nir-requirements/README.md): when they differ, the program requirements and the supervisor's instructions take precedence.

## Quick start

1. For a small study, start with the "Research brief", "Research questions", "Experimental protocol", and "Analysis plan" pages.
2. For an independent project or a publication, use the "Full independent study" as the table of contents of your working protocol.
3. Complete the plan **before** obtaining the key results. If the plan changes, do not rewrite history: add an entry to the deviation log.
4. Keep the confirmatory analysis planned in advance separate from the exploratory analysis that emerged after you became familiar with the data.
5. Before finishing, hand the materials to a person who did not take part in the work and ask them to reproduce the main result by following the instructions.

## How to read the markers

- **★ Required** — the minimum information without which the study cannot be meaningfully assessed.
- **◇ Extended** — useful for a publication, high-risk work, or an experienced team.
- **Not applicable** — an acceptable answer only when accompanied by a brief justification.
- Text in square brackets is replaced with the researcher's answer.
- A checkbox is ticked only when there is verifiable evidence: a link, file, calculation, protocol, or decision.
- Each page ends with a "Glossary" section that explains non-obvious terms and abbreviations.

## How to use the set depending on your experience

**If this is your first study:**

1. Read this README and the glossary at the end of the page.
2. Fill in only the **★** items in the "Research brief", "Research questions", "Experimental protocol", and "Analysis plan". You may skip the **◇** items for now.
3. Look up an unfamiliar term in the glossary of the page where you found it.
4. Keep the "Research log" from day one: short dated entries are more useful than a detailed report written from memory.
5. Before key milestones (topic approval, launching the experiment, completion), go through the corresponding section of the "Review checklists" and discuss the outcome with your supervisor.

**If you have research experience:**

1. Use the "Full independent study" as an end-to-end protocol and move to the topic-specific templates only for details.
2. Fill in the **◇** items where the work is being prepared for publication, carries high risk, or is done by a team.
3. Check the templates against your discipline's reporting standard (see EQUATOR under "Methodological foundation") and the requirements of the publication venue.
4. Use the "Review checklists" to review other people's work and to independently check your own.

## For LLM agents

The [Guide for LLM agents](agent-guide.md) describes how an LLM assistant should apply these templates when helping a researcher: choosing a template, filling it in without inventing facts, adapting to the user's experience, and checking the result.

## Navigation

| Stage | Template | Outcome |
|---|---|---|
| Whole cycle | [Full independent study](full-study.md) | End-to-end protocol and publication package |
| Initiation | [Research brief](research-brief.md) | Problem, boundaries, decision, and resources |
| Problem framing | [Research questions](questions.md) | Testable questions and success criteria |
| Foundation | [Literature review](literature-review.md) | Map of knowledge, gaps, and quality of evidence |
| Predictions | [Hypotheses](hypotheses.md) | Falsifiable predictions and alternatives |
| Testing | [Experimental protocol](experiment.md) | Design, procedures, controls, and stopping rules |
| Data | [Data and datasets](data.md) | Provenance, quality, licenses, and transformations |
| Method | [Method or algorithm](method-algorithm.md) | Unambiguous and implementable description of the method |
| Inference | [Analysis plan](analysis.md) | Metrics, models, uncertainty, and robustness checks |
| Traceability | [Research log](research-log.md) | Chronology of decisions, runs, and deviations |
| Verifiability | [Reproducibility and artifacts](reproducibility.md) | A package that can be independently run and checked |
| Responsibility | [Ethics, safety, and privacy](ethics.md) | Risks, limitations, approvals, and control measures |
| Communication | [Publication or R&D report](publication.md) | Manuscript and a "claim → evidence" map |
| Quality control | [Review checklists](review.md) | Stage-by-stage checks by the author, supervisor, and reviewer |

## General research cycle

`Problem → knowledge review → questions → hypotheses → protocol → data → experiment → analysis → artifacts → publication → independent verification`

The cycle may loop back. Any return to an earlier stage after the results have been seen is recorded as a protocol change with the date, the reason, and the impact on interpretation.

## Minimum standard of good research

- [ ] The problem and the expected decision are formulated separately from the desired result.
- [ ] The main question allows the answers "there is no effect", "the method is not better", or "the data are insufficient".
- [ ] The question, method, data, metric, and conclusion are linked.
- [ ] The main hypotheses and analysis are fixed before the final results are seen.
- [ ] Alternative explanations and ways to distinguish between them are stated.
- [ ] The provenance, license, and transformations of the data can be traced.
- [ ] The effect size and uncertainty are reported, not just a threshold decision.
- [ ] Negative and ambiguous results are not hidden.
- [ ] Conclusions are no broader than the population, environment, and conditions studied.
- [ ] Code, data, and instructions are available, or the reason for restricted access is explicitly explained.

## Methodological foundation

The set synthesizes general principles without copying industry checklists verbatim:

- [OECD Frascati Manual](https://www.oecd.org/en/publications/frascati-manual-2015_9789264239012-en.html) — criteria for R&D and types of research.
- [PRISMA 2020](https://www.prisma-statement.org/prisma-2020) and [PRISMA-S](https://pmc.ncbi.nlm.nih.gov/articles/PMC8270366/) — transparency of reviews and literature searches.
- [OSF Registrations](https://help.osf.io/article/330-welcome-to-registrations) and [TOP Guidelines 2025](https://www.cos.io/initiatives/top-guidelines) — preregistration, openness, and verifiability of claims.
- [FAIR Principles](https://doi.org/10.1038/sdata.2016.18) — findability, accessibility, interoperability, and reusability of data.
- [National Academies: Reproducibility and Replicability in Science](https://www.nationalacademies.org/read/25303/chapter/2) and [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current) — reproducibility and research artifacts.
- [EQUATOR](https://www.equator-network.org/toolkits/selecting-the-appropriate-reporting-guideline/) — choosing a discipline-specific reporting standard.
- [CRediT](https://credit.niso.org/) and [COPE](https://publicationethics.org/core-practices) — author contributions and publication ethics.

Date of the last methodological review: **August 25, 2026**.

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **R&D (research and development)** — systematic creative work aimed at producing new knowledge or new applications of existing knowledge. According to the Frascati Manual, it is distinguished by five criteria: novelty, creativity, uncertainty of outcome, a systematic approach, and transferability or reproducibility.
- **Reproducibility** — obtaining consistent results when the analysis is rerun with the same data, code, and steps. Disciplines use the term differently, so a publication should state its own definition.
- **Research artifact** — any material a result rests on: protocol, data, code, configurations, environment, tables, and figures. Available artifacts let others check and reuse the work.
- **Deviation log** — a dated list of changes to the frozen protocol or analysis plan: what changed, why, whether results were already visible, and how this affects interpretation. It lets readers tell what was planned from what changed along the way.
- **Confirmatory analysis** — analysis whose hypotheses and rules were fixed before the results were seen. Only such analysis supports a claim that a hypothesis was tested.
- **Exploratory analysis** — analysis that arises after looking at the data. It is useful for generating hypotheses, but its results must be clearly labeled and tested on independent data.
- **Falsifiability** — the property of a hypothesis for which an observation that would refute it can be named in advance. A hypothesis compatible with any result tests nothing.
- **Robustness checks** — repeating the analysis under other plausible choices (model specification, metric, exclusion rules, subsets) to confirm that the substantive conclusion does not depend on them.
- **Effect size** — the quantitative magnitude of a difference or association, such as a difference in means, an odds ratio, or a metric gain. Unlike a p-value, it shows how large and practically important an effect is.
- **Uncertainty** — the range of plausible values for an estimate, usually expressed as an interval, a standard error, or the spread across repeated runs. Without it, a single number cannot be interpreted properly.
- **Population** — the set of people, objects, or situations to which a conclusion is meant to apply. The sample is the part actually observed; conclusions should not extend beyond the population and conditions studied.
- **Frascati Manual** — the OECD guidance on defining and measuring R&D. It sets out five criteria of R&D and three types of activity: basic research, applied research, and experimental development.
- **PRISMA (Preferred Reporting Items for Systematic Reviews and Meta-Analyses)** — a reporting guideline for systematic reviews and meta-analyses: a checklist and a diagram of the study selection flow (PRISMA flow diagram). PRISMA-S is an extension for reporting literature searches. Following the checklist makes a review transparent but does not by itself guarantee the quality of its design.
- **OSF (Open Science Framework)** — a free platform from the Center for Open Science for storing project materials and registering them, including study preregistrations and review protocols.
- **TOP Guidelines (Transparency and Openness Promotion)** — Center for Open Science recommendations for journals, funders, and research organizations on transparency standards: sharing data, code, and materials, study registration, and verifiability of claims.
- **Preregistration** — a time-stamped record of hypotheses, design, and analysis plan made before data are collected or examined, usually in a public registry. It makes it possible to separate confirmatory from exploratory analysis.
- **FAIR (Findable, Accessible, Interoperable, Reusable)** — principles stating that data and metadata should be findable, accessible, interoperable, and reusable. FAIR does not require data to be open: access may be restricted as long as the access conditions are clearly described.
- **Replication (replicability)** — testing the same scientific question with new data, often by another team, in another setting, or with another implementation. Consistent results increase confidence in the conclusion.
- **National Academies** — the U.S. National Academies of Sciences, Engineering, and Medicine. Their report "Reproducibility and Replicability in Science" (2019) provides widely used definitions of reproducibility and replicability and recommendations for achieving them.
- **ACM Artifact Review and Badging** — the Association for Computing Machinery policy for reviewing research artifacts of papers and awarding badges: Artifacts Available, Artifacts Evaluated (Functional, Reusable), and Results Validated (Reproduced, Replicated).
- **EQUATOR Network** — an international initiative to improve the quality and transparency of research reporting (primarily in health research). It maintains a database of reporting guidelines and helps choose the right one for a given design.
- **Reporting guideline** — a checklist of what a publication must describe for a given study design, for example CONSORT for randomized trials or PRISMA for systematic reviews. It helps avoid omitting essential details of methods and results.
- **CRediT (Contributor Roles Taxonomy)** — a standard taxonomy of 14 contributor roles in research (for example, Conceptualization, Methodology, Software, Formal analysis) that makes each author's contribution explicit.
- **COPE (Committee on Publication Ethics)** — an international organization that publishes standards of publication ethics (Core Practices) and guidance for editors, authors, and reviewers, including on authorship, conflicts of interest, and corrections to the published record.
