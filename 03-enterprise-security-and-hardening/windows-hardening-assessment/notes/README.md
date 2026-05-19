# Investigation Notes

## Assessment Context

This assessment focused on identifying exposed network services, validating insecure configurations, reviewing SMB-related visibility, and performing hardening activities within a Windows Server environment.

The workflow emphasized exposure reduction, service hardening, account security improvements, and post-remediation verification activities commonly associated with defensive security operations.

---

## Assessment Methodology

The assessment workflow followed a structured process consisting of:

1. Initial exposure enumeration
2. Service validation activities
3. SMB visibility review
4. Vulnerability validation
5. Administrative access review
6. Hardening implementation
7. Post-remediation reassessment
8. Exposure reduction verification

The methodology prioritized defensive visibility and remediation validation over offensive demonstration activities.

---

## Network Enumeration Notes

Initial network enumeration identified multiple externally accessible services exposed on the target system, including:

- FTP
- HTTP
- SMB
- NetBIOS-related services

The enumeration workflow demonstrated how exposed services increase attack surface visibility within Windows environments.

![Initial Nmap Exposure Scan](../screenshots/01-initial-nmap-exposure-scan.png)

---

## FTP Exposure Notes

The FTP service permitted anonymous authentication and unrestricted file upload capability during assessment activities.

Observed exposure conditions included:

- Anonymous authentication acceptance
- Unauthenticated file access
- Unauthorized file upload capability
- Lack of secure transport protections

The assessment highlighted the operational risks associated with legacy cleartext services and weak authentication controls.

### Anonymous FTP Visibility

![Anonymous FTP Access](../screenshots/02-anonymous-ftp-access.png)

### Unauthorized Upload Validation

![FTP File Upload Validation](../screenshots/03-ftp-file-upload-validation.png)

---

## IIS Exposure Notes

The target environment exposed a default IIS web interface that had not been configured for operational use.

Observed conditions included:

- Default web configuration exposure
- Unnecessary active services
- Increased attack surface visibility
- Incomplete hardening posture

The assessment reinforced the importance of reviewing and removing unnecessary services from production environments.

![Default IIS Exposure](../screenshots/04-default-iis-page-exposure.png)

---

## SMB Visibility Notes

SMB enumeration activities confirmed accessible SMB-related visibility prior to remediation activities.

The assessment demonstrated how exposed SMB services may contribute to:

- Unauthorized share discovery
- Administrative visibility exposure
- Increased attack surface conditions
- Elevated operational risk

![SMB Share Enumeration](../screenshots/05-smb-share-enumeration.png)

---

## Vulnerability Validation Notes

Validation activities confirmed vulnerable SMB exposure conditions associated with MS17-010 during the assessment workflow.

The assessment highlighted the operational impact of:

- Unpatched systems
- Weak SMB exposure controls
- Inadequate hardening
- Delayed remediation activities

![MS17-010 Validation](../screenshots/06-ms17-010-vulnerability-validation.png)

---

## Elevated Access Validation Notes

Validation activities confirmed elevated command execution capability on the target environment during the assessment process.

The workflow demonstrated how insufficient hardening controls can contribute to elevated access exposure within Windows environments.

![Elevated Access Validation](../screenshots/07-post-exploitation-shell-access.png)

---

## Hardening Workflow Notes

Hardening activities focused on reducing exposed services and improving local account security posture.

Implemented hardening actions included:

- IIS role removal
- Guest account deactivation
- Exposure reduction validation
- SMB access restriction improvements

### IIS Service Hardening

![IIS Role Removal](../screenshots/08-iis-role-removal.png)

### Guest Account Hardening

![Guest Account Disabled](../screenshots/10-guest-account-disabled.png)

---

## Post-Remediation Validation Notes

Post-remediation reassessment activities confirmed reduced exposure visibility after hardening implementation.

Observed improvements included:

- Reduced exposed services
- Improved SMB restrictions
- Stronger authentication enforcement
- Reduced attack surface visibility

### Post-Hardening Enumeration

![Post-Hardening Exposure Verification](../screenshots/09-post-hardening-nmap-scan.png)

### SMB Restriction Validation

![SMB Enumeration Blocked](../screenshots/11-smb-enumeration-blocked.png)

---

## Administrative Review Notes

Administrative group visibility was reviewed to identify privileged access exposure and validate administrative access control visibility.

The assessment reinforced the operational importance of continuously reviewing privileged account assignments within Windows environments.

![Administrative Account Review](../screenshots/12-administrative-account-review.png)

---

## Tooling Observations

The assessment demonstrated how commonly available security tools can provide visibility into:

- Exposed services
- Weak authentication controls
- SMB-related exposure
- Administrative access visibility
- Post-remediation reassessment
- Exposure reduction validation

The workflow also demonstrated the operational value of combining:

- Enumeration
- Validation
- Hardening
- Reassessment

within defensive security operations.

---

## Assessment Limitations

This assessment focused on exposure visibility and hardening validation activities within a controlled lab environment.

The assessment did not include:

- Live malware analysis
- Memory forensics
- Endpoint detection engineering
- Threat attribution
- Reverse engineering workflows
- Enterprise-scale infrastructure analysis

---

## Analyst Notes

The assessment demonstrated how exposed services, weak authentication controls, and insufficient hardening practices can increase attack surface visibility within Windows environments.

The workflow also reinforced the operational importance of remediation validation, reassessment procedures, and exposure reduction activities during defensive security operations.
