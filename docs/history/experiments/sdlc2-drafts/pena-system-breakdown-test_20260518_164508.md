# PENA System Breakdown and Executable Stub Test Plan

## 1. Purpose

This document defines the next low-level design step for the PENA Agent.

The goal is to move from UML-level architecture into a structured component breakdown that can later become executable code.

This is still specification work, not production implementation.

The immediate objective is to create:

1. A clear hierarchical system and subsystem breakdown.
2. A set of independently testable component stubs.
3. One realistic end-to-end hardcoded execution path.
4. A first executable PENA use case aligned with the real intent of the project.

---

## 2. Root System

```text
PENA Agent
```

The PENA Agent is the top-level system.

Its role is to ingest information, interpret it against user/project context, evaluate trust and relevance, summarize it, produce useful digest output, and generate observable execution traces.

---

## 3. Success Criteria

The Step 3 breakdown succeeds when three fronts are satisfied.

### 3.1 Conceptual Coherence

The whole structure must be easy to understand.

A reader should be able to see:

- what the PENA Agent does
- which subsystems exist
- how the subsystems collaborate
- where each responsibility belongs
- how the full system can be developed by divide and conquer

### 3.2 Executable Agent Path

The agent must be executable from the beginning.

Even if every internal component is stubbed, the system should run one complete deterministic path and return the expected result.

### 3.3 Real PENA End-to-End Test

The test must not be a dumb “hello world” test.

It must represent a real PENA use case:

- realistic input
- realistic context
- realistic trust and relevance reasoning
- realistic digest output
- observable execution trace

The outputs may be hardcoded at first, but the use case must express the true intent of PENA.

---

## 4. Golden Path Stub Execution

### 4.1 Definition

The first executable path is:

```text
Golden Path Scenario 001: Curated AI News Digest
```

### 4.2 Scenario

Given:

- one hardcoded source article
- one hardcoded user intent profile
- one hardcoded context package
- one hardcoded expected trust score
- one hardcoded expected relevance score
- one hardcoded expected summary
- one hardcoded expected digest output

When:

- the PENA Agent runs

Then:

- it executes the full pipeline
- each subsystem receives and returns structured data
- the final digest is produced
- execution logs are generated
- the output matches the expected golden result

### 4.3 Golden Path Pipeline

```text
Ingestion
→ Context Resolution
→ Trust and Relevance Scoring
→ LLM Summarization
→ Digest Generation
→ Observability
→ Final Digest Output
```

### 4.4 Governing Rule

```text
The system is fake internally, but real structurally.
```

The first implementation uses hardcoded outputs, but the interfaces, component boundaries, execution sequence, and test expectations should be realistic.

---

## 5. First-Line Subsystems

```text
PENA Agent
├── 01 Runtime Orchestration
├── 02 Context Management
├── 03 Ingestion
├── 04 Trust and Relevance Scoring
├── 05 LLM Summarization
├── 06 Digest Generation
├── 07 Observability and Logging
├── 08 Learning Extraction
├── 09 Repository Knowledge Base
├── 10 Configuration
├── 11 Developer Toolchain
└── 12 Test Harness
```

---

## 6. Subsystem Breakdown

### 6.1 Runtime Orchestration

Responsible for coordinating the full agent execution.

```text
01 Runtime Orchestration
├── Agent Entry Point
├── Pipeline Controller
├── Step Dispatcher
├── Execution State Manager
├── Error Boundary
└── Final Result Assembler
```

Primary collaborators:

- Configuration
- Ingestion
- Context Management
- Trust and Relevance Scoring
- LLM Summarization
- Digest Generation
- Observability
- Test Harness

Primary interfaces:

- command-line entry point
- internal pipeline call interface
- execution result object
- execution trace event stream

---

### 6.2 Context Management

Responsible for loading and resolving the context that guides the agent.

```text
02 Context Management
├── User Intent Profile Loader
├── Project Context Loader
├── Context Package Resolver
├── Context Prioritizer
├── Context Snapshot Builder
└── Context Validation Reporter
```

