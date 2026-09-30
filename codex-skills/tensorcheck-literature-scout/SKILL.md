---
name: tensorcheck-literature-scout
description: Perform rigorous related-work and novelty research for TensorCheck across ML deployment testing, differential testing, compiler/runtime debugging, failure-condition inference, fuzzing, numerical analysis, and configuration debugging. Use before novelty claims, research questions, related-work writing, or major feature decisions.
metadata:
  version: "1.0.0"
---

# TensorCheck Literature Scout

## Mission

Find the closest prior work and identify the smallest defensible research gap.

Search neighboring fields, not only papers that use the same vocabulary as TensorCheck.

## Mandatory Research Axes

Search:
1. PyTorch/ONNX verification.
2. ONNX Runtime numerical and quantization debugging.
3. TensorRT/Polygraphy comparison and reduction.
4. Cross-framework differential testing.
5. DL compiler testing/fuzzing.
6. Failure-condition learning.
7. Configuration debugging.
8. Active/adaptive testing.
9. Floating-point root-cause analysis.
10. Delta debugging and shrinking.
11. Model conversion fault localization/repair.
12. Runtime/export mismatch issue reports.

## Known Neighboring Work to Verify

At minimum check current status and follow-ups for:
- PyTorch ONNX verification
- onnx-diagnostic
- ONNX Runtime quantization debugging
- Polygraphy
- CRADLE
- NNSmith
- TensorScope
- LEMON
- COMET
- Muffin
- TitanFuzz
- Alhazen
- Avicenna / semantic debugging
- BugDoc
- TTrace
- FetaFix
- OODTE
- Herbgrind
- PyTorch accuracy minifier
- Model Explorer

Do not assume the list is complete.

## Search Strategy

Use method-oriented, domain-oriented, and citation-snowballing searches.

For the closest work:
1. inspect references;
2. inspect later citations/follow-ups;
3. inspect authors' newer work;
4. inspect repositories and issues;
5. check whether the method has become a tool.

## Evidence Rules

For every claimed gap:
- cite closest prior work;
- state exactly what it does;
- state exactly what TensorCheck adds;
- mark confidence high/medium/tentative;
- say "I did not find" rather than "does not exist" unless justified.

Never infer novelty from GitHub search alone.

## Required Matrix

| Work | Year | Target | Input generation | Config search | Learns failure conditions | Localizes divergence | Counterfactual validation | Minimization | Limitation vs TensorCheck |

Separate:
- direct competitors,
- methodological neighbors,
- reusable infrastructure.

## Reject Weak Novelty Claims

Reject claims that reduce to:
- compare outputs,
- compare intermediates,
- first bad node,
- graph reduction,
- generic decision tree over configuration.

## Output

### Confirmed overlaps
### Remaining candidate gaps
### Threats to novelty
### What to read next
### Decision: keep / modify / abandon
