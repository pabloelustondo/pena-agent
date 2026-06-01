# SDLC2 — Canonical Steps, Artifacts, and Repository Folder Structure

## Purpose

This document captures an important refinement in the PENA-Agent project.

The SDLC2 lifecycle already existed visually as a set of main boxes around the loop. During repository design, we clarified that these boxes are not only abstract process steps. They also correspond to artifact domains that can guide the GitHub / VS Code project structure.

This document records:

- the refined canonical SDLC2 steps,
- how they relate to the original visual model,
- how they map to repository folders,
- why numeric prefixes are useful,
- and why the Validate / ReviewQaSec box is not new, but already existed in the SDLC diagram.

---

# Key Realization

The repository structure should reflect the lifecycle, but not mechanically copy every phrase from the lifecycle diagram.

Some lifecycle elements are:

- cognitive states,
- process phases,
- artifact collections,
- runtime environments,
- validation gates,
- learning outputs.

Therefore, the repository needs artifact-oriented folder names that preserve the canonical SDLC2 order while remaining practical for GitHub and VS Code.

---

# Original SDLC Visual Model

The existing SDLC visual model already contained these major elements:

```text
Context
Intent
Plan / Roadmap
Specs
Vibe / POC
Design / Build / Test
Validate
Observability
Learn
Context
```

The right-side box in the diagram was already:

```text
Code Review
- Guardrails
- Quality
- Security
→ Validate
```

This means the validation stage was always present.

The recent discussion did not introduce a new lifecycle concept. It clarified and operationalized an existing one.

---

# Important Validation of the Original Diagram

The refined repository model validates the original SDLC diagram.

The original diagram already had the correct architectural separation:

```text
Vibe / POC
→ Design / Build / Test
→ Validate
→ Runtime / Observability / Learn
→ Context
```

This is important because many AI-assisted development workflows collapse implementation and validation into one vague stage.

SDLC2 keeps them separate.

That separation is especially important in the AI era because AI-assisted generation increases the need for:

- human review,
- quality checks,
- security review,
- benchmarks,
- guardrails,
- architectural validation,
- and governance.

---

# AI Is Cross-Cutting, Not a Single Step

Another important refinement:

AI assistance should not be represented as only one lifecycle phase.

In the original visual model, the center already contained:

```text
Humans + AI + Agents
Humans in the Loop
```

This means AI assistance is cross-cutting.

All SDLC2 stages may be AI-assisted:

- context gathering,
- intent clarification,
- benchmark research,
- planning,
- specification writing,
- POC creation,
- build and test,
- validation,
- runtime support,
- observability analysis,
- learning extraction.

Therefore, the previous phrase “AI-assisted Build” is less precise as a lifecycle step, because it implies that only the build phase is AI-assisted.

The cleaner model is:

```text
BuildTest
```

with AI assistance understood as ambient across the whole lifecycle.

---

# Refined Canonical SDLC2 Steps

The refined canonical loop is:

```text
01 Context
02 Intent
03 Benchmark
04 Planning
05 Specs
06 VibePOC
07 BuildTest
08 Validate
09 Runtime
10 Observability
11 Learning
↺ Context
```

This is currently the clearest operational form.

---

# Why Benchmark Comes Before Planning

Benchmark remains early because it grounds the project before planning and specification.

The benchmark phase asks:

- What already exists?
- What are we comparing against?
- What is the baseline?
- What does “good enough” mean?
- What should we copy, improve, or avoid?

For PENA, one early benchmark is:

```text
At least as useful as Flipboard, then going beyond it through contextual summarization and epistemic assistance.
```

Benchmarking before planning reduces vague ambition and improves practical direction.

---

# Why Planning Comes Before Specs

This ordering was refined as:

```text
Benchmark
→ Planning
→ Specs
```

Planning before specs helps organize the work before writing detailed constraints.

Planning defines:

- scope,
- sequence,
- milestones,
- work breakdown,
- near-term priorities,
- first POC boundaries.

Specs then define:

- precise requirements,
- expected behavior,
- constraints,
- acceptance criteria,
- data structures,
- system contracts.

This keeps specifications from becoming unfocused or premature.

