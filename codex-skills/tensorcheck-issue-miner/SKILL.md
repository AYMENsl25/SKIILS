---
name: tensorcheck-issue-miner
description: Mine PyTorch, ONNX, ONNX Runtime, TensorRT, and related issue trackers for real cross-runtime mismatch bugs that can become TensorCheck benchmark or pilot cases. Use when building datasets, choosing pilot bugs, validating demand, or creating reproducible benchmark cases.
metadata:
  version: "1.0.0"
---

# TensorCheck Issue Miner

## Mission

Find real deployment/runtime mismatch bugs with enough evidence to become reproducible TensorCheck cases.

Prefer confirmed or fixed issues with known causes over vague reports.

## Search Targets

Prioritize:
- pytorch/pytorch
- onnx/onnx
- microsoft/onnxruntime
- NVIDIA/TensorRT
- relevant exporter/runtime projects

Search for:
- incorrect output
- numerical mismatch
- PyTorch vs ONNX
- ONNX Runtime wrong result
- FP16 mismatch
- optimization changes output
- dynamic shape failure
- resize/interpolate mismatch
- broadcasting mismatch
- batch=1
- odd dimensions
- exporter regression
- execution provider divergence
- model conversion wrong prediction

## Acceptance Criteria

Prefer cases with:
1. model/minimal code;
2. specific source and target runtime;
3. reproducible numerical or semantic mismatch;
4. trigger condition or searchable trigger space;
5. known fix/root cause when possible;
6. versions;
7. public reproducible data;
8. reasonable runtime.

## Extract Schema

```yaml
id:
source_url:
project:
status:
reported_version:
fixed_version:
reference_runtime:
target_runtime:
model_type:
operation_or_region:
input_properties:
deployment_properties:
failure_metric:
known_trigger:
known_root_cause:
minimal_repro_available:
hardware_requirements:
estimated_runtime:
benchmark_value:
notes:
```

## Root-Cause Categories

- shape semantics
- dynamic shapes
- precision
- operator semantics
- interpolation/coordinate conventions
- broadcasting
- train/eval state
- constant folding
- graph optimization
- execution provider
- quantization
- unsupported-op fallback
- numerical stability
- exporter bug
- runtime kernel bug
- unknown

## Diversity Rule

Seek different failure classes and model families. Do not fill the benchmark with variants of one Resize bug.

## Verification

Before accepting:
1. reproduce if practical;
2. pin versions;
3. save expected/actual metrics;
4. ensure the issue is not just poor tolerance selection;
5. record current-version behavior;
6. preserve a historical environment if fixed.

## Output

Rank candidates by:
- pilot suitability,
- benchmark value,
- reproduction difficulty,
- trigger-search value.
