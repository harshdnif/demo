
## Remove Arbitrary Security Windows Service

### Detection Name
Remove Arbitrary Security Windows Service

### Description
Remove Arbitrary Security Windows Service under investigation. Detects attempts to delete critical Windows services.

### Annotations
- **CVE**: -
- **Technique**: T1565-Data Manipulation
- **Sub-Technique**: T1565.001-Data Manipulation: Stored Data Manipulation
- **Tactic**: Impact
- **D3FEND**:
- **Platform**: Windows
- **Group**: [APT38 (G0082)](https://attack.mitre.org/groups/G0082)
- **Campaign**: [Remove Arbitrary Security Windows Service (campaign_id_12345)](https://www.dnif.it/en/kb/campaigns/remove-arbitrary-security-windows-service)
- **Software**: [MultiLayer Wiper (S1135)](https://attack.mitre.org/software/S1135), [SUNSPOT (S0562)](https://attack.mitre.org/software/S0562)
- **NIST**: [PR.IR](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-ir), [ID.AM](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/id/id-am), [ID.RA](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/id/id-ra), [PR.AA](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-aa), [DE.CM](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/de/de-cm), [PR.DS](https://csf.tools/reference/nist-cybersecurity-framework/v2-0/pr/pr-ds)
- **CIS**: [CIS 6](https://www.cisecurity.org/controls/access-control-management), [CIS 8](https://www.cisecurity.org/controls/audit-log-management), [CIS 12](https://www.cisecurity.org/controls/network-infrastructure-management)
- **Agent**: -

### Type

TTP (Tactics, Techniques, and Procedures)

### Logging Required

- Sysmon or equivalent endpoint security solution with process creation, file creation, and registry modification event monitoring enabled.

- Windows Security Event Logs

- Process Creation Logs

- Windows Registry Modification Logs


### Recommended Actions

- Identify all processes created or added within the same timeframe.

- Check for any changes in user privileges or roles.

- Review logs for any failed login attempts.

- Monitor network traffic for any unusual patterns.

- Check for any modifications to critical system files.

### Considerations

- During scheduled maintenance or updates, legitimate services might be stopped or removed temporarily. Ensure to cross-check with the maintenance schedule before raising an alert.

- Some third-party software installations might remove or modify existing services as part of their installation process. Verify if any new software was installed around the time of the alert.

- System administrators might manually remove or modify services for troubleshooting or optimization purposes. Confirm with the IT team if any such actions were taken intentionally.


### Mitigation

- [Encrypt Sensitive Information (M1041)](https://attack.mitre.org/mitigations/M1041)

- [Remote Data Storage (M1029)](https://attack.mitre.org/mitigations/M1029)

- [Restrict File and Directory Permissions (M1022)](https://attack.mitre.org/mitigations/M1022)


### References:
- MITRE. (n.d.). MITRE ATT&CK. https://attack.mitre.org/
- Center for Internet Security (CIS). (n.d.). CISecurity homepage. https://www.cisecurity.org/
- MITRE. (n.d.). MITRE D3FEND. https://d3fend.mitre.org/
- National Institute of Standards and Technology. (n.d.). Cybersecurity framework. https://www.nist.gov/cyberframework
