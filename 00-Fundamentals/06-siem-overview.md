# SIEM Overview – SOC Fundamentals Documentation

## Introduction

Security Information and Event Management (SIEM) is a core technology used in a Security Operations Center (SOC). SIEM platforms collect, normalize, correlate, and analyze logs from multiple sources to detect security threats, generate alerts, and support incident response.

This documentation demonstrates foundational understanding of SIEM concepts, detection logic, and SOC analyst workflows based on hands-on learning and simulations.

---

## What is SIEM?

A SIEM solution aggregates logs and security events from across an organization, including endpoints, servers, network devices, and security tools. It applies correlation rules and analytics to identify suspicious or malicious activity.

### Key Functions of SIEM

- Centralized log collection
- Real-time alerting
- Correlation of events from multiple sources
- Incident investigation and reporting
- Compliance and audit support

---

## Common Log Sources

SIEM tools ingest data from various sources, such as:

- Windows Event Logs (WinEventLog)
- Linux system logs
- Firewalls and IDS/IPS
- Endpoint Detection and Response (EDR)
- Authentication services (Active Directory)
- Email security systems

---

## Important Windows Event Codes

Some commonly monitored Windows Event IDs include:

- **4688** – Process Creation
- **4624** – Successful Logon
- **4625** – Failed Logon
- **1102** – Audit Log Cleared

These events are critical for detecting attacker activity during different phases of an attack.

---

## Example SIEM Detection Rule – Command Execution (whoami)

SIEM platforms use detection rules to identify suspicious behavior based on defined conditions.

### Detection Logic

If the following conditions are met:

- **Log Source:** WinEventLog  
- **EventCode:** 4688 (Process Creation)  
- **NewProcessName:** Contains `whoami`

### Rule Outcome

➡️ **Trigger Alert:**  
**WHOAMI Command Execution DETECTED**

### Why This Rule is Important

- The `whoami` command is frequently used during reconnaissance
- Helps attackers determine current user privileges
- Commonly observed during early compromise stages

### SOC Analyst Response

1. Identify the affected host and user
2. Validate whether execution was legitimate
3. Review parent and child processes
4. Search for additional reconnaissance commands
5. Escalate if malicious behavior is confirmed

---

## Detection of Log Clearing Activity

Clearing logs is a common attacker technique used to hide evidence after a system compromise. SIEM tools can detect this behavior by monitoring event logs and network indicators.

### Log Clearing Indicator

- **Port:** 104  
  This port may be associated with attempts to clear or manipulate logs, depending on the method or tool used.

### Why This Matters

- Indicates post-exploitation activity
- Suggests attacker intent to cover tracks
- High-risk behavior requiring immediate attention

### SOC Analyst Action

- Identify the user and host responsible
- Confirm whether the action was authorized
- Analyze activity before and after the event
- Escalate if malicious intent is confirmed

---

## Alert Lifecycle in SIEM

A typical SIEM alert follows these stages:

1. Alert generation
2. Analyst triage
3. Investigation and enrichment
4. Classification (True Positive / False Positive)
5. Escalation or closure
6. Documentation and reporting

Proper handling ensures efficient SOC operations and reduced alert fatigue.

---

## SIEM vs Traditional Log Management

| Feature | SIEM | Log Management |
|------|------|---------------|
| Real-time alerting | Yes | No |
| Correlation rules | Yes | No |
| Incident investigation | Yes | Limited |
| Compliance reporting | Yes | Partial |

---

## MITRE ATT&CK Mapping

SIEM detections are commonly aligned with the MITRE ATT&CK framework:

- **T1087 – Account Discovery**
- **T1059 – Command and Scripting Interpreter**
- **T1070 – Indicator Removal on Host**
- **Tactic:** Discovery, Defense Evasion

Mapping detections improves threat visibility and SOC maturity.

---

## Conclusion

SIEM is a foundational SOC technology that enables analysts to detect, investigate, and respond to security incidents efficiently. Understanding detection logic, event codes, and attacker behavior is essential for effective SOC operations.

This documentation reflects practical SIEM knowledge gained through hands-on learning and SOC-focused training.

---

*Created as part of my SOC learning journey using TryHackMe and foundational cybersecurity coursework.*
