
## Failed Config Changes by Same User

### Detection Name
Failed Config Changes by Same User

### Description
Failed configuration changes by the same user within 15 minutes.

### Annotations
- **CVE**: -
- **Technique**: T1565-Data Manipulation
- **Sub-Technique**: T1565.001-Data Manipulation: Stored Data Manipulation
- **Tactic**: Impact
- **D3FEND**:  [D3-FIM](https://d3fend.mitre.org/technique/d3f:FileIntegrityMonitoring/), [D3-FH](https://d3fend.mitre.org/technique/d3f:FileHashing/), [D3-FE](https://d3fend.mitre.org/technique/d3f:FileEncryption/), [D3-FR](https://d3fend.mitre.org/technique/d3f:FileRemoval/), [D3-LFP](https://d3fend.mitre.org/technique/d3f:LocalFilePermissions/)
- **Platform**: Windows, Windows, Windows
- **Group**: [APT38 (G0082)](https://attack.mitre.org/groups/G0082)
- **Campaign**: [None](None)
- **Software**: [MultiLayer Wiper (S1135)](https://attack.mitre.org/software/S1135), [SUNSPOT (S0562)](https://attack.mitre.org/software/S0562)
- **NIST**: [DE.AE](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/de/de-ae), [DE.CM](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/de/de-cm), [PR.DS](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-ds), [PR.AA](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-aa)
- **CIS**: [CIS 6](https://www.cisecurity.org/controls/access-control-management)
- **Agent**: -

### Type

TTP (Tactics, Techniques, and Procedures)

### Logging Required

- Sysmon or equivalent endpoint security solution with process creation, file creation, and registry modification event monitoring enabled.

- Windows Security Event Logs

- Process Creation Logs

- Windows Registry Modification Logs


### Recommended Actions

- Identify the specific configuration changes attempted by the user.

- Check for any successful configuration changes by the same user in the recent past.

- Review the user's login activity to see if there are any unusual patterns.

- Check for any other failed actions by the same user in different streams.

- Correlate with threat intelligence to see if the user's IP or actions match any known malicious patterns.

### Considerations

- A user might be testing new configurations and intentionally causing failures to ensure that the system handles errors correctly. This could result in multiple failed configuration changes within a short period.

- Temporary network or system issues could cause legitimate configuration changes to fail repeatedly. These issues might be resolved without any malicious intent, leading to false positive alerts.

- A user might not have the correct permissions to make configuration changes, leading to repeated failed attempts. This could be due to a misconfiguration in the user’s access rights rather than an actual attack.


### Mitigation

- [Encrypt Sensitive Information (M1041)](https://attack.mitre.org/mitigations/M1041)

- [Remote Data Storage (M1029)](https://attack.mitre.org/mitigations/M1029)

- [Restrict File and Directory Permissions (M1022)](https://attack.mitre.org/mitigations/M1022)


### References:
- MITRE. (n.d.). MITRE ATT&CK. https://attack.mitre.org/
- Center for Internet Security (CIS). (n.d.). CISecurity homepage. https://www.cisecurity.org/
- MITRE. (n.d.). MITRE D3FEND. https://d3fend.mitre.org/
- National Institute of Standards and Technology. (n.d.). Cybersecurity framework. https://www.nist.gov/cyberframework
