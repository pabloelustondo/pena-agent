# Context Management Subcomponents

## Purpose

This document defines the subcomponents for the `Context Management` subsystem.

## Subcomponent Tree

```text
Context Management
├── User Intent Profile Loader
├── Project Context Loader
├── Context Package Resolver
├── Context Prioritizer
├── Context Snapshot Builder
└── Context Validation Reporter
```

## User Intent Profile Loader

Purpose: Loads the user active intent profile.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
Scenario id or user id.
```

Outputs:

```text
UserIntentProfile.
```

Collaborators:

```text
Runtime Orchestration
Observability and Logging
Adjacent upstream/downstream subsystem
```

Stub behavior:

```text
Return deterministic output for Golden Path Scenario 001.
Do not call external systems.
Do not call a real LLM.
Do not use a real database.
```

Independent test:

```text
Given deterministic input,
when the subcomponent runs in stub mode,
then it returns the expected deterministic output and emits a traceable event.
```

## Project Context Loader

Purpose: Loads active project context for PENA.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
Project id.
```

Outputs:

```text
ProjectContext.
```

Collaborators:

```text
Runtime Orchestration
Observability and Logging
Adjacent upstream/downstream subsystem
```

Stub behavior:

```text
Return deterministic output for Golden Path Scenario 001.
Do not call external systems.
Do not call a real LLM.
Do not use a real database.
```

Independent test:

```text
Given deterministic input,
when the subcomponent runs in stub mode,
then it returns the expected deterministic output and emits a traceable event.
```

## Context Package Resolver

Purpose: Combines user and project context.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
UserIntentProfile and ProjectContext.
```

Outputs:

```text
ContextPackage.
```

Collaborators:

```text
Runtime Orchestration
Observability and Logging
Adjacent upstream/downstream subsystem
```

Stub behavior:

```text
Return deterministic output for Golden Path Scenario 001.
Do not call external systems.
Do not call a real LLM.
Do not use a real database.
```

Independent test:

```text
Given deterministic input,
when the subcomponent runs in stub mode,
then it returns the expected deterministic output and emits a traceable event.
```

## Context Prioritizer

Purpose: Selects relevant themes and keywords.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ContextPackage.
```

Outputs:

```text
PrioritizedContext.
```

Collaborators:

```text
Runtime Orchestration
Observability and Logging
Adjacent upstream/downstream subsystem
```

Stub behavior:

```text
Return deterministic output for Golden Path Scenario 001.
Do not call external systems.
Do not call a real LLM.
Do not use a real database.
```

Independent test:

```text
Given deterministic input,
when the subcomponent runs in stub mode,
then it returns the expected deterministic output and emits a traceable event.
```

## Context Snapshot Builder

Purpose: Builds the immutable context snapshot for the run.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
PrioritizedContext.
```

Outputs:

```text
ContextSnapshot.
```

Collaborators:

```text
Runtime Orchestration
Observability and Logging
Adjacent upstream/downstream subsystem
```

Stub behavior:

```text
Return deterministic output for Golden Path Scenario 001.
Do not call external systems.
Do not call a real LLM.
Do not use a real database.
```

Independent test:

```text
Given deterministic input,
when the subcomponent runs in stub mode,
then it returns the expected deterministic output and emits a traceable event.
```

## Context Validation Reporter

Purpose: Reports missing or inconsistent context fields.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ContextSnapshot.
```

Outputs:

```text
ContextValidationReport.
```

Collaborators:

```text
Runtime Orchestration
Observability and Logging
Adjacent upstream/downstream subsystem
```

Stub behavior:

```text
Return deterministic output for Golden Path Scenario 001.
Do not call external systems.
Do not call a real LLM.
Do not use a real database.
```

Independent test:

```text
Given deterministic input,
when the subcomponent runs in stub mode,
then it returns the expected deterministic output and emits a traceable event.
```

## Summary

The `Context Management` subsystem should be independently understandable, independently stubbed, and independently testable.
