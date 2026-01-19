# Elastic Stack: The Basics

## Overview
The Elastic Stack (commonly known as the ELK Stack) is a set of open-source tools used for collecting, storing, searching, and visualizing large volumes of data. In a Security Operations Center (SOC), it is widely used as a SIEM solution to monitor logs, detect threats, and investigate incidents.

The Elastic Stack is composed of four main components:
- Elasticsearch
- Logstash
- Kibana
- Beats

---

## Elasticsearch
Elasticsearch is the core component of the Elastic Stack. It is a distributed search and analytics engine designed to store and quickly retrieve large amounts of data.

### SOC Use Case
- Stores security logs (authentication, network, endpoint, etc.)
- Enables fast searching and correlation of events
- Supports threat hunting and forensic investigations

---

## Logstash
Logstash is a data processing pipeline that ingests data from multiple sources, parses it, and sends it to Elasticsearch.

### SOC Use Case
- Normalizes logs from different systems
- Parses raw logs into structured fields
- Helps correlate logs from multiple sources

---

## Beats
Beats are lightweight data shippers installed on endpoints or servers to send data to Logstash or Elasticsearch.

### Common Beats in SOC
- Filebeat: Collects log files
- Winlogbeat: Collects Windows Event Logs
- Packetbeat: Collects network traffic data
- Metricbeat: Collects system metrics

### SOC Use Case
- Collect endpoint and server logs
- Monitor network activity
- Detect suspicious behavior early

---

## Kibana
Kibana is the visualization and dashboarding tool for Elasticsearch data.

### SOC Use Case
- Visualize security events and alerts
- Build dashboards for monitoring threats
- Perform interactive investigations
- Analyze trends and anomalies

---

## Elastic Stack in a SOC Environment
In a SOC, the Elastic Stack is used to:
- Centralize logs from multiple sources
- Detect suspicious or malicious activity
- Investigate alerts and incidents
- Support threat hunting operations

---

## Key Takeaways
- Elasticsearch stores and searches security data
- Logstash processes and normalizes logs
- Beats collect logs from systems and endpoints
- Kibana visualizes and investigates security events
- Elastic Stack functions as a powerful SIEM platform in SOC operations
