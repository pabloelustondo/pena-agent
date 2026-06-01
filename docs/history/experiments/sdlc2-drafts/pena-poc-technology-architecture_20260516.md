# PENA POC Technology Architecture

**Project:** PENA-Agent  
**Repository:** `pena-agent`  
**Date:** 2026-05-16  
**Status:** Prototype technology decision record  
**Trust level:** Reviewed project decision, candidate production direction  

---

# 1. Purpose

This document records the current technology architecture decision for the PENA proof of concept.

The purpose is not to compare every possible framework, language, or server option.

The purpose is to stabilize the initial prototype stack so the project can move forward with reduced ambiguity.

The selected stack is intended to be:

- simple enough for the first POC,
- modern enough to remain relevant,
- compatible with AI-assisted development,
- comfortable enough for hands-on work,
- and strong enough to remain a candidate for a future production version.

This is a pragmatic decision, not an ideological one.

---

# 2. Decision Summary

The initial PENA POC technology stack is:

| Layer | Decision |
|---|---|
| Frontend web application | Next.js |
| Frontend language | TypeScript |
| UI foundation | React through Next.js |
| Styling | Tailwind CSS |
| Backend service | Python |
| Backend API | FastAPI |
| Initial storage | Local files and SQLite |
| Later storage candidate | PostgreSQL |
| Repository | GitHub |
| IDE | VS Code |
| Specifications | Markdown |
| AI assisted development tools | Codex, Copilot, Claude, Gemini, and others, evaluated separately |

The core direction is:

```text
Next.js web interface
        ↓
FastAPI backend API
        ↓
Python PENA agent runtime
        ↓
Local files / SQLite initially, PostgreSQL later if needed
```

---

# 3. Core Architectural Principle

The PENA agent brain should not live inside the frontend.

The frontend should provide:

- user interaction,
- context upload,
- settings management,
- digest viewing,
- simple administration,
- and observability views.

The backend should own:

- ingestion logic,
- summarization pipelines,
- source evaluation,
- ranking logic,
- context management,
- agent orchestration,
- persistence,
- and runtime observability.

This keeps the web interface thin enough for fast iteration while preserving a clean backend architecture.

---

# 4. Why Next.js

Next.js is selected as the web framework for the PENA POC.

The reason is practical.

PENA needs a simple web interface now, but that interface may grow into a real product surface later.

Next.js gives a good path from:

```text
simple single page admin interface
```

to:

```text
structured full-stack web application
```

without forcing an early technology change.

Next.js is also useful for personal learning and professional currency. It builds on React, which is already widely used, while adding a more complete application framework around it.

For this project, Next.js is attractive because it supports:

- modern React development,
- TypeScript-first code,
- file-based routing,
- server-side capabilities when needed,
- easy local development,
- good AI coding assistant support,
- and a mature deployment ecosystem.

The goal is not to use every feature of Next.js immediately.

The goal is to choose a framework that starts small but does not become a dead end.

---

# 5. Why TypeScript

TypeScript is selected for the web application.

The reasons are:

- clearer contracts between frontend and backend,
- safer refactoring,
- better IDE support,
- better AI-assisted code generation,
- stronger maintainability,
- and alignment with modern frontend development practice.

For PENA, TypeScript is especially useful because the UI will exchange structured objects with the backend, such as:

- context files,
- uploaded documents,
- digest requests,
- digest results,
- article metadata,
- source quality notes,
- user settings,
- observability reports.

Those objects should be explicit.

The frontend should not become a loosely typed JavaScript layer that drifts away from backend contracts.

---

# 6. Why Python

Python remains the main backend and agent runtime language.

This decision is already aligned with the earlier PENA technical direction.

Python is the lowest-friction language for the first PENA agent because it has strong support for:

- AI SDKs,
- agent frameworks,
- embeddings,
- retrieval workflows,
- summarization pipelines,
- evaluation scripts,
- data processing,
- notebooks,
- observability experiments,
- and rapid prototyping.

The project is not choosing Python because it is the only possible backend language.

It is choosing Python because it gives the best early path for an AI-agent-centered prototype.

Other languages may become useful later, but they are not needed for the first POC.

---

# 7. Why FastAPI

FastAPI is selected as the initial Python web API framework.

The backend should expose clean HTTP endpoints to the Next.js frontend.

FastAPI is a good fit because it is:

- lightweight,
- Python-native,
- well-suited to typed API models,
- easy to run locally,
- compatible with async workflows,
- friendly to OpenAPI generation,
- and straightforward for AI coding assistants to understand.

The API layer should remain simple at first.

Initial endpoints may include:

```text
GET  /health
POST /context/upload
GET  /context/files
POST /digest/run
GET  /digest/{id}
GET  /observability/events
GET  /settings
POST /settings
```

The first version does not need complex orchestration.

It needs clean boundaries.

---

# 8. Initial Web Interface Scope

The first web interface should be intentionally modest.

It should not try to become a polished consumer product immediately.

Initial pages or sections:

| Area | Purpose |
|---|---|
| Dashboard | Show basic project status and recent activity |
| Context Upload | Upload files or paste text into the local PENA context |
| Context Library | View available context files and metadata |
| Digest Runner | Trigger a digest for a topic or source set |
| Digest Viewer | Read generated summaries and source quality notes |
| Settings | Manage basic model, source, and context preferences |
| Observability | View logs, runs, errors, and evaluation notes |

This matches the SDLC2 idea that the initial focus is workflow, observability, architecture, and learning loops, not polished UI.

