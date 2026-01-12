# Detect (quick checklist)

## Wazuh
- Check alerts that mention:
  - SSH auth success/failure
  - sudo / privilege escalation events
  - Suricata alerts (forwarded from eve.json)

## Suricata
- Confirm Suricata is running and generating alerts:
  - `sudo systemctl status suricata`
  - `tail -n 50 /var/log/suricata/eve.json | jq -c '.'` (optional)

## Simple validation
- Run a controlled scan (e.g., nmap) against LinuxHost and confirm Suricata alerts appear in Wazuh.
- Trigger HTTP requests that match `pass.html` patterns and confirm Suricata rule hits.
