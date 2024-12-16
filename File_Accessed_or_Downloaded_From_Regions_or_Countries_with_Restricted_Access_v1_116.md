
## File Accessed or Downloaded From Regions or Countries with Restricted Access

### Detection Name
File Accessed or Downloaded From Regions or Countries with Restricted Access

### Description
Detecting unauthorized access attempts to a secure network by monitoring login patterns.

### Annotations
- **CVE**: -
- **Technique**: T1567-Exfiltration Over Web Service
- **Sub-Technique**: T1567.001-Exfiltration Over Web Service: Exfiltration to Code Repository
- **Tactic**: Credential Access
- **D3FEND**:  [D3-SDM](https://d3fend.mitre.org/technique/d3f:SystemDaemonMonitoring/), [D3-PSA](https://d3fend.mitre.org/technique/d3f:ProcessSpawnAnalysis/)
- **Platform**: Linux, Windows, macOS
- **Group**: None
- **Campaign**: None
- **Software**: [Empire (S0363)](https://attack.mitre.org/software/S0363)
- **NIST**: [RS.AN](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/rs/rs-an), [DE.CM](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/de/de-cm), [PR.DS](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-ds)
- **CIS**: [CIS 4](https://www.cisecurity.org/controls/secure-configuration-of-enterprise-assets-and-software), [CIS 3](https://www.cisecurity.org/controls/data-protection), [CIS 5](https://www.cisecurity.org/controls/account-management), [CIS 1](https://www.cisecurity.org/controls/inventory-and-control-of-enterprise-assets)
- **Agent**: -

### Type

TTP (Tactics, Techniques, and Procedures)

### Logging Required

- Sysmon or equivalent endpoint security solution with process creation, file creation, and registry modification event monitoring enabled.

- Windows Security Event Logs

- Process Creation Logs

- Windows Registry Modification Logs


### Recommended Actions

- Verify the legitimacy of the accessed or downloaded files.

- Identify the users involved in these activities.

- Check for any unusual patterns in file access or download activities.

- Review the network logs for any suspicious connections from the specified regions.

- Conduct a risk assessment on the accessed or downloaded files.

### Considerations

- A company might have legitimate business operations or partnerships in countries like China (CN) or North Korea (KP), leading to authorized file access or downloads from these regions.

- Employees might be using VPN services that route their internet traffic through servers located in restricted countries, causing false alerts for file access or downloads.

- Incorrect or outdated geolocation data might misidentify the source country of the access, leading to false positives in the alert system.


### Mitigation


- [Audit (M1047)](https://attack.mitre.org/mitigations/M1047)



- [Data Backup (M1053)](https://attack.mitre.org/mitigations/M1053)



- [Remote Data Wipe (M1029)](https://attack.mitre.org/mitigations/M1029)



- [Network Segmentation (M1030)](https://attack.mitre.org/mitigations/M1030)



### References:
- MITRE. (n.d.). MITRE ATT&CK. https://attack.mitre.org/
- Center for Internet Security (CIS). (n.d.). CISecurity homepage. https://www.cisecurity.org/
- MITRE. (n.d.). MITRE D3FEND. https://d3fend.mitre.org/
- National Institute of Standards and Technology. (n.d.). Cybersecurity framework. https://www.nist.gov/cyberframework
