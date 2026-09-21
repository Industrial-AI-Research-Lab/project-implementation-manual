# NIR Project Requirements and Assessment Framework

## Additional format: group project

A group project is an additional format available only upon application by a NIR supervisor.

Students may not independently form a group to carry out this type of project. It is available only to first-year students.

### What is assessed?

- the scale and depth of the task;
- whether project volume matches the number of participants: its volume and complexity must equal the combined work the participants could have completed individually;
- scientific and/or technological novelty;
- technical standard and implementation quality;
- integrity of the result and consistency of decisions made by different participants;
- readiness for practical use and/or further development; and
- participants' ability to work as a team and meet deadlines.

### Required results

- a public implementation repository containing every participant's work; all participants must be contributors, and authorship of code sections must be assessable;
- a presentation describing the shared problem, solution architecture, allocation of work, implementation process, and main results;
- an individual report from every participant describing their part, its results, and their personal contribution;
- a description of task allocation and relationships among project components;
- a demonstration of the working result where a software or technological product applies;
- an assessment of every participant's contribution by the supervisor and/or team members;
- evidence that each participant's actual work matches their stated role and demonstrates sufficient complexity and independence; and
- where necessary, evidence from commit history, an issue or task tracker, experiments, documentation, and other artifacts.

### Specific features

A group project addresses one complex task whose volume and complexity are comparable to the combined expected work of all participants' individual projects. A project with N participants must therefore contain work equivalent to N individual projects. Every participant must have an independent, substantively significant part whose results can be identified and assessed separately.

Mechanically dividing one task into several small pieces is not sufficient. Each contribution must include independent work requiring the program's professional competencies, and the participants' results must be integrated into one final project outcome.

The supervisor does not need to divide the project into formal subtopics.

Students should not be informed about this project type until supervisors submit applications.

# Extended Assessment Criteria for Master's NIR Projects

## 1. General assessment principles

Projects are assessed at six levels:

- **5A** — excellent / high-level project; all requirements are met in full;
- **4B** — good / high level, but not every requirement is fully met;
- **4C** — good / sufficiently high level;
- **3D** — satisfactory / minimum sufficient level;
- **3E** — satisfactory / borderline sufficient level; and
- **2FX** — unsatisfactory / substantial revision is required.

The grade depends not only on the amount of work completed, but on all of the following:

1. relevance and justification of the problem statement;
2. depth of problem development;
3. quality and independence of the result;
4. quality of experimental or practical validation;
5. presence and quality of comparison with existing solutions and alternatives;
6. code and repository quality;
7. quality of the main written artifact;
8. presentation and talk quality;
9. the student's ability to explain decisions and results;
10. alignment between the result and the declared project type; and
11. for group and collaborative projects, teamwork quality and individual contribution.

## Mandatory conditions for a 5A grade

A 5A grade cannot be awarded if any of the following fundamental conditions is missing.

### 1. All mandatory artifacts are present

The project must include every artifact required for its type:

- a code repository where required;
- a scientific preprint, technology report, or solution description;
- a presentation;
- an industry-partner review for an industrial project;
- a team-contribution assessment for a collaborative project; and
- an individual contribution report for a group project.

A missing mandatory artifact automatically limits the maximum grade below 5A. A link alone does not constitute a quality artifact: its content must satisfy the project requirements.

### 2. The result is compared with existing solutions

For 5A, the project must show how the proposed solution differs from existing approaches and how effective it is relative to them. The comparison must include:

- relevant methods, algorithms, models, systems, or tools;
- clearly defined metrics;
- identical or comparable experimental conditions;
- quantitative results; and
- interpretation of the observed differences.

“Our method is better” without quantitative evidence is not a comparison.

Acceptable measures include:

- quality: Accuracy, F1, ROC-AUC, BLEU, ROUGE, pass@k, and similar metrics;
- speed: latency and throughput;
- computational efficiency: training time, GPU hours, and memory;
- cost: token count, API-call cost, and inference cost;
- reliability: failure rate and success rate;
- generation quality: task success rate and human evaluation; and
- for industrial tasks: business metrics, economic impact, and reductions in time or resource use.

