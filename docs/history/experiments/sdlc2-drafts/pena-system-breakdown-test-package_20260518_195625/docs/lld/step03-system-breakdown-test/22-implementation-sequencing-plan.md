# 22 Implementation Sequencing Plan

## Phase 1: Structural Stub

```text
1. Create folder structure.
2. Create data contract classes or dictionaries.
3. Implement run_golden_path().
4. Implement subsystem stubs.
5. Implement execution trace.
6. Implement expected output comparison.
7. Add one end-to-end test.
```

## Phase 2: Replace One Stub at a Time

```text
1. Config Loader
2. Input Reader
3. Content Normalizer
4. Context Snapshot Builder
5. Score Aggregator
6. Digest Formatter
7. Trace Validator
8. Summary Generator with real LLM call
```

## Rule

Never replace more than one major stub at a time without a passing golden path test.
