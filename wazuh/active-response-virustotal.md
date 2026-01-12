# Active Response - Malware Elimination with VirusTotal

## Objective
Automatically remove malicious files detected by Wazuh FIM and confirmed by VirusTotal.

## Monitoring scope
- Windows Downloads directory:
  C:\Users\<USER>\Downloads

```xml
<directories realtime="yes">C:\Users\admin\Downloads</directories>
```

## VirusTotal integration
```xml
<integration>
  <name>virustotal</name>
  <api_key>VIRUSTOTAL_API_KEY</api_key>
  <group>syscheck</group>
  <alert_format>json</alert_format>
</integration>
```

## Active Response command
```xml
<command>
  <name>remove-threat</name>
  <executable>remove-threat.exe</executable>
  <timeout_allowed>no</timeout_allowed>
</command>
```

```xml
<active-response>
  <disabled>no</disabled>
  <command>remove-threat</command>
  <location>local</location>
  <rules_id>87105</rules_id>
</active-response>
```

## Alert rules
```xml
<group name="virustotal,">
  <rule id="100092" level="12">
    <if_sid>657</if_sid>
    <match>Successfully removed threat</match>
    <description>Threat successfully removed by active response</description>
  </rule>

  <rule id="100093" level="12">
    <if_sid>657</if_sid>
    <match>Error removing threat</match>
    <description>Error removing detected threat</description>
  </rule>
</group>
```
## Result
When a malicious file is detected and confirmed by VirusTotal,
the file is automatically deleted from the system.
