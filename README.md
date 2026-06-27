# Atomic Sigma Crosswalk

This repository is a minimal public-safe collaboration lab for documenting one small detection translation path:

Atomic Red Team-style telemetry -> Sigma rule -> Splunk SPL -> Microsoft Sentinel KQL -> validation notes.

## Purpose

The purpose is to preserve a clear, reviewable translation workflow for one future collaborator-provided candidate. It is not a production detection package and does not claim coverage of any enterprise environment.

## Collaboration Roles

- Raylee: repo scaffold, public-safe documentation boundaries, translation notes.
- Bobby: first ATT&CK / Atomic candidate and telemetry context.

## Proof Boundary

This repo is scaffold-only until a collaborator provides a candidate and supporting telemetry context.

The repo does not claim:

- production readiness
- live SOC validation
- enterprise coverage
- completed detection engineering
- successful Atomic test execution
- working Splunk or Sentinel detections
- correctness of any Sigma rule

No private, customer, or sensitive data belongs in this repository.

## Current Status

Awaiting first ATT&CK / Atomic candidate from collaborator.

## Documentation

* [Workflow](docs/workflow.md)
* [Validation Plan](docs/validation-plan.md)
* [Field Mapping](docs/field-mapping.md)
* [Public Safety](docs/public-safety.md)

## License

This project is licensed under the MIT License.
