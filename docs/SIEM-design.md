# 📐 SIEM System Design

## 1. Objective

Design a centralized system to collect, parse, analyze, and detect cybersecurity events from various sources in a simulated enterprise network.

## 2. Architecture Diagram

![SIEM Architecture](architecture.png)

## 3. Components

| Component      | Description |
|----------------|-------------|
| Elasticsearch  | Stores and indexes log data |
| Logstash       | Parses and enriches incoming logs |
| Kibana         | Visualizes and monitors events |
| Filebeat       | Shipper agent for endpoint logs |
| pfSense        | Firewall providing network logs |
| Suricata       | IDS/IPS for network-based attack detection |
| Client (Win/Linux) | Generates normal and malicious activity |
| Attacker VM    | Simulates APT-based attacks (MITRE tactics) |

## 4. Log Sources

- Windows Event Logs
- Linux Syslog
- Suricata IDS logs
- pfSense firewall logs

## 5. Log Flow

Client Logs → Filebeat → Logstash → Elasticsearch → Kibana Dashboards


## 6. Features

- Real-time log monitoring and alerting
- MITRE ATT&CK-based threat detection
- Visual dashboards for threat intelligence
- Custom detection rule development