Without comparison with alternatives, 5A is impossible.

### 3. The result is reproducible

Another researcher or developer must be able to determine:

- which data were used and how they were prepared;
- which model or algorithm was used;
- which parameters were selected;
- how to run the code;
- how to obtain the main results; and
- which experimental limitations apply.

### 4. The student understands their own work

At the defense, the student must independently and confidently explain the problem, method, solution architecture, key algorithms, experimental design, metrics, baseline, results, limitations, and causes of the observed results.

Working code does not compensate for a lack of understanding. Inability to explain a substantial part of the work is grounds for lowering the grade regardless of the artifacts present.

# Assessment by Project Type

## Scientific project

### What is assessed

- scientific novelty;
- correctness of the scientific problem statement;
- quality of the review of existing approaches;
- justification of the proposed method;
- experiment quality;
- comparison with baselines and/or state-of-the-art methods;
- statistical and methodological soundness;
- publication readiness; and
- reproducibility.

### 5A — high-level scientific result

The student produces a substantively new scientific result that is convincingly supported experimentally or theoretically, with all requirements for the problem statement, results, justification, and presentation met in full.

The problem is relevant and clear; limitations of existing methods are shown; a specific hypothesis or research question and explicit novelty are stated; the method makes an independent contribution; relevant alternatives are compared quantitatively; a strong baseline and, where possible, current state-of-the-art methods are used; ablation or component analysis is performed; the experimental design supports the conclusions; results are robust and interpretable; limitations are explicit; a complete preprint and reproducible repository are provided; every artifact is present; the presentation communicates the scientific contribution; and the student answers the committee confidently.

**Mandatory condition:** without quantitative comparison with existing solutions, 5A cannot be awarded.

### 4B — strong scientific result

The work is scientifically strong but has individual shortcomings. It may include an interesting problem, an original method, sound experiments, several baselines, quantitative metrics, and convincing results. However, the experimental scope or comparisons may be incomplete, ablation may be limited, evaluation may cover too few datasets, some results may need confirmation, or the paper may not yet be ready for submission. The student understands and can explain the research.

### 4C — good result with substantial gaps

An independent and substantive result exists, but the scientific evidence is incomplete. The method and experiments exist, quantitative results and at least a basic comparison are provided, and an advantage or difference is shown. However, the baseline, important comparisons, number of experiments, component analysis, proof of novelty, hypothesis, or preprint quality has substantial gaps. This is real research work, but not yet a complete study.

### 3D — minimally sufficient scientific result

The work shows subject knowledge and some original result, but the study is substantially incomplete. A relevant task, implemented method, individual experiments, and results exist, and the student understands the basic idea. However, experiments and comparisons are weak, the baseline may be absent or incorrect, metrics are insufficiently justified, novelty is unconvincing, results need confirmation, and artifacts need major revision.

### 3E — borderline scientific result

There is evidence of work at the minimum acceptable level: a task, implementation, individual results, and a basic explanation. Experiments are extremely limited; comparison is absent or uninformative; metrics are superficial; novelty is not demonstrated; conclusions exceed the evidence; and artifacts are incomplete or poor. A 3E is not “almost 4”; substantial revision is needed.

### 2FX — unsatisfactory scientific project

There is no convincing research result. Experiments may be absent or superficial; results lack analysis; the student does not understand the methodology; novelty or valid comparison is absent; conclusions do not follow from experiments; essential artifacts are missing; or the repository cannot verify the claims. Running a model on a few examples and reporting several numbers without a scientific conclusion is a typical 2FX case.

The grade is also 2FX when no supervisor was secured for the semester or no supervisor feedback and grade were provided before the NIR defense. Supervisor feedback and a grade are required for admission to the defense.

## Technological project

### What is assessed

- relevance and quality of the technological problem statement;
- technical novelty;
- architecture and implementation quality;
- code quality, reproducibility, and testing;
- comparison with existing solutions; and
- practical value.

### 5A — high-standard technological solution

