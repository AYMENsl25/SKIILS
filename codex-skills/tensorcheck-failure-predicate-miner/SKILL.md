---
name: tensorcheck-failure-predicate-miner
description: Discover interpretable conditions that predict when a user's ML model diverges across runtimes by searching tensor-input and deployment-configuration space, learning compact predicates, and validating them with counterfactual experiments. Use for TensorCheck's core research task.
metadata:
  version: "1.0.0"
---

# TensorCheck Failure Predicate Miner

## Mission

Turn passing/failing executions into an interpretable, validated rule such as:

`batch == 1 AND width % 2 == 1 AND dtype == FP16`

Optimize for developer-understandable conditions, not just classifier accuracy.

## Features

### Tensor features
- rank
- dimensions
- dtype
- numel
- layout/contiguity/strides when relevant
- selected value statistics when justified

### Derived predicates
- `dim_i == 1`
- divisibility by 2/4/8/16/32
- `dim_i == dim_j`
- relationships across input tensors
- batch/sequence predicates

Avoid huge arbitrary threshold sets by default.

### Deployment features
- ONNX opset
- exporter mode
- dynamic/static shapes
- precision
- ORT optimization level
- execution provider
- relevant flags

### Labels
- PASS
- DIVERGENCE
- CRASH
plus continuous error metrics.

## Initial Learner

Start with interpretable models:
- shallow decision tree
- rule list
- Boolean predicates

Keep complexity small.

## Active Search

1. collect diverse initial samples;
2. fit a compact rule;
3. locate uncertain boundaries/interactions;
4. choose a high-information experiment;
5. run it;
6. update the rule;
7. stop when stable or budget exhausted.

## Counterfactual Validation

Challenge every final rule.

Example:

```text
Fail:
width=255, FP16, OPT_ALL

Counterfactual 1:
width=256, FP16, OPT_ALL -> PASS

Counterfactual 2:
width=255, FP32, OPT_ALL -> PASS

Counterfactual 3:
width=255, FP16, OPT_BASIC -> PASS
```

## Avoid Spurious Rules

Use held-out configurations and multiple seeds where practical. Check whether rules proxy tensor size, cached exports, seeds, or unsupported conditions.

## Metrics

- precision
- recall
- F1
- support
- rule length
- seed stability
- executions required
- exact/semantic ground-truth recovery

## Output

### Learned rule
### Confidence/support
### Passing/failing witnesses
### Counterfactual evidence
### Unknown search region
### Next best experiment
