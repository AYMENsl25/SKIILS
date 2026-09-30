---
name: pytorch-upstream-contributor
description: Guide TensorCheck-related contributions to PyTorch by using current PyTorch contribution practices, issue triage, exporter debugging, test selection, PR review expectations, and official PyTorch Agent Skills where available.
metadata:
  version: "1.0.0"
---

# PyTorch Upstream Contributor

## Goal

Contribute TensorCheck-discovered issues or fixes upstream responsibly.

## Workflow

1. Verify issue on a supported/current PyTorch build when possible.
2. Search existing GitHub issues and PRs.
3. Identify subsystem:
   - torch.onnx / torch.export
   - compiler
   - operator
   - testing
   - docs
4. Use the repository's current contribution instructions.
5. Prefer official PyTorch Agent Skills when they directly cover the task.
6. Add the smallest regression test.
7. Avoid broad refactors in bugfix PRs.
8. Follow maintainer feedback precisely.

## Evidence

For ONNX mismatch reports include:
- source model/reproducer
- export call/options
- opset
- expected PyTorch tensor
- ORT tensor
- numerical metrics
- version/commit
- minimal failing input
- known passing counterfactual

Do not claim an exporter bug until reference semantics are understood.