A complete working technological system solves a relevant task and demonstrates advantages over existing solutions. The technological problem, relevance, alternatives, constraints, and independent technical solution are clearly defined. Quantitative comparison uses relevant metrics. Practical value and testing are shown; complex systems include component analysis; the repository has a strong README, launch instructions, pinned dependencies, tests, structured code, and documented decisions; a high-quality technology report and clear presentation are provided; and the student confidently explains technical decisions.

A working system without comparison cannot receive 5A.

### 4B — strong technological result

A working system solves the task well, with independent implementation, good architecture, adequate testing, a usable repository, documentation, measurable results, and comparison with some existing solutions. Benchmark breadth, baselines, testing, optimization, or performance analysis may be incomplete, but the result is a complete technological product.

### 4C — good technological result

A working prototype solves the task, but technical development is incomplete. Architecture, testing, documentation, interface, scenario coverage, comparison, or operational measurements may be weak. The result nevertheless works and demonstrates independent technical work.

### 3D — minimally sufficient technological result

A runnable prototype or technical component exists, but functionality, code quality, documentation, testing, comparison, architecture, and practical applicability have substantial limitations. The result can still be launched and demonstrated.

### 3E — borderline technological result

Implementation fragments, experiments, a prototype, or an individual technical effect exist, but the system is unstable, poorly documented, difficult to reproduce, untested, not compared with alternatives, or addresses only a small part of the task.

### 2FX — unsatisfactory technological project

There is no working or verifiable technological result. Code may be absent, fail to run, or not match the task. The result may be far smaller than claimed, the repository may contain superficial or non-working code, evidence may be absent, the student may not understand the architecture, experiments may be missing, or only numbers and screenshots may exist without a working solution.

## Industrial project

### What is assessed

An industrial project must solve a real or realistic practical problem rather than merely demonstrate an ML or LLM application. Assessment covers industrial relevance, correctness of the problem statement, business or production context, solution quality, deployment potential, quantitative impact, comparison with the current process, implementation quality, and work with the industrial customer.

### 5A — highly developed solution to a relevant industrial problem

The solution addresses a relevant industrial need, has a clear user or customer, solves a specific problem, demonstrates practical value, quantitatively improves the existing approach or process, has measurable impact and a comparison with current practice, is confirmed by an industry representative, has a high-quality implementation, and has realistic deployment prospects.

A substantive industry review, technical artifact, project description, presentation, and quantitative results are mandatory. Saying that a company could use the solution is not enough; the project must show why the company needs it and what impact it provides.

### 4B — strong industrial result

The task is genuinely relevant, and a working solution has clear application potential. Quantitative results, comparison with the current process, evidence of partner interest, and a quality implementation exist. Full piloting, economic-impact analysis, dataset breadth, or testing breadth may still be incomplete.

### 4C — good industrial result

The working solution has clear practical value, but industrial development is limited. A prototype, real problem, potential user, and measurable results exist, but a full pilot, adequate comparison, precise economic estimate, deployment infrastructure, or technical maturity is missing.

### 3D — minimally sufficient industrial result

The work is connected to a real industrial problem and produces some result, but the task may be too broad, impact unmeasured, comparison weak, the prototype limited, industry confirmation superficial, or deployment unrealistic.

### 3E — borderline industrial result

AI is applied to a potentially practical task, but practical significance is not demonstrated. A demo prototype and individual results may exist, but convincing impact, comparison with current practice, evidence of applicability, or a complete implementation is missing.

### 2FX — unsatisfactory industrial project

Practical relevance is not demonstrated or no result exists. The task may be artificial, lack an industrial user, be unrelated to a real process, have no measured impact, have a non-working prototype, lack the required review, or leave the student unable to explain why industry needs the solution.

## Collaborative project

### What is assessed

A collaborative project evaluates both the overall outcome and the student's individual contribution: quality and independence of their part, deadlines, teamwork, communication, integration, technical or research complexity, and understanding of the overall result.

### 5A — high-level teamwork and an independent, significant contribution

The student performs a substantively challenging part, independently defines and completes subtasks, materially affects the result, interacts regularly, meets deadlines, documents the work well, provides a reproducible result, understands its place in the overall system, explains technical decisions, and demonstrates strong professional and soft skills. Evidence of the team contribution is mandatory. Participation alone cannot earn 5A.

