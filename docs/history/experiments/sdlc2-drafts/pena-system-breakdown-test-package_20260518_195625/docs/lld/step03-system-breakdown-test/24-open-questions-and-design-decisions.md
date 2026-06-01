# 24 Open Questions and Design Decisions

## Accepted Design Decisions

```text
1. The first implementation will be deterministic.
2. The first implementation will use hardcoded data.
3. The first implementation will not call real LLMs.
4. The first implementation will not use external systems.
5. The first implementation will be a walking skeleton.
6. The first test must represent real PENA intent.
```

## Open Questions

```text
1. Should data contracts be Python dataclasses, Pydantic models, or simple dictionaries first?
2. Should the first console output be plain text only, JSON only, or both?
3. Should trace events be stored in memory, written to file, or both?
4. Should the package use pytest immediately?
5. Should the first implementation include CLI arguments or only run_golden_path()?
6. Should Learning Extraction be active in GP-001 or stubbed as no-op?
```

## Suggested Answers

```text
1. Use dataclasses or simple dictionaries.
2. Provide both object result and readable console output.
3. Store trace in memory first, optionally write JSON later.
4. Use pytest if convenient.
5. Expose only run_golden_path() first.
6. Return one hardcoded learning insight.
```
