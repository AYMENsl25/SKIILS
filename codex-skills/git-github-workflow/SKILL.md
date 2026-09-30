---
name: git-github-workflow
description: Manage disciplined Git and GitHub workflows for TensorCheck: branches, commits, diffs, pull requests, merge preparation, changelog-worthy changes, and safe repository hygiene.
metadata:
  version: "1.0.0"
---

# Git + GitHub Workflow

## Goal

Create small, reviewable changes with traceable intent.

## Workflow

1. Understand current branch and working tree.
2. Create a narrowly scoped branch.
3. Make one coherent change at a time.
4. Run relevant tests and linting.
5. Review the diff before commit.
6. Write an imperative commit subject describing behavior.
7. Keep PRs focused.
8. Include testing evidence in the PR body.

## Commit Guidance

Good:
`Add tensor shape predicate extraction`

Weak:
`updates`

## PR Body

Include:
- problem
- approach
- alternatives/tradeoffs
- tests
- benchmark impact if relevant
- screenshots/report examples if UI/output changed
- follow-ups intentionally deferred

Never mix large formatting refactors with behavior changes unless required.
