---
name: customer-problem-discovery
description: Define the real customer problem before defining the product.
---

# Customer Problem Discovery

## Purpose
Define the real customer problem before defining the product.

## Trigger when
- what problem should we solve
- define customer pain
- customer discovery
- product problem

## Required inputs
- audience
- context
- existing observations

## Workflow
1. Describe the customer's job-to-be-done.
2. Map current workflow and friction.
3. Identify triggers, constraints, alternatives, and consequences.
4. Separate stated wants from underlying jobs.
5. Write problem statements and rank by evidence strength.
6. Propose cheap validation tests.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- JTBD
- problem statements
- current workflow
- pain points
- constraints
- validation tests

## Quality checks
- Problem before solution.
- Evidence strength included.
- No invented customer quotes.

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
