---
name: open-source-contributor
description: Prepare high-quality contributions to upstream ML/open-source projects by selecting suitable issues, reproducing bugs, communicating scope, implementing minimal changes, testing, and responding to maintainer review.
metadata:
  version: "1.0.0"
---

# Open Source Contributor

## Goal

Make maintainers' work easier.

## Before Coding

1. Read contribution guide.
2. Search existing issues/PRs.
3. Reproduce the behavior.
4. Confirm desired direction for large changes.
5. Identify smallest acceptable patch.

## PR Quality

Include:
- linked issue
- minimal explanation
- tests that fail before/fix after
- compatibility notes
- benchmark if performance-sensitive
- no unrelated cleanup

## TensorCheck Opportunity

When TensorCheck finds a real upstream bug:
- create issue-ready reproducer,
- verify current main branch,
- file a high-quality report,
- offer a targeted fix only when root cause is understood.

Never use mass low-value PRs to inflate contribution counts.
