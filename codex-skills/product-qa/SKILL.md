---
name: product-qa
description: Run a systematic pre-launch quality gate across content, UX, files, rights, accessibility, and claims.
---

# Product Qa

## Purpose
Run a systematic pre-launch quality gate across content, UX, files, rights, accessibility, and claims.

## Trigger when
- QA product
- prelaunch check
- validate product
- release review

## Required inputs
- release candidate
- source claims
- license
- target platforms

## Workflow
1. Check completeness.
2. Check factual claims.
3. Check links.
4. Check spelling/grammar.
5. Check visual consistency.
6. Check accessibility.
7. Check file integrity.
8. Check device/import compatibility.
9. Check rights/licenses.
10. Check product listing matches delivered files.
11. Log defects and severity.
12. Block release for critical defects.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- QA report
- defect list
- severity
- release status
- retest checklist

## Quality checks
- Critical defects block release.
- Claims must have evidence.
- Delivered files must match advertised contents.

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
