# 16 Data Contracts

## Purpose

This document defines initial implementation-independent data contracts for the golden path.

## SourceArticle

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

## NormalizedArticle

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

## ContextSnapshot

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

## ScoredArticle

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

## StructuredSummary

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

## DigestItem

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

## ExecutionTrace

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

## AgentRunResult

```text
AgentRunResult
├── scenario_id
├── status
├── digest
├── scores
├── trace_summary
├── validation_result
└── errors
```
