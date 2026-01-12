# Red Team / Blue Team Utilities - Wazuh + Suricata (Cyberprotection Systems)

This repository contains **minimal reusable utilities** from the course lab to support a Red Team / Blue Team exercise:
- Wazuh agent snippet to ingest Suricata EVE JSON
- Custom Suricata rules requested by the lab
- Short playbooks for detection / analysis / response

## What to check
1. `wazuh/suricata-eve-localfile.xml` (Wazuh agent configuration snippet)
2. `suricata/custom-pass-html.rules` (custom IDS rules)
3. `playbooks/` (operational checklists)

## Lab mapping
- Wazuh correlation on endpoint events + alert enrichment
- Suricata IDS on LinuxHost + forwarding `eve.json` into Wazuh
- Validation with controlled tests (e.g., nmap, HTTP request patterns)
