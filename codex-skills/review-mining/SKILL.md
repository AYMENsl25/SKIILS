---
name: review-mining
description: Turn customer reviews and discussions into structured needs, complaints, desired outcomes, and language patterns.
---

# Review Mining

## Purpose
Turn customer reviews and discussions into structured needs, complaints, desired outcomes, and language patterns.

## Trigger when
- analyze reviews
- what customers complain about
- review mining
- customer language

## Required inputs
- review sources
- product/category
- customer segment

## Workflow
1. Collect a representative set of reviews where permitted.
2. Tag comments into desired outcomes, frustrations, confusion, praise, missing features, switching reasons, and vocabulary.
3. Count recurring themes when the sample permits.
4. Preserve representative short phrases without overquoting.
5. Convert themes into product hypotheses.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- theme map
- top pains
- top desired outcomes
- buyer vocabulary
- product opportunities

## Quality checks
- Do not treat a few reviews as population-level truth.
- Distinguish frequent from memorable comments.
- Avoid exposing private personal data.

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
