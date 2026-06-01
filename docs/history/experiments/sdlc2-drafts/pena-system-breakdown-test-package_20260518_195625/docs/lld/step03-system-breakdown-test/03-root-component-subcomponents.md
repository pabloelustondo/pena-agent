# 03 Root Component Subcomponents

## Root Component

```text
PENA Agent
```

## Direct Root-Level Components

```text
PENA Agent
├── Agent Run Facade
├── Agent Runtime
├── Execution Mode Resolver
├── Subsystem Registry
├── Execution Context
├── Runtime Orchestrator
├── Agent Result Assembler
└── Agent Error Boundary
```

## Root Rule

```text
PENA Agent owns the run.
Subsystems own the work.
```

## Root-Level Flow

```text
Agent Run Facade
→ Agent Runtime
→ Execution Mode Resolver
→ Subsystem Registry
→ Execution Context
→ Runtime Orchestrator
→ Agent Result Assembler
→ AgentRunResult
```

## Public Interface

```text
run_golden_path() -> AgentRunResult
```

## Stub Contract

```text
Input: run_golden_path()
Expected Behavior: Execute Golden Path Scenario 001.
Expected Output:
AgentRunResult.status = SUCCESS
AgentRunResult.scenario_id = GP-001
AgentRunResult.validation_result = PASSED
```
