---
name: competitor-analysis
description: Compare alternatives in a structured way to find differentiation opportunities.
---

# Competitor Analysis

## Purpose
Compare alternatives in a structured way to find differentiation opportunities.

## Trigger when
- compare competitors
- competitor analysis
- what are alternatives
- how can we differentiate

## Required inputs
- competitor list or category
- target customer
- intended product

## Workflow
1. Collect each competitor's audience, promise, format, price, included assets, proof, UX, distribution, and complaints.
2. Normalize comparisons.
3. Identify table-stakes vs differentiators.
4. Find underserved use cases and overused claims.
5. Recommend positioning hypotheses, not unsupported superiority claims.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- comparison matrix
- table-stakes
- differentiators
- gaps
- positioning hypotheses

## Quality checks
- Use same comparison dimensions.
- Avoid unfair comparisons.
- Note missing data.

## Handoff rules
- Hand off to `llm-council` when the choice is high impact and reasonable expert perspectives conflict.
- Hand off to `product-qa` before a commercial release.
- Hand off to `analytics-and-iteration` after launch when performance data exists.

## Failure modes to avoid
- Building before defining the customer problem.
- Treating competitor popularity as proof of profitability.
- Copying competitor creative or proprietary content.
- Producing generic advice without a decision or artifact.
- Hiding uncertainty.
- Optimizing presentation while the product itself has weak value.

## Evaluation cases
1. Can the skill state what evidence is missing?
2. Can it distinguish facts from assumptions?
3. Does it produce a concrete output, not just commentary?
4. Does it preserve user constraints?
5. Does it avoid unsupported claims?
