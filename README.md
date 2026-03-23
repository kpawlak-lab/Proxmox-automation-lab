# Automated SOC & Incident Response Lab

## Objective
The goal of this project is to build a fully functional, enterprise-simulated local laboratory to practice Threat Hunting, Log Centralization, and Incident Response Automation. The environment simulates a corporate network under attack and demonstrates the automated triage of security alerts.

## Technologies Used
* **Hypervisor:** Proxmox VE
* **Network & Firewall:** pfSense
* **Infrastructure:** Windows Server 2022 (Active Directory), Windows 11
* **Telemetry & EDR:** Microsoft Sysmon
* **SIEM:** Splunk Enterprise
* **SOAR (Automation):** n8n
* **Threat Intelligence:** VirusTotal API

## Architecture Diagram
///draw.io ///

## Use Cases & Detections Developed

### 1. Active Directory Brute-Force Detection
* **Attack Tool:** Hydra / Kali Linux
* **Telemetry:** Windows Security Event ID 4625
* **Detection Logic:** [Link to SPL query]

### 2. Automated Alert Triage (SOAR)
* **Trigger:** Splunk Webhook triggered by malicious PowerShell execution.
* **Enrichment:** Automated API call to VirusTotal to check file hash reputation.
* **Response:** Formatted alert pushed to a Slack channel with incident details.
* **Playbook:** ///Link to n8n///
