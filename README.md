# AgroDefend-Network-Threat-Detection
Threat detection and log correlation in a virtual enterprise network using Wazuh, pfSense, and MITRE ATT&amp;CK techniques.
[![Project Status](https://img.shields.io/badge/status-active-brightgreen)](https://github.com/JohnIdogo/AgroDefend-Network-Threat-Detection)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

**Project Type:** Enterprise SOC Deployment  
**Role:** Consultant-Led Engagement  
**Client:** AgroDefend Inc.  
**Tools & Technologies:** Wazuh, pfSense, Ubuntu, Windows 10, Kali Linux  
**Status:** Active & Improving  
**Date Completed:** May 2025

---

## 📌 Overview

This project simulates a full-scale SOC (Security Operations Center) environment for **AgroDefend Inc.**, a fictional agricultural technology company. The engagement includes designing a segmented network, deploying Wazuh as a SIEM solution, simulating realistic attack vectors, and performing correlation analysis based on MITRE ATT&CK techniques.

---

## 🎯 Objectives

- Deploy a segmented network (WAN, CorpNet, DMZ, IT Dept) using **pfSense**
- Configure **Wazuh SIEM** for centralized log management and alerting
- Simulate real-world attacks (SSH brute-force, directory enumeration, RDP compromise)
- Detect, analyze, and correlate threats using logs from Linux and Windows endpoints
- Map threats to MITRE ATT&CK for executive-level reporting

---

## 🔍 Attack Simulations

### 🔐 SSH Brute Force (T1110.001, T1021.004)
- **Target:** Ubuntu in DMZ
- **Logs:** `/var/log/auth.log`, Wazuh rule 5760
- **Tools:** Kali + Hydra

### 🌐 Directory Enumeration (Web Recon)
- **Target:** Apache Web Server
- **Detection:** Wazuh alert 31101, HTTP 404 patterns
- **Tools:** Dirb/Gobuster simulation

### 🖥️ RDP Credential Compromise (T1550.002, T1021.001)
- **Target:** Windows 10 host
- **Access:** NTLM via logon type 3
- **Tools:** Wazuh rule 92657

---

## 📈 Key Findings

- SSH brute-force attacks detected via log and alert correlation
- Apache directory scan behavior flagged using Wazuh detection rules
- Lateral movement from CorpNet to DMZ confirmed via Windows Event ID 4624
- Threat patterns validated with MITRE mappings and alert rule correlation

---

## 🛠️ Repository Contents

| Folder | Description |
|--------|-------------|
| `docs/` | Final PDF report and presentation deck |
| `architecture/` | Network diagram and pfSense configurations |
| `logs/` | Raw logs from Linux, Apache, and Windows |
| `simulations/` | Screenshots and notes for each simulated attack |
| `wazuh_alerts/` | Screenshots of triggered alerts from Wazuh SIEM |

---

## ✅ Security Recommendations

1. Enforce **MFA** for SSH and RDP
2. Block unnecessary lateral traffic between network segments
3. Implement **Zero Trust Architecture**
4. Retain logs for at least **90 days**
5. Enable **geo-blocking** and **alert thresholds** in Wazuh
6. Conduct **quarterly tabletop exercises**

---

## 📄 MITRE ATT&CK Techniques

| Technique ID | Description              |
|--------------|--------------------------|
| T1110.001     | Password Guessing        |
| T1021.004     | SSH Remote Services      |
| T1078.002     | Valid Accounts           |
| T1550.002     | Pass the Hash            |
| T1021.001     | Remote Desktop Protocol  |

---

## 🔏 Licensing & Ownership

This project is licensed under the **MIT License**.  
All content was developed for portfolio and educational purposes in a controlled lab environment.

> **Attribution:** Created by **John Idogo** – Cybersecurity Consultant | SOC Analyst | Threat Hunter | GRC | Third Party Risk

---

## 👤 About Me

I'm **John Idogo**, a cybersecurity analyst with a passion for threat detection, SOC engineering, and defensive security strategy.

- 🔗 [LinkedIn](www.linkedin.com/in/john-idogo-5b991735a)  
- 🐙 [GitHub](https://github.com/JohnIdogo)  
- 📧 Email: Johnidogo@yahoo.com

> *This project is for educational and demonstration purposes only. All simulated attacks were performed in an isolated, non-production environment.*
