# Digest Generation Subcomponents

## Purpose

This document defines the subcomponents for the `Digest Generation` subsystem.

## Subcomponent Tree

```text
Digest Generation
├── Digest Item Builder
├── Digest Formatter
├── Priority Labeler
├── Recommendation Builder
├── Explanation Formatter
├── Output Renderer
└── Digest Validation Reporter
```

## Digest Item Builder

Purpose: Builds the digest item object.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
StructuredSummary and ScoredArticle.
```

Outputs:

```text
DigestItem.
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

## Digest Formatter

Purpose: Formats digest for console, Markdown, or JSON.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
DigestItem.
```

Outputs:

```text
FormattedDigest.
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

## Priority Labeler

Purpose: Assigns digest priority.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ScoredArticle.
```

Outputs:

```text
PriorityLabel.
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

## Recommendation Builder

Purpose: Creates action or save recommendation.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
DigestItem and ContextSnapshot.
```

Outputs:

```text
Recommendation.
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

## Explanation Formatter

Purpose: Formats why-relevant explanation.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ScoreExplanation and summary.
```

Outputs:

```text
FormattedExplanation.
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

## Output Renderer

Purpose: Renders the final user-facing output.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
FormattedDigest.
```

Outputs:

```text
DigestOutput.
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

## Digest Validation Reporter

Purpose: Validates required digest fields.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
DigestOutput.
```

Outputs:

```text
DigestValidationReport.
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

The `Digest Generation` subsystem should be independently understandable, independently stubbed, and independently testable.
