# Validation Plan

## Purpose

Define what must be true before this repo claims a detection translation is complete.

## Validation Levels

* Level 0: Scaffold exists
* Level 1: Candidate context documented
* Level 2: Sigma rule proposed
* Level 3: SPL/KQL translations drafted
* Level 4: Syntax and field mapping reviewed
* Level 5: Repository-local validation evidence added
* Level 6: Public-safe summary approved

## Current Status

Level 1 pending collaborator contribution.

## Required Evidence Before Claims

Before claiming Sigma rule correctness, the repo needs documented review of the rule logic, field mappings, logsource assumptions, and candidate scope.

Before claiming a Splunk detection works, the repo needs public-safe evidence that the SPL was reviewed against the documented field mapping and validated in an appropriate Splunk context.

Before claiming a Sentinel detection works, the repo needs public-safe evidence that the KQL was reviewed against the documented field mapping and validated in an appropriate Sentinel context.

Before claiming Atomic execution was performed by this repo, the repo needs public-safe execution evidence created for this repo without private data, raw sensitive telemetry, lab IP addresses, or secrets.

Before claiming production readiness, the repo needs evidence beyond this collaboration scaffold, including review of operational fit, deployment assumptions, false positive boundaries, and environment-specific constraints.

None of those claims are currently made.
