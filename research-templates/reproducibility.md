# Reproducibility and Research Artifacts Template

Here, **reproducibility** means obtaining a consistent computational result with the same data, code, and steps; **replication** means testing the same scientific question on new data. These terms vary across disciplines, so state your own definition in the publication.

## 0. Package goal

- ★ Main result to be reproduced: [table/figure/number/model]
- ★ Entry point: [command/script]
- ★ Expected result and tolerance: [ ]
- ★ Time and computational resources: [ ]
- ★ Supported platform: [ ]
- Level: [internal check / available package / independent reproducibility / replication]

## 1. Artifact manifest

| ID | Artifact | Purpose | Version/ID/hash | License | Access | Created/verified by |
|---|---|---|---|---|---|---|
| A1 | Protocol | [ ] | [ ] | [ ] | [ ] | [ ] |
| A2 | Raw data/metadata | [ ] | [ ] | [ ] | [ ] | [ ] |
| A3 | Processing code | [ ] | [commit] | [ ] | [ ] | [ ] |
| A4 | Analysis code | [ ] | [commit] | [ ] | [ ] | [ ] |
| A5 | Environment | [ ] | [lock/image digest] | [ ] | [ ] | [ ] |
| A6 | Figures/tables | [ ] | [ ] | [ ] | [ ] | [pipeline] |

Include only relevant artifacts in the package, but explain the absence of every critical element.

## 2. Package structure

```text
research-package/
  README.md
  LICENSES.md
  CITATION.cff
  protocol/
  data/
    README.md
    raw-or-access-instructions/
    processed/
    checksums.txt
  src/
  configs/
  environment/
  scripts/
    prepare_data
    run_analysis
    make_figures
    verify_outputs
  results/
  docs/
```

The names are illustrative. What matters is an unambiguous chain from the input to the claimed output.

## 3. README/runbook

### Required sections

1. What is reproduced and which version of the publication it corresponds to.
2. Hardware, OS/runtime, and disk space requirements.
3. Obtaining the data and verifying checksums.
4. Installation from a clean environment.
5. Commands for preparation, running the analysis, and generating the results.
6. Expected files/values and acceptable deviations.
7. Runtime/cost estimate.
8. Troubleshooting of known issues.
9. Licenses, citation, contact, and support period.

### Minimal run

```text
1. [create/obtain a clean environment]
2. [install the pinned dependencies]
3. [obtain the data version and verify the hash]
4. [run a single command or an exact sequence]
5. [run verify_outputs]
6. [compare against the expected manifest]
```

## 4. Environment

- OS/base image: [version/digest]
- Runtime/compiler: [ ]
- Dependency lock: [file]
- Hardware/accelerator/driver: [ ]
- Locale/timezone/encoding: [if relevant]
- Environment variables: [names and purpose only; no secrets]
- External services/API/model snapshot: [version and date]
- Determinism settings: [ ]
- Known platform differences: [ ]

A container helps, but it does not replace data, instructions, licenses, or verification of the result.

## 5. Data and provenance

- Raw data version/identifier/checksum: [ ]
- Source and access date: [ ]
- Data dictionary/datasheet: [ ]
- Pipeline raw → processed → analysis: [ ]
- Split manifest and seed: [ ]
- Restricted data: [why it is closed, how to request it, available synthetic/toy sample]
- Retention and availability horizon: [ ]

Do not publish data in violation of consent, license, or privacy for the sake of formal "openness".

## 6. Code and configuration

- Repository/tag/commit: [ ]
- License: [ ]
- Entry points: [ ]
- All parameters moved into a versioned config: [ ]
- Seeds and nondeterministic operations: [ ]
- Unit/integration/regression tests: [commands and status]
- Toy/small example: [ ]
- Link between the commit and an archival snapshot/DOI: [ ]
- No undocumented manual steps: [check]

## 7. Output verification

| Output | Expected value/property | Tolerance | Verification command | Why variation is possible |
|---|---|---|---|---|
| Table 1 | [schema/values] | [ ] | [ ] | [ ] |
| Figure 2 | [file/hash or summary] | [ ] | [ ] | [ ] |
| Main metric | [ ] | [ ] | [ ] | [ ] |

For stochastic results, verify a consistent distribution/interval and the number of repetitions, not necessarily a byte-identical file.

## 8. Independent verification

### Tester report

- The tester did not take part in creating the artifact: [yes/no]
- Date and environment: [ ]
- Starting point: [clean machine/container]
- Steps performed: [ ]
- Result obtained: [ ]
- Match within tolerance: [yes/no]
- Ambiguities/manual interventions: [ ]
- Defects and fixes: [IDs]
- Outcome: [functional / reusable / failed / blocked]

## 9. Readiness based on ACM artifact review

### Functional

- [ ] The inventory and documentation are complete.
- [ ] The artifacts are consistent with the publication.
- [ ] The main workflow runs.
- [ ] There is evidence of verification/validation.

### Reusable

- [ ] The structure and interfaces are understandable outside the team.
- [ ] Licenses, examples, and the ability to change parameters/data are provided.
- [ ] Community standards are followed.

