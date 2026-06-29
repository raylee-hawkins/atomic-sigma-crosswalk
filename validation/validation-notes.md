# Validation Notes

## Candidate

Candidate 001 covers T1059.001 encoded PowerShell process creation with a
higher-confidence Sysmon EID 3 correlation expectation.

## Telemetry Source

Pending.

## Expected Behavior

Process-only matches are investigate tier. Matches correlated with Sysmon
EID 3 network activity by ProcessGuid within 300 seconds are signal
candidate tier until validation is completed.

## Observed Fields

Pending.

## Sigma Mapping

Bobby submitted the Sigma process-creation candidate. Repository-local
validation is pending.

## Splunk Translation Notes

Raylee drafted the Splunk SPL with placeholder index and sourcetype
mapping comments. Repository-local Splunk validation is pending.

## Sentinel Translation Notes

Bobby drafted the Sentinel KQL process-creation translation. Sentinel
table naming is connector-dependent, and live Sentinel validation is
pending.

## Validation Result

Pending. No validation has been completed or claimed.

## Known Limits

No repository-local Atomic test execution, Splunk validation, Sentinel
validation, or production readiness is claimed.

## Public-Safe Claim

A draft Candidate 001 branch exists with collaborator-submitted Sigma/KQL
content, Raylee's Splunk draft, and public-safe translation notes.
