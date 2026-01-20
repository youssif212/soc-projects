# Pyramid of Pain

## Overview
The Pyramid of Pain is a security concept that categorizes indicators of compromise (IOCs) based on how difficult they are for attackers to change. The higher the indicator is on the pyramid, the more pain it causes the attacker when defenders detect and block it.

This model helps SOC analysts prioritize detections that have long-term defensive value.

---

## Objective
Understand how different types of indicators impact attacker operations and how defenders should prioritize detections in a SOC environment.

---

## Levels of the Pyramid

### Hash Values
Examples:
- MD5
- SHA-1
- SHA-256

**Description:**
Hashes uniquely identify files such as malware samples.

**SOC Perspective:**
- Very easy for attackers to change
- Minor modifications generate new hashes
- Useful only for known malware

**Defensive Value:** Low

---

### IP Addresses
Examples:
- Command and Control (C2) server IPs
- Malicious source IPs

**SOC Perspective:**
- Attackers can rotate or replace IPs quickly
- Shared infrastructure may cause false positives
- Useful for short-term blocking

**Defensive Value:** Low–Medium

---

### Domain Names
Examples:
- Malicious domains
- Phishing domains

**SOC Perspective:**
- Harder to change than IPs but still disposable
- Domain generation algorithms (DGA) reduce effectiveness
- Requires monitoring DNS activity

**Defensive Value:** Medium

---

### Network Artifacts
Examples:
- User-Agent strings
- URI patterns
- C2 traffic patterns

**SOC Perspective:**
- More difficult for attackers to modify
- Useful for behavioral detections
- Effective for network-based monitoring

**Defensive Value:** Medium–High

---

### Tools
Examples:
- Mimikatz
- Metasploit
- Cobalt Strike

**SOC Perspective:**
- Tools are reused across campaigns
- Detection forces attackers to retool
- Increases attacker cost and complexity

**Defensive Value:** High

---

### Tactics, Techniques, and Procedures (TTPs)
Examples:
- Credential dumping
- Lateral movement techniques
- Persistence mechanisms

**SOC Perspective:**
- Hardest for attackers to change
- Focuses on behavior rather than indicators
- Most reliable detection strategy

**Defensive Value:** Very High

---

## SOC Analyst Takeaway
- Low-level indicators are useful for quick blocking
- High-level indicators provide long-term protection
- SOC detections should focus on behavior and techniques
- TTP-based detections reduce alert fatigue and increase attacker disruption

---

## Conclusion
The Pyramid of Pain demonstrates that not all indicators are equal. SOC analysts should prioritize detections that force attackers to change how they operate, not just what infrastructure they use.
