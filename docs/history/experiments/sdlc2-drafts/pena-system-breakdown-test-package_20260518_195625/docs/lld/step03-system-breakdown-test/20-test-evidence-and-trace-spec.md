# 20 Test Evidence and Trace Specification

## Required Trace Events

```text
CONFIG_LOADED
SOURCE_INGESTED
CONTEXT_RESOLVED
SCORING_COMPLETED
SUMMARY_GENERATED
DIGEST_GENERATED
TRACE_RECORDED
VALIDATION_COMPLETED
RESULT_ASSEMBLED
```

## Trace Event Contract

```text
TraceEvent
├── run_id
├── scenario_id
├── step_name
├── status
├── timestamp
├── input_ref
├── output_ref
└── message
```

## Test Evidence Bundle

```text
TestEvidenceBundle
├── actual_agent_result
├── expected_agent_result
├── execution_trace
├── validation_report
└── comparison_result
```

## Validation Rule

The test passes only if all required trace events exist, all required output fields exist, expected values match actual values, and no fatal errors exist.
