# Respond

## Containment options
- Block offending src IP temporarily on LinuxHost firewall (lab-safe).
- If Windows endpoint involved, isolate host from network (lab context) and preserve logs.

## Preservation
- Copy relevant sections of:
  - `/var/log/suricata/eve.json`
  - `/var/log/auth.log` (Linux)
  - Wazuh alert details (screenshots/export if needed)

## Recovery
- Remove temporary blocks after validation.
- Document what rule/config caused detection and what changed.
