# Template for Finding, Evaluating, and Processing Data and Datasets

This page combines a data search protocol, a short datasheet, and a data management plan. Its main goal is to make the provenance of every analytical value traceable from source to result.

## 0. Data needs card

- ★ Related RQs/Hs: [links]
- ★ Unit of analysis: [ ]
- ★ Required variables/signals: [ ]
- ★ Population, domain, period: [ ]
- ★ Minimum volume/diversity: [and justification]
- ★ Required license/access mode: [ ]
- ★ Unacceptable sources/collection methods: [ ]
- Plan B if no suitable data exist: [collection / synthetic data / simulation / narrow the RQ]

## 1. Dataset search protocol

### Sources

- domain-specific and government repositories;
- scientific data catalogs and supplementary materials to publications;
- registries/benchmark platforms;
- APIs and open data from organizations;
- requests to authors/owners;
- internal data with a documented right of use;
- original data collection under a separate protocol.

### Search log

| ID | Source/catalog | Query/filters | Date | Found | Candidates | Limitation |
|---|---|---|---|---:|---|---|
| DS-S1 | [ ] | `[full query]` | [ ] | [n] | [IDs] | [ ] |

### Candidate register

| ID | Name/version | URL/DOI | Fit to RQ | Volume/coverage | License | Quality | Risk | Decision |
|---|---|---|---|---|---|---|---|---|
| D1 | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [include/exclude] |

Record the reason for every excluded candidate. Do not choose a dataset merely because it is expected to yield the best result.

## 2. Suitability criteria

| Criterion | Requirement | How it is checked | Result |
|---|---|---|---|
| Concept fit | [the variables actually measure what is needed] | [domain review] | [ ] |
| Population fit | [the population matches the intended inference] | [metadata] | [ ] |
| Coverage | [periods/classes/conditions] | [profile] | [ ] |
| Accuracy/label quality | [threshold] | [audit/sample adjudication] | [ ] |
| Completeness | [missing-value threshold] | [profile] | [ ] |
| Timeliness | [currency] | [date] | [ ] |
| Independence | [no overlap/leakage] | [dedup/entity match] | [ ] |
| Rights/ethics | [permitted use] | [license/consent] | [ ] |
| Reproducible access | [stable version] | [DOI/snapshot/checksum] | [ ] |

## 3. Datasheet for the selected dataset

### 3.1 Identity and purpose

- ★ Name: [ ]
- ★ Version/snapshot date: [ ]
- ★ Creator/owner/contact: [ ]
- ★ Persistent ID/URL: [ ]
- ★ Original purpose of creation: [ ]
- ★ Permitted and discouraged uses: [ ]
- Related publications/previous versions: [ ]

### 3.2 Composition

- ★ What a single record represents: [ ]
- ★ Number of records/entities/groups: [ ]
- ★ Schema and units: [link to data dictionary]
- ★ Target variable/labels: [ ]
- ★ Geography, languages, period: [ ]
- ★ Subgroups and rare cases: [ ]
- Relationships between records/clustering: [ ]
- Missing and special values: [ ]

### 3.3 Provenance and collection

- ★ Source of each data category: [ ]
- ★ Who/what collected the data and under what conditions: [ ]
- ★ Sampling/recruitment: [ ]
- ★ Collection period and frequency: [ ]
- ★ Instruments/sensors/APIs and their versions: [ ]
- ★ Consent/legal basis/terms: [ ]
- Known changes to the process over time: [ ]

### 3.4 Annotation

- Is there annotation: [yes/no]
- Instructions and label ontology: [link]
- Who annotated, their training and qualifications: [ ]
- Number of annotators per item: [ ]
- Agreement and adjudication: [ ]
- Gold/quality-control items: [ ]
- Uncertainty/disagreement preserved or smoothed out: [ ]

### 3.5 Rights, privacy, and harm

- ★ License and its version: [ ]
- ★ Rights to redistribution and derived data: [ ]
- ★ Personal/sensitive attributes: [ ]
- ★ Re-identification risk: [ ]
- ★ Consent and the possibility of withdrawal: [ ]
- ★ Vulnerable/underrepresented groups: [ ]
- ★ Potential harmful uses: [ ]
- Access restrictions and request procedure: [ ]
- Legal/ethical review: [link/decision]

### 3.6 Known limitations

