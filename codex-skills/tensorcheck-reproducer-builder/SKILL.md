---
name: tensorcheck-reproducer-builder
description: Turn a TensorCheck mismatch into a minimal, issue-ready reproducible artifact with pinned environment, failing and passing witnesses, reduced inputs/model when useful, and a concise README. Use after a failure condition has been confirmed or when preparing an upstream bug report.
metadata:
  version: "1.0.0"
---

# TensorCheck Reproducer Builder

## Mission

Produce a reproducer a framework/runtime maintainer can run quickly and trust.

Minimization is engineering value, not a novelty claim.

## Preferred Bundle

```text
reproducer/
├── README.md
├── requirements.txt
├── environment.json
├── source_model.py
├── model.onnx
├── failing_input.*
├── passing_input.*
├── expected_output.*
├── actual_output.*
└── run_repro.py
```

## README Requirements

State:
1. problem in one sentence;
2. reference runtime;
3. target runtime;
4. exact environment;
5. one command to reproduce;
6. expected behavior;
7. actual behavior;
8. numerical metrics;
9. trigger condition if known;
10. minimal failing witness;
11. nearest passing witness;
12. suspected cause only if evidence supports it.

## Reduce Three Things

### Input
Shrink batch, dimensions, values, and unnecessary inputs.

### Model
Use existing reducers/extractors when possible.

### Configuration
Remove unnecessary flags/settings until the smallest failing condition remains.

The target is minimizing:
`model x input x configuration`.

## Validation

A reproducer is done when:
- it fails from a clean environment;
- it passes in a known fixed/reference condition if available;
- the mismatch is deterministic enough;
- no secrets/private data are included;
- dependencies are pinned.

## Maintainer-Friendly Target

Prefer:
- under one minute when feasible,
- minimal dependencies,
- one command,
- no notebook requirement,
- tensor-level mismatch.

## Output

Separate:
- confirmed facts,
- trigger condition,
- suspected root cause,
- workaround.