---

# Why VibePOC Is Separate

VibePOC is intentionally separate from production code.

It may include code, but that code is exploratory.

VibePOC artifacts may be:

- quick scripts,
- throwaway experiments,
- wrong-language prototypes,
- UI sketches,
- prompt experiments,
- agent experiments,
- API probes,
- data tests.

This stage is allowed to be rough.

Its purpose is:

- exploration,
- creativity,
- risk reduction,
- feasibility testing,
- and learning.

A POC may later influence the real implementation, but it should not automatically become production code.

---

# Why BuildTest Is Separate

BuildTest is the stage for real implementation.

This is what would traditionally be called the main codebase.

BuildTest includes:

- production-oriented code,
- unit tests,
- integration tests,
- structured modules,
- maintainable design,
- refactoring,
- implementation aligned with specs.

This is where the project moves from exploration into disciplined engineering.

---

# Why Validate Is Separate

Validate corresponds to the right-side box in the original SDLC visual model.

It includes:

- code review,
- QA,
- security,
- guardrails,
- benchmarks,
- architecture review,
- quality checks,
- compliance-style review where relevant.

This stage is not optional.

In AI-assisted engineering, Validate becomes more important, not less important.

The reason is simple:

AI may accelerate implementation, but it can also accelerate:

- hidden defects,
- hallucinated assumptions,
- insecure dependencies,
- overcomplicated designs,
- inconsistent patterns,
- and unreviewed generated code.

Validate is the stage where the system is checked before moving toward runtime.

---

# Runtime Clarification

Runtime should not be confused with source code.

Runtime refers to artifacts and mechanisms related to deploying, running, and operating the system.

Runtime artifacts may include:

- Docker files,
- deployment scripts,
- configuration files,
- environment files,
- run commands,
- generated outputs,
- scheduled job scripts,
- service startup scripts,
- local execution notes.

The source code belongs primarily to BuildTest.

The deploy/run artifacts belong to Runtime.

---

# Observability Clarification

Observability is the phase and artifact domain for understanding what actually happens.

It may include:

- logs,
- metrics,
- traces,
- evaluation reports,
- generated digests,
- behavior comparisons,
- quality measurements,
- tool performance notes,
- AI-agent behavior observations.

Observability is not only production monitoring.

In SDLC2, observability also applies to:

- development workflow,
- AI-agent behavior,
- specification quality,
- benchmark results,
- and human review patterns.

---

# Learning Clarification

Learning is the distilled knowledge extracted from feedback and observability.

It is not raw logs.

It is not every note.

Learning artifacts should capture:

- reusable insights,
- validated principles,
- lessons learned,
- patterns to repeat,
- mistakes to avoid,
- SDLC2 refinements,
- project-level conclusions.

Learning feeds back into Context.

This closes the loop.

---

# Canonical Repository Folder Structure

Numeric prefixes are useful because they preserve canonical lifecycle order in GitHub, VS Code, and file explorers.

Recommended folder structure:

```text
01-context/
02-intent/
03-benchmark/
04-planning/
05-specs/
06-vibepoc/
07-buildtest/
08-validate/
09-runtime/
10-observability/
11-learning/
```

This order mirrors the refined SDLC2 loop.

---

# Folder Purpose Table

| Folder | Lifecycle Step | Purpose |
|---|---|---|
| `01-context/` | Context | Background knowledge, SDLC2 material, references, accumulated memory |
| `02-intent/` | Intent | Goals, desired outcomes, product direction, methodology direction |
| `03-benchmark/` | Benchmark | Comparisons, baseline systems, competitive analysis, quality targets |
| `04-planning/` | Planning | Roadmaps, milestones, task breakdowns, execution sequencing |
| `05-specs/` | Specs | Requirements, constraints, acceptance criteria, system contracts |
| `06-vibepoc/` | VibePOC | Exploratory prototypes, experiments, quick scripts, idea validation |
| `07-buildtest/` | BuildTest | Production-oriented source code and tests |
| `08-validate/` | Validate | Review, QA, security, guardrails, benchmark validation |
| `09-runtime/` | Runtime | Deployment, run scripts, configuration, Docker, operational artifacts |
| `10-observability/` | Observability | Logs, metrics, reports, evaluations, behavior observations |
| `11-learning/` | Learning | Distilled insights, lessons, reusable knowledge, SDLC2 refinements |

