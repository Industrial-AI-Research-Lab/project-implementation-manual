# Method or Algorithm Description Template

The description should allow a competent researcher to implement the method without guessing essential details, and allow a reviewer to understand its assumptions, complexity, sources of randomness, and limits of applicability.

## 0. Card

- ★ Method name and version: [ ]
- ★ Purpose: [which problem it solves]
- ★ Related RQs/Hs: [ ]
- ★ Author/source/license: [ ]
- ★ Reference implementation: [URL + commit/tag]
- Status: [concept / prototype / validated / production candidate]

## 1. Problem statement

- ★ Input space: [type, shape, units, valid range]
- ★ Output space: [type, shape, units, semantics]
- ★ Objective function/criterion: [formula or exact definition]
- ★ Constraints: [computational, physical, business, ethical]
- ★ Preconditions: [what must be true]
- ★ Postconditions: [what is guaranteed when the preconditions hold]
- Non-goals: [what the method intentionally does not address]

### Notation

| Symbol/term | Definition | Type/dimension | Units |
|---|---|---|---|
| [x] | [ ] | [ ] | [ ] |

Define each symbol before its first use. Distinguish between data, method parameters, learnable parameters, and hyperparameters.

## 2. Intuition and distinction

> The method uses **[key idea]** to **[improvement mechanism]**, unlike **[closest baseline]**, which **[limitation]**.

- New part: [what is genuinely new]
- Borrowed components: [references and licenses]
- Why a gain is expected: [mechanistic explanation]
- When no gain is expected: [boundary conditions]
- Simplest alternative: [baseline]

## 3. Interface contract

| Element | Specification |
|---|---|
| Inputs | [name: type, shape, units, valid range] |
| Outputs | [name: type, shape, units, meaning] |
| Errors | [condition → type/message/status] |
| Determinism | [yes/no; under which settings] |
| State | [stateless/stateful; what is persisted] |
| Side effects | [files, network, external systems] |
| Compatibility | [versions/formats] |

## 4. Algorithm

### Steps

1. Check [preconditions and input validation].
2. Build [intermediate representation].
3. Perform [main operation] according to the rule [formula/reference].
4. Check [invariant/stopping criterion].
5. Return [output] and [diagnostics].

### Pseudocode

```text
Algorithm METHOD_NAME(input X, parameters θ, config C):
    require PRECONDITION(X, C)
    state ← INITIALIZE(X, θ, C)
    for t ← 1 to C.max_steps:
        proposal ← UPDATE(state, X, θ, C)
        state ← APPLY(state, proposal)
        assert INVARIANT(state)
        if STOP(state, t, C):
            return RESULT(state), DIAGNOSTICS(state, t)
    return RESULT(state), {status: "max_steps_reached", ...}
```

Replace all capitalized functions with exact rules. If a step contains a heuristic, describe the tie-breaking order and the behavior in edge cases.

## 5. Correctness

- Invariant(s): [what is preserved at every step]
- Termination: [why/when the algorithm stops]
- Guarantee: [exact theorem/property]
- Assumptions of the guarantee: [complete list]
- Proof sketch: [chain of reasoning]
- Counterexample when assumptions are violated: [ ]
- Numerical stability/precision: [ ]

If there is no formal guarantee, do not disguise an empirical observation with the word "proven".

## 6. Complexity and resources

| Resource | Worst case | Typical/expected | Depends on | Measurement |
|---|---|---|---|---|
| Time | [O(...)] | [ ] | [n, d, ...] | [benchmark] |
| Memory | [O(...)] | [ ] | [ ] | [ ] |
| Storage/network | [ ] | [ ] | [ ] | [ ] |
| Computational cost/energy | [ ] | [ ] | [ ] | [ ] |

## 7. Parameters, tuning, and randomness

| Parameter | Role | Range/default | How chosen | Sensitivity |
|---|---|---|---|---|
| [ ] | [ ] | [ ] | [theory/train/validation] | [ ] |

- Sources of randomness: [initialization, sampling, hardware]
- Seeds and number of independent repetitions: [ ]
- Deterministic settings: [ ]
- What is selected on train, on validation, and **never** on test: [ ]
- The tuning budget is the same for baselines: [how this is ensured]

## 8. Experimental evaluation

- Datasets/environments and versions: [ ]
- Strong baselines and why they were chosen: [ ]
- Same data/resources/tuning budget: [ ]
- Primary metrics and the practically important threshold: [ ]
- Number of runs/seeds and aggregation: [ ]
- Uncertainty/error bars: [ ]
- Statistical/comparison plan: [link]
- Compute: [hardware, runtime, cost]

### Ablations

| Component | Variant without it/replacement | Which hypothesis it tests | Result |
|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] |

An ablation should test the causal role of a component in the claimed gain, not merely produce a large table.

## 9. Failure modes and limitations

| Condition | Observed behavior | How to detect | Consequence | Mitigation/fallback |
|---|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] |

Check: empty/minimal/maximal input; schema violations; extreme values; distribution shift; adversarial input; resource shortage; nondeterminism; order dependence; degradation of an external API.

## 10. Test examples

| Test ID | Input | Expected output/property | Tolerance | Purpose |
|---|---|---|---|---|
| T1 | [small hand-worked example] | [exact result] | [ ] | [correctness] |
| T2 | [boundary] | [ ] | [ ] | [edge case] |
| T3 | [invalid] | [error] | [ ] | [validation] |
| T4 | [reference dataset] | [metric range] | [ ] | [regression] |

