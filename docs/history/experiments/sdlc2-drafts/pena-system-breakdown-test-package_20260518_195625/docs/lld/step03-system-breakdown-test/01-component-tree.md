# 01 Component Tree

## Root

```text
PENA Agent
```

## Root Purpose

The PENA Agent transforms selected information into a trusted, relevant, contextualized digest for the user.

## First-Line Subsystems

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

## Golden Path Execution View

```text
PENA Agent
└── Runtime Orchestration
    ├── Configuration
    ├── Ingestion
    ├── Context Management
    ├── Trust and Relevance Scoring
    ├── LLM Summarization
    ├── Digest Generation
    ├── Observability and Logging
    └── Test Harness
```

## Component Specification Rule

Each component spec must answer:

```text
1. What is this component responsible for?
2. What is it not responsible for?
3. What inputs does it receive?
4. What outputs does it produce?
5. Which collaborators does it call or depend on?
6. How can it be stubbed and tested independently?
```
