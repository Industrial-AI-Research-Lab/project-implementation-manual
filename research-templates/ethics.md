# Ethics, Safety, Privacy, and Limitations Template

Complete this template before data collection and revisit it whenever the goal, data, method, or affected groups change. It is a structured preparation for decision-making, not a substitute for an ethics committee, a security specialist, or a legal assessment.

## 0. Applicability screening

Mark "yes/no/unclear" and explain:

- The research involves people, their behavior, communications, or biological materials: [ ]
- Personal, sensitive, restricted, or re-identifiable data are used: [ ]
- Vulnerable groups or power imbalances are involved: [ ]
- The intervention could cause physical, psychological, economic, or reputational harm: [ ]
- Dual-use knowledge, a vulnerability, or a dangerous capability is created: [ ]
- Critical systems, safety/security, or service availability are affected: [ ]
- The result could affect rights, access to resources, or significant decisions about people: [ ]
- Animals/hazardous substances/field interventions are used: [ ]
- There are substantial computational/environmental costs: [ ]
- There is a conflict of interest or pressure toward a desired result: [ ]

If at least one item is "yes/unclear", determine the required formal approval before launch.

## 1. Goal, social value, and necessity

- ★ The benefit/knowledge the work is carried out for: [ ]
- ★ Who is expected to benefit: [ ]
- ★ Who bears the risk, and whether this group coincides with the beneficiaries: [ ]
- ★ Why the goal cannot be achieved in a less risky way: [ ]
- ★ Proportionality of the risk to the expected value: [justification]
- Alternatives that were rejected: [ ]

## 2. Map of affected parties

| Group | How affected | Benefit | Potential harm | Voice/participation | Measure |
|---|---|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

Include people who are not participants but may be harmed by the model, dataset, publication, or downstream use.

## 3. Consent and participation

- Who is recruited and how: [ ]
- Information provided: [purpose, procedures, risks, data, contact]
- Form and recording of consent: [ ]
- Voluntariness and the ability to withdraw without penalty: [ ]
- Compensation and the risk of undue influence: [ ]
- Deception/incomplete disclosure: [necessary? debriefing?]
- Vulnerable participants/additional safeguards: [ ]
- Data reuse and scope of consent: [ ]
- Data withdrawal procedure: [up to what point it is possible]

## 4. Privacy and data management

- ★ Minimum necessary fields: [ ]
- ★ Identifiers and the possibility of linkage: [ ]
- ★ Legal/ethical basis: [consent, contract; do not treat public availability as automatic permission]
- ★ Pseudonymization/anonymization and residual re-identification risk: [ ]
- ★ Role-based access and logging: [ ]
- ★ Encryption/transfer/backup: [ ]
- ★ Retention period and deletion: [ ]
- ★ Published aggregates and suppression: [ ]
- Data breach response: [ ]

## 5. Risks and measures

| ID | Scenario | Affected | Likelihood | Severity | Prevention | Detection | Response | Residual risk | Owner |
|---|---|---|---|---|---|---|---|---|---|
| R1 | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

Consider:

- erroneous decisions and false confidence;
- discrimination and uneven error across groups;
- leakage/re-identification;
- psychological, financial, reputational, and physical harm;
- security abuse, circumvention of safeguards, and dual use;
- automation without human oversight;
- incorrect transfer of conclusions;
- dependence on a vendor/model and hidden changes;
- environmental/resource cost;
- harm from publishing details or artifacts.

## 6. Fairness and representativeness

- Relevant groups and why: [ ]
- Representation in the data/sample: [ ]
- Quality of labels/measurements by group: [ ]
- Metrics and uncertainty by group: [ ]
- Risk of proxy discrimination: [ ]
- Which types of errors are more costly, and for whom: [ ]
- What cannot be solved by "data balancing" alone: [structural/contextual factors]
- Downstream impact monitoring plan: [ ]

## 7. Security and dual use

- Capability/information the work creates: [ ]
- Potential adversary and misuse path: [ ]
- Sensitive details/artifacts: [ ]
- Threat model and security review: [link]
- Sandbox/isolation/rate limit/access control: [ ]
- Responsible disclosure: [contact and timeline]
- Publication restrictions: [what, why, who approved]
- Kill switch/stop rule: [ ]

## 8. Research and publication integrity

- Funding and sponsor influence: [ ]
- Conflicts of interest: [ ]
- Authorship and contributions: [CRediT/other scheme]
- Who owns the data/code/IP: [ ]
- Plan for publishing negative results: [ ]
- Handling of errors, corrections, and retractions: [ ]
- Prohibition of fabrication, falsification, plagiarism, and hidden selective reporting: [confirmed]

## 9. Use of generative AI

- Tool, vendor, model/version, and date: [ ]
- Tasks: [search/code/editing/analysis/translation]
- What data was shared and whether this is permitted: [ ]
- Retained prompts/outputs/configs: [ ]
- Human verification of facts, references, code, and analysis: [ ]
- Risk of hallucination, bias, leakage, copyright infringement: [ ]
- Disclosure in the publication according to the venue's rules: [ ]
- AI is not listed as an author, and responsibility remains with people: [ ]

## 10. Approvals

| Body/role | Required? | Materials | Decision/ID | Date | Conditions/term |
|---|---|---|---|---|---|
| Ethics/IRB | [ ] | [ ] | [ ] | [ ] | [ ] |
| Data owner/DPO | [ ] | [ ] | [ ] | [ ] | [ ] |
| Security | [ ] | [ ] | [ ] | [ ] | [ ] |
| Legal/IP | [ ] | [ ] | [ ] | [ ] | [ ] |
| Domain safety | [ ] | [ ] | [ ] | [ ] | [ ] |

