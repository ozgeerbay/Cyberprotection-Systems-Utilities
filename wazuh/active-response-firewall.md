# Active Response - Blocking Malicious IPs (Apache)

## Objective
Automatically block IP addresses with bad reputation when accessing an Apache web server.

## Log source
- Apache access log:
  /var/log/apache2/access.log

## Wazuh configuration summary

### Log monitoring
```xml
<localfile>
  <log_format>syslog</log_format>
  <location>/var/log/apache2/access.log</location>
</localfile>
```

### Reputation list
- AlienVault reputation database
- Converted from IPSet to CDB list
- Stored as:
  /var/ossec/etc/lists/blacklist-alienvault

### Detection rule
```xml
<group name="attack,">
  <rule id="100100" level="10">
    <if_group>web|attack|attacks</if_group>
    <list field="srcip" lookup="address_match_key">etc/lists/blacklist-alienvault</list>
    <description>IP address found in AlienVault reputation database.</description>
  </rule>
</group>
```

### Active Response
```xml
<active-response>
  <command>firewall-drop</command>
  <location>local</location>
  <rules_id>100100</rules_id>
  <timeout>60</timeout>
</active-response>
```

## Result
When a request is received from a blacklisted IP, Wazuh automatically blocks the source IP
at the host firewall level.
