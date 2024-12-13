
## Failed Config Changes by Same User

### Detection Name
Failed Config Changes by Same User

### Description
Detects multiple failed configuration changes by the same user within 15 minutes.

### Annotations
- **CVE**: -
- **Technique**: T1562-Impair Defenses
- **Sub-Technique**: T1562.002-Impair Defenses: Disable Windows Event Logging
- **Tactic**: Defense Evasion
- **D3FEND**:  [something6](https://defend.com), [something6](https://defend.com)
- **Platform**: Windows, DNIF
- **Group**: [Something2](https://group.com), [Something2](https://group.com)
- **Campaign**: [Something1](https://campaign.com), [Something1](https://campaign.com)
- **Software**: [Something3](https://software.com), [Something3](https://software.com)
- **NIST**: [Something4](https://nist.com), [Something4](https://nist.com)
- **CIS**: [Something5](https://cis.com), [Something5](https://cis.com)
- **Agent**: -

### Type

TTP (Tactics, Techniques, and Procedures)

### Logging Required

- Sysmon or equivalent endpoint security solution with process creation, file creation, and registry modification event monitoring enabled.

- Windows Security Event Logs.

- Process Creation Logs

- Windows Registry Modification Logs


### Recommended Actions

- Review recent login activities for anomalies

- Examine network traffic for suspicious patterns

- Check for recent changes in user permissions

- Investigate alerts triggered by security tools

### Considerations

- A user might be testing configuration changes in a controlled environment, leading to multiple failed attempts that are not malicious.

- During scheduled maintenance, configuration changes might fail due to system updates or temporary unavailability, causing false alerts.

- A user may not have the correct permissions to make configuration changes, resulting in repeated failed attempts that are not indicative of an attack.


### Mitigation


- [something7](https://mitigation.com)



- [something7](https://mitigation.com)



### References:
- MITRE. (n.d.). MITRE ATT&CK. https://attack.mitre.org/
- Center for Internet Security (CIS). (n.d.). CISecurity homepage. https://www.cisecurity.org/
- MITRE. (n.d.). MITRE D3FEND. https://d3fend.mitre.org/
- National Institute of Standards and Technology. (n.d.). Cybersecurity framework. https://www.nist.gov/cyberframework