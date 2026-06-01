# PENA / SDLC2 — UML Specification Plan

## Introduction

This document defines the initial UML-oriented specification strategy for the PENA-Agent project.

The objective is not merely to create diagrams.

The objective is to create:

- semantic architecture,
- AI-readable specifications,
- structured engineering context,
- and an executable knowledge representation layer

for both humans and AI-assisted engineering systems.

The approach intentionally combines:

```text
specification discipline
+
iterative exploration
+
architectural clarity
+
controlled vibe
```

Meaning:

```text
vibe energy is allowed,
but it must crystallize into explicit specification artifacts.
```

---

# Why UML for PENA

PENA-Agent is evolving into both:

1. a real AI-agent system,
2. and a laboratory for SDLC2 / AI-assisted engineering methodology.

As the repository grows, purely conversational descriptions become insufficient.

We need:

- stable architecture,
- reusable semantic representations,
- structured context,
- explicit workflows,
- domain models,
- interaction models,
- runtime models,
- and operational observability structures.

UML provides a mature language for representing these concepts.

---

# Important Clarification

The objective is NOT:

```text
“Big Design Up Front”
```

The objective is:

```text
iterative semantic crystallization
```

The diagrams evolve together with:
- implementation,
- observability,
- learning,
- and runtime feedback.

This aligns directly with SDLC2.

---

# UML Version

Current OMG UML standard:

```text
UML 2.5.1
```

There is currently no formal UML 3 standard in active practical use.

---

# Why Textual UML

The project will intentionally prioritize:

```text
TEXTUAL UML
```

instead of drawing-first approaches.

Primary candidate:

```text
PlantUML
```

Reasons:

- Git-friendly
- Markdown-friendly
- Diff-friendly
- AI-friendly
- VS Code-friendly
- Easy versioning
- Easy iterative refinement
- Easy generation from AI systems
- Easy rendering later

The diagram source itself becomes:
- specification,
- context,
- and semantic memory.

---

# Core SDLC2 Principle

The UML artifacts are not merely documentation.

They become:

```text
active engineering context
```

This is consistent with the SDLC2 observation that:

```text
context behaves as organizational memory
```

and not merely passive documentation.

---

# Overall UML Specification Strategy

The plan is to create a sequence of UML-oriented slides / artifacts.

These are not merely presentation slides.

They are intended to become:

- repository context,
- AI grounding artifacts,
- engineering specifications,
- and reusable semantic architecture.

---

# Proposed UML Specification Deck

---

# Slide 1 — PENA Vision and Identity

## Purpose

Establish:
- project identity,
- system purpose,
- and SDLC2 relationship.

## Diagram Type

```text
High-level context / conceptual diagram
```

## Main Concepts

- PENA-Agent
- Personal Epistemic News Aggregator
- AI-assisted engineering laboratory
- SDLC2 validation environment
- Humans + AI + Agents

## Main Goal

Show that the project is intentionally both:
- a useful system,
- and a methodology experiment.

---

# Slide 2 — System Context Diagram

## Purpose

Show the external ecosystem around PENA.

## Diagram Type

```text
Context / architectural interaction diagram
```

## Main Actors

- User
- News sources
- AI providers
- GitHub repository
- Runtime environment
- Observability system
- Knowledge artifacts

## Main Goal

Show where PENA lives operationally.

---

# Slide 3 — Use Case Model

## Purpose

Describe system capabilities from the user perspective.

## Diagram Type

```text
UML Use Case Diagram
```

## Initial Use Cases

- Collect articles
- Filter noise
- Evaluate source quality
- Summarize information
- Categorize content
- Generate digest
- Adapt to user context
- Capture feedback
- Produce observability reports

## Main Goal

Clarify what the system actually does.

---

# Slide 4 — Actor Model

## Purpose

Clarify the participating entities.

## Diagram Type

```text
Actor / role model
```

## Actors

- Human user
- Developer / architect
- AI assistant
- LLM provider
- External source provider
- Scheduler
- Repository
- Runtime pipeline

## Main Goal

Clarify:
- human responsibilities,
- AI responsibilities,
- and runtime responsibilities.

---

# Slide 5 — Domain / Data Model

## Purpose

Define the core conceptual objects.

## Diagram Type

```text
UML Class Diagram
```

## Candidate Classes

- UserContext
- Source
- Article
- Digest
- Summary
- TrustSignal
- RelevanceScore
- Observation
- Feedback
- LearningArtifact
- RuntimeEvent

## Main Goal

Create the first semantic backbone of the system.

---

# Slide 6 — Context Provenance and Trust Model

## Purpose

Represent semantic trust and lifecycle maturity.

## Diagram Type

```text
UML Class Diagram + State concepts
```

## Semantic Trust Levels

- Generated
- Experimental
- Reviewed
- Canonical
- Deprecated

## Lifecycle Maturity Levels

