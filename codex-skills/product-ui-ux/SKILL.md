---
name: product-ui-ux
description: Design or audit the product and product-page user experience for clarity, usability, accessibility, and conversion.
---

# Product Ui Ux

## Purpose
Design or audit the product and product-page user experience for clarity, usability, accessibility, and conversion.

## Trigger when
- UX audit
- design product experience
- product page UX
- improve layout

## Required inputs
- product format
- screens/pages
- audience
- device targets
- brand constraints

## Workflow
1. Map primary user journey.
2. Check information hierarchy.
3. Check first-use/onboarding.
4. Check navigation and findability.
5. Check visual hierarchy, typography, spacing, contrast, and responsive behavior.
6. Check product preview strategy.
7. Check CTA placement and purchase clarity.
8. Document issues by severity and recommendation.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- UX flow
- issues
- recommended hierarchy
- wireframe/content structure
- accessibility checks

## Quality checks
- Prioritize usability before decoration.
- No dark patterns.
- Test mobile where applicable.

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
