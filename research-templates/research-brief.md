# Research Brief and Problem Statement Template

The brief answers the question: **why investigate, what uncertainty is being resolved, and what decision will change**. It is useful to fit it into 1–3 pages; details are moved to the other templates.

## Fill-in form

### 1. Identification

- ★ Working title: [title]
- ★ Client/problem owner: [name or role]
- ★ Researcher/team: [names and roles]
- ★ Start date and checkpoint date: [dates]
- ★ Type of output: [new knowledge / publication / decision / prototype / algorithm / dataset / standard]
- Maturity status before and after: [description or TRL, if applicable]

### 2. Problem without a premature solution

> In the context of **[environment/user/system]**, we observe **[verifiable fact or symptom]**, which leads to **[consequence]**. We do not yet know **[key uncertainty]**. Without the study, the decision **[which one]** will be made on the basis of **[insufficient data/assumption]**.

- ★ Source of the observation: [metric, data, interview, publication]
- ★ Scale and frequency: [magnitudes and period]
- ★ Why this matters now: [trigger]
- What is a symptom and what is a presumed cause: [separate them]

### 3. Why this is R&D

Check the five criteria from the Frascati Manual. Not everything that is new to the team constitutes research.

| Criterion | Evidence in this task |
|---|---|
| Novelty | [what knowledge/application does not yet exist] |
| Creativity | [what non-obvious concept or method is required] |
| Uncertainty of outcome | [what may fail and why the outcome is not known in advance] |
| Systematic approach | [plan, resources, protocol, recording of results] |
| Transferability/reproducibility | [how the knowledge can be verified or reused] |

- Type: [basic research / applied research / experimental development]
- If this is not R&D: [engineering, analytical, educational, or operational task]

### 4. Decision and stakeholders

- ★ Decision after the study: [choose A/B; continue/stop; publish; invest]
- ★ Decision maker: [role]
- ★ Date by which the knowledge is valuable: [date]
- Users of the result: [who]
- Affected groups, including those not directly involved: [who may benefit or be harmed]
- What happens if the decision is wrong: [false-positive/false-negative conclusion]

### 5. Aim and contribution

> The aim is to **[obtain/estimate/explain/compare] [object]** under **[boundaries]** in order to **[decision or scientific contribution]**.

- ★ Expected new contribution: [empirical / methodological / theoretical / dataset / negative result]
- ★ Difference from the closest work/practice: [specifically]
- Desired result: [what we hope to see]
- Neutral statement of the result: [allows for any outcome]

### 6. Scope

| In scope | Out of scope | Why |
|---|---|---|
| [population/environment/version/period] | [exclusion] | [justification] |

- Unit of analysis: [person, query, model, organization, run]
- Geography/language/domain: [boundaries]
- Time horizon: [boundaries]
- Acceptable extrapolation: [where the conclusion may be transferred]

### 7. Prior knowledge and assumptions

| ID | Statement | Status | Basis | What happens if it is wrong |
|---|---|---|---|---|
| A1 | [statement] | [fact/assumption/opinion] | [reference] | [impact] |

- ★ The three most critical assumptions: [A1–A3]
- ★ What has already been tried: [methods and results]
- Contradicting data: [references]

### 8. Completion criteria

- ★ The study is sufficiently informative if: [precision/quality/power to discriminate between alternatives]
- ★ Practically significant threshold: [value, units, basis]
- ★ An "inconclusive" result is declared if: [conditions]
- ★ Stop criteria: [inability to obtain data, ethical risk, cost, lack of variation]
- ◇ Value of additional information: [which next measurement could change the decision]

### 9. Resources and constraints

| Resource | Available | Needed | Constraint/owner |
|---|---|---|---|
| People | [ ] | [ ] | [ ] |
| Data | [ ] | [ ] | [ ] |
| Compute/equipment | [ ] | [ ] | [ ] |
| Time | [ ] | [ ] | [ ] |
| Budget | [ ] | [ ] | [ ] |
| Expertise | [ ] | [ ] | [ ] |

### 10. Top-level risks

| Risk | Likelihood | Impact | Early signal | Measure | Owner |
|---|---|---|---|---|---|
| [risk] | [estimate] | [estimate] | [indicator] | [measure] | [role] |

