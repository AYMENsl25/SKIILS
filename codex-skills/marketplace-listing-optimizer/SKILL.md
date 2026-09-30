---
name: marketplace-listing-optimizer
description: Adapt a digital product for marketplace discovery and conversion without keyword stuffing or misleading claims.
---

# Marketplace Listing Optimizer

## Purpose
Adapt a digital product for marketplace discovery and conversion without keyword stuffing or misleading claims.

## Trigger when
- Etsy listing
- Notion listing
- marketplace listing
- SEO listing

## Required inputs
- marketplace
- product
- keywords
- audience
- assets
- platform rules

## Workflow
1. Review current platform field/rule requirements.
2. Choose search-intent keywords.
3. Write precise title.
4. Write first lines for fast clarity.
5. Explain included assets and compatibility.
6. Select appropriate category/tags.
7. Plan preview images.
8. Add FAQ/license/format notes.
9. Check for prohibited or misleading claims.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- listing title
- description
- tags/keywords
- image plan
- FAQ
- metadata

## Quality checks
- Platform rules verified current.
- No keyword stuffing.
- No false scarcity/reviews.
- Compatibility is explicit.

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
