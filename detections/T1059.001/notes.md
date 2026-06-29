# Translation Notes: T1059.001 Encoded PowerShell C2 Correlation

## Sigma Rule Summary
Detects encoded PowerShell execution via Sysmon EID 1 process creation.
Full signal confidence requires a corresponding EID 3 network connection
sharing the same ProcessGuid within 300 seconds. The Sigma rule covers
the process creation side only. Cross-source correlation is enforced at
the pipeline level in Signal Proof, not at the rule level.

## Field Mapping

| Sigma Field | Splunk SPL Field | Sentinel KQL Field | Notes |
|---|---|---|---|
| Image | Image | Image | Consistent across both |
| CommandLine | CommandLine | CommandLine | Consistent across both |
| ProcessGuid | ProcessGuid | ProcessGuid | Critical join field |
| ParentImage | ParentImage | ParentImage | Consistent across both |
| User | User | User | Consistent across both |

## Translation Gaps

### Splunk
To be documented by Raylee after SPL build and tuning.

### Sentinel KQL
SysmonEvent table name may vary depending on connector configuration.
Some environments ingest Sysmon via SecurityEvent table instead.

Performance gap: Original translation used endswith and contains chained with or operators. Replaced with has_any() following peer review.
has_any() is vectorized and significantly more efficient at enterprise scale.

Fidelity gap: Standalone EID 1 match on encoded PowerShell is low fidelity in isolation. Encoded PowerShell fires frequently from legitimate tooling in enterprise environments. The three-item filter list is insufficient to suppress noise at scale without the EID 3 network correlation anchor.
Full signal confidence requires a corresponding Sysmon EID 3 network connection event sharing the same ProcessGuid within 300 seconds.
Standalone EID 1 match is INVESTIGATE tier only.

KQL translation peer reviewed externally. Live Sentinel validation pending workspace access.

## Validation Status

| Artifact | Status |
|---|---|
| Sigma rule | Validated against Atomic Red Team T1059.001 corpus |
| Splunk SPL | Pending Raylee review and tuning |
| Sentinel KQL | Written, untested, pending live validation |
| Notes | In progress |