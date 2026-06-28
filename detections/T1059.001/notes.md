# Translation Notes: T1059.001 Encoded PowerShell Candidate

## Sigma Rule Summary
Bobby's Sigma candidate detects encoded PowerShell execution via Sysmon
EID 1 process creation. Full signal confidence requires a corresponding
EID 3 network connection sharing the same ProcessGuid within 300 seconds.
The Sigma rule covers the process-creation side only. Cross-source
correlation is represented in candidate notes and the Splunk draft, not
completed repo-local validation.

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
Raylee drafted an initial SPL translation with:

- process-only matches classified as investigate tier
- EID 1 plus EID 3 ProcessGuid correlation within 300 seconds classified
  as signal candidate tier
- placeholder index and sourcetype comments only

Repository-local Splunk validation is pending.

### Sentinel KQL
Bobby drafted the Sentinel KQL process-creation translation. SysmonEvent
table naming may vary depending on connector configuration; some
environments ingest Sysmon through SecurityEvent instead. The current KQL
does not implement the full EID 3 correlation. Live Sentinel validation is
pending unless repo evidence is added later.

## Validation Status

| Artifact | Status |
|---|---|
| Bobby Sigma | Submitted; process-creation side of the candidate |
| Bobby Sentinel KQL | Drafted; process-creation translation; live validation pending |
| Raylee Splunk SPL | Drafted; validation pending |
| EID 3 correlation | Represented in candidate correlation notes and Splunk draft; validation pending |
| Public-safe claim | Draft cross-platform translation artifacts exist; validation is not complete |