### 4B — strong team contribution

The student independently completes a substantial part to a high standard, meets deadlines, communicates effectively, integrates the result, explains the work, and noticeably affects the outcome. Individual limitations in depth, independence, or communication remain.

### 4C — good team contribution

The student completes assigned tasks and is a full team member, but independence is limited, some tasks need constant supervision, documentation is incomplete, deadlines may slip, or the contribution is less significant than those of stronger team members. The student still completes and understands their part.

### 3D — minimally sufficient team contribution

An identifiable contribution related to the final project exists, but the student needs substantial team help, completes tasks only partially, sometimes misses deadlines, contributes within a narrow scope, communicates imperfectly, or lacks understanding of the overall architecture.

### 3E — borderline team contribution

Participation is formal and the contribution minimal. Only small supporting tasks may be completed; other participants may redo work; deadlines may be substantially missed; communication may be weak; and the contribution may be difficult to separate.

### 2FX — unsatisfactory team contribution

The student did not complete their part or the contribution cannot be verified. Tasks may be incomplete, the result not integrated, the student unable to explain it, substantial work completed by others, deadlines systematically missed, or communication absent.

## Group project

A group project differs from a collaborative project because its single shared project must have a scale equal to the combined work of all participants. For N people, volume and complexity must match N individual projects. Assessment covers the shared result, scale, complexity, individual contributions, and integration.

### 5A — outstanding group result

The group creates a complex integrated result whose scale matches the combined work of its participants. The task is relevant; scale matches team size; everyone owns an independent, substantive area; every contribution is identifiable; components form one result; relevant alternatives are compared quantitatively; metrics and component analysis are appropriate; the result is reproducible; repository and documentation are strong; all artifacts and individual reports are present; the presentation shows both the shared result and individual contributions; every participant explains their part and its relationships; and teamwork is effective.

A one-person project artificially divided among several students cannot receive 5A.

### 4B — strong group result

A complete complex project exists. Scale largely meets team requirements, work is allocated, components are integrated, measurable results and comparisons exist, repository and documentation are strong, and most individual contributions are substantive. Benchmarking, individual components, experiments, integration, or balance of contributions may have isolated weaknesses.

### 4C — good group result

The project has sufficient scale and is genuinely collaborative. Several independent components and a working shared result exist; contributions can be identified; and basic quantitative results and some comparisons are present. Some parts may be underdeveloped, integration or experiments incomplete, documentation weak, or individual contributions insufficiently substantive.

### 3D — minimally sufficient group result

Different participants completed several parts and a shared prototype exists, but scale or quality is insufficient. The volume may be too small for the number of participants, some people may do only supporting work, components may be poorly integrated, experiments and comparisons weak, or repository quality inadequate.

### 3E — borderline group result

The project is formally group-based but does not meet the required scale. Several participants may work on one small task, most work may be done by one or two people, contributions may be hard to distinguish, the final result small, integration superficial, and quantitative evaluation weak.

### 2FX — unsatisfactory group project

There is no unified working result; volume is far below the combined expected work; individual contributions cannot be identified; much of the stated work is absent; components are not integrated; artifacts or evidence of operation are missing; participants cannot explain their contributions; or the project is one small individual task merely declared a group project.

# Artifact Criteria

## Code and repository quality

Repository quality is assessed separately for every project with a software implementation.

### 5A level

The repository has a clear structure and informative README; states the problem; provides installation and launch instructions; reproduces the main experiments; pins dependencies; includes configuration files and necessary tests; uses modular, readable code without obvious duplication and with clear names; has a development history spanning the semester; organizes experiment results; excludes secrets and API keys; and documents the architecture of complex systems.

### 4B level

The repository is well organized and the solution can be launched, but some documentation, testing, or structural details need improvement.

### 4C level

The code works, but documentation is weak, launch is difficult, modularity or tests are insufficient, or structure is unclear.

### 3D level

The code demonstrates an individual result, but reproducibility is limited.

### 3E level

Code exists, but launching it and verifying the result are substantially difficult.

