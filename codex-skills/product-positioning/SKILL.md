---
name: product-positioning
description: Create a clear market position that states who the product is for, what outcome it creates, and why it is meaningfully different.
---

# Product Positioning

## Purpose
Create a clear market position that states who the product is for, what outcome it creates, and why it is meaningfully different.

## Trigger when
- position product
- value proposition
- differentiate product
- who is this for

## Required inputs
- audience
- problem
- product
- alternatives
- evidence

## Workflow
1. Define primary audience.
2. Define painful current state.
3. Define desired outcome.
4. Name primary alternative.
5. Choose credible differentiation.
6. Write one-sentence positioning statement.
7. Generate message pillars and proof requirements.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- positioning statement
- value proposition
- message pillars
- proof map
- anti-positioning / who it is not for

## Quality checks
- Avoid vague words like 'revolutionary'.
- Differentiation must be defensible.
- No unsupported superlatives.

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
