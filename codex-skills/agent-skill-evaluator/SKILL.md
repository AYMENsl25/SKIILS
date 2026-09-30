---
name: agent-skill-evaluator
description: Evaluate whether an Agent Skill actually improves agent performance using controlled with-skill vs without-skill tasks, blind scoring rubrics, regression tasks, token-cost tracking, and failure analysis.
metadata:
  version: "1.0.0"
---

# Agent Skill Evaluator

## Goal

Do not assume a skill is useful because its prompt sounds good.

## Evaluation Design

For each skill:
1. define 5-20 realistic tasks;
2. define an objective rubric;
3. run baseline without skill;
4. run with skill;
5. randomize/blind outputs for judging when possible;
6. compare quality and token/time cost;
7. inspect regressions.

## Metrics

- task success
- rubric score
- critical-error rate
- consistency
- unnecessary verbosity
- tokens/context loaded
- tool-call efficiency

## TensorCheck Pack

Especially evaluate whether skills:
- reduce novelty overclaiming,
- improve benchmark design,
- produce better issue reproducers,
- keep architecture in scope.

Retain, rewrite, or delete skills based on measured value.
