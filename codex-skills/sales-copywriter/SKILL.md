---
name: sales-copywriter
description: Write outcome-focused product copy that is clear, specific, credible, and consistent with the product's evidence.
---

# Sales Copywriter

## Purpose
Write outcome-focused product copy that is clear, specific, credible, and consistent with the product's evidence.

## Trigger when
- write sales copy
- product description
- headline
- CTA
- landing copy

## Required inputs
- positioning
- audience language
- offer
- proof
- tone

## Workflow
1. Extract customer problem and desired outcome.
2. Choose one primary promise.
3. Write headline/subheadline.
4. Write benefit-led sections.
5. Convert features to outcomes.
6. Use specificity and proof.
7. Remove hype and unsupported claims.
8. Produce CTA and FAQ language.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- headline options
- subheadline
- benefit copy
- product description
- CTA
- FAQ copy

## Quality checks
- No fabricated proof.
- No guaranteed outcomes.
- Avoid generic AI phrasing.
- Keep vocabulary aligned with customer language.

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
