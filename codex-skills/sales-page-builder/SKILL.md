---
name: sales-page-builder
description: Create the structure and content plan for a high-clarity digital-product sales page.
---

# Sales Page Builder

## Purpose
Create the structure and content plan for a high-clarity digital-product sales page.

## Trigger when
- build landing page
- sales page
- product page structure

## Required inputs
- positioning
- offer
- proof
- visual assets
- pricing

## Workflow
1. Write hero with outcome + audience + CTA.
2. Explain problem and desired state.
3. Show real product preview/demo.
4. Explain what's included.
5. Translate features into benefits.
6. Add who-it-is-for/use cases.
7. Add genuine proof.
8. Add pricing/tiers.
9. Add FAQ.
10. Repeat CTA.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- page outline
- section copy brief
- visual brief
- CTA map
- proof placement

## Quality checks
- Outcome visible above fold.
- Real previews, not only decorative mockups.
- No fake testimonials.
- Pricing is understandable.

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