### 2FX

Code is absent, does not run, does not match the stated solution, or cannot verify the result.

## Presentation and defense quality

Presentation quality is assessed separately from project content.

### 5A

The presentation is clear, quickly introduces the problem and relevance, reviews existing solutions, states the gap and original contribution, explains the architecture or method and experimental design, presents quantitative results and comparisons, discusses limitations, and draws conclusions strictly from the data. The speaker does not read slides, speaks independently, answers questions, understands details, engages with committee comments, and explains why the observed results occurred.

### 4B

The presentation is clear and sequential, motivates the problem, describes the main alternatives and contribution, explains the method and experiments, presents quantitative results and comparisons, interprets them correctly, and supports evaluation of the result. The student speaks mostly independently, understands the work, explains key decisions and limitations, answers the main questions, and may struggle only with a few deep or unexpected questions.

### 4C

The main content is understandable, but some results are poorly visualized, the narrative is inconsistent, motivation is weak, or answers are not always confident.

### 3D

The overall idea is understandable, but slides contain too much text, too few results, weak methodological explanation, broken logic, or superficial answers.

### 3E

The presentation formally contains project information but does not allow meaningful assessment. The speaker has a weak grasp of the work, cannot explain some decisions, or cannot answer substantive questions.

### 2FX

The defense cannot establish that the student understands and completed the claimed work. The student may be unable to explain the method, comparisons, metrics, or results; a substantial part of the presentation may be automatically generated text; or basic questions may go unanswered.

# Overall Interpretation of Grades

| Grade | General description |
|---|---|
| **5A** | A complete, relevant, independent, and convincingly demonstrated result. Every mandatory artifact is present, quantitative comparison uses relevant alternatives, and the student understands and can defend the result. |
| **4B** | A strong, nearly complete result. Main requirements, comparison, and measurable results are present, but individual substantial shortcomings remain. |
| **4C** | A good substantive result with noticeable gaps in experiments, comparison, technical development, or presentation. |
| **3D** | A minimally sufficient result: real work was completed, but many requirements remain underdeveloped. |
| **3E** | A borderline sufficient result: there is evidence of independent work and some result, but the project is substantially incomplete. |
| **2FX** | No convincing result exists, or its quality, reproducibility, or independence cannot be verified. Substantial revision is required. |

# The “building it is not enough” principle

The committee assesses not only whether a result exists, but whether its quality has been demonstrated.

It is not enough to implement a model, obtain one metric, show an attractive chart, compare two versions of the student's own method, claim superiority without explaining the baseline, claim novelty or industrial applicability, or show a working prototype without analyzing existing alternatives.

The project must demonstrate:

**problem → relevance → existing solutions → research gap → original contribution → method → experiment → metrics → comparison → analysis → conclusion.**

For complex systems:

**system → components → contribution of each component → ablation or component analysis → comparison with alternatives → overall effect.**

# Maximum-grade caps

| Situation | Maximum grade |
|---|---|
| Not all mandatory artifacts are present | no higher than 4B |
| No quantitative comparison with existing alternatives | no higher than 4C |
| No substantive baseline or alternative | no higher than 3D |
| No component-contribution analysis for a complex multi-component system | no higher than 4C |
| The student cannot explain a substantial part of their own work | no higher than 3D |
| Relevance has not been demonstrated | no higher than 4C |
| No working or verifiable result | no higher than 3E; 2FX if no substantive result exists |
| The repository cannot verify the claimed result | no higher than 4C |
| An industrial project lacks the mandatory partner evaluation or review | no higher than 4B |
| A group project's volume is substantially below the participants' combined expected work | no higher than 4C |
| Individual contributions cannot be identified in a group project | no higher than 4C |
| The presentation does not communicate the problem, method, and results | no higher than 4C |
| The student cannot answer basic questions about their work | no higher than 3D |

A formal artifact does not automatically satisfy its requirement. A few lines in a README are not quality documentation, and a table of numbers is not necessarily a valid experimental comparison.

# Final-grade principle

