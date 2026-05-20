# Investigation Notes

## Assessment Context

This assessment focused on identifying insecure Linux service configurations, excessive network exposure, weak authentication controls, and privileged account risks within a controlled Ubuntu-based lab environment.

The workflow combined exposure validation, credential analysis, service hardening, and remediation verification activities commonly associated with Linux security administration and defensive hardening operations.

---

## Assessment Methodology

The assessment followed a structured workflow consisting of:

1. Initial network service enumeration
2. Anonymous FTP access validation
3. Sensitive file retrieval testing
4. Password hash review
5. Offline password cracking validation
6. Root SSH authentication review
7. Telnet exposure validation
8. SMB share enumeration
9. Unauthorized SMB write testing
10. Privileged account review
11. Service removal and hardening
12. Package update operations
13. Post-remediation validation

The methodology emphasized realistic exposure review and defensive remediation activities rather than persistence or destructive exploitation.

---

## Initial Exposure Notes

Initial Nmap enumeration identified multiple externally accessible services exposed to the network.

Observed services included:

- FTP
- SSH
- Telnet
- HTTP
- SMB

The exposure demonstrated excessive attack surface visibility within the Linux environment.

### Initial Service Enumeration

![Initial Nmap Scan](../screenshots/01-initial-nmap-service-exposure.png)

---

## FTP Exposure Notes

Anonymous FTP authentication was successfully validated.

The environment permitted unauthorized access to exposed files through anonymous login workflows.

The assessment highlighted risks associated with:

- Weak file access controls
- Sensitive data exposure
- Anonymous authentication
- Unrestricted file retrieval

### Anonymous FTP Login

![Anonymous FTP Login](../screenshots/02-anonymous-ftp-login.png)

---

## Sensitive File Exposure Notes

Sensitive Linux authentication files were retrieved during exposure validation activities.

Observed files included:

- `/etc/passwd`
- `/etc/shadow`

The assessment demonstrated how exposed services can enable credential harvesting opportunities.

### Passwd File Retrieval

![Passwd File Download](../screenshots/03-passwd-file-download.png)

### Shadow File Retrieval

![Shadow File Download](../screenshots/04-shadow-file-download.png)

---

## Password Security Notes

Retrieved password hashes were reviewed and subjected to offline cracking validation.

The assessment demonstrated how weak passwords increase exposure risk after credential file compromise.

### Shadow Hash Review

![Shadow Hash Review](../screenshots/05-shadow-hash-review.png)

### Password Cracking Validation

![John Password Cracking](../screenshots/06-john-password-cracking-results.png)

---

## SSH Exposure Notes

Direct root SSH authentication was successfully validated.

The workflow highlighted risks associated with:

- Remote privileged authentication
- Excessive administrative exposure
- Increased brute-force attack surface
- Weak remote access controls

### Root SSH Access

![Root SSH Access](../screenshots/07-root-ssh-access-validation.png)

---

## Telnet Exposure Notes

The environment exposed Telnet services allowing plaintext remote authentication.

The assessment reinforced the risks associated with:

- Unencrypted credential transmission
- Legacy protocol exposure
- Insecure remote administration
- Network credential interception

### Telnet Authentication Exposure

![Telnet Login](../screenshots/08-telnet-insecure-login.png)

---

## Apache Exposure Notes

The Apache HTTP service remained enabled with default configuration visibility.

The assessment demonstrated unnecessary web exposure and default service visibility within the environment.

### Default Apache Web Exposure

![Apache Default Page](../screenshots/09-default-apache-web-page.png)

---

## SMB Exposure Notes

SMB shares allowed unauthorized enumeration and file upload operations.

The assessment demonstrated exposure associated with:

- Weak SMB permissions
- Unauthorized file access
- Unrestricted share visibility
- Remote file manipulation

### SMB Share Enumeration

![SMB Enumeration](../screenshots/10-anonymous-smb-share-enumeration.png)

### Unauthorized SMB Write

![Unauthorized SMB Write](../screenshots/11-unauthorized-smb-file-write.png)

---

## Privileged Account Notes

The environment contained a duplicate UID 0 account capable of root-equivalent access.

The assessment demonstrated risks associated with:

- Hidden privileged accounts
- Unauthorized persistence
- Privilege escalation
- Administrative bypass opportunities

### Duplicate UID 0 Review

![Duplicate UID 0](../screenshots/12-duplicate-uid-zero-account-review.png)

### UID 0 Account Removal

![UID 0 Removal](../screenshots/13-duplicate-root-account-removal.png)

---

## Hardening Activity Notes

Multiple unnecessary services were removed during remediation activities.

Removed services included:

- VSFTPD
- Telnet
- Apache HTTP Server

The workflow demonstrated practical Linux hardening operations associated with attack surface reduction.

### VSFTPD Removal

![VSFTPD Removal](../screenshots/14-vsftpd-service-removal.png)

### Telnet Removal

![Telnet Removal](../screenshots/15-telnet-service-removal.png)

### Apache Removal

![Apache Removal](../screenshots/16-apache-service-removal.png)

---

## Linux Update Notes

System packages were reviewed and updated during remediation activities.

The workflow reinforced the importance of:

- Patch management
- Software maintenance
- Vulnerability reduction
- Package lifecycle management

### Linux Package Updates

![APT Update Process](../screenshots/17-linux-system-package-update.png)

---

## Post-Remediation Validation Notes

Post-hardening validation confirmed reduced SMB accessibility after security configuration changes.

The assessment demonstrated successful restriction of previously exposed SMB functionality.

### SMB Access Restriction Validation

![SMB Access Denied](../screenshots/18-post-hardening-smb-access-denied.png)

---

## Tooling Observations

The assessment demonstrated how common Linux administration and security tools provide visibility into:

- Network exposure
- Weak authentication
- Credential security
- Remote access exposure
- SMB permissions
- Privileged accounts
- Service management
- Hardening validation

The workflow also demonstrated the operational value of combining:

- Enumeration
- Credential review
- Exposure validation
- Hardening activities
- Remediation verification

within Linux defensive security operations.

---

## Assessment Limitations

This assessment focused on Linux hardening and exposure reduction activities within a controlled lab environment.

The assessment did not include:

- Kernel exploitation
- Memory forensics
- EDR telemetry integration
- Threat hunting operations
- Container security
- Cloud infrastructure hardening
- Enterprise Linux fleet management

---

## Analyst Notes

The assessment demonstrated how weak service configurations, exposed authentication mechanisms, insecure legacy protocols, and excessive network visibility can significantly increase attack surface risk within Linux systems.

The remediation workflow improved overall defensive posture through service reduction, privileged account cleanup, authentication hardening, and exposure mitigation activities.
