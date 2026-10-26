# Detection Notes

## Failed logons

**Event ID:** 4625  
**Goal:** identify repeated failed authentication attempts that may indicate password guessing or brute-force behavior.

### Tuning ideas

- Increase the threshold for noisy service accounts.
- Exclude known scanners or test systems.
- Group by user, host, and source IP.
- Correlate with successful logon events after repeated failures.

## Suspicious PowerShell

**Event ID:** 4688 when process creation auditing is enabled  
**Goal:** surface PowerShell executions containing potentially risky command-line patterns.

### Example indicators

- Encoded commands
- Execution policy bypass
- Download activity
- Invoke-Expression usage
- Suspicious web requests

### Tuning ideas

- Exclude approved administrative scripts.
- Add known-good automation accounts.
- Review parent/child processes where telemetry is available.
- Correlate PowerShell activity with network connections and authentication events.

## Detection philosophy

A detection is not automatically an incident. Alerts should be validated with context, related events, account behavior, host activity, and expected administrative workflows before escalation.
