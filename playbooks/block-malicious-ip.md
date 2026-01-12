# Playbook - Block Malicious IP

## Detection
- Apache access logs monitored by Wazuh
- Source IP checked against AlienVault reputation list

## Analysis
- Identify request source IP
- Confirm IP presence in blacklist
- Verify triggering rule ID 100100

## Response
- Wazuh Active Response executes firewall-drop
- IP blocked for a limited time window

## Outcome
- Attacker access to web server is prevented automatically
