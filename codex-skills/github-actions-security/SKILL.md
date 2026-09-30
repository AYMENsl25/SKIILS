---
name: github-actions-security
description: Security-review GitHub Actions workflows for TensorCheck, especially permissions, untrusted PR input, secrets, shell interpolation, artifact handling, dependency pinning, and agentic CI workflows.
metadata:
  version: "1.0.0"
---

# GitHub Actions Security

## Goal

Treat CI YAML as executable code with repository credentials.

## Review

Check:
- event triggers
- `pull_request_target`
- token permissions
- secret exposure
- fork behavior
- `${{ }}` interpolation into shells
- checkout ref
- artifact trust
- cache poisoning
- unpinned actions
- generated scripts
- agent tools running with write permissions

## Reporting

Only report a vulnerability when a concrete attack path is plausible.

For each finding:
- attacker capability
- trigger
- data/control flow
- impact
- remediation