- Working
- Dev
- Release
- Main

## Main Goal

Represent:

```text
semantic trust
+
process maturity
=
operational confidence
```

---

# Slide 7 — Main Digest Generation Sequence

## Purpose

Model the first operational workflow.

## Diagram Type

```text
UML Sequence Diagram
```

## Main Sequence

```text
User request
→ Load context
→ Retrieve sources
→ Evaluate trust
→ Summarize
→ Rank relevance
→ Generate digest
→ Present digest
→ Capture feedback
```

## Main Goal

Describe the primary runtime interaction.

---

# Slide 8 — Feedback and Learning Loop

## Purpose

Represent the SDLC2 operational loop.

## Diagram Type

```text
UML Sequence Diagram
```

## Main Sequence

```text
Runtime
→ Observability
→ Human review
→ Learning extraction
→ Context update
→ Next iteration
```

## Main Goal

Show that learning is part of the system architecture.

---

# Slide 9 — Activity Diagram: Runtime Pipeline

## Purpose

Represent operational flow.

## Diagram Type

```text
UML Activity Diagram
```

## Main Activities

- Ingest
- Normalize
- Deduplicate
- Categorize
- Summarize
- Evaluate trust
- Rank relevance
- Generate digest
- Persist observations

## Main Goal

Describe the runtime processing pipeline.

---

# Slide 10 — Component Architecture

## Purpose

Represent major system modules.

## Diagram Type

```text
UML Component Diagram
```

## Candidate Components

- Ingestion engine
- Context manager
- Summarization engine
- Trust evaluator
- Ranking engine
- Digest generator
- Observability engine
- Knowledge repository
- Runtime orchestrator

## Main Goal

Separate responsibilities clearly.

---

# Slide 11 — Deployment / Runtime Architecture

## Purpose

Represent execution environments.

## Diagram Type

```text
UML Deployment Diagram
```

## Candidate Nodes

- Developer laptop
- VS Code
- GitHub repository
- Python runtime
- External AI APIs
- News APIs / RSS
- Local storage
- Observability artifacts

## Main Goal

Clarify where the system executes.

---

# Slide 12 — SDLC2 Repository Cognitive Architecture

## Purpose

Represent repository structure as semantic architecture.

## Diagram Type

```text
UML Package Diagram
```

## Main Packages

```text
01-context
02-intent
03-benchmark
04-planning
05-specs
06-vibepoc
07-buildtest
08-validate
09-runtime
10-observability
11-learning
```

## Main Goal

Show the repository itself as:
- organizational memory,
- semantic structure,
- and AI grounding architecture.

---

# Optional Future Diagrams

Possible future additions:

- State Machine Diagrams
- Communication Diagrams
- Object Diagrams
- Timing Diagrams
- AI-agent interaction diagrams
- Knowledge graph representations
- Observability topology diagrams
- Semantic provenance maps

---

# Initial Recommended Folder Structure

```text
05-specs/
└── uml/
    ├── plan/
    ├── context/
    ├── usecases/
    ├── domain/
    ├── sequence/
    ├── activity/
    ├── component/
    ├── deployment/
    └── runtime/
```

---

# Initial Recommended File Naming

Examples:

```text
01-system-context.puml
02-use-case-model.puml
03-domain-model.puml
04-digest-sequence.puml
05-runtime-activity.puml
06-component-architecture.puml
07-runtime-deployment.puml
08-sdlc2-cognitive-architecture.puml
```

---

# Important SDLC2 Architectural Insight

The UML models are not:
- isolated diagrams,
- static documents,
- or presentation-only artifacts.

They are intended to become:

```text
AI-readable semantic specifications
```

This is one of the most important conceptual directions emerging from PENA.

The specifications become:
- operational context,
- repository memory,
- and AI grounding structures.

---

# Emerging SDLC2 Principle

A refined principle emerging from this discussion:

```text
Vibe should amplify specification energy,
not replace specification discipline.
```

or more operationally:

```text
Exploration may start informally,
but should progressively crystallize into explicit semantic artifacts.
```

---

# Recommended First Deliverable

Recommended first artifact:

```text
05-specs/uml/01-system-context.puml
```

Then continue with:

1. Use Case Model
2. Domain Model
3. Main Runtime Sequence
4. Component Architecture
5. SDLC2 Cognitive Architecture

This ordering moves from:
- broad conceptual understanding
toward:
- detailed operational structure.

---

# Final Reflection

One of the strongest ideas emerging from this UML initiative is that:

```text
modern AI-assisted engineering increasingly depends on explicit semantic structure.
```

UML is therefore not being used merely as:
- traditional enterprise documentation.

Instead, it becomes part of:
- the operational context,
- AI grounding layer,
- repository cognition,
- and SDLC2 semantic architecture.

The repository evolves from:
- a code container

toward:
- a structured knowledge and reasoning environment.
