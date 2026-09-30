---
name: dependency-license-security-audit
description: Review proposed Python/Node dependencies for maintenance, license compatibility, security, supply-chain risk, transitive weight, and whether the dependency is justified for TensorCheck.
metadata:
  version: "1.0.0"
---

# Dependency, License, and Supply-Chain Audit

## Before Adding a Dependency

Check:
- what problem it solves
- standard-library alternative
- maintenance activity
- release cadence
- license
- known vulnerabilities
- transitive dependency size
- install scripts/native binaries
- supported Python/platform versions

## TensorCheck Preference

Core dependencies should be minimal.

Heavy framework/runtime integrations should be optional where possible.

## Security

Never trust:
- arbitrary install scripts
- downloaded binaries
- unknown skill scripts
- dependencies that request credentials for unrelated purposes

Record why each major dependency exists.