Primary collaborators:

- Repository Knowledge Base
- Configuration
- Runtime Orchestration
- Trust and Relevance Scoring
- LLM Summarization

Primary interfaces:

- context package input
- context snapshot output
- context validation report

---

### 6.3 Ingestion

Responsible for receiving and normalizing source material.

```text
03 Ingestion
├── Input Reader
├── Source Adapter
├── Article Parser
├── Metadata Extractor
├── Content Normalizer
├── Duplicate Detector
└── Ingestion Validation Reporter
```

Primary collaborators:

- Runtime Orchestration
- Configuration
- Trust and Relevance Scoring
- Observability

Primary interfaces:

- source input object
- normalized article object
- ingestion event messages
- validation report

---

### 6.4 Trust and Relevance Scoring

Responsible for evaluating whether the input is trustworthy and useful for the user/project intent.

```text
04 Trust and Relevance Scoring
├── Source Trust Evaluator
├── Content Quality Evaluator
├── User Relevance Evaluator
├── Project Relevance Evaluator
├── Score Aggregator
├── Reasoning Explanation Builder
└── Score Validation Reporter
```

Primary collaborators:

- Ingestion
- Context Management
- Repository Knowledge Base
- LLM Summarization
- Observability

Primary interfaces:

- normalized article input
- context snapshot input
- trust score output
- relevance score output
- scoring explanation output

---

### 6.5 LLM Summarization

Responsible for producing a structured summary guided by context and scoring.

```text
05 LLM Summarization
├── Prompt Builder
├── Model Client Adapter
├── Summary Generator
├── Key Insight Extractor
├── User Relevance Explainer
├── Summary Quality Checker
└── Summary Validation Reporter
```

Primary collaborators:

- Context Management
- Trust and Relevance Scoring
- Configuration
- Digest Generation
- Observability

Primary interfaces:

- summarization request
- model response
- structured summary
- summary quality report

Initial stub behavior:

- no real LLM call
- return deterministic hardcoded summary for Golden Path Scenario 001

---

### 6.6 Digest Generation

Responsible for transforming summaries into final user-facing output.

```text
06 Digest Generation
├── Digest Item Builder
├── Digest Formatter
├── Priority Labeler
├── Recommendation Builder
├── Explanation Formatter
├── Output Renderer
└── Digest Validation Reporter
```

Primary collaborators:

- LLM Summarization
- Trust and Relevance Scoring
- Context Management
- Observability
- Test Harness

Primary interfaces:

- structured summary input
- scored article input
- digest item output
- final digest output

---

### 6.7 Observability and Logging

Responsible for making the execution visible and testable.

```text
07 Observability and Logging
├── Execution Logger
├── Step Trace Recorder
├── Input Output Snapshot Recorder
├── Error Logger
├── Metrics Collector
├── Test Evidence Recorder
└── Run Report Builder
```

Primary collaborators:

- all runtime subsystems
- Test Harness

Primary interfaces:

- trace events
- log records
- execution report
- test evidence artifact

---

### 6.8 Learning Extraction

Responsible for identifying reusable insights from processed content.

```text
08 Learning Extraction
├── Learning Signal Detector
├── Concept Extractor
├── Pattern Extractor
├── Action Candidate Extractor
├── Knowledge Update Recommender
└── Learning Validation Reporter
```

Primary collaborators:

- LLM Summarization
- Context Management
- Repository Knowledge Base
- Digest Generation

Primary interfaces:

- summary input
- extracted concept output
- recommended knowledge update output

Initial Golden Path status:

- optional or stubbed as no-op
- can return one hardcoded learning insight

---

### 6.9 Repository Knowledge Base

Responsible for storing project/user knowledge artifacts.

```text
09 Repository Knowledge Base
├── Document Repository Adapter
├── Context Artifact Reader
├── Knowledge Index Reader
├── Provenance Resolver
├── Version Resolver
└── Knowledge Retrieval Reporter
```

