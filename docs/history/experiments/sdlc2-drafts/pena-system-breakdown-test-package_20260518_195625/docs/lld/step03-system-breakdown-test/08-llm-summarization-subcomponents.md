# LLM Summarization Subcomponents

## Purpose

This document defines the subcomponents for the `LLM Summarization` subsystem.

## Subcomponent Tree

```text
LLM Summarization
├── Prompt Builder
├── Model Client Adapter
├── Summary Generator
├── Key Insight Extractor
├── User Relevance Explainer
├── Summary Quality Checker
└── Summary Validation Reporter
```

## Prompt Builder

Purpose: Builds summarization prompt or request payload.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
NormalizedArticle, ContextSnapshot, ScoredArticle.
```

Outputs:

```text
SummarizationRequest.
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

## Model Client Adapter

Purpose: Abstracts real or stubbed model invocation.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
SummarizationRequest.
```

Outputs:

```text
ModelResponse.
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

## Summary Generator

Purpose: Produces short summary and key points.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ModelResponse or stub data.
```

Outputs:

```text
StructuredSummary.
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

## Key Insight Extractor

Purpose: Extracts the core reusable insight.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
StructuredSummary.
```

Outputs:

```text
KeyInsight.
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

## User Relevance Explainer

Purpose: Explains why the item matters to the user.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
StructuredSummary and ContextSnapshot.
```

Outputs:

```text
UserRelevanceExplanation.
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

## Summary Quality Checker

Purpose: Checks required summary fields.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
StructuredSummary.
```

Outputs:

```text
SummaryQualityReport.
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

## Summary Validation Reporter

Purpose: Reports validation result for summary contract.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
StructuredSummary.
```

Outputs:

```text
SummaryValidationReport.
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

The `LLM Summarization` subsystem should be independently understandable, independently stubbed, and independently testable.
