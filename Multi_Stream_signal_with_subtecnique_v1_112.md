
## Multi Stream signal with subtecnique

### Detection Name
Multi Stream signal with subtecnique

### Description
Multi Stream signal with subtechnique under investigation for Linux and macOS.

### Annotations
- **CVE**: -
- **Technique**: T1222-File and Directory Permissions Modification
- **Sub-Technique**: T1222.002-File and Directory Permissions Modification: Linux and Mac File and Directory Permissions Modification
- **Tactic**: Defense Evasion
- **D3FEND**:  [D3-PSA](https://d3fend.mitre.org/technique/d3f:ProcessSpawnAnalysis/)
- **Platform**: L, i, n, u, x, ,,  , m, a, c, O, S
- **Group**: [APT32 (G0050)](https://attack.mitre.org/groups/G0050), [Rocke (G0106)](https://attack.mitre.org/groups/G0106), [TeamTNT (G0139)](https://attack.mitre.org/groups/G0139)
- **Campaign**: None
- **Software**: None
- **NIST**: [PR.DS](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-ds), [ID.AM](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/id/id-am), [DE.CM](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/de/de-cm)
- **CIS**: [CIS 1](https://www.cisecurity.org/controls/inventory-and-control-of-enterprise-assets), [CIS 5](https://www.cisecurity.org/controls/account-management), [CIS 4](https://www.cisecurity.org/controls/secure-configuration-of-enterprise-assets-and-software)
- **Agent**: -

### Type

TTP (Tactics, Techniques, and Procedures)

### Logging Required

- Sysmon or equivalent endpoint security solution with process creation, file creation, and registry modification event monitoring enabled.

- Windows Security Event Logs

- Process Creation Logs

- Windows Registry Modification Logs


### Recommended Actions

- Review recent login attempts for suspicious activity

- Check for any unusual data transfer activities

- Verify integrity of critical system files

- Monitor for any new or unknown processes running on servers

### Considerations

- During scheduled system updates, multiple streams such as FIREWALL, EP-NETWORK, EP-SERVICE, and EP-PROCESS might log numerous events. These activities could be mistaken for suspicious behavior, leading to false positives.

- Changes in network configurations, such as firewall rule updates or service restarts, can generate a high volume of logs across multiple streams. These legitimate activities might trigger alerts if not properly accounted for.

- A sudden increase in legitimate network traffic, such as during a company-wide video conference or data backup, can produce a spike in logs across multiple streams. This could be misinterpreted as an attack if thresholds are not adjusted accordingly.


### Mitigation


- [Privileged Account Management (M1026)](https://attack.mitre.org/mitigations/M1026)



- [Restrict File and Directory Permissions (M1022)](https://attack.mitre.org/mitigations/M1022)



### References:
- MITRE. (n.d.). MITRE ATT&CK. https://attack.mitre.org/
- Center for Internet Security (CIS). (n.d.). CISecurity homepage. https://www.cisecurity.org/
- MITRE. (n.d.). MITRE D3FEND. https://d3fend.mitre.org/
- National Institute of Standards and Technology. (n.d.). Cybersecurity framework. https://www.nist.gov/cyberframework
