# 🏗️ System Architecture

## Overview

The DevSecOps Cybersecurity Platform is designed to provide continuous security monitoring, threat detection, and analysis capabilities.

The architecture combines security monitoring tools, intrusion detection mechanisms, and attack simulation environments.

---

# Global Architecture

```
                    Cyber Attacker Simulation
                              |
                              |
                         Kali Linux
                              |
                              |
                  Network Traffic Generation
                              |
                              ▼
                        Suricata IDS
                              |
                              |
                    Intrusion Detection
                              |
                              ▼
                         Wazuh SIEM
                              |
                              |
              Security Events Collection & Analysis
                              |
                              ▼
                   Monitoring and Response
```

---

# Components Description

## Kali Linux

Role:
- Security testing environment
- Attack simulation
- Network reconnaissance
- Vulnerability testing

Tools:
- Nmap
- Hydra
- Wireshark

---

## Suricata IDS

Role:
- Network traffic analysis
- Intrusion detection
- Suspicious activity identification

Capabilities:
- Rule-based detection
- Network monitoring
- Alert generation

---

## Wazuh SIEM

Role:
- Centralized security monitoring
- Log collection
- Alert management

Capabilities:
- Security event analysis
- Threat visibility
- Incident monitoring

---

## Linux Infrastructure

The platform uses Linux-based environments to deploy security components and simulate enterprise infrastructures.

---

# Security Workflow

1. Attack simulation generates suspicious activities.

2. Network traffic is analyzed by Suricata.

3. Security events are collected by Wazuh.

4. Alerts are analyzed for threat detection.

5. Security monitoring helps improve incident response.
