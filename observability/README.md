# Observability

This folder holds observability infrastructure, dashboards, metrics, and analysis tools.

## Structure

- **metrics/** — Metric definitions, tracking, aggregation
- **dashboards/** — Observability dashboards, queries
- **analysis/** — Ad-hoc analysis scripts, notebooks
- **traces/** — Distributed tracing, request flows
- **logs/** — Log aggregation, structured logging

Observability is a first-class artifact. Every feature should have:
1. Clear success metrics (tied to benchmarks)
2. Observable behavior (logs, metrics, traces)
3. Feedback loops (what did we learn?)

This enables the learning phase of the SDLC loop.