- Selection/coverage bias: [ ]
- Measurement/label bias: [ ]
- Survivorship/publication bias: [ ]
- Temporal drift: [ ]
- Missingness mechanism: [ ]
- Duplicates/linked entities: [ ]
- Benchmark contamination: [ ]
- Limitations of external validity: [ ]

## 4. Acceptance audit

### Quality profile

| Check | Method | Threshold | Actual | Decision/correction |
|---|---|---|---|---|
| Schema/types/ranges | [ ] | [ ] | [ ] | [ ] |
| Missing values | [ ] | [ ] | [ ] | [ ] |
| Duplicates/entity overlap | [ ] | [ ] | [ ] | [ ] |
| Label validity | [ ] | [ ] | [ ] | [ ] |
| Class/subgroup balance | [ ] | [ ] | [ ] | [ ] |
| Temporal consistency | [ ] | [ ] | [ ] | [ ] |
| Outliers/impossible values | [ ] | [ ] | [ ] | [ ] |
| Leakage/contamination | [ ] | [ ] | [ ] | [ ] |

Preserve the original values. A correction made without a log destroys provenance.

## 5. Splits and leakage prevention

- ★ Unit of splitting: [record/user/object/time/organization]
- ★ Train/validation/test or discovery/confirmation rule: [ ]
- ★ Proportions/periods and seed: [ ]
- ★ Stratification/grouping: [ ]
- ★ When the test set was frozen: [date + checksum]
- ★ Who had access to test labels: [ ]
- Check for near-duplicates and shared entities: [ ]
- External test/temporal validation: [ ]
- Decisions prohibited after viewing the test set: [ ]

If the same entity appears in different splits, ordinary random splitting often creates leakage. Split at the level of the causally linked unit.

## 6. Transformations

| Step ID | Input version | Code/commit | Operation | Parameters | Output | Check | Reversibility |
|---|---|---|---|---|---|---|---|
| T01 | [raw hash] | [commit] | [ ] | [ ] | [path/hash] | [ ] | [yes/no] |

- ★ The raw layer is immutable: [location and permissions]
- ★ All analytical data are built by a script/documented procedure: [link]
- ★ Fit-dependent transformations are fitted only on train/discovery data: [how]
- ★ Manual corrections are represented as a versioned patch: [link]
- Normalization/imputation/feature engineering: [exact rules]
- Removed records: [register of reasons]

## 7. Data management plan

| Topic | Decision |
|---|---|
| Formats and standards | [open/machine-readable formats, data dictionary] |
| Names and structure | [directory/file naming convention] |
| Identifiers/versions | [DOI/tag/checksum] |
| Storage and backup | [location, frequency, restore test] |
| Access and roles | [least privilege, access log] |
| Encryption/secrets | [at rest/in transit; secrets stored separately] |
| Retention/deletion | [period, basis, responsible person] |
| Publication | [repository, date, embargo] |
| Restricted access | [public metadata, access procedure] |
| Cost and owner | [ ] |

FAIR does not mean "necessarily open to everyone": data may require authentication, but the metadata, identifier, access conditions, and provenance must be clear.

## 8. Release manifest

| Artifact | Purpose | Format | Version/hash | License/access | Created by |
|---|---|---|---|---|---|
| raw snapshot | [ ] | [ ] | [ ] | [ ] | [source] |
| processed data | [ ] | [ ] | [ ] | [ ] | [pipeline commit] |
| data dictionary | [ ] | [ ] | [ ] | [ ] | [ ] |
| datasheet | [ ] | [ ] | [ ] | [ ] | [ ] |
| quality report | [ ] | [ ] | [ ] | [ ] | [ ] |
| split manifest | [ ] | [ ] | [ ] | [ ] | [ ] |

## Quality check

- [ ] Data needs are derived from the RQ, not from whichever dataset is available.
- [ ] The search and the reasons for selecting/excluding candidates are recorded.
- [ ] The version, provenance, license, and access date are unambiguous.
- [ ] Construct fit, representativeness, and known biases have been checked.
- [ ] Duplicates, entities, and temporal structure are accounted for in the splits.
- [ ] Test/confirmation data are protected from iterative peeking.
- [ ] Raw data are immutable; transformations are versioned.
- [ ] Personal data are minimized; residual risk is documented.
- [ ] For restricted data, metadata and the request procedure are available where permissible.
- [ ] The release includes a data dictionary, datasheet, and quality report.

