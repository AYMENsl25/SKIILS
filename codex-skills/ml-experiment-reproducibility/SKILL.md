---
name: ml-experiment-reproducibility
description: Make ML and TensorCheck experiments reproducible by controlling seeds, environments, package versions, model artifacts, configuration files, hardware metadata, outputs, and run manifests.
metadata:
  version: "1.0.0"
---

# ML Experiment Reproducibility

## Goal

A different developer should be able to reproduce the result without guessing hidden settings.

## Capture

For every experiment record:
- git commit
- command
- config
- Python version
- package versions
- PyTorch / ONNX / ORT versions
- opset
- execution provider
- optimization level
- dtype
- random seeds
- hardware/OS
- input artifact hash
- model artifact hash
- result metrics

## Rules

- Configuration belongs in structured YAML/JSON/TOML, not scattered constants.
- Do not overwrite prior runs.
- Store machine-readable results.
- Separate generated artifacts from source code.
- Preserve historical bug environments when current versions no longer reproduce them.
- Never claim reproducibility without rerunning from a clean environment.

## Recommended Run Layout

```text
runs/<case>/<timestamp>/
  config.json
  environment.json
  metrics.json
  stdout.log
  artifacts/
```
