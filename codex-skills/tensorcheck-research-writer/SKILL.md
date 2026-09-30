---
name: tensorcheck-research-writer
description: Turn TensorCheck experiments and literature findings into defensible research writing for a graduation thesis, proposal, related-work section, methodology, results, and limitations. Use after evidence exists; do not use to manufacture novelty or results.
metadata:
  version: "1.0.0"
---

# TensorCheck Research Writer

## Mission

Write precise research text that separates prior work, proposed contribution, measured result, and speculation.

## Contribution Wording

Prefer:

> We investigate whether tensor-aware active testing can infer interpretable failure predicates over the joint input and deployment-configuration space of cross-runtime ML models.

Avoid "first ever", "revolutionary", or "solves deployment bugs" unless rigorously supported.

## Related Work

Organize by problem:
1. differential testing
2. failure-condition learning
3. DL compiler/runtime fuzzing
4. numerical localization
5. configuration debugging
6. model conversion debugging
7. minimization/reproduction

For each cluster:
- summarize capability;
- identify closest work;
- state TensorCheck's difference.

## Method Section

Specify:
- reference/target runtimes
- tensor/config search space
- divergence oracle
- predicate generation
- learner
- active experiment policy
- counterfactual validation
- localization adapter
- benchmark
- metrics

## Results Discipline

Report:
- baselines
- per-case + aggregate results
- seeds/variance
- execution budgets
- failures/timeouts
- ablations

Do not turn correlation into causal language unless interventions support it.

## Limitations

Consider:
- few real bugs
- historical versions
- search cost
- incomplete predicate vocabulary
- tolerance selection
- graph fusion
- backend-specific behavior
- limited generalization

## Final Check

1. Is every novelty claim grounded?
2. Are methods reproducible?
3. Are results separated from hypotheses?
4. Are threats explicit?
5. Would a skeptical reviewer understand exactly what TensorCheck adds?