Primary collaborators:

- Context Management
- Trust and Relevance Scoring
- Learning Extraction
- Configuration

Primary interfaces:

- document lookup request
- context artifact output
- provenance metadata output

Initial Golden Path status:

- hardcoded repository response

---

### 6.10 Configuration

Responsible for runtime parameters, environment settings, and feature toggles.

```text
10 Configuration
├── Config Loader
├── Environment Resolver
├── Pipeline Mode Resolver
├── Model Settings Resolver
├── Feature Toggle Resolver
└── Config Validation Reporter
```

Primary collaborators:

- Runtime Orchestration
- all subsystems

Primary interfaces:

- configuration file
- environment variables
- runtime config object

Initial Golden Path mode:

```text
pipeline_mode = golden_path_stub_001
```

---

### 6.11 Developer Toolchain

Responsible for local development ergonomics and project execution support.

```text
11 Developer Toolchain
├── Local Run Script
├── Test Runner Script
├── Stub Data Generator
├── Documentation Generator
├── Diagram Renderer
└── Developer Workflow Guide
```

Primary collaborators:

- Test Harness
- Configuration
- Documentation artifacts
- PlantUML diagrams

Primary interfaces:

- shell commands
- Makefile or task runner
- generated artifacts

---

### 6.12 Test Harness

Responsible for verifying that the system behaves as expected.

```text
12 Test Harness
├── Golden Path Test Runner
├── Stub Contract Validator
├── Expected Output Comparator
├── Trace Validator
├── Regression Test Reporter
└── Test Evidence Publisher
```

Primary collaborators:

- Runtime Orchestration
- Digest Generation
- Observability
- Configuration

Primary interfaces:

- test scenario definition
- expected output artifact
- actual output artifact
- test report

---

## 7. Basic Unit Specification Template

Each subsystem and subcomponent should eventually receive a Markdown specification using this template.

```markdown
# Component Name

## 1. Purpose

## 2. Responsibility Boundary

## 3. Parent System

## 4. Subcomponents

## 5. Inputs

## 6. Outputs

## 7. Interfaces

### API Interface

### Message/Event Interface

### File/Artifact Interface

### Configuration Interface

## 8. Collaborators

## 9. Internal Flow

## 10. Data Objects

## 11. Stub Behavior

## 12. Testable Units

## 13. Observability Points

## 14. Open Questions
```

---

## 8. Initial Data Contracts

### 8.1 Source Article

```text
SourceArticle
├── source_id
├── source_name
├── title
├── url
├── author
├── published_at
├── raw_text
└── metadata
```

### 8.2 Normalized Article

```text
NormalizedArticle
├── article_id
├── source
├── title
├── canonical_url
├── normalized_text
├── extracted_metadata
└── ingestion_status
```

### 8.3 Context Snapshot

```text
ContextSnapshot
├── user_profile_id
├── active_intents
├── project_context
├── relevance_keywords
├── trusted_sources
├── blocked_sources
└── timestamp
```

### 8.4 Scored Article

```text
ScoredArticle
├── article_id
├── trust_score
├── relevance_score
├── quality_score
├── aggregate_score
├── score_explanation
└── decision
```

### 8.5 Structured Summary

```text
StructuredSummary
├── article_id
├── short_summary
├── key_points
├── why_it_matters
├── risks_or_caveats
├── user_relevance_explanation
└── summary_quality_status
```

### 8.6 Digest Item

```text
DigestItem
├── digest_item_id
├── title
├── source
├── summary
├── why_relevant
├── recommendation
├── priority
├── trust_score
├── relevance_score
└── source_url
```

### 8.7 Execution Trace

```text
ExecutionTrace
├── run_id
├── scenario_id
├── started_at
├── completed_at
├── steps
├── input_snapshot
├── output_snapshot
├── errors
└── status
```

---

## 9. Golden Path Expected Output

For the first executable test, the final output should resemble this structure.