---

# 9. Initial Storage Direction

The first POC should avoid unnecessary database complexity.

Recommended progression:

```text
Stage 1: local files and Markdown
Stage 2: SQLite for simple structured state
Stage 3: PostgreSQL if the model needs stronger persistence
Stage 4: vector database or embedding store only when retrieval needs justify it
```

This keeps the system simple while preserving growth options.

Initial local artifacts may include:

```text
/context-files/
/digests/
/runs/
/logs/
/settings.json
```

SQLite can later hold:

- uploaded context metadata,
- digest runs,
- source records,
- article metadata,
- model usage,
- evaluation scores,
- user preferences.

PostgreSQL should not be introduced until there is a real persistence need.

---

# 10. Suggested Repository Placement

The current SDLC2 repository structure should remain the primary organizing principle.

Inside that structure, the POC implementation can be placed under the implementation area while keeping documentation and specs separate.

Recommended practical structure:

```text
pena-agent/
  01-context/
  02-intent/
  03-benchmark/
  04-planning/
  05-specs/
  06-vibepoc/
  07-buildtest/
    backend/
      app/
      tests/
      pyproject.toml
    web/
      app/
      components/
      lib/
      package.json
  08-validate/
  09-runtime/
  10-observability/
  11-learning/
```

Alternative if implementation becomes large:

```text
pena-agent/
  backend/
  web/
  01-context/
  02-intent/
  ...
```

The first version should prefer SDLC2 clarity over conventional monorepo fashion.

The repository is part of the methodology experiment, not only a code container.

---

# 11. What Is Fixed For Now

The following decisions are fixed for the POC unless a concrete problem appears:

```text
Frontend: Next.js
Frontend language: TypeScript
Backend: Python
Backend API framework: FastAPI
Initial storage: local files, then SQLite
IDE: VS Code
Repository: GitHub
Specs and project memory: Markdown
```

These are not the main benchmark variables.

The project should not spend cycles repeatedly comparing Angular, React, Vue, Svelte, Flask, Django, Node, Java, or Go for this first POC.

That would create decision churn.

The technology stack is now stable enough to proceed.

---

# 12. What Remains Open For Comparison

The comparison area is not the web framework.

The comparison area is AI-assisted engineering and agent execution.

The project may compare:

- Codex,
- GitHub Copilot,
- Claude,
- Gemini,
- OpenAI models,
- Anthropic models,
- Google models,
- agent orchestration patterns,
- prompt/spec workflows,
- model escalation strategies,
- cost/performance tradeoffs,
- and observability methods.

In other words:

```text
Keep product technology stable.
Compare AI engineering workflows.
```

This is important because PENA is both a useful product prototype and a laboratory for AI-assisted software engineering.

Changing too many variables at once would make learning harder.

---

# 13. Candidate Production Direction

Although this is a POC stack, it is not a throwaway stack.

The selected architecture can plausibly evolve toward production.

A possible production-oriented evolution is:

```text
Next.js frontend
FastAPI backend
Python agent services
PostgreSQL persistence
Object storage for uploaded documents
Queue for background digest jobs
Observability dashboard
Authentication and authorization
Optional vector database for retrieval
```

The first prototype should not implement all of this.

But the technology direction does not block this evolution.

That is the key reason this stack is a reasonable candidate production path.

---

# 14. First Implementation Slice

The first useful slice should be small and visible.

Recommended first vertical slice:

```text
Upload context text or file
        ↓
Store it locally
        ↓
Show it in the web UI
        ↓
Run a simple digest request
        ↓
Display the generated digest
        ↓
Write logs and run metadata
```

This validates the complete path:

```text
web UI → API → Python agent logic → storage → output → observability
```

This is more valuable than building many isolated components.

---

# 15. First Milestone Definition

A reasonable first milestone:

```text
PENA POC 1, Manual Context Upload and Digest Generation
```

Acceptance criteria:

- user can open the local web app,
- user can upload or paste context,
- backend stores the uploaded context,
- user can trigger a digest run,
- backend generates a structured digest,
- frontend displays the digest,
- run metadata is recorded,
- basic errors are visible,
- logs are saved for observability.

This creates a working end-to-end loop without overengineering.

---

# 16. Technology Decision Record

## Decision

Use Next.js, TypeScript, Python, and FastAPI as the fixed technology foundation for the PENA POC.

## Rationale

The stack is modern, practical, learnable, AI-friendly, and capable of growing from a simple prototype into a production candidate.

## Consequences

Positive consequences:

- stable technology baseline,
- reduced framework debate,
- clear frontend/backend separation,
- strong AI development ecosystem,
- professional learning value,
- production evolution path.

Tradeoffs:

- two-language stack,
- some Next.js learning curve,
- frontend/backend contracts must be managed clearly,
- local development setup needs both Node.js and Python.

These tradeoffs are acceptable.

---

# 17. Final Position

For now, the PENA prototype technology architecture is:

```text
Next.js web application
TypeScript frontend
FastAPI backend
Python agent runtime
Local files / SQLite persistence
Markdown-first project memory
GitHub + VS Code development environment
```

This decision should be treated as stable for the POC.

The project should proceed with implementation rather than reopening framework comparison.

The main experimental comparison should now move to AI tools, AI workflows, model choices, context management, observability, and agent behavior.

That keeps the project focused.

The product technology becomes the stable platform.

The AI-assisted engineering methodology becomes the experiment.
