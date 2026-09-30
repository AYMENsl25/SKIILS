---
name: research-paper-reader
description: Read technical ML/software-testing papers critically for TensorCheck by extracting problem, assumptions, method, evaluation, datasets, baselines, limitations, reproducibility details, and exact overlap with the proposed contribution.
metadata:
  version: "1.0.0"
---

# Research Paper Reader

## Read in Layers

### Pass 1
Capture:
- problem
- contribution
- setting
- headline results

### Pass 2
Extract:
- algorithm
- inputs/outputs
- assumptions
- search space
- oracle
- experimental budget
- baselines

### Pass 3
Audit:
- threats to validity
- missing ablations
- hidden dependencies
- what is actually new
- whether code/data exist

## TensorCheck Comparison

Always answer:
1. Does this work learn failure conditions?
2. Does it vary inputs?
3. Does it vary configuration?
4. Does it combine both?
5. Are predicates interpretable?
6. Is sampling active?
7. Does it localize?
8. Does it validate counterfactuals?
9. Does it minimize/reproduce?
10. What exact gap remains?

Never summarize only the abstract.
