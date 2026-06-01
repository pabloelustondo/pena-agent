# Benchmarks

This folder holds target behaviors, success criteria, and reference implementations.

## Structure

- **pena-benchmark.md** — Primary PENA benchmark (Flipboard comparison + epistemic assistance)
- **feature-benchmarks/** — Feature-level targets and acceptance criteria
- **comparison/** — Tool evaluations, AI platform comparisons
- **data/** — Benchmark test data, example inputs/outputs
- **metrics.md** — Quantitative targets (latency, accuracy, relevance, etc.)

Benchmarks drive all downstream work:
1. Define what "success" means
2. Inform specs (how to implement success)
3. Enable observability (measure against target)
4. Guide learning (why didn't we hit the target?)

Every feature should have an explicit benchmark before implementation begins.
