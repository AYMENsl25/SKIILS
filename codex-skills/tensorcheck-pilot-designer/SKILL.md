---
name: tensorcheck-pilot-designer
description: Design small, falsifiable TensorCheck feasibility pilots and graduation-project experiments. Use when choosing research questions, variables, controls, seeded bugs, real bug cases, sampling budgets, baselines, metrics, or deciding whether the core idea is feasible before building the full system.
metadata:
  version: "1.0.0"
---

# TensorCheck Pilot Designer

## Mission

Design the smallest experiment that can disprove or support the current TensorCheck hypothesis.

The first pilot tests failure-condition discovery, not the full product.

## Preferred Scope

Reference: PyTorch
Target: ONNX Runtime CPU
Representation: ONNX

Initial variables:
- tensor shape
- dtype
- dynamic/static export
- ONNX opset when practical
- ORT optimization level

Avoid GPU/TensorRT/WebGPU/Vision/Quantum unless required.

## Default Pilot Question

> Can a tensor-aware learner recover interpretable trigger conditions for cross-runtime divergence using fewer executions than naive/random sampling?

## Experimental Design

For each case define:
1. ground truth/root cause;
2. search variables;
3. ranges;
4. divergence oracle;
5. execution budget;
6. baselines;
7. learner;
8. active-sampling policy;
9. metrics;
10. seeds/repetitions.

## Use Real + Seeded Bugs

Seeded examples:
- `width % 2 == 1 AND dtype == FP16`
- `batch == 1 AND optimization == ALL`
- `sequence_length % 8 != 0 AND dynamic_shapes == True`

Use real historical issues for external validity.

## Feature Design

Raw:
- rank, dimensions, dtype, numel, batch

Derived:
- dim equals 1
- dim modulo 2/4/8/16/32
- dim equality relations
- cross-input shape relations
- justified thresholds

Prefer meaningful tensor predicates to arbitrary thresholds.

## Baselines

At minimum:
1. random sampling,
2. fixed grid when feasible,
3. shallow tree on raw features,
4. shallow tree on tensor-aware features,
5. TensorCheck active selection.

## Metrics

- predicate precision/recall/F1
- exact/semantic ground-truth recovery
- rule complexity
- executions required
- wall-clock cost
- stability across seeds
- failure-region coverage

## Budget Analysis

Always report:
- total candidate space,
- executed configurations,
- percent explored,
- exports/re-exports,
- average and total runtime.

Cache reusable artifacts.

## Threats to Validity

Discuss:
- seeded vs real bugs,
- historical-version dependence,
- overfitting,
- tolerance calibration,
- feature correlations,
- active-learning bias,
- benchmark representativeness.

## Go / No-Go

Continue only if the pilot shows at least one:
- meaningful rules on real bugs,
- fewer executions than baselines,
- tensor predicates improve quality,
- counterfactual witnesses are useful.
