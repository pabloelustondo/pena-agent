# Specifications

This folder holds formal and semi-formal specifications for PENA features, components, and workflows.

## Structure

- **pena.md** — Core PENA agent specification (features, behavior, constraints)
- **benchmarks/** — Reference implementations or target behaviors
- **feature-*.md** — Individual feature specifications
- **api/** — API contracts, schemas, interfaces
- **runtime/** — Runtime behavior expectations, performance targets

Specs are created iteratively from:
1. Intent → Benchmark → Detailed Spec
2. Runtime feedback → Spec refinement
3. Learning insights → Spec evolution

All specs connect back to benchmarks. All implementations connect back to specs.