---

# Why Use Numeric Prefixes

Numeric prefixes help preserve the canonical order.

Without numbers, folders sort alphabetically:

```text
benchmark/
buildtest/
context/
intent/
learning/
...
```

This loses lifecycle meaning.

With numeric prefixes:

```text
01-context/
02-intent/
03-benchmark/
...
```

the repository itself visually teaches the lifecycle.

This is useful for:

- humans,
- AI agents,
- future collaborators,
- GitHub browsing,
- VS Code navigation,
- and long-term project memory.

The folder structure becomes a semantic map.

---

# Naming Notes

## `06-vibepoc/`

This folder intentionally keeps POC separate from production code.

Possible alternatives:

```text
06-vibe-poc/
06-poc/
06-experiments/
```

Current recommendation:

```text
06-vibepoc/
```

because it preserves the SDLC2 term directly.

## `07-buildtest/`

Possible alternatives:

```text
07-src/
07-build-test/
07-implementation/
```

Current recommendation:

```text
07-buildtest/
```

because it preserves the SDLC2 stage and makes clear that production code and tests belong together conceptually.

If needed, it may later contain:

```text
07-buildtest/
├── src/
└── tests/
```

## `08-validate/`

This replaces the longer phrase:

```text
ReviewQaSec
```

as a folder name.

`Validate` is better because:

- it matches the original SDLC visual model,
- it is shorter,
- it is broader,
- it includes review, QA, security, benchmarks, and guardrails.

Internally it may contain:

```text
08-validate/
├── review/
├── qa/
├── security/
├── benchmarks/
└── guardrails/
```

---

# Process Step vs Artifact Domain

A crucial SDLC2 refinement:

The lifecycle step and the folder are related, but not identical.

Example:

```text
BuildTest
```

is a lifecycle phase.

The folder:

```text
07-buildtest/
```

is an artifact domain containing source code, tests, and implementation-related assets.

Similarly:

```text
Validate
```

is a process stage.

The folder:

```text
08-validate/
```

contains review notes, QA reports, security findings, and benchmark validation artifacts.

This distinction matters.

The SDLC loop describes how work flows.

The repository structure describes where accumulated artifacts live.

---

# Current SDLC2 Artifact Principle

A refined principle emerging from this discussion:

> The repository structure should mirror the SDLC2 lifecycle enough to preserve canonical meaning, but use artifact-oriented names practical for GitHub, VS Code, and AI agents.

This avoids two extremes:

1. Pure process names that are awkward as folders.
2. Pure technical folders that lose lifecycle meaning.

The numeric structure gives both:

- lifecycle order,
- artifact clarity.

---

# Recommended First Repository Structure Commit

The next structural commit could create these folders using placeholder files, for example `.gitkeep` or `README.md` in each folder.

Recommended commit message:

```text
docs: establish SDLC2-aligned repository structure
```

or:

```text
chore: add canonical SDLC2 folder structure
```

If the folders include explanatory README files, use:

```text
docs: add canonical SDLC2 folder structure
```

---

# Minimal Folder README Pattern

Each folder can eventually contain a short `README.md` explaining its purpose.

Example for `01-context/README.md`:

```md
# 01-context

This folder contains accumulated background knowledge and organizational memory for the PENA-Agent project.

It includes SDLC2 materials, references, handovers, observations, and other context that helps humans and AI agents understand the project.
```

This makes each folder self-explaining.

It also improves AI-agent grounding.

---

# Final Reflection

This refinement is important because it connects three layers:

```text
SDLC2 lifecycle
↓
Repository artifact structure
↓
AI-assisted engineering context
```

The original SDLC diagram already contained the major boxes.

The repository structure now turns those boxes into an ordered artifact system.

This validates the main SDLC2 model and makes it operational inside GitHub and VS Code.

The project is no longer merely using a repository.

The repository itself is becoming a structured representation of the SDLC2 lifecycle.
