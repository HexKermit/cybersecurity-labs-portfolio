# Windows Server Hardening & Exposure Reduction Assessment

## Investigation Overview

This project documents a Windows Server security assessment and hardening workflow focused on identifying exposed services, validating insecure configurations, reviewing administrative exposure, and verifying post-hardening remediation effectiveness.

The investigation included network exposure enumeration, anonymous service validation, SMB visibility review, vulnerability validation activities, service hardening, account security improvements, and post-remediation verification workflows.

![Exposure Review](screenshots/01-initial-nmap-exposure-scan.png)

---

## Security Assessment Scope

The assessment focused on the following security areas:

- Network exposure enumeration
- Anonymous FTP access validation
- SMB share visibility review
- IIS default configuration exposure
- MS17-010 vulnerability validation
- Administrative access review
- Windows service hardening
- Exposure reduction verification
- Post-remediation network analysis

---

## Tools Used

| Tool | Purpose |
|------|----------|
| Nmap | Network exposure enumeration |
| smbclient | SMB share enumeration |
| FTP Client | Anonymous FTP validation |
| Metasploit Framework | Vulnerability validation |
| Windows Server Manager | Service hardening |
| Windows Command Prompt | Administrative review |

---

## Analysis Areas

### Initial Exposure Enumeration

Initial network enumeration identified multiple exposed services, including FTP, HTTP, SMB, and NetBIOS-related services accessible from the network.

![Initial Nmap Scan](screenshots/01-initial-nmap-exposure-scan.png)

---

### Anonymous FTP Exposure Validation

The investigation confirmed anonymous FTP authentication exposure and validated unauthenticated access to the FTP service.

![Anonymous FTP Access](screenshots/02-anonymous-ftp-access.png)

---

### FTP Write Access Validation

The assessment confirmed unauthorized file upload capability through anonymous FTP access, demonstrating insecure write permissions on the exposed service.

![FTP Upload Validation](screenshots/03-ftp-file-upload-validation.png)

---

### IIS Exposure Review

The target system exposed the default IIS web interface, indicating unnecessary or default web service exposure within the environment.

![Default IIS Exposure](screenshots/04-default-iis-page-exposure.png)

---

### SMB Share Enumeration

SMB enumeration activities identified accessible shares and administrative network exposure visibility.

![SMB Share Enumeration](screenshots/05-smb-share-enumeration.png)

---

### MS17-010 Vulnerability Validation

The assessment validated exposure associated with the MS17-010 SMB vulnerability and confirmed vulnerable SMB exposure conditions prior to remediation activities.

![MS17-010 Validation](screenshots/06-ms17-010-vulnerability-validation.png)

---

### Elevated Access Validation

Validation activities confirmed elevated command execution capability on the target system during the assessment workflow.

![Elevated Access Validation](screenshots/07-post-exploitation-shell-access.png)

---

### IIS Service Hardening

Hardening activities included removal of unnecessary IIS-related services and reduction of externally exposed attack surface areas.

![IIS Role Removal](screenshots/08-iis-role-removal.png)

---

### Post-Hardening Exposure Verification

Post-remediation network enumeration confirmed reduced service exposure and successful hardening validation.

![Post-Hardening Nmap Scan](screenshots/09-post-hardening-nmap-scan.png)

---

### Guest Account Hardening

The Guest account was disabled to reduce unauthorized local access exposure and improve endpoint security posture.

![Guest Account Disabled](screenshots/10-guest-account-disabled.png)

---

### SMB Access Restriction Validation

Post-hardening SMB enumeration attempts resulted in access denial responses, validating improved access control enforcement.

![SMB Access Denied](screenshots/11-smb-enumeration-blocked.png)

---

### Administrative Access Review

Administrative group membership visibility was reviewed to identify privileged account exposure within the system.

![Administrative Account Review](screenshots/12-administrative-account-review.png)

---

## Investigation Findings

- Identified exposed FTP, HTTP, SMB, and NetBIOS-related services
- Confirmed anonymous FTP authentication exposure
- Validated unauthorized FTP file upload capability
- Reviewed SMB share visibility and administrative exposure
- Confirmed vulnerable SMB exposure conditions prior to remediation
- Reduced attack surface through IIS role removal
- Disabled unnecessary Guest account access
- Verified post-hardening exposure reduction through rescanning activities
- Confirmed SMB access restrictions after remediation activities

---

## Defensive Value

This project demonstrates operational security concepts associated with:

- Exposure enumeration
- Service hardening
- Attack surface reduction
- SMB security review
- Administrative access review
- Vulnerability validation
- Remediation verification
- Post-hardening assessment workflows

---

## Environment Details

| Component | Details |
|-----------|---------|
| Target Platform | Windows Server 2016 |
| Assessment Type | Security Hardening Assessment |
| Network Services | FTP, HTTP, SMB |
| Assessment Platform | Kali Linux |
| Validation Workflow | Pre/Post Hardening Review |

---

## Analyst Assessment

The assessment demonstrated how exposed network services, insecure default configurations, and weak access controls can increase attack surface visibility within Windows environments.

The workflow also highlighted the operational importance of remediation validation, exposure reduction verification, and post-hardening reassessment activities during defensive security operations.
