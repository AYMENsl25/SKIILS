---
name: performance-profiling
description: Profile TensorCheck and ML-debugging workloads for CPU time, wall time, memory, export cost, runtime executions, and algorithmic bottlenecks before optimizing.
metadata:
  version: "1.0.0"
---

# Performance Profiling

## Rule

Measure before optimizing.

## TensorCheck Cost Model

Track separately:
- export time
- model load/session creation
- inference time
- feature extraction
- learner fit
- active-selection overhead
- localization
- report generation

## Profile

Use appropriate tools for:
- wall-clock timing
- Python CPU profiling
- memory snapshots
- PyTorch profiler where framework work dominates

## Optimization Priorities

1. Reduce unnecessary model executions.
2. Cache safe reusable exports/sessions.
3. Batch experiments when semantics permit.
4. Avoid materializing giant intermediate tensors unnecessarily.
5. Optimize Python only after execution count is under control.

Always preserve correctness tests while optimizing.