## 11. Monitoring and incidents

- Safety/privacy quality indicators: [ ]
- Pause/stop threshold: [ ]
- Who can stop the research: [ ]
- Incident reporting channel: [ ]
- Notification deadline: [ ]
- Debrief/remediation for those affected: [ ]
- Review of the risk assessment: [date/trigger]

## 12. Limitations and responsible communication

- What the conclusions do not allow you to claim: [ ]
- Which groups/environments were not studied: [ ]
- How to avoid stigmatizing/causal wording: [ ]
- Which uncertainty and residual risks must be brought into the summary: [ ]
- Which details must not be published, and why: [ ]

## Pre-launch check

- [ ] Formal approvals were obtained before the corresponding actions.
- [ ] Benefit and risk are distributed fairly, and affected non-participants have been considered.
- [ ] Data are minimized; access, retention, and incident response are defined.
- [ ] Consent is genuinely informed and voluntary, where required.
- [ ] Fairness is assessed in the context of harm, not through a single aggregate metric.
- [ ] Dual-use and security scenarios have measures and owners.
- [ ] Residual risk has been accepted by a specific authorized person.
- [ ] Conflicts, contributions, and AI use will be disclosed.
- [ ] Stop/pause rules and the incident channel are known to the team.
- [ ] Public communication does not exceed the limits of the evidence.

Methodological basis: [COPE Core Practices](https://publicationethics.org/core-practices), [NIST AI RMF](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-ai-rmf-10), [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist), [CRediT](https://credit.niso.org/).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Dual-use** — knowledge, technology, or artifacts created for beneficial purposes that can also be used to cause harm, for example for attacks or circumventing safeguards.
- **Conflict of interest** — circumstances (funding, affiliation, personal gain) that may influence, or appear to influence, how research is conducted and interpreted. It must be disclosed.
- **Downstream use** — subsequent use of a model, dataset, or result by other people and systems, often beyond the authors' control and for other purposes.
- **Informed consent** — a participant's voluntary agreement given after a clear explanation of the purpose, procedures, risks, data use, and the right to withdraw without penalty.
- **Undue influence** — pressure or rewards so substantial that they undermine the voluntariness of the decision to take part.
- **Deception and debriefing** — deception is deliberately incomplete or misleading information given to participants about the study's purpose; it is allowed only with justification and approval and requires debriefing, that is, later disclosure of the true purpose to participants.
- **Record linkage** — combining data about the same person or object from different sources. It increases the value of the data but also the risk of re-identification.
- **Pseudonymisation and anonymisation** — pseudonymisation replaces identifiers with codes, but the link can be restored using a separately stored key; anonymisation makes identifying a person impossible by reasonable means. Pseudonymised data are generally still considered personal data.
- **Re-identification** — recovering a person's identity from nominally de-identified data, for example from a combination of attributes or by linking with other datasets.
- **Suppression** — hiding cells with very small counts in published aggregates, since they could reveal specific individuals.
- **Residual risk** — the risk that remains after control measures are applied. It must be explicitly accepted by an authorized person.
- **Fairness** — for models and data, the absence of unjustifiably unequal errors, quality, or consequences across groups. It is assessed in light of the context of harm, not by a single aggregate metric.
- **Proxy discrimination** — unequal treatment of a group through features correlated with a protected characteristic (for example, postal code standing in for ethnicity), even when the characteristic itself is not used.
- **Threat model** — a description of who might misuse a system or knowledge, their goals and capabilities, and which attack paths must be prevented.
- **Responsible disclosure** — a process in which a discovered vulnerability is first reported confidentially to the system owner, who is given time to fix it, before details are published.
- **Kill switch** — a mechanism prepared in advance to immediately stop a system, intervention, or experiment when acceptable thresholds are exceeded.
- **CRediT (Contributor Roles Taxonomy)** — a standard taxonomy of 14 contributor roles in research (for example, Conceptualization, Methodology, Software, Formal analysis) that makes each author's contribution explicit.
- **Retraction** — the official withdrawal of a published article because of serious errors or misconduct. Retracted studies must not be relied on as evidence.
- **Fabrication, falsification, plagiarism** — the three main forms of research misconduct: making up data or results; manipulating data, procedures, or results; and using others' ideas, text, or results without attribution.
- **Selective reporting** — reporting only the "successful" results, metrics, or analyses while hiding the rest. It distorts the overall body of evidence.
- **Hallucination** — a plausible-sounding but incorrect or fabricated output of a generative model, such as a nonexistent reference. It requires human verification.
- **IRB (Institutional Review Board)** — an institutional committee that reviews and approves research involving people from the standpoint of ethics and participant protection.
- **DPO (Data Protection Officer)** — the person responsible for personal data protection in an organization, who advises on the lawfulness and security of its processing.
- **COPE (Committee on Publication Ethics)** — an international organization that publishes standards of publication ethics (Core Practices) and guidance for editors, authors, and reviewers, including on authorship, conflicts of interest, and corrections to the published record.
- **NIST AI RMF (AI Risk Management Framework)** — a framework from the U.S. National Institute of Standards and Technology (NIST) for identifying, assessing, and managing risks of artificial intelligence systems.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
