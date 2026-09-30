---
name: pytest-property-testing
description: Design robust Python tests using pytest and property-based testing for TensorCheck, including parity checks, edge cases, fixtures, parameterization, deterministic randomness, regression tests, and Hypothesis-style input generation.
metadata:
  version: "1.0.0"
---

# Pytest + Property Testing

## Goal

Test behavior and invariants rather than implementation details.

## Test Layers

1. Unit tests for pure functions.
2. Contract tests for backend adapters.
3. Integration tests for PyTorch -> ONNX -> ORT.
4. Regression tests for mined real bugs.
5. Property tests for tensor shapes/configurations.

## Principles

- One behavior per test.
- Use Arrange / Act / Assert.
- Prefer parameterization to duplicated tests.
- Seed random generators.
- Mark slow/integration/GPU tests explicitly.
- Keep default CI fast.
- Assert numerical tolerances deliberately; never use arbitrary huge tolerances to make tests pass.

## Property-Based Testing

Good generated dimensions:
- batch: 1, 2, powers of two
- odd/even sizes
- boundary sizes
- divisibility by 2/4/8/16/32
- equal/unequal dimensions

Shrink failing cases and preserve the smallest useful witness.

## ML-Specific Assertions

Check:
- shape
- dtype
- finite values
- max/mean absolute error
- relative error where meaningful
- deterministic metadata
