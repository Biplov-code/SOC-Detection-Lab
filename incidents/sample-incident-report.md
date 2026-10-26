# Sample Incident Report — Repeated Failed Logons

## Summary

A detection identified repeated Windows failed-logon events associated with a single account within a short period. The activity was reviewed as a possible password-guessing scenario.

## Evidence reviewed

- Windows Security Event ID 4625
- Account name
- Source IP address
- Affected computer
- First and last observed timestamps
- Total failed-attempt count

## Triage steps

1. Confirm whether the account owner expected the authentication attempts.
2. Review successful logons around the same time window.
3. Check whether the source IP is known or expected.
4. Determine whether additional accounts show similar activity.
5. Review the endpoint for related suspicious events.

## Assessment

Example classification: **Medium severity / requires validation**.

Repeated failed authentication can result from user error, stale credentials, misconfigured services, or malicious password guessing. Context is required before escalation.

## Recommended response

- Reset credentials if compromise is suspected.
- Review MFA status and account protections.
- Temporarily disable or restrict the account if risk is high.
- Investigate the source host/IP and related authentication events.
- Document findings and close or escalate based on evidence.

## MITRE ATT&CK

Potential mapping: **T1110 — Brute Force**.

> This report is a sanitized lab example and does not represent a real employer incident.
