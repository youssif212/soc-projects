\# Endpoint Detection and Response (EDR) – SOC Documentation



\## Overview



Endpoint Detection and Response (EDR) is a critical security solution used by Security Operations Centers (SOC) to monitor, detect, investigate, and respond to threats at the endpoint level. Endpoints include workstations, servers, and other devices that connect to an organization's network.



EDR solutions go beyond traditional antivirus by providing continuous visibility, detailed telemetry, behavioral detection, and active response capabilities.







---



\## Why EDR Is Important in a SOC



Traditional antivirus solutions rely mainly on signature-based detection, which can miss modern and unknown threats. EDR addresses this gap by:



\- Continuously monitoring endpoint activity

\- Detecting suspicious behavior rather than known signatures

\- Enabling rapid investigation and response

\- Providing historical data for threat hunting and incident response



EDR plays a key role in identifying advanced threats such as ransomware, credential dumping, and lateral movement.



---



\## EDR Architecture (High-Level)



An EDR solution typically consists of the following components:



\### 1. Endpoint Agent

\- Installed on endpoints (servers, workstations)

\- Collects detailed telemetry such as:

&nbsp; - Process execution

&nbsp; - File activity

&nbsp; - Network connections

&nbsp; - Registry changes

&nbsp; - User activity



\### 2. Central Management Platform

\- Receives telemetry from endpoint agents

\- Correlates events and applies detection logic

\- Generates alerts and detections

\- Provides investigation and response interfaces for SOC analysts



---



\## Telemetry Collected by EDR



EDR solutions provide deep visibility into endpoint behavior, including:



\- Process creation and parent-child relationships

\- Command-line arguments

\- File creation, modification, and deletion

\- Network connections (IP addresses, ports, domains)

\- User and privilege context

\- Persistence mechanisms



This telemetry allows SOC analysts to reconstruct attacker activity and understand the full attack chain.



---



\## Detection Capabilities



EDR solutions detect threats using behavioral and heuristic techniques such as:



\- Suspicious process behavior

\- Abuse of legitimate system tools (LOLBins)

\- Privilege escalation attempts

\- Lateral movement indicators

\- Malicious script execution



Unlike antivirus, EDR can detect \*\*unknown or fileless attacks\*\* based on behavior rather than signatures.



---



\## Response Capabilities



EDR provides powerful response actions that SOC analysts can use during investigations, including:



\- Isolating an endpoint from the network

\- Terminating malicious processes

\- Quarantining or deleting files

\- Collecting forensic artifacts

\- Executing remote commands for investigation



These actions help contain threats quickly and reduce potential impact.



---



\## Investigating Alerts in EDR



During the module, investigations were performed on simulated EDR detections. A typical SOC investigation using EDR includes:



1\. Reviewing the alert details and severity

2\. Analyzing process trees and execution flow

3\. Examining command-line arguments and file activity

4\. Identifying the root cause of the detection

5\. Determining whether the activity is malicious or benign

6\. Taking appropriate response actions if required



---



\## EDR vs Traditional Antivirus



| Feature | Antivirus | EDR |

|------|---------|-----|

| Detection Method | Signature-based | Behavioral \& telemetry-based |

| Visibility | Limited | Deep endpoint visibility |

| Threat Hunting | Not supported | Supported |

| Incident Response | Minimal | Advanced response actions |

| Historical Data | Limited | Extensive |



---





## **Career Application**
This knowledge directly applies to SOC analyst responsibilities:
- **Triage:** Quickly assess EDR alerts using behavioral indicators
- **Investigation:** Use EDR telemetry to trace attack chains
- **Response:** Execute containment actions via EDR platform
- **Improvement:** Provide feedback to tune EDR detection rules

## **Next Steps for Learning**
- Hands-on with commercial EDR platforms (CrowdStrike, SentinelOne)
- Practice with open-source EDR alternatives (Wazuh, Osquery)
- Deep dive into MITRE ATT&CK framework mapping

\## Conclusion



Endpoint Detection and Response (EDR) is a foundational tool for modern SOC operations. It provides the visibility, detection, and response capabilities required to detect advanced threats and respond effectively to incidents.



Completing the \*Introduction to EDR\* module established a strong baseline for working with endpoint security solutions and prepared me for deeper SOC investigations involving malware analysis, incident response, and threat hunting.



---