Check separately: data access and licenses; privacy; safety; conflicts of interest; dependence on an external service; impossibility of replication; publication bias; technological immaturity.

### 11. Artifact plan

- ★ Before launch: [brief, review, RQs, protocol, analysis plan, risk review]
- ★ During the work: [log, raw data manifest, code, environment versions]
- ★ After the work: [report, tables/figures, data/code, limitations, decision memo]
- Storage location and access rules: [link]

## Quality check

- [ ] The problem is described through observed facts rather than in the form of a desired solution.
- [ ] It is clear which uncertainty makes the task a research task.
- [ ] There is a specific decision owner and a deadline by which the result is valuable.
- [ ] The aim allows for a negative or null result.
- [ ] The scope and non-goals are visible.
- [ ] Practical significance is not replaced by statistical significance.
- [ ] Stop criteria are formulated before the main expenditure of resources.
- [ ] Risks include affected people and data limitations, not just timelines.

## Common mistakes

- "Prove that our method is better" — replace with a neutral comparison against a predefined criterion.
- "Create a new algorithm" — this is an output, not a research problem.
- "Study topic X" — there is no decision, no scope, and no verifiable result.
- Novelty only within the organization — check the external literature and existing solutions.
- TRL used as a measure of a paper's quality — it is a technology maturity scale, not a measure of a conclusion's credibility.

Methodological basis: [OECD Frascati Manual](https://www.oecd.org/en/publications/frascati-manual-2015_9789264239012-en.html), [NASA Technology Readiness Levels](https://www.nasa.gov/directorates/somd/space-communications-navigation-program/technology-readiness-levels/).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **TRL (Technology Readiness Level)** — a technology maturity scale introduced by NASA, from 1 (basic principles observed and reported) to 9 (system proven through successful operation in its real environment). It describes technology maturity, not the reliability of a scientific conclusion.
- **R&D (research and development)** — systematic creative work aimed at producing new knowledge or new applications of existing knowledge. According to the Frascati Manual, it is distinguished by five criteria: novelty, creativity, uncertainty of outcome, a systematic approach, and transferability or reproducibility.
- **Frascati Manual** — the OECD guidance on defining and measuring R&D. It sets out five criteria of R&D and three types of activity: basic research, applied research, and experimental development.
- **Basic research, applied research, experimental development** — the three types of R&D in the Frascati Manual: acquiring new knowledge without a specific application in view; acquiring knowledge directed at a specific practical aim; and using knowledge to create or improve products and processes.
- **False positive and false negative** — wrongly concluding that an effect exists when it does not, and that there is no effect when there is one. The cost of each error determines how strict the decision criteria should be.
- **Unit of analysis** — the entity on which results are computed and interpreted: a person, query, model, organization, or run. Its choice determines sampling, data splits, and the statistical model.
- **Extrapolation** — extending a conclusion beyond the population, conditions, or range of values in which it was obtained. It is acceptable only with separate justification.
- **Assumption** — a statement taken as true without being tested within the current work. Critical assumptions should be stated explicitly: if they are wrong, the conclusion may not hold.
- **Practical significance** — whether an effect is large enough to change a decision in practice; the threshold is set in advance on domain grounds. It is not the same as statistical significance.
- **Stop criteria (stopping criteria)** — conditions, set in advance, under which a study is stopped or paused: data cannot be obtained, risk becomes unacceptable, the budget is exceeded, or the work proves futile. They are set before the main resources are spent.
- **Value of information** — an estimate of how much the next measurement or study could change a decision. It helps determine whether further data collection is worthwhile.
- **Publication bias** — the tendency to publish mainly positive and statistically significant results. Because of it, the literature overstates effects and negative results get lost.
- **Raw data manifest** — a list of the original, unprocessed data files with their source, date obtained, and checksums. It confirms that the raw data have not been altered.
- **Decision memo** — a short document for the decision-maker: what was learned, how reliable the evidence is, which decision is recommended, and what it costs and risks.
- **Null and negative results** — results that show no expected effect or no advantage of a method. With sufficient precision they are valid knowledge and should be reported.
- **Non-goals** — an explicit list of what a study or method deliberately does not address. It helps keep the scope of the work in check and prevents overreaching conclusions.
- **Statistical significance** — the conventional conclusion that a p-value is below a preselected threshold (for example, 0.05). It says nothing about the size or practical importance of an effect.
