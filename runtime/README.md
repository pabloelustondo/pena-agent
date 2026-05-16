# Runtime

This folder holds production code, deployment configurations, and live system behavior.

## Structure

- **src/** — Core application code
- **config/** — Environment configs, secrets management
- **docker/** — Container definitions
- **scripts/** — Operational scripts, data loaders, maintenance tasks
- **logs/** — Runtime logs, execution traces (gitignored bulk data)

Code here is evaluated against:
1. Specifications (does it implement the spec?)
2. Benchmarks (does it meet the target?)
3. Observability (can we see what's happening?)
4. Learning feedback (what did we learn from execution?)
