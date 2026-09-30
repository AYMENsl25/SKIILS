---
name: llm-council
description: Run a structured multi-perspective decision process for high-impact product choices.
---

# Llm Council

## Purpose
Run a structured multi-perspective decision process for high-impact product choices.

## Trigger when
- use council
- LLM council
- have agents decide
- multi-agent decision

## Required inputs
- decision question
- constraints
- evidence packet
- candidate options

## Workflow
1. Create independent roles: research, product strategy, UX, marketing, technical, risk/QA.
2. Have each role analyze using the same evidence.
3. Require assumptions and uncertainty.
4. Aggregate agreements/disagreements.
5. Resolve with explicit decision criteria.
6. Return chosen path plus dissent and conditions that would change the decision.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- role analyses
- agreement map
- dissent
- decision rationale
- reversal conditions

## Quality checks
- Do not let one role see another's conclusion before independent analysis when possible.
- Council opinion is not evidence.
- Use external facts separately.

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