The final grade is determined by the weakest critical components, not a simple arithmetic mean. Excellent code, presentation, and a working prototype cannot produce 5A if the required metric-based comparison is absent. Likewise, an interesting scientific hypothesis without experiments cannot earn a high grade solely for potential novelty.

A 5A is awarded only when relevance, quality, novelty or practical value, experimental soundness, advantage over or difference from existing solutions, artifact quality, and student understanding are all demonstrated simultaneously.

# Project Assessment Matrix

## 1. General assessment matrix

This matrix applies to scientific, technological, industrial, collaborative, and group projects.

| Criterion | 5A | 4B | 4C | 3D | 3E | 2FX |
|---|---|---|---|---|---|---|
| **1. Problem relevance** | High scientific, technological, or industrial relevance; who needs the result and why is clear and supported by context analysis. | Relevant and convincingly justified, but context is not fully developed. | Relevant, but justification is superficial or too general. | Relevance is evident but barely justified. | Relevance is asserted with almost no convincing argument. | Relevance is unproven or the task lacks substantive value. |
| **2. Problem statement** | Inputs, outputs, constraints, success criteria, and a specific research or technological question are clearly formalized. | Clear and correct with individual details needing refinement. | Formulated, but success criteria or constraints are imprecise. | General intent is clear, but formalization is weak. | Vague with almost no success criteria. | The task being solved cannot be understood. |
| **3. Analysis of existing solutions** | Substantive analysis of relevant alternatives, baselines, and/or state of the art motivates the proposed approach. | Main alternatives and their strengths and weaknesses are covered. | Alternatives are covered superficially or incompletely. | Several alternatives are named without deep analysis. | Alternatives are mentioned formally. | Alternatives are absent or irrelevant. |
| **4. Comparison and metrics** | Quantitative comparison with relevant alternatives uses justified metrics and comparable conditions, with interpreted results. | Quantitative comparison with several relevant alternatives exists, but could be broader. | At least a basic quantitative comparison exists but is limited. | Comparison is partial, weak, or methodologically limited. | Individual numbers do not support meaningful comparison. | Comparison is absent or cannot support a quality conclusion. |
| **5. Original result** | Independent, substantively significant result fully matches the task. | High-quality independent result with minor limitations. | Working result with limited depth or completeness. | Partial result. | Individual result fragments. | No significant result. |
| **6. Experimental or practical validation** | Systematic evaluation across experiments or scenarios uses suitable metrics, controlled conditions, analysis, and robust conclusions. | High-quality but not exhaustive evaluation. | Evaluation exists with limited experiments. | Individual experiments exist. | Demonstration is mainly illustrative. | Evaluation is absent or cannot support the result. |
| **7. Result analysis** | Causes, strengths, weaknesses, limitations, errors, and parameter sensitivity are explained. | Well interpreted, but limitation analysis is incomplete. | Main results are interpreted without deep analysis. | Conclusions are present but only superficially tied to results. | Conclusions are mainly descriptive. | Conclusions do not follow from the evidence. |
| **8. Code and repository quality** | Professional structure, README, launch, dependencies, documentation, tests, reproducibility, and clean readable code. | Well organized with minor shortcomings. | Working code with noticeable documentation, structure, or testing problems. | Produces the result, but quality and reproducibility are limited. | Code exists, but launch and verification are difficult. | Code is absent, non-working, or inconsistent with the claim. |
| **9. Project artifacts** | Every mandatory artifact is complete and verifies its part of the result. | All main artifacts exist; some need revision. | Most exist, but some are substantially incomplete. | Significant elements are missing. | Only basic materials are present. | Key mandatory artifacts are missing. |
| **10. Presentation** | Logical, concise, and visual; shows problem → alternatives → gap → solution → experiment → comparison → result → conclusions. | Strong structure and visuals with some underdeveloped elements. | Understandable but overloaded or insufficiently evidence-based. | Communicates the general idea but poorly explains the result. | Formal and weakly reflects the work. | Does not communicate the task and result. |
| **11. Defense and answers** | Confidently explains key decisions and limitations and answers difficult questions with evidence. | Understands the work; a few questions cause difficulty. | Understands the main work but lacks some detail. | Answers basic questions without deep understanding. | Can explain only the general idea. | Cannot explain a substantial part of the work. |
| **12. Independence** | Clearly high independence; the student understands and controls all important result components. | Predominantly independent work. | Sufficient independence, but some decisions depended heavily on the supervisor or team. | Limited independence. | Most work required substantial help. | Independence cannot be demonstrated. |

