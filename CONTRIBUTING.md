# Contributing

This repo uses a small public-safe contribution flow.

## Workflow

* Do not push directly to main.
* Use a scoped branch for candidate work.
* First candidate branch: `candidate/T1059-001-powershell-encoded-c2`
* Submit changes through a pull request.
* Keep claims tied to evidence.
* Do not include private, customer, sensitive, or raw telemetry data.
* Do not claim production coverage, live SOC validation, or working detections unless that evidence is present in the repo.

## Detection Content Rules

Detection content should stay scoped to:

* one ATT&CK technique
* one Atomic Red Team candidate
* one Sigma rule
* one Splunk SPL translation
* one Microsoft Sentinel KQL translation
* one validation note
