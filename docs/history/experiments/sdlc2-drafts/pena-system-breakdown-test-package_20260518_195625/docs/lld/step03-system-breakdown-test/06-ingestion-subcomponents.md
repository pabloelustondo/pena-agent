# Ingestion Subcomponents

## Purpose

This document defines the subcomponents for the `Ingestion` subsystem.

## Subcomponent Tree

```text
Ingestion
├── Input Reader
├── Source Adapter
├── Article Parser
├── Metadata Extractor
├── Content Normalizer
├── Duplicate Detector
└── Ingestion Validation Reporter
```

## Input Reader

Purpose: Loads the source item for the run.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
Scenario id.
```

Outputs:

```text
SourceArticle.
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

## Source Adapter

Purpose: Normalizes source-specific metadata.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
SourceArticle.
```

Outputs:

```text
AdaptedSourceItem.
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

## Article Parser

Purpose: Extracts article fields from raw input.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
AdaptedSourceItem.
```

Outputs:

```text
ParsedArticle.
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

## Metadata Extractor

Purpose: Extracts author, date, source, URL, and metadata.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ParsedArticle.
```

Outputs:

```text
ArticleMetadata.
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

## Content Normalizer

Purpose: Creates a normalized internal article representation.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
ParsedArticle and ArticleMetadata.
```

Outputs:

```text
NormalizedArticle.
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

## Duplicate Detector

Purpose: Detects whether the item was already processed.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
NormalizedArticle.
```

Outputs:

```text
DuplicateCheckResult.
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

## Ingestion Validation Reporter

Purpose: Reports ingestion quality and completeness.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
NormalizedArticle.
```

Outputs:

```text
IngestionValidationReport.
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

The `Ingestion` subsystem should be independently understandable, independently stubbed, and independently testable.
