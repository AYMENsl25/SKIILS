---
name: onnx-runtime-contributor
description: Prepare issues and contributions for ONNX Runtime arising from TensorCheck findings, including optimization-level isolation, execution-provider differences, minimal ONNX models, numerical evidence, and regression tests.
metadata:
  version: "1.0.0"
---

# ONNX Runtime Contributor

## Goal

Convert TensorCheck findings into maintainable ORT issues or patches.

## Debug Before Filing

Compare:
- optimization disabled
- basic
- extended
- all
where supported.

Record:
- ORT version
- provider
- model opset
- input dtype/shape
- CPU vs alternate provider if relevant

## Reproducer

Prefer:
- minimal ONNX model
- generated input
- one Python script
- expected vs actual tensor metrics

## Classification

Determine whether likely:
- graph optimizer
- shape inference
- execution provider
- kernel
- quantization
- fallback
- unsupported semantics

Do not attach huge production models when a reduced graph reproduces the problem.
