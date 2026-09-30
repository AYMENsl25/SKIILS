---
name: market-research
description: Research market demand, category behavior, competitors, pricing, trends, and distribution channels before product decisions are made.
---

# Market Research

## Purpose
Research market demand, category behavior, competitors, pricing, trends, and distribution channels before product decisions are made.

## Trigger when
- research this market
- is there demand
- what sells in this category
- market opportunity
- digital product research

## Required inputs
- product/category idea
- target customer
- geography if relevant
- platform constraints
- budget/time constraints

## Workflow
1. Define the decision the research must support.
2. Break the market into customer, problem, alternatives, pricing, channels, and evidence.
3. Search primary marketplace/platform sources plus credible secondary evidence.
4. Separate observable facts from inference.
5. Identify recurring demand signals and saturation risks.
6. Return opportunities, risks, unknowns, and next experiments.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- market map
- demand signals
- competitor set
- pricing observations
- channel options
- gaps/hypotheses
- research confidence

## Quality checks
- No claim of profitability without evidence.
- Use dated/current sources for trend claims.
- Distinguish popularity from revenue.
- Include contrary evidence.

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
