---
name: ml-observability-logging
description: Design structured logs, run events, metrics, traces, and diagnostic artifacts for TensorCheck so long experiment searches can be inspected, resumed, compared, and debugged.
metadata:
  version: "1.0.0"
---

# ML Observability + Logging

## Goal

Make long experiment/search runs explain themselves.

## Structured Events

Record:
- run start/end
- export start/end
- configuration chosen
- execution result
- metrics
- predicate update
- next-experiment decision
- localization action
- artifact path

## Logging Rules

- machine-readable first
- human-readable console second
- no secrets
- do not log full huge tensors by default
- include stable case/run IDs
- preserve traceback and environment for crashes

## Resume

Search state should be serializable so interrupted experiments can continue without repeating expensive runs.