## 2. Project-type-specific criteria

The general matrix is supplemented by one specialized block.

### 2.1. Scientific project

| Criterion | 5A | 4B | 4C | 3D | 3E | 2FX |
|---|---|---|---|---|---|---|
| **Scientific novelty** | A clear new result whose difference from existing approaches is proven. | Substantive new result with limited novelty. | Elements of novelty are insufficiently demonstrated. | Minimal novelty. | Novelty is barely demonstrated. | No scientific novelty. |
| **Scientific methodology** | Hypothesis or research question, method, and experiment align; conclusions strictly follow from experiments. | Correct with individual limitations. | Generally correct, but evidence is insufficient. | Significant methodological flaws. | Mainly demonstrational study. | Scientific method is effectively absent. |
| **Ablation or component analysis** | Complete and convincing analysis of key contributions. | Main components are analyzed. | Limited analysis. | Components are analyzed formally. | Analysis is almost absent. | Contributions cannot be assessed. |
| **Publication readiness** | Preprint is effectively submission-ready and follows scientific-paper structure and argumentation. | Near ready. | Complete draft needing major revision. | Fragmentary paper material. | Only a work description. | No scientific text. |

### 2.2. Technological project

| Criterion | 5A | 4B | 4C | 3D | 3E | 2FX |
|---|---|---|---|---|---|---|
| **Technical novelty** | Original solution substantially differs from existing approaches. | Independent technical decisions. | Individual novel elements. | Limited novelty. | Mostly ready-made solutions. | No independent technical result. |
| **Architecture** | Well-justified, scalable, and logically decomposed. | High-quality architecture. | Works but needs improvement. | Partially developed. | Superficial. | Absent or non-working. |
| **Engineering quality** | Code, tests, documentation, and reproducibility meet a professional standard. | Good engineering standard. | Working prototype with visible debt. | Major technical limitations. | Minimal prototype. | No working solution. |

### 2.3. Industrial project

| Criterion | 5A | 4B | 4C | 3D | 3E | 2FX |
|---|---|---|---|---|---|---|
| **Practical relevance** | Solves a specific significant problem for a real user or organization. | Clearly needed. | Has limited practical value. | Potentially applicable. | Value is weakly supported. | No practical value. |
| **Impact** | Quantitatively measured and confirmed. | Measured incompletely. | Quantitative estimate with limitations. | Approximate estimate. | Claimed without adequate evidence. | No demonstrated impact. |
| **Deployment potential** | Near pilot or deployment; constraints and requirements are developed. | Realistic potential. | Substantial additional work required. | Limited potential. | Mostly hypothetical. | Impossible or unjustified. |
| **Industry evaluation** | Substantive review confirms quality and value. | Positive partner assessment. | Positive but insufficiently detailed feedback. | Superficial assessment. | Minimal confirmation. | Required confirmation is absent. |

### 2.4. Collaborative project

| Criterion | 5A | 4B | 4C | 3D | 3E | 2FX |
|---|---|---|---|---|---|---|
| **Individual contribution** | Challenging independent part with substantial impact. | Significant independent contribution. | Substantive but limited in complexity. | Required work completed. | Minimal. | Absent or unverified. |
| **Teamwork** | Highly effective and helps the team solve problems. | Effective. | Generally effective with isolated issues. | Needs team help. | Communication is difficult. | Does not fulfill team responsibilities. |
| **Deadlines** | All tasks are timely and the student supports the shared schedule. | Almost all met. | Isolated delays. | Regular delays. | Major delays. | Systematic non-completion. |
| **Integration** | High-quality, documented integration. | Good integration. | Integrated with some issues. | Partial. | Poor. | Not integrated. |

### 2.5. Group project

