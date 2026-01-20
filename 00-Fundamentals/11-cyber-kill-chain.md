# Cyber Kill Chain

## Overview
The Cyber Kill Chain is a framework developed to describe the stages of a cyber attack from initial reconnaissance to achieving objectives. It helps SOC analysts understand attacker behavior and identify opportunities to detect and disrupt attacks at different stages.

---

## Objective
Understand each stage of the Cyber Kill Chain and how defenders can detect, prevent, or disrupt attacker activity.

---

## Stages of the Cyber Kill Chain

### Reconnaissance
**Description:**
The attacker gathers information about the target, such as IP ranges, domains, employees, and technologies.

**SOC Detection Opportunities:**
- Suspicious scanning activity
- Unusual DNS requests
- OSINT monitoring

---

### Weaponization
**Description:**
The attacker creates a malicious payload by combining malware with an exploit.

**SOC Detection Opportunities:**
- Limited direct visibility
- Threat intelligence correlation
- Malware research and tracking

---

### Delivery
**Description:**
The attacker delivers the payload to the victim.

Examples:
- Phishing emails
- Malicious attachments
- Drive-by downloads

**SOC Detection Opportunities:**
- Email security alerts
- Web proxy logs
- Attachment analysis

---

### Exploitation
**Description:**
The malicious code is executed by exploiting a vulnerability.

**SOC Detection Opportunities:**
- Endpoint alerts
- Application crash logs
- Exploit behavior monitoring

---

### Installation
**Description:**
The attacker installs malware to maintain persistence.

**SOC Detection Opportunities:**
- Persistence mechanisms
- Registry changes
- Scheduled tasks or services

---

### Command and Control (C2)
**Description:**
The compromised system communicates with attacker infrastructure.

**SOC Detection Opportunities:**
- Suspicious outbound traffic
- Beaconing behavior
- Abnormal DNS or HTTP patterns

---

### Actions on Objectives
**Description:**
The attacker achieves their goal.

Examples:
- Data exfiltration
- Privilege escalation
- Lateral movement

**SOC Detection Opportunities:**
- Unusual data transfers
- Access to sensitive systems
- Privilege abuse detection

---

## Breaking the Kill Chain
Stopping an attack at **any stage** can prevent full compromise.

SOC teams aim to:
- Detect early stages to reduce impact
- Use layered security controls
- Correlate alerts across stages

---

## SOC Analyst Perspective
- Early detection reduces damage
- Visibility across endpoints, network, and logs is critical
- Kill Chain analysis improves incident response decisions
- Helps analysts explain attacks clearly to stakeholders

---

## Relationship to Other Frameworks
- Complements MITRE ATT&CK
- Provides a linear view of attacks
- Useful for explaining incidents and building detections

---

## Conclusion
The Cyber Kill Chain provides a structured way to understand, detect, and disrupt cyber attacks. SOC analysts use it to identify attacker progress and respond effectively before objectives are achieved.
