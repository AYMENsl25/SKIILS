---
name: tensorcheck-architecture-guardian
description: Review TensorCheck implementation plans and code architecture for modularity, scope control, testability, reuse of mature tooling, and future backend extensibility. Use before major refactors, new backends, new dependencies, CLI redesigns, or when agents are about to overengineer the project.
metadata:
  version: "1.0.0"
---

# TensorCheck Architecture Guardian

## Mission

Keep TensorCheck small enough to finish and modular enough to grow.

## Separate Responsibilities

1. execution
2. comparison/oracles
3. feature extraction
4. experiment selection
5. predicate learning
6. interventions
7. localization adapters
8. reproduction/reporting

Do not put everything in one CLI flow.

## Suggested Modules

```text
tensorcheck/
├── backends/
├── compare/
├── features/
├── search/
├── predicates/
├── interventions/
├── localization/
├── reproduce/
├── reports/
└── cli/
```

## Backend Contract

Backends should expose only needed capabilities:
- prepare/load model
- run
- metadata
- optional intermediate capture

Use capability checks instead of forcing all backends to support everything.

## Reuse Rule

Before implementing a low-level feature ask:
1. does PyTorch provide it?
2. does ONNX Runtime provide it?
3. does onnx-diagnostic provide it?
4. does Polygraphy provide it?
5. can we wrap the mature tool?

Prefer adapters.

## Dependency Rule

Add a dependency only if it removes real complexity, is maintained, license-compatible, and does not make core unnecessarily heavy.

Put integrations behind optional extras.

## Scope

Core:
- PyTorch
- ONNX
- ONNX Runtime CPU
- joint input/config discovery
- active sampling
- counterfactual validation
- benchmark/reproducer

Future:
- TensorRT
- WebGPU/WASM
- CV
- Quantum

## Code Quality

Require:
- typed public APIs
- deterministic tests
- small pure feature/metric functions
- benchmark fixtures
- no hidden global state
- structured result objects
- JSON output in addition to CLI display

## Review Output

For each proposal:
- problem solved
- core vs optional
- existing tool to reuse
- API boundary
- data-model change
- tests
- risks
- decision: accept / simplify / defer / reject
