---
name: python-production-engineer
description: Write, refactor, and review modern production-quality Python for TensorCheck and related ML tooling. Use for APIs, modules, typing, error handling, project structure, dependency boundaries, refactors, and maintainability decisions.
metadata:
  version: "1.0.0"
---

# Python Production Engineer

## Goal

Produce clear, typed, testable Python that is easy to change.

## Defaults

- Target modern supported Python.
- Prefer standard library before adding dependencies.
- Use type hints on public APIs.
- Prefer dataclasses or small typed objects for structured results.
- Keep pure logic separate from I/O and framework calls.
- Raise specific exceptions with actionable messages.
- Avoid hidden global state.
- Make randomness explicit through seeds or RNG objects.
- Keep functions small enough to test independently.

## TensorCheck Rules

Separate:
- backend execution,
- metrics,
- feature extraction,
- experiment search,
- predicate learning,
- reporting.

Do not allow PyTorch/ONNX Runtime imports to leak into unrelated core modules when adapters can isolate them.

## Review Checklist

- API is minimal and typed.
- Inputs/outputs are explicit.
- Errors preserve useful context.
- Files/classes have one main responsibility.
- No unnecessary abstraction.
- Tests can exercise behavior without external services.
- Expensive framework initialization is not repeated unnecessarily.