| Criterion | 5A | 4B | 4C | 3D | 3E | 2FX |
|---|---|---|---|---|---|---|
| **Scale** | Volume and complexity equal N full individual projects for N participants. | Meets most scale requirements. | Sufficient, but some participants are underloaded. | Noticeably too small. | Group-based only formally. | One small individual project in practice. |
| **Task allocation** | Everyone owns an independent challenging area. | Good with minor imbalance. | Allocated, but some tasks are too simple. | Formal allocation. | Most work is done by one or two people. | Roles are undefined. |
| **Integration** | All components form one complete result. | Good with isolated gaps. | Main components integrated. | Partial. | Weakly connected. | No unified result. |
| **Individual contribution** | Every participant has a measurable, substantive contribution. | Most are significant. | Identifiable but unequal. | Some are minimal. | Hard to separate. | Cannot be verified. |
| **Team result** | High-quality integration makes the whole substantially exceed separate components. | Strong unified result. | Working shared result. | Exists with weak integration. | Formal. | No shared result. |

# Using the Matrix at the Defense

The committee should not begin with “Which grade should we award?” Instead, follow four steps.

## Step 1. Assess mandatory criteria

Confirm that the task is relevant and correctly stated; existing solutions are analyzed; quantitative metrics and comparison exist; the result was actually obtained and validated; every mandatory artifact is present; code and repository are verifiable; the presentation supports assessment; and the student understands the work.

## Step 2. Select a level for each criterion

For every criterion, select **5A / 4B / 4C / 3D / 3E / 2FX**.

## Step 3. Check the caps

Check for missing artifacts, comparison and metrics, demonstrated relevance, reproducibility, student understanding, and project-type-specific requirements.

## Step 4. Determine the final grade

Do not calculate an arithmetic mean.

> The final grade is the highest level for which every critical requirement at that level is met.

An average set of 5A-level scores is insufficient when any mandatory 5A condition is missing.

# Quick Checklist for Committee Members

## Can the project receive 5A?

Every answer must be yes.

- [ ] Is the task genuinely relevant?
- [ ] Is relevance demonstrated rather than merely claimed?
- [ ] Are the problem statement and success criteria clear?
- [ ] Are existing solutions analyzed?
- [ ] Is there a relevant baseline or alternative?
- [ ] Are there quantitative metrics?
- [ ] Is there quantitative comparison with alternatives?
- [ ] Are comparison conditions comparable?
- [ ] Is superiority over or a useful difference from alternatives demonstrated?
- [ ] Does a complex system include component analysis?
- [ ] Are all mandatory artifacts present?
- [ ] Is the repository high-quality and reproducible?
- [ ] Does the code match the claimed result?
- [ ] Does the presentation communicate the result well?
- [ ] Does the student understand the work?
- [ ] Can the student answer committee questions?
- [ ] Are the project type's specific requirements met?

If any answer is no, 5A is not awarded.

# Quick Checklist: 4B versus 4C

## 4B

The project works completely, has an independent result, quantitative results, comparison with alternatives, quality artifacts, a good repository, a strong defense, and only isolated rather than systemic shortcomings.

## 4C

The project works, has a substantive independent result and at least basic experimental validation, but comparison is limited, evidence is incomplete, artifacts, code, or documentation have problems, the presentation or defense has noticeable weaknesses, or important requirements remain unmet.

# Quick Checklist: 3D versus 3E

## 3D

“The work was genuinely completed, but remains substantially underdeveloped.” A working result, independent work, basic validation, and a clear task exist, but many requirements are unmet.

## 3E

“There is evidence of work, but almost no complete result.” Individual implementations, experiments, or a partial result exist, but the project cannot convincingly demonstrate solution quality.

# When Choosing Between Two Grades

Ask: **“What is missing?”**

## 4B → 4C

- a stronger baseline;
- quantitative comparison;
- experiments;
- better repository quality;
- more convincing analysis; or
- a stronger presentation.

## 5A → 4B

- complete comparison with relevant alternatives;
- a quantitative advantage or significant result;
- high-quality experimental design;
- component analysis;
- reproducibility;
- an excellent presentation and defense; or
- fulfillment of all project-type-specific requirements.
