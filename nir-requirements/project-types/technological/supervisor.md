# Technological Project — Guidance for Supervisors

This document supplements the general requirements. A technological project must define in advance not only its functionality, but also how the technical quality of the solution will be demonstrated.

## When defining the topic

The wording must identify a technological problem and a measurable improvement criterion. The topic must not be reduced to “build a service with X” or “integrate library Y” without an independent technical result.

Define the following in advance:

- existing alternatives and tools;
- the technical limitation the project must overcome;
- the student's architectural contribution;
- benchmark metrics such as quality, latency, throughput, resource usage, cost, and failure rate;
- test scenarios;
- reproducibility and deployment requirements; and
- whether component-contribution analysis is needed.

## What to monitor

- the repository is maintained throughout the project rather than uploaded just before the defense;
- the architecture is documented and remains consistent with the implementation;
- critical components have tests;
- dependencies and configurations are pinned;
- benchmarks use comparable conditions; and
- the demonstration confirms actual operability rather than merely showing screenshots.

## Critical grading risks

- a working system without comparison does not receive 5A;
- a repository that cannot be verified limits the grade to 4C;
- missing component analysis for a complex system limits the grade to 4C; and
- if the technical result consists mainly of ready-made solutions without an independent contribution, the technical-novelty criterion will receive a low score.

## Final artifact

The technology report must explain not only what was built, but also why the architecture was selected, which alternatives were considered, how the system was tested, which metrics were used for comparison, and where its limitations lie.
