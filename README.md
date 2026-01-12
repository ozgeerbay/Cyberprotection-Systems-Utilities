# Active Response Automation & Red/Blue Team Utilities  
## Cyberprotection Systems

This repository contains **minimal, practical, and reusable utilities** developed during the **Cyberprotection Systems** laboratory sessions.  
The focus is on **detection, analysis, and automated response** to security incidents using **Wazuh**, **Suricata**, and **Atomic Red Team**.

The content is intentionally kept concise and operational, following a **Blue Team / Defensive Validation** approach rather than offensive tooling.

---

## Covered Laboratory Works

### Laboratory 1 – Detection and Correlation
- Wazuh deployment and event correlation
- Linux authentication and privilege escalation monitoring
- Windows telemetry with Sysmon
- Suricata IDS integration with Wazuh
- Custom Suricata detection rules
- Validation using controlled scans and HTTP pattern detection

---

### Laboratory 2 – Analysis and Containment of Security Incidents
- Atomic Red Team (ART) installation and usage
- Execution and analysis of MITRE ATT&CK techniques:
  - **T1048** – Exfiltration
  - **T1486** – Impact / Ransomware behaviour
- Alert analysis and correlation in Wazuh
- Network behaviour analysis using PCAP replay and traffic injection

---

### Laboratory 3 – Active Response Automation to Attacks
- Automated blocking of malicious IP addresses accessing an Apache server
- Integration of IP reputation lists with Wazuh
- Use of Wazuh Active Response for firewall-based containment
- File Integrity Monitoring (FIM) combined with VirusTotal
- Automated malware removal using a custom Active Response script
- Validation using the EICAR test file

---

## Repository Structure (High-Level)

- **wazuh/**  
  Documentation of detection rules, reputation lists, VirusTotal integration, and active response configuration.

- **suricata/**  
  Custom IDS rules used for detection and validation.

- **atomic-red-team/**  
  Reference commands and usage notes for executing and inspecting MITRE ATT&CK techniques.

- **active-response/**  
  Custom Active Response script used for automated threat removal.

- **playbooks/**  
  Short operational playbooks describing detection, analysis, and response workflows.

---

## Scope and Notes

- This repository does **not** include full binaries or external tools.
- Only **configuration snippets, scripts, and operational documentation** are provided.
- All attacks are executed in **controlled laboratory environments** for defensive validation purposes.
- The repository is intended to demonstrate **practical understanding of SIEM/XDR capabilities**, not offensive exploitation.

---

## Intended Use

- Academic laboratory evaluation
- Defensive security validation
- Blue Team training and automation reference
- Incident detection and response workflows
