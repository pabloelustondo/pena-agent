# Learning Extraction Subcomponents

## Purpose

This document defines the subcomponents for the `Learning Extraction` subsystem.

## Subcomponent Tree

```text
Learning Extraction
├── Learning Signal Detector
├── Concept Extractor
├── Pattern Extractor
├── Action Candidate Extractor
├── Knowledge Update Recommender
└── Learning Validation Reporter
```

## Learning Signal Detector

Purpose: Detects whether article contains reusable knowledge.

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
LearningSignal.
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

## Concept Extractor

Purpose: Extracts important concepts.

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
ConceptList.
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

## Pattern Extractor

Purpose: Extracts architectural or process patterns.

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
PatternList.
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

## Action Candidate Extractor

Purpose: Extracts possible future actions.

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
ActionCandidateList.
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

## Knowledge Update Recommender

Purpose: Recommends context or knowledge-base updates.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
Concepts, patterns, actions.
```

Outputs:

```text
KnowledgeUpdateRecommendation.
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

## Learning Validation Reporter

Purpose: Validates extracted learning output.

Responsibility boundary:

```text
Owns its specific transformation or decision.
Does not own upstream orchestration or downstream rendering unless explicitly stated.
```

Inputs:

```text
LearningOutput.
```

Outputs:

```text
LearningValidationReport.
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

The `Learning Extraction` subsystem should be independently understandable, independently stubbed, and independently testable.
