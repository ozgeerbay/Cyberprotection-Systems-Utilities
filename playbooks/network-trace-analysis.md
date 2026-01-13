# Network Trace Analysis (pcap replay)

## Objective
Analyse malicious network behaviour using captured traffic and validate detection in Wazuh.

## Tools
- Wireshark
- tcpreplay

## Analysis steps
1. Open malware.pcap in Wireshark.
2. Identify:
   - private IP addresses
   - subnet of compromised host
3. Replay traffic:
```bash
sudo tcpreplay -v -i <interface> -M10 malware.pcap
```

## Expected results

- Network-based alerts in Wazuh.
- Possible detection of:
  - C2 communication
  - Exfiltration patterns
  - Known malicious indicators
 
## Conclusion

Replayed traffic allows safe reproduction of real malware network behaviour and validation of detection capabilities.