### Available

- [ ] An archival repository provides a persistent identifier.
- [ ] The version is linked to the publication.
- [ ] Access and preservation restrictions are clear.

### Results validated

- [ ] An independent party obtained the main results.
- [ ] Conditions and discrepancies are documented.

## 10. Replication plan

- Scientific question and key effect: [ ]
- What is kept the same: [method/operationalization]
- What is independently changed: [new sample/environment/implementation]
- Consistency criterion: [not only a p-value]
- How to distinguish contextual heterogeneity from error: [ ]
- Registration and publication of any outcome: [ ]

## Quality check

- [ ] There is a single verifiable path from a clean environment to the main result.
- [ ] Versions of the data, code, config, and environment are immutably pinned.
- [ ] The instructions include expected outputs and tolerances.
- [ ] Time, hardware, and cost are stated realistically.
- [ ] Raw/intermediate/final data and provenance are distinguishable.
- [ ] No secrets or personal data have made it into the package.
- [ ] Restricted access to critical artifacts is explained rather than hidden.
- [ ] An independent person has performed a smoke test.
- [ ] The archived version has a persistent identifier or a long-term preservation plan.
- [ ] The terms reproducibility/replication are explicitly defined.

Methodological basis: [National Academies: Reproducibility and Replicability in Science](https://www.nationalacademies.org/read/25303/chapter/2), [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current), [FAIR Principles](https://doi.org/10.1038/sdata.2016.18), [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Reproducibility** — obtaining consistent results when the analysis is rerun with the same data, code, and steps. Disciplines use the term differently, so a publication should state its own definition.
- **Research artifact** — any material a result rests on: protocol, data, code, configurations, environment, tables, and figures. Available artifacts let others check and reuse the work.
- **Replication (replicability)** — testing the same scientific question with new data, often by another team, in another setting, or with another implementation. Consistent results increase confidence in the conclusion.
- **Entry point** — the single command or script from which reproduction of the main result starts.
- **Tolerance** — the acceptable numerical deviation of a reproduced result from the reported one, due, for example, to randomness or hardware differences.
- **Manifest** — a list of files or artifacts with their purpose, version or checksum, license, and access conditions. It makes it possible to verify that a package is complete and unchanged.
- **Lockfile and container** — a lockfile pins the exact versions of all dependencies; a container (for example, a Docker image) packages the entire software environment, and the image digest uniquely identifies its version. Both make it possible to run the code in the same environment later or on another machine.
- **CITATION.cff** — a file in the Citation File Format containing machine-readable metadata for citing software or a dataset.
- **Checksum (hash)** — a short string computed from a file's contents. Any change to the file changes it, so it confirms that exactly the intended version is being used.
- **Runbook** — step-by-step instructions that let an outsider obtain the data, set up the environment, run the pipeline, and check the result.
- **Determinism** — the property of a method producing the same result for the same inputs and settings. Nondeterminism can arise from randomness, parallel computation, or hardware specifics.
- **Provenance** — the documented history of data: source, collection method, and every transformation up to the value used in the analysis.
- **Data dictionary** — a description of each variable: name, meaning, type, units, allowed values, and how missing values are coded.
- **Datasheet** — a standardized description of a dataset: purpose, composition, provenance, collection, labeling, limitations, and recommended uses. It is based on the Datasheets for Datasets approach.
- **Train/validation/test split** — dividing data into a part for training, a part for tuning and model selection, and a held-out part for the final evaluation. For studies without model training, the analogue is discovery/confirmation: data for finding hypotheses and separate data for testing them.
- **Seed (random seed)** — the initial value of a pseudorandom number generator. Fixing the seed makes random steps repeatable, and running with several seeds shows how much the result varies.
- **Toy example and synthetic data** — a small simplified or artificially generated dataset on which code can be checked without access to real or restricted data.
- **Unit, integration, and regression tests** — unit tests check individual functions, integration tests check that components work together, and regression tests check that previous results have not changed unexpectedly after modifications.
- **DOI, persistent identifier (Digital Object Identifier)** — a stable reference to a digital object (an article, dataset, or code archive) that keeps working when the storage location changes. DOI is the most common kind of such identifier.
- **ACM Artifact Review and Badging** — the Association for Computing Machinery policy for reviewing research artifacts of papers and awarding badges: Artifacts Available, Artifacts Evaluated (Functional, Reusable), and Results Validated (Reproduced, Replicated).
- **Smoke test** — a quick basic check that a package installs and its main workflow runs without errors. It does not replace full verification of the results.
- **National Academies** — the U.S. National Academies of Sciences, Engineering, and Medicine. Their report "Reproducibility and Replicability in Science" (2019) provides widely used definitions of reproducibility and replicability and recommendations for achieving them.
- **FAIR (Findable, Accessible, Interoperable, Reusable)** — principles stating that data and metadata should be findable, accessible, interoperable, and reusable. FAIR does not require data to be open: access may be restricted as long as the access conditions are clearly described.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
