---
name: python-packaging-release
description: Package and release TensorCheck as a modern Python project using pyproject.toml, optional extras, semantic versions, build validation, PyPI/TestPyPI workflows, changelogs, and backward-compatible public APIs.
metadata:
  version: "1.0.0"
---

# Python Packaging + Release

## Goal

Make installation predictable and keep optional integrations lightweight.

## Packaging

Use `pyproject.toml`.

Prefer extras:
- `tensorcheck[dev]`
- future `tensorcheck[vision]`
- future `tensorcheck[web]`
- future `tensorcheck[quantum]`

Do not force heavy optional runtimes into the core dependency set.

## Release Gate

Before release:
- unit/integration tests pass
- clean build
- install wheel in fresh env
- import smoke test
- CLI smoke test
- changelog/release notes
- version updated once
- public API changes documented

## Versioning

Use semantic intent:
- patch: compatible bugfix
- minor: compatible feature
- major: breaking API

Pre-1.0 may evolve faster, but document breaking changes.
