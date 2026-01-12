# Analyze (quick checklist)

## Suricata evidence
From `eve.json` extract:
- timestamp
- src_ip / dest_ip / proto
- alert.signature / alert.severity
- http fields (if present)

## Wazuh correlation
- Match Suricata alert timestamp with Wazuh alert timestamp.
- Confirm Wazuh shows agent metadata + rule metadata (rule id/level/groups).
- If the same src_ip appears in multiple alerts (scan + auth failures), note it as correlation.