## 11. ML/AI supplement

- Architecture and exact version/number of parameters: [ ]
- Objective/loss and all its terms: [ ]
- Training data, filtering, and contamination checks: [ ]
- Splits and access to test: [ ]
- Optimizer, schedule, batch, epochs/steps, early stopping: [ ]
- Checkpoint selection rule: [validation only]
- Pretrained components and licenses: [ ]
- Prompts/system instructions/decoding for LLMs: [ ]
- Model/API snapshot and access date: [ ]
- Compute and emissions/cost, if significant: [ ]
- Robustness, subgroup, safety, and misuse evaluation: [ ]
- Human evaluation: [sampling, rubric, blinding, agreement]

## Quality check

- [ ] Inputs, outputs, units, and errors are specified as a contract.
- [ ] The pseudocode is unambiguous and covers stop/tie/edge rules.
- [ ] Guarantees are separated from empirical observations.
- [ ] Parameters and tuning do not use test.
- [ ] Baselines receive a comparable budget and data.
- [ ] Ablations are linked to the claimed mechanism.
- [ ] Seeds, repetitions, compute, and environment versions are reported.
- [ ] There are minimal examples, boundary tests, and regression tests.
- [ ] Failure modes and limitations are visible in the main text.
- [ ] The implementation is pinned to a commit/tag and a license.

Methodological basis: [NeurIPS Paper Checklist](https://nips.cc/public/guides/PaperChecklist), [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current), [National Academies on reproducibility](https://www.nationalacademies.org/read/25303/chapter/2).

## Glossary

Explanations of non-obvious terms and abbreviations used on this page. Experienced researchers can skip this section.

- **Reference implementation** — the authors' canonical implementation of a method, used to check the description and compare other implementations against.
- **Precondition and postcondition** — a precondition is what must be true before a method runs; a postcondition is what the method guarantees on output when the preconditions hold.
- **Non-goals** — an explicit list of what a study or method deliberately does not address. It helps keep the scope of the work in check and prevents overreaching conclusions.
- **Hyperparameter** — a parameter set before training or running a method (learning rate, number of layers, threshold), as opposed to learned parameters that the method fits from data.
- **Baseline** — the reference point for comparison: current practice, or a simple or strong existing method. A new method's gain is meaningful only relative to a fairly tuned, strong baseline.
- **Boundary conditions** — the conditions beyond which an effect disappears or reverses and the conclusion no longer applies.
- **Interface contract** — a precise specification of a method's inputs, outputs, units, valid values, errors, and side effects that users can rely on.
- **Determinism** — the property of a method producing the same result for the same inputs and settings. Nondeterminism can arise from randomness, parallel computation, or hardware specifics.
- **Side effects** — changes beyond the returned result: writing files, network requests, or modifying external systems.
- **Invariant** — a condition that remains true at every step of an algorithm. It is used to prove correctness and for checks in code.
- **Tie-breaking** — the rule for choosing when several options have the same score. Without it, the result may depend on data order or implementation details.
- **Asymptotic complexity (big-O notation)** — an estimate of how time or memory grows with input size. Worst case is the estimate for the least favorable input; typical/expected is for the usual or average case.
- **Seed (random seed)** — the initial value of a pseudorandom number generator. Fixing the seed makes random steps repeatable, and running with several seeds shows how much the result varies.
- **Tuning budget** — the amount of compute, time, or number of trials spent on hyperparameter search. A comparison is fair only if the new method and the baselines get a comparable budget.
- **Error bars** — a graphical representation of the uncertainty of an estimate: a confidence interval, standard error, or spread across seeds. It must be stated what exactly they show.
- **Ablation (ablation study)** — an experiment in which a component of a method is removed or replaced to test its contribution to the overall gain.
- **Failure modes** — the conditions under which a method performs poorly or breaks, and how this shows up. Describing them explicitly shows the limits of applicability.
- **Distribution shift** — a difference between the data a method encounters in use and the data it was developed or trained on. It is a common cause of performance degradation.
- **Adversarial input** — an input deliberately crafted to make a method fail.
- **Regression test** — a test that checks that previous results have not degraded or changed unexpectedly after code changes.
- **Objective (loss)** — the quantity a method minimizes or maximizes during training or optimization. All of its terms and weights must be described.
- **Benchmark contamination** — benchmark test examples ending up in a model's training data, for example through training on web data. Results on such a benchmark are inflated.
- **Early stopping** — ending training when performance on validation data stops improving. The criterion must use validation data, not test data.
- **Checkpoint selection** — the rule for choosing which model state saved during training is used for the final evaluation. It must rely only on validation data.
- **Decoding (decoding parameters)** — settings for generating LLM output (temperature, top-p, maximum length, and so on). They noticeably affect results, so they are recorded together with the model version.
- **NeurIPS Paper Checklist** — the checklist authors complete when submitting a paper to the NeurIPS conference, covering reproducibility, transparency, limitations, ethics, and broader impacts of the work.
- **ACM Artifact Review and Badging** — the Association for Computing Machinery policy for reviewing research artifacts of papers and awarding badges: Artifacts Available, Artifacts Evaluated (Functional, Reusable), and Results Validated (Reproduced, Replicated).
- **National Academies** — the U.S. National Academies of Sciences, Engineering, and Medicine. Their report "Reproducibility and Replicability in Science" (2019) provides widely used definitions of reproducibility and replicability and recommendations for achieving them.
