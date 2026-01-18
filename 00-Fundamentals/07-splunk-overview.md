# Splunk: The Basics — SOC Documentation

> Author: Youssif Samer  
> Role: SOC Analyst (Entry-Level)  
> Platform: TryHackMe — Splunk: The Basics  

---

## Overview

This documentation summarizes the core concepts learned in the **Splunk: The Basics** room on TryHackMe. Splunk is a widely used **Security Information and Event Management (SIEM)** platform that enables Security Operations Center (SOC) analysts to collect, search, analyze, and visualize machine-generated data for security monitoring and incident response.

This document is written for **portfolio and SOC analyst preparation purposes**.

---

## What is Splunk?

Splunk is a data analytics and SIEM platform that ingests logs and events from multiple sources, including:

- Endpoints
- Servers
- Network devices
- Applications
- Security tools

Splunk allows SOC analysts to:
- Detect security threats
- Investigate incidents
- Create alerts and dashboards
- Perform threat hunting

---

## Splunk Architecture (High-Level)

Splunk consists of several core components:

### Forwarder
- Installed on endpoints or servers
- Collects logs and forwards them to the indexer
- Universal Forwarder is commonly used in SOC environments

### Indexer
- Receives data from forwarders
- Parses, indexes, and stores events
- Enables fast and efficient searching

### Search Head
- Used by SOC analysts
- Executes search queries
- Displays dashboards, reports, and alerts

---

## Data in Splunk

### Events
An **event** is a single log entry containing:
- Timestamp
- Source
- Sourcetype
- Raw event data

### Index
An **index** is where Splunk stores data.

Common examples:
- `main`
- `security`
- `windows`

Proper indexing improves performance and investigation efficiency.

---

## Splunk Search Processing Language (SPL)

Splunk uses **Search Processing Language (SPL)** to query data.

### Basic Search Format
index=<index_name> <keyword>

### Example Searches

Search for failed logon attempts:
index=windows EventCode=4625


Search for process creation events:
index=windows EventCode=4688


Search for suspicious command execution:
index=windows whoami


---

## Field Filtering

Splunk automatically extracts useful fields.

Common SOC investigation fields:
- `EventCode`
- `User`
- `Host`
- `Source`
- `NewProcessName`
- `CommandLine`

Example:
index=windows EventCode=4688 NewProcessName=whoami.exe


---

## Time Range Selection

Time filtering helps reduce noise and focus investigations.

Analysts can search:
- Last 15 minutes
- Last 24 hours
- Custom time ranges

This is critical during incident response.

---

## Detection and Alert Logic (SOC Use Case)

Splunk can generate alerts based on defined detection logic.

### Example Detection Rule

If Log Source is WinEventLog
AND EventCode is 4688
AND NewProcessName contains "whoami"
THEN Trigger Alert: WHOAMI Command Execution Detected


### Log Clearing Activity (Suspicious Behavior)
- Windows log clearing activity commonly uses **EventCode 104**
- Indicates potential attacker attempting to hide traces

---

## SOC Investigation Workflow Example

Scenario: Suspicious command execution detected

Steps:
1. Identify affected host
2. Review process creation event
3. Analyze command-line arguments
4. Validate user context
5. Determine verdict:
   - True Positive
   - False Positive
6. Escalate or close alert

---

## Why Splunk Matters in a SOC

Splunk enables:
- Centralized log visibility
- Faster threat detection
- Reduced Mean Time to Detect (MTTD)
- Effective incident investigation

Splunk is one of the **most widely used SIEM tools** in SOC environments.

---

## Conclusion

The **Splunk: The Basics** room provides a strong foundation in SIEM concepts, Splunk architecture, and SPL searching. These skills are essential for SOC analysts to monitor environments, investigate alerts, and respond to security incidents effectively.

This documentation demonstrates practical SOC-level understanding of Splunk.

---

## Skills Demonstrated

- SIEM fundamentals
- Splunk architecture
- SPL searching
- Windows Event Log analysis
- SOC alert investigation mindset