Methodological basis: [FAIR Guiding Principles](https://doi.org/10.1038/sdata.2016.18), [Datasheets for Datasets](https://doi.org/10.1145/3458723), [UKRI research data management guidance](https://www.ukri.org/publications/guidance-on-best-practice-in-the-management-of-research-data/), [NIST AI RMF](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-ai-rmf-10).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Datasheet** — a standardized description of a dataset: purpose, composition, provenance, collection, labeling, limitations, and recommended uses. It is based on the Datasheets for Datasets approach.
- **DMP (Data Management Plan)** — a document describing how data will be collected, documented, stored, protected, shared, and deleted during and after a project.
- **Provenance** — the documented history of data: source, collection method, and every transformation up to the value used in the analysis.
- **DOI, persistent identifier (Digital Object Identifier)** — a stable reference to a digital object (an article, dataset, or code archive) that keeps working when the storage location changes. DOI is the most common kind of such identifier.
- **Adjudication** — a procedure for reaching a final decision when independent annotators or raters disagree, for example discussion or a ruling by a third expert.
- **Data leakage** — information from test or confirmation data reaching training, tuning, or analysis choices. It inflates performance estimates and leads to false conclusions.
- **Checksum (hash)** — a short string computed from a file's contents. Any change to the file changes it, so it confirms that exactly the intended version is being used.
- **Data dictionary** — a description of each variable: name, meaning, type, units, allowed values, and how missing values are coded.
- **Gold/quality-control items** — items with a known correct answer that are mixed into annotation tasks to check the quality of annotators' work.
- **Re-identification** — recovering a person's identity from nominally de-identified data, for example from a combination of attributes or by linking with other datasets.
- **Selection bias and coverage bias** — a systematic mismatch between the data and the target population caused by how units entered the dataset or by parts of the population being left out.
- **Measurement bias and label bias** — systematic error in measurements or labels, for example due to the instrument, the instructions, or the annotators. It may differ across subgroups.
- **Survivorship bias** — a distortion that arises because only "surviving" objects (companies still operating, records that were preserved) enter the data, while those that dropped out are invisible.
- **Publication bias** — the tendency to publish mainly positive and statistically significant results. Because of it, the literature overstates effects and negative results get lost.
- **Temporal drift** — a change over time in the data distribution or in the relationship between features and outcome. A model or conclusion based on older data may become outdated.
- **Missingness mechanism** — the reason values are missing: completely at random (MCAR), at random given observed variables (MAR), or depending on the missing value itself (MNAR). The mechanism determines which handling methods are valid.
- **Benchmark contamination** — benchmark test examples ending up in a model's training data, for example through training on web data. Results on such a benchmark are inflated.
- **Train/validation/test split** — dividing data into a part for training, a part for tuning and model selection, and a held-out part for the final evaluation. For studies without model training, the analogue is discovery/confirmation: data for finding hypotheses and separate data for testing them.
- **Near-duplicates and shared entities** — nearly identical records, or records about the same object (user, patient, document), in different parts of a split. They cause leakage between train and test.
- **Temporal validation** — testing a model or conclusion on data from a later period than the data used to build it. It mimics real use in the future.
- **Fit-dependent transformations** — transformations whose parameters are computed from the data, such as mean normalization, imputation, or feature selection. They must be fitted only on train/discovery data; otherwise leakage occurs.
- **Imputation** — filling in missing values with estimates such as the mean, a model prediction, or multiple imputation. The chosen method affects the result and must be documented.
- **Feature engineering** — creating new input variables for a model or analysis from the original data.
- **Least privilege** — the principle that each person and process gets only the minimum access needed for their task.
- **Encryption at rest and in transit** — encrypting data while stored and while transmitted over a network, respectively.
- **Retention** — the set period for keeping data and the rule for deleting it when the period ends.
- **Embargo** — a period during which data or a publication have been deposited but are not yet publicly available.
- **FAIR (Findable, Accessible, Interoperable, Reusable)** — principles stating that data and metadata should be findable, accessible, interoperable, and reusable. FAIR does not require data to be open: access may be restricted as long as the access conditions are clearly described.
- **Manifest** — a list of files or artifacts with their purpose, version or checksum, license, and access conditions. It makes it possible to verify that a package is complete and unchanged.
- **NIST AI RMF (AI Risk Management Framework)** — a framework from the U.S. National Institute of Standards and Technology (NIST) for identifying, assessing, and managing risks of artificial intelligence systems.
- **UKRI research data management guidance** — best-practice guidance on managing research data from UK Research and Innovation, the UK's national research funding agency.
