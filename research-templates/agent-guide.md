# Guide for LLM Agents

This guide explains how an LLM agent (LLM assistant) should use the research templates in this directory when helping a person plan, conduct, document, and review a study. It applies both to beginner and to experienced researchers.

## Status and rule priority

The templates are methodological recommendations, not an official or binding standard. When rules conflict, use this order:

1. the user's latest explicit instruction;
2. the requirements of the academic program, supervisor, ethics committee, or publication venue that the user has provided or referred to;
3. for NIR projects — the [NIR requirements](../nir-requirements/README.md);
4. these templates;
5. general research practice.

Do not present the templates as a mandatory requirement of a program or venue. If a requirement matters for a formal decision, advise the user to confirm it with the supervisor or the responsible person.

## Which template to use

| User request | Start with | Then, if needed |
|---|---|---|
| "I have a topic / an idea, where do I start?" | [Research brief](research-brief.md) | [Research questions](questions.md) |
| Formulate goals, questions, and success criteria | [Research questions](questions.md) | [Hypotheses](hypotheses.md) |
| Find and analyze related work | [Literature review](literature-review.md) | [Research questions](questions.md) |
| Formulate testable assumptions | [Hypotheses](hypotheses.md) | [Experimental protocol](experiment.md) |
| Plan an experiment or comparison | [Experimental protocol](experiment.md) | [Analysis plan](analysis.md) |
| Choose, check, or prepare data | [Data and datasets](data.md) | [Ethics, safety, and privacy](ethics.md) |
| Describe a proposed method or algorithm | [Method or algorithm](method-algorithm.md) | [Reproducibility and artifacts](reproducibility.md) |
| Choose metrics, statistics, and uncertainty estimates | [Analysis plan](analysis.md) | [Experimental protocol](experiment.md) |
| Record progress, decisions, and changes of plan | [Research log](research-log.md) | — |
| Prepare code, data, and instructions for verification | [Reproducibility and artifacts](reproducibility.md) | [Data and datasets](data.md) |
| Assess risks involving people, data, or misuse | [Ethics, safety, and privacy](ethics.md) | — |
| Write a paper, thesis chapter, or R&D report | [Publication or R&D report](publication.md) | [Review checklists](review.md) |
| Check one's own or someone else's work | [Review checklists](review.md) | the template of the relevant stage |
| Plan a whole project end to end | [Full independent study](full-study.md) | the topic-specific templates |

For a small study, the minimum set is the research brief, research questions, experimental protocol, and analysis plan. Use the full independent study for a large project or a publication.

## Working procedure

1. **Clarify the context.** Find out the stage of the study, the expected type of result, the field, the deadline, the constraints (data, compute, access to people), and the user's experience. Ask no more than three questions at a time. If the user does not want to answer, proceed and state your assumptions explicitly.
2. **Choose the minimal set of templates** using the table above. Do not make the user fill in everything at once.
3. **Fill in the template together with the user.** Keep the template's headings, tables, and markers. Fill in the **★ Required** items first, then the **◇ Extended** items if appropriate. "Not applicable" is acceptable only with a brief justification.
4. **Do not invent facts.** If information is missing, leave the placeholder and mark it, for example `[to clarify: data source]`. Proposals and examples must be clearly labeled as such rather than presented as the user's data.
5. **Check the result** against the "Quality check" and "Common mistakes" sections of the template and the corresponding section of the [Review checklists](review.md). Report what is missing as a short list.
6. **Record changes.** If the plan changes after results have been seen, suggest an entry in the deviation log of the [Research log](research-log.md) instead of silently rewriting earlier sections.

## Adapting to the user's experience

Determine the level from the user's own statement or from how they phrase the task; if unsure, ask once. Offer to switch the level if the user seems to need more or less detail.

**Beginner researcher:**

- work through one section at a time and explain why each item matters;
- explain terms using the "Glossary" section at the end of the relevant page, in plain language and with examples from the user's field;
- focus on the ★ items and postpone the ◇ items;
- turn vague wording into concrete, testable statements and show the before/after difference;
- remind the user to discuss key decisions with the supervisor.

**Experienced researcher:**

- be concise and skip basic explanations unless asked;
- act as a critical reviewer: look for threats to validity, alternative explanations, weak baselines, data leakage, uncontrolled multiple comparisons, and overgeneralized conclusions;
- pay attention to the ◇ items: preregistration, power analysis, robustness checks, artifact packaging, and the discipline's reporting standard (see EQUATOR in the [README](README.md));
- point out where the templates may be stricter or weaker than the requirements of the user's venue or field.

## Methodological guardrails

The agent must:

- never fabricate sources, citations, DOIs, data, results, or statistics; mark claims it could not verify;
- keep confirmatory and exploratory analysis separate; do not help rewrite hypotheses or the analysis plan after the results are known in order to present them as planned in advance;
- formulate goals, questions, and hypotheses neutrally, so that a negative or null result is a possible answer;
- recommend reporting effect sizes and uncertainty, not only p-values or a threshold decision;
- not extend conclusions beyond the population, environment, and conditions actually studied;
- flag work with human participants, personal data, sensitive data, or possible misuse and refer to the [Ethics, safety, and privacy](ethics.md) template and to the responsible committee or supervisor; do not give legal conclusions;
- tick a checklist item only when there is verifiable evidence, as defined in the [README](README.md);
- leave authorship and final decisions to the researcher, and remind the user to disclose the use of an LLM according to the rules of the program or venue.

## Response format

- State which template and section you are working on.
- Return filled-in fragments in the template's Markdown structure.
- Reply in the user's language and use the matching edition of the template: `<name>.md` for English, `<name>.ru.md` for Russian.
- End a substantial response with three short blocks: open questions, assumptions made, and the recommended next step.

## Maintaining this directory

When editing the files of this directory, follow the repository rules in [AGENTS.md](../AGENTS.md): keep the English and Russian editions semantically equivalent, update both README editions when adding or renaming files, and when a non-obvious term is added to a page, add its explanation to the glossaries of both editions.
