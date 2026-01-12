# Impact / Ransomware Behaviour (T1486)

## Objective
Analyse ransomware-like behaviour and its detection by Wazuh.

## Execution context
- Platform: Windows VM
- Tool: Atomic Red Team
- Technique: T1486 (Data Encrypted for Impact)

## Expected detection (Wazuh)
Primary rule groups expected to alert:
- Malware activity
- File integrity monitoring
- Suspicious process behaviour

## Analysis steps
1. Execute ART test #10 (lab-safe environment).
2. Inspect Wazuh alerts triggered during execution.
3. Analyse:
   - process responsible
   - file system activity
   - severity and rule classification

## Observations
- Encryption activity triggers high-impact alerts.
- Behaviour strongly correlates with ransomware TTPs.

## Conclusion
Impact techniques such as T1486 are critical and typically produce high-confidence alerts in SIEM/XDR solutions.
