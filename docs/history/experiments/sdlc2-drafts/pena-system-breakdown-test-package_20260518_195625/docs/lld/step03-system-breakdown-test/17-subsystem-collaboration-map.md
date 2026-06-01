# 17 Subsystem Collaboration Map

## Golden Path Collaboration

```text
Agent Run Facade
→ Agent Runtime
→ Execution Mode Resolver
→ Subsystem Registry
→ Execution Context
→ Runtime Orchestrator
→ Configuration
→ Ingestion
→ Context Management
→ Trust and Relevance Scoring
→ LLM Summarization
→ Digest Generation
→ Observability and Logging
→ Test Harness
→ Agent Result Assembler
→ AgentRunResult
```

## Data Flow

```text
SourceArticle
→ NormalizedArticle
→ ContextSnapshot
→ ScoredArticle
→ StructuredSummary
→ DigestItem
→ AgentRunResult
```

## Trace Flow

```text
Every subsystem emits a step trace event.

TraceEvent
→ StepTraceRecorder
→ ExecutionTrace
→ TestHarness.TraceValidator
→ TestEvidenceBundle
```
