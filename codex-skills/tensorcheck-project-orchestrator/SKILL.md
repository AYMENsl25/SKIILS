---
name: tensorcheck-project-orchestrator
description: Coordinate TensorCheck research and engineering work across literature review, issue mining, pilot experiments, PyTorch-ONNX debugging, failure-condition discovery, benchmarking, and reproducibility. Use when a task spans multiple TensorCheck workstreams or when deciding what to do next without losing scope.
metadata:
  version: "1.0.0"
---

# TensorCheck Project Orchestrator

## Mission

Coordinate work on TensorCheck without allowing the project to drift into an unfocused "everything ML" tool.

TensorCheck's current research core is:

> Learn and experimentally validate interpretable failure conditions over the joint space of tensor inputs and deployment configuration for cross-runtime ML divergence.

The preferred initial deployment path is:

`PyTorch -> ONNX -> ONNX Runtime`

Keep Vision, WebGPU, TensorRT, and Quantum as future extensions unless the user explicitly changes scope.

## Priorities

1. Prove the core failure-condition discovery idea.
2. Build a reproducible pilot.
3. Establish baselines and related work.
4. Produce a benchmark and evaluation protocol.
5. Add localization and issue-ready reproduction.
6. Harden architecture.
7. Only then consider large extensions.

## Workflow

1. Classify the task: research, issue mining, pilot, parity debugging, predicate discovery, benchmark, reproduction, or architecture.
2. Identify the smallest deliverable that advances the project.
3. State what evidence is required.
4. Prefer a falsifiable experiment over speculative implementation.
5. Record assumptions and unresolved risks.
6. End with a concrete artifact or next action.

## Guardrails

Do not:
- Claim novelty without a current literature search.
- Reimplement mature PyTorch/ONNX Runtime/Polygraphy/onnx-diagnostic capabilities without a documented reason.
- Treat intermediate-tensor comparison alone as novelty.
- Treat graph reduction alone as novelty.
- Add Quantum/WebGPU/TensorRT/CV to the first pilot without a research need.
- Optimize UI before validating the core method.
- Use top-1 class disagreement as the only parity oracle.

## Decision Rule

If a feature does not improve trigger discovery, interpretability, experiment efficiency, diagnosis confidence, reproducibility, or benchmark quality, defer it.

## Definition of Done

Produce at least one of:
- sourced research conclusion,
- benchmark candidate,
- executable experiment,
- measurable result,
- reproducible failure artifact,
- implementation issue,
- architecture decision.
