---
name: tensorcheck-benchmark-evaluator
description: Build and evaluate TensorCheck benchmarks against existing tools and baselines using real and seeded cross-runtime bugs. Use when designing thesis evaluation, measuring research claims, running ablations, comparing active search to random/grid sampling, or reporting results.
metadata:
  version: "1.0.0"
---

# TensorCheck Benchmark Evaluator

## Mission

Make TensorCheck claims measurable and falsifiable.

## Benchmark Composition

Use:
- real public bugs with known/fixed causes when possible;
- controlled seeded bugs with exact triggers.

Maintain diversity across:
- shape/dynamic shape
- precision
- operator semantics
- broadcasting
- optimization
- execution provider
- exporter behavior
- numerical stability

## Baselines

For trigger discovery:
- random sampling
- fixed grid
- shallow tree on raw features
- generic config-debug baseline if reproducible
- tensor-aware features without active search
- TensorCheck active search

For localization:
- first divergent intermediate
- PyTorch/ONNX verification
- onnx-diagnostic/equivalent
- TensorCheck orchestration if it adds value

Never use strawman baselines.

## Metrics

### Predicate learning
- precision/recall/F1
- support
- rule complexity
- semantic ground-truth recovery
- seed stability

### Search efficiency
- executions
- wall-clock time
- exports/re-exports
- percent of space explored

### Localization
- top-1/top-k accuracy
- false attribution
- overhead

### Reproducer
- model reduction
- input reduction
- config reduction
- reproduction reliability

## Ablations

Test:
- tensor-derived predicates
- active sampling
- counterfactual validation
- configuration features
- value-statistic features

## Research Integrity

Do not:
- tune on the test set;
- hide unexplained cases;
- count variants of one root cause as independent;
- claim broad industry generality from toy bugs.

## Output

1. Benchmark
2. Baselines
3. RQs
4. Metrics
5. Results
6. Ablations
7. Failure analysis
8. Threats to validity
9. Reproduction instructions