```text
PENA Digest Result

Scenario:
Golden Path Scenario 001: Curated AI News Digest

Input:
One hardcoded AI-related article.

Decision:
Include in digest.

Reason:
The article is from a trusted source, relates to AI agents, and is relevant to the PENA/SDLC2 project context.

Digest Item:
- Title: [hardcoded article title]
- Summary: [hardcoded summary]
- Why it matters: [hardcoded project relevance explanation]
- Trust score: [hardcoded score]
- Relevance score: [hardcoded score]
- Recommendation: Save for PENA agent architecture research.

Execution:
Completed successfully.

Trace:
All pipeline steps completed.
```

---

## 10. Documentation Set to Generate

```text
docs/lld/step03-system-breakdown-test/
├── pena-system-breakdown-test-00-overview.md
├── pena-system-breakdown-test-01-component-tree.md
├── pena-system-breakdown-test-02-golden-path-use-case-001.md
├── pena-system-breakdown-test-03-executable-stub-contract.md
├── pena-system-breakdown-test-04-data-contracts.md
├── pena-system-breakdown-test-05-runtime-orchestration.md
├── pena-system-breakdown-test-06-context-management.md
├── pena-system-breakdown-test-07-ingestion.md
├── pena-system-breakdown-test-08-trust-relevance-scoring.md
├── pena-system-breakdown-test-09-llm-summarization.md
├── pena-system-breakdown-test-10-digest-generation.md
├── pena-system-breakdown-test-11-observability-logging.md
├── pena-system-breakdown-test-12-learning-extraction.md
├── pena-system-breakdown-test-13-repository-knowledge-base.md
├── pena-system-breakdown-test-14-configuration.md
├── pena-system-breakdown-test-15-developer-toolchain.md
└── pena-system-breakdown-test-16-test-harness.md
```

---

## 11. Generation Sequence

### Phase 1: Stabilize the Concept

Generate:

1. overview
2. component tree
3. golden path use case
4. executable stub contract

Outcome:

- the whole idea becomes conceptually easy to grasp

### Phase 2: Stabilize Interfaces

Generate:

1. data contracts
2. subsystem interfaces
3. collaborator map

Outcome:

- component boundaries become clear

### Phase 3: Stabilize Testability

Generate:

1. golden path test harness spec
2. expected output artifact
3. trace validation rules

Outcome:

- the first executable test becomes precise

### Phase 4: Prepare for Code

Generate:

1. project folder mapping
2. stub component implementation plan
3. test execution plan

Outcome:

- Codex or Copilot can implement the walking skeleton from the specs

---

## 12. Walking Skeleton Principle

The first executable system should not attempt full intelligence.

It should prove structure.

```text
Hardcoded inputs
→ real component boundaries
→ deterministic stub outputs
→ real execution path
→ real test result
```

This creates the first PENA walking skeleton.

---

## 13. Relationship to UML

The UML diagrams remain the architectural map.

This Step 3 documentation translates UML into:

- component responsibilities
- subsystem boundaries
- testable units
- data contracts
- collaboration paths
- executable stub behavior

The flow is:

```text
UML
→ System Breakdown
→ Component Contracts
→ Golden Path Stub
→ End-to-End Test
→ Real Implementation
```

---

## 14. Next Best Action

The next concrete document to generate should be:

```text
pena-system-breakdown-test-01-component-tree.md
```

Then:

```text
pena-system-breakdown-test-02-golden-path-use-case-001.md
```

Then:

```text
pena-system-breakdown-test-03-executable-stub-contract.md
```

These three documents will give the project enough structure to start the first executable stub implementation safely.

---

## 15. Summary

This step converts the PENA Agent from an architectural idea into a decomposed, testable system.

The critical move is the realistic Golden Path Scenario.

The agent will initially be deterministic and hardcoded, but it will already express the real intent of PENA:

```text
Find meaningful information.
Evaluate it against trusted context.
Explain why it matters.
Produce a useful digest.
Make the execution observable.
```

That is the foundation for the first serious PENA end-to-end test.
