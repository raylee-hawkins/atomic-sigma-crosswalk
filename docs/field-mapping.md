# Field Mapping

## Candidate Context

T1059.001 PowerShell encoded command execution followed by outbound network connection in a controlled lab context.

Technique: T1059.001 PowerShell

Telemetry source: Sysmon Event ID 1 and Sysmon Event ID 3

Join key: ProcessGuid

## Sysmon Process Creation

Fields to map later:

* UtcTime / TimeCreated
* Computer / host
* User
* Image
* CommandLine
* ParentImage
* ParentCommandLine
* ProcessGuid
* ProcessId

## Sysmon Network Connection

Fields to map later:

* UtcTime / TimeCreated
* Computer / host
* User
* Image
* ProcessGuid
* ProcessId
* DestinationIp
* DestinationHostname
* DestinationPort
* Protocol

## Translation Notes

Do not hardcode index, sourcetype, table names, or lab IPs until repo evidence supports them.

## Open Questions

* Exact Sigma logsource
* Exact Splunk sourcetype
* Exact Sentinel table
* Field normalization assumptions
* False positive boundaries
