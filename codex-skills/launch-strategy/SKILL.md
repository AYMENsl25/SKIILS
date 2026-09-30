---
name: launch-strategy
description: Create a channel-specific launch plan that reaches the intended audience and produces measurable learning.
---

# Launch Strategy

## Purpose
Create a channel-specific launch plan that reaches the intended audience and produces measurable learning.

## Trigger when
- launch plan
- go to market
- how should we launch
- product launch

## Required inputs
- product
- audience
- channels
- assets
- budget
- launch date/window

## Workflow
1. Set launch objective.
2. Choose primary audience/channel.
3. Prepare product page and previews.
4. Plan prelaunch content/lead capture where useful.
5. Create launch messages by channel.
6. Define launch calendar.
7. Define metrics and thresholds.
8. Prepare support/refund/feedback flow.
9. Run post-launch review.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- launch plan
- channel plan
- content calendar
- asset checklist
- metrics

## Quality checks
- Do not spread across too many channels.
- Define one primary CTA.
- Separate vanity metrics from business metrics.

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
