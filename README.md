# SOC Detection Lab

Hands-on security operations lab for practicing log analysis, detection logic, alert triage, and incident documentation using Windows security events and SIEM-style queries.

## What this project demonstrates

- Security monitoring fundamentals
- Windows event log analysis
- Detection engineering concepts
- Brute-force and failed-login detection
- Suspicious PowerShell activity detection
- Alert triage and incident documentation
- MITRE ATT&CK mapping
- SIEM query development

## Detection scenarios

### 1. Repeated failed logons

Detect multiple failed Windows logons from the same account or source within a short time window. This scenario can help identify password guessing or brute-force activity.

### 2. Suspicious PowerShell execution

Identify PowerShell command lines containing potentially risky behavior such as encoded commands, download activity, or execution-policy bypass attempts.

### 3. Privileged account activity

Review administrative account events and authentication activity to identify unexpected or unusual privileged access.

## Repository structure

```text
SOC-Detection-Lab/
├── README.md
├── detections/
│   ├── failed-logons.kql
│   └── suspicious-powershell.kql
├── incidents/
│   └── sample-incident-report.md
└── docs/
    └── detection-notes.md
```

## Investigation workflow

1. Review the alert and associated event data.
2. Identify the account, host, source, timestamp, and event type.
3. Determine whether the activity is expected or suspicious.
4. Review related events around the same time window.
5. Map the behavior to a relevant MITRE ATT&CK technique when appropriate.
6. Document findings, severity, evidence, and recommended remediation.

## Important note

The detections and incident examples in this repository use generic or sanitized lab data. They are intended for portfolio and learning purposes and do not contain employer or production information.
