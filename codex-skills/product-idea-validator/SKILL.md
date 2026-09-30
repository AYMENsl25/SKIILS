---
name: product-idea-validator
description: Test whether a product idea deserves to be built and define the smallest useful validation experiment.
---

# Product Idea Validator

## Purpose
Test whether a product idea deserves to be built and define the smallest useful validation experiment.

## Trigger when
- validate this idea
- should we build
- MVP
- test product idea

## Required inputs
- idea
- audience
- problem evidence
- competitive context
- constraints

## Workflow
1. Check problem strength.
2. Check audience specificity.
3. Check alternatives and differentiation.
4. Check willingness-to-pay evidence if available.
5. Estimate build complexity.
6. Identify riskiest assumptions.
7. Design MVP or smoke test.
8. Define pass/fail learning criteria.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- assumption map
- risk ranking
- MVP definition
- validation experiment
- decision evidence needed

## Quality checks
- Do not declare guaranteed success.
- Keep MVP minimal.
- Test riskiest assumption first.

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
