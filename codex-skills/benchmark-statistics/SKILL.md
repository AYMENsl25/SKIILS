---
name: benchmark-statistics
description: Design and analyze TensorCheck benchmark results with appropriate descriptive statistics, confidence intervals, repeated seeds, paired comparisons, effect sizes, plots, and cautious interpretation.
metadata:
  version: "1.0.0"
---

# Benchmark Statistics

## Goal

Make evaluation conclusions proportional to the evidence.

## For Stochastic Methods

Run multiple seeds and report:
- mean/median
- standard deviation or IQR
- confidence intervals when justified
- per-case results

## Comparisons

Prefer paired comparisons when the same benchmark cases are run by both methods.

Report effect size and raw values, not only p-values.

## Small Benchmarks

When real bug count is small:
- show each case,
- avoid sweeping generalization,
- separate seeded and real cases,
- use bootstrap/nonparametric summaries carefully.

## Plots

Useful:
- executions-to-discovery
- precision/recall per case
- rule complexity
- runtime breakdown
- cumulative success vs budget

Never hide failures/timeouts from aggregate plots.
