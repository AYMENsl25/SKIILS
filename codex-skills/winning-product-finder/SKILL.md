---
name: winning-product-finder
description: Find high-traction or strongly presented digital products and extract reusable patterns without copying proprietary content.
---

# Winning Product Finder

## Purpose
Find high-traction or strongly presented digital products and extract reusable patterns without copying proprietary content.

## Trigger when
- find winning products
- best digital products
- successful examples
- top products
- benchmark products

## Required inputs
- category
- platforms
- target customer
- price band

## Workflow
1. Define what 'winning' means for this task: ratings, reviews, adds, rankings, public revenue, launch traction, or design quality.
2. Search for products with observable traction signals.
3. Capture product positioning, offer structure, presentation pattern, pricing, proof, and packaging.
4. Do not equate reviews/popularity with verified revenue.
5. Synthesize repeated patterns and white-space opportunities.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- benchmark table
- traction signal
- presentation pattern
- offer structure
- lessons to reuse
- gaps

## Quality checks
- No fabricated revenue.
- No copying full descriptions/designs.
- Cite the signal used to classify each benchmark.

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
