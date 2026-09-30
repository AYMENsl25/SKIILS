---
name: tensorcheck-parity-debugger
description: Debug numerical and semantic parity failures between PyTorch, exported ONNX, and ONNX Runtime while leveraging existing verification/localization tools instead of reimplementing them. Use when outputs differ across runtimes, export succeeds but predictions change, or a benchmark case needs localization.
metadata:
  version: "1.0.0"
---

# TensorCheck Parity Debugger

## Mission

Establish whether a mismatch is real, characterize it precisely, and localize it with minimal custom machinery.

## Debug Order

### 1. Freeze environment
Record Python, PyTorch, ONNX, ONNX Runtime, opset, exporter options, ORT providers, optimization level, dtype, device, train/eval state, and seeds.

### 2. Compare final tensors
Check shape, dtype, finite values, max/mean absolute error, relative error, RMSE, and cosine similarity when meaningful.

Do not rely only on predicted labels.

### 3. Establish a noise floor
Use repeated/reference executions where appropriate.
Use FP64 only when semantically appropriate; it is not universal ground truth.

### 4. Separate pipeline stages
Where possible compare:
- original PyTorch
- raw ONNX
- ORT optimization disabled
- increasing optimization levels
- execution providers

### 5. Reuse mature tooling
Prefer PyTorch ONNX verification, onnx-diagnostic, ORT tools, and Polygraphy where relevant.

### 6. Separate introduced vs propagated error
Feed clean/reference inputs into suspicious nodes/subgraphs when tooling permits.

### 7. Map to source
Use exporter metadata/stack traces/module hierarchy.
Never assume 1:1 correspondence after optimization/fusion.

## Diagnostic Categories

- operator semantics
- interpolation/coordinate convention
- shape inference
- dynamic shapes
- broadcasting
- train/eval
- precision
- constant folding
- optimization pass
- execution provider
- quantization
- fallback
- fusion
- layout/stride

## Evidence Standard

A diagnosis must be supported by interventions or local replay, not merely node-type correlation.

## Output

### Failure summary
### Triggering configuration
### Localization
### Evidence
### Alternative explanations
### Next most-informative experiment
