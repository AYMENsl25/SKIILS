---
name: digital-product-packager
description: Turn source content into a clean, versioned, distributable digital product bundle.
---

# Digital Product Packager

## Purpose
Turn source content into a clean, versioned, distributable digital product bundle.

## Trigger when
- package product
- make download bundle
- prepare release files
- zip product

## Required inputs
- source assets
- target formats
- license
- version
- platform requirements

## Workflow
1. Define release manifest.
2. Normalize filenames.
3. Build/export target formats.
4. Add README/quick-start.
5. Add license/terms if applicable.
6. Add version metadata.
7. Validate files open/import.
8. Remove temporary/private files.
9. Create final ZIP/package.
10. Generate checksum/manifest if useful.

## Decision rules
- Separate evidence, inference, and assumptions.
- Prefer the smallest action that can answer the current uncertainty.
- Ask for human approval before irreversible external actions when applicable.
- Never fabricate traction, customer quotes, reviews, revenue, or test results.
- When current marketplace/platform facts matter, verify them with current sources.

## Outputs
- release folder
- ZIP
- manifest
- README
- version notes

## Quality checks
- No secrets/private drafts.
- Files open successfully.
- Correct license included.
- Naming is consistent.

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
