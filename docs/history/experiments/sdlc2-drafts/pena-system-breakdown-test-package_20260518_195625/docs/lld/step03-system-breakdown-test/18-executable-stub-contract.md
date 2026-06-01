# 18 Executable Stub Contract

## Public Interface

```text
run_golden_path() -> AgentRunResult
```

## Required Runtime Behavior

```text
1. Use scenario GP-001.
2. Use golden_path_stub mode.
3. Do not call external systems.
4. Do not call a real LLM.
5. Do not require a real database.
6. Produce deterministic output.
7. Produce execution trace.
8. Validate output against expected result.
```

## Required Subsystem Stub Contracts

```text
ConfigurationStub.load() -> RuntimeConfig
HardcodedArticleIngestionStub.ingest() -> NormalizedArticle
HardcodedContextManagementStub.resolve() -> ContextSnapshot
HardcodedScoringStub.score() -> ScoredArticle
HardcodedSummaryStub.summarize() -> StructuredSummary
HardcodedDigestStub.generate() -> DigestItem
InMemoryTraceStub.record() -> ExecutionTrace
GoldenPathTestHarnessStub.validate() -> TestValidationResult
```

## Required Final Assertions

```text
AgentRunResult.status == SUCCESS
AgentRunResult.scenario_id == GP-001
AgentRunResult.validation_result == PASSED
AgentRunResult.digest.title == Multi-Agent Orchestration Patterns for Enterprise AI Systems
AgentRunResult.scores.trust_score == 92
AgentRunResult.scores.relevance_score == 96
```
