# AGENTS.md — Instructions for AI Agents

This file provides orientation for AI agents working in this repository.

---

## Before you write any code

1. Read `docs/product/` to understand what PENA is and what it is intended to do.
2. Read `docs/sdlc2/` to understand the engineering methodology in use.
3. Check `docs/history/` for prior experiments and observations — treat this as historical context, not automatically canonical.

---

## Repository layout

```
README.md          — Project entry point
AGENTS.md          — This file
docs/
  product/         — Product context: domain, goals, assumptions, constraints
  sdlc2/           — SDLC2 methodology lifecycle artifacts (01-context through 11-learning)
  history/         — Past experiments, SDLC2 observations, learning trail
src/               — Application source code (not yet implemented)
tests/             — Tests (not yet implemented)
```

---

## Working principles

- **Do not start coding before checking docs.** Product intent and methodology context must come first.
- **Treat `docs/product/` as product context.** Domain, assumptions, constraints, and tools live here.
- **Treat `docs/sdlc2/` as methodology reference.** It describes how this project is built, not what it does.
- **Treat `docs/history/` as historical, not automatically authoritative.** Prior experiments may be superseded. Read critically.
- **Preserve uncertainty.** Do not invent decisions that have not been made. If something is unclear, note it rather than guessing.
- **Prefer small, reviewable changes.** One concern per commit. Do not batch unrelated edits.
- **Do not overbuild.** Implement only what is explicitly required by the current task.
- **Do not add dependencies, CI pipelines, or runtime configuration** unless explicitly asked.
- **Do not rewrite documents that only need minor updates.**
- **Keep Markdown simple.** No unnecessary structure or formatting.

---

## Project status (as of 2026-06-01)

PENA is in early-stage design. No application code exists yet. The repository contains:
- Product context documents
- SDLC2 lifecycle scaffolding
- Historical design experiments and observations

Source code will live in `src/` when implementation begins.
