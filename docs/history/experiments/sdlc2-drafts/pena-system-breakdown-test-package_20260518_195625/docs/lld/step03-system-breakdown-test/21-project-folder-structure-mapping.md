# 21 Project Folder Structure Mapping

## Suggested Structure

```text
pena-agent/
├── README.md
├── docs/
│   └── lld/
│       └── step03-system-breakdown-test/
├── src/
│   └── pena_agent/
│       ├── __init__.py
│       ├── main.py
│       ├── runtime/
│       ├── config/
│       ├── ingestion/
│       ├── context/
│       ├── scoring/
│       ├── summarization/
│       ├── digest/
│       ├── observability/
│       ├── learning/
│       ├── repository/
│       └── testing/
├── tests/
│   ├── test_golden_path.py
│   ├── test_contracts.py
│   └── fixtures/
└── scripts/
    ├── run_golden_path.sh
    └── test_golden_path.sh
```

## Initial Bias

Use a simple Python package first. Avoid frameworks until the walking skeleton runs.
