# pena-agent

**PENA — Personal Epistemic News Aggregator**

PENA is an early-stage personal AI assistant designed to help a knowledge worker find relevant information, filter noise, evaluate source quality, and produce summaries adapted to their domain and context.

The system is intentionally both a real product under development and a live software engineering experiment.

---

## Status

Early-stage. No application code exists yet. The repository currently holds product context, SDLC2 lifecycle scaffolding, and historical design experiments.

---

## What PENA aims to do

- Aggregate information from trusted sources.
- Filter noise and surface signal relevant to a specific person's domain and interests.
- Evaluate source trustworthiness.
- Produce concise, contextually adapted summaries.
- Learn from user feedback over time.

This is not a generic news feed. The goal is epistemic assistance: helping a person navigate information complexity more intelligently.

---

## Repository layout

```
README.md          — This file
AGENTS.md          — Instructions for AI agents working in this repo
LICENSE
docs/
  product/         — Product context: domain, goals, assumptions, constraints
  sdlc2/           — SDLC2 methodology lifecycle artifacts
  history/         — Past experiments and observations
src/               — Application source code (not yet implemented)
tests/             — Tests (not yet implemented)
```

See [docs/README.md](docs/README.md) for a full explanation of the documentation layout.

---

## Engineering methodology

This project follows a knowledge-centric, spec-driven engineering approach called SDLC2.
See [docs/sdlc2/](docs/sdlc2/) for lifecycle artifacts and `.instructions.md` for the development loop.

---

## For AI agents

Read [AGENTS.md](AGENTS.md) before making any changes.
