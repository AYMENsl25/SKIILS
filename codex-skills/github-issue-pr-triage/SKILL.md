---
name: github-issue-pr-triage
description: Triage GitHub issues and pull requests for TensorCheck or upstream projects by reproducing reports, classifying root-cause areas, identifying duplicates, extracting minimal evidence, and deciding the next action.
metadata:
  version: "1.0.0"
---

# GitHub Issue and PR Triage

## Issue Workflow

1. Restate the observed behavior.
2. Identify expected behavior.
3. Check versions/environment.
4. Determine whether a reproducer exists.
5. Attempt reproduction when practical.
6. Classify:
   - confirmed bug
   - likely bug
   - unsupported configuration
   - user error
   - documentation gap
   - feature request
   - cannot reproduce
7. Search duplicates.
8. Define next evidence needed.

## TensorCheck Tags

Useful categories:
- exporter
- runtime
- dynamic-shape
- precision
- optimization
- predicate-search
- reproducer
- benchmark
- documentation

## PR Review Readiness

Before deep review check:
- tests exist,
- CI status,
- issue linkage,
- scope,
- public API change,
- benchmark/regression evidence.
