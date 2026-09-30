---
name: ml-benchmark-runner
description: Execute ML/TensorCheck benchmark suites reliably with warmups, repeated runs, environment capture, isolation, timeouts, structured outputs, caching rules, and artifact preservation.
metadata:
  version: "1.0.0"
---

# ML Benchmark Runner

## Goal

Make benchmark execution trustworthy and rerunnable.

## Before Run

- freeze config
- capture environment
- verify model/input hashes
- create unique output directory
- set seeds
- define timeout
- determine cache policy

## Timing

Separate:
- export
- session setup
- inference
- analysis/search overhead

Use warmups for runtime timing where appropriate.

## Failures

Record separately:
- numerical divergence
- runtime crash
- timeout
- unsupported configuration
- export failure

Do not silently drop failed configurations.

## Output

Write machine-readable JSON/CSV plus human-readable summary.
