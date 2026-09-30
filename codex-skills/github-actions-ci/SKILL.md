---
name: github-actions-ci
description: Design and maintain reliable GitHub Actions CI for Python/ML projects, including test matrices, caching, lint/type checks, integration tests, artifact uploads, and release gates.
metadata:
  version: "1.0.0"
---

# GitHub Actions CI

## Goal

Fast feedback on ordinary changes; deeper checks on merge/release paths.

## Suggested TensorCheck CI

Fast jobs:
- ruff/lint
- formatting check
- type check
- unit tests

Matrix:
- supported Python versions
- selected stable PyTorch/ORT versions when affordable

Separate:
- integration export tests
- historical regression environments
- performance benchmarks
- optional GPU tests

## Rules

- Pin third-party actions to trusted versions/SHAs when appropriate.
- Use least-privilege permissions.
- Cache dependencies safely.
- Avoid downloading huge ML artifacts in every job.
- Upload logs and TensorCheck reports on failure.
- Never put secrets into untrusted PR execution paths.
