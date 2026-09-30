---
name: code-review-quality
description: Perform focused software code review for correctness, maintainability, numerical reliability, testing, performance, and API design. Use on TensorCheck PRs and implementation diffs.
metadata:
  version: "1.0.0"
---

# Code Review Quality

## Priority

Review in this order:
1. correctness
2. numerical correctness
3. data loss/security
4. tests
5. API compatibility
6. performance
7. maintainability
8. style

## TensorCheck-Specific Checks

- Same input really reaches both runtimes.
- Train/eval state is controlled.
- Dtypes/shapes are recorded.
- Error thresholds are justified.
- Randomness is seeded.
- Search code does not leak evaluation labels.
- Cached exports are invalidated correctly.
- Failed configurations are distinguished from runtime crashes.
- Structured results are returned, not only printed.

## Finding Format

Severity + location + behavior + evidence + suggested fix.

Do not fill review with style nits that formatters can handle.
