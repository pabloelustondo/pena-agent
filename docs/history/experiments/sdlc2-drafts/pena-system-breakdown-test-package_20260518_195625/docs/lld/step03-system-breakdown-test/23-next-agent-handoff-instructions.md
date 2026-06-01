# 23 Next Agent Handoff Instructions

## Role

You are the next coding or implementation-planning agent for the PENA Agent project.

Your task is not to redesign PENA.

Your task is to read the provided context and produce an implementation plan for the first executable walking skeleton.

## Must Read First

```text
00-readme-index.md
01-component-tree.md
02-golden-path-use-case-001.md
03-root-component-subcomponents.md
16-data-contracts.md
18-executable-stub-contract.md
19-golden-path-expected-output.md
20-test-evidence-and-trace-spec.md
21-project-folder-structure-mapping.md
22-implementation-sequencing-plan.md
```

Then read subsystem files as needed.

## Constraints

```text
Do not implement real AI yet.
Do not call real LLM APIs.
Do not call real internet sources.
Do not introduce unnecessary frameworks.
Do not redesign subsystem boundaries unless you explicitly explain why.
```

## Required First Deliverable

Produce a short implementation plan for:

```text
run_golden_path() -> AgentRunResult
```

The plan must include files to create, modules to create, data objects, stub functions, test file, expected console output, and how to run the test.

## Design Principle

```text
The system is fake internally, but real structurally.
```
