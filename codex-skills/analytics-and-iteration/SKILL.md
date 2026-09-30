---
name: analytics-and-iteration
description: Measure product performance and turn behavior/feedback into prioritized product improvements.
---

# Analytics And Iteration

## Purpose
Measure product performance and turn behavior/feedback into prioritized product improvements.

## Trigger when
- analyze product metrics
- improve conversion
- post launch
- iterate product

## Required inputs
- traffic
- conversion
- sales
- refunds
- activation/use
- reviews
- support feedback

## Workflow
1. Define funnel.
2. Validate data quality.
3. Track acquisition -> product page -> checkout -> delivery -> activation -> retention/refund.
4. Segment where useful.
5. Identify largest drop-offs.
6. Combine quantitative and qualitative evidence.
7. Form hypotheses.
8. Prioritize experiments by impact, confidence, effort.
9. Record outcomes and update product.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- funnel report
- issues
- hypotheses
- experiment backlog
- iteration plan

## Quality checks
- Do not optimize vanity metrics alone.
- Check sample size and tracking quality.
- Record failed experiments too.

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
