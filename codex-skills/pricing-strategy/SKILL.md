---
name: pricing-strategy
description: Develop a testable pricing model using market references, perceived value, costs, positioning, and willingness-to-pay evidence.
---

# Pricing Strategy

## Purpose
Develop a testable pricing model using market references, perceived value, costs, positioning, and willingness-to-pay evidence.

## Trigger when
- price this product
- pricing tiers
- how much should we charge

## Required inputs
- product
- audience
- competitor pricing
- costs
- positioning
- sales channel

## Workflow
1. Identify comparable price anchors.
2. Estimate customer value and switching friction.
3. Account for fees/costs/taxes where relevant.
4. Choose pricing model: one-time, subscription, usage, tiered, PWYW, etc.
5. Define test range rather than false precision.
6. Define metrics for price experiments.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- pricing model
- price hypotheses
- tier prices/ranges
- experiment plan
- guardrail metrics

## Quality checks
- Avoid claiming optimal price from competitor prices alone.
- Use ranges when evidence is weak.
- Consider refund/conversion effects.

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
