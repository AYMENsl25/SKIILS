---
name: offer-builder
description: Convert a useful product into a clear commercial offer with appropriate scope, bonuses, tiers, and risk-reduction elements.
---

# Offer Builder

## Purpose
Convert a useful product into a clear commercial offer with appropriate scope, bonuses, tiers, and risk-reduction elements.

## Trigger when
- build offer
- bundle product
- what should be included
- product tiers

## Required inputs
- core product
- audience
- desired outcome
- pricing context
- delivery format

## Workflow
1. Define core outcome.
2. List only assets that help achieve that outcome.
3. Separate essentials from bonuses.
4. Design tiers only if differences are meaningful.
5. Clarify license, updates, support, prerequisites, and delivery.
6. Create offer stack and comparison table.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- offer stack
- tier structure
- included files
- bonus logic
- support/update terms
- comparison table

## Quality checks
- No filler bonuses.
- Each tier has a distinct customer use case.
- Avoid fake scarcity.

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
