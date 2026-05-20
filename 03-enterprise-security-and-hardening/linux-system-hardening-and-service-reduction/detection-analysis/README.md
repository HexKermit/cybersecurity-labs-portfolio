# Detection Analysis

## Overview

This document reviews the detection opportunities and defensive visibility associated with the identified Linux security weaknesses observed during the assessment.

The analysis focuses on exposed services, authentication activity, privilege escalation indicators, unauthorized access patterns, and hardening validation opportunities.

---

## Network Exposure Detection Opportunities

### Excessive Service Exposure

Initial enumeration identified several externally accessible services:

- FTP (21)
- SSH (22)
- Telnet (23)
- HTTP (80)
- SMB (139/445)

Related Screenshot:
- `01-initial-nmap-service-exposure.png`

### Detection Recommendations

Defenders should monitor for:

- Unusual network scans
- Repeated connection attempts
- Enumeration behavior
- External service discovery activity

Potential Detection Sources:
- IDS/IPS alerts
- Firewall logs
- NetFlow telemetry
- SIEM correlation rules

---

## FTP Security Detection

### Anonymous FTP Authentication

The FTP server permitted anonymous authentication access.

Related Screenshot:
- `02-anonymous-ftp-login.png`

### Detection Opportunities

Monitor for:
- Anonymous login attempts
- Unusual FTP sessions
- Large outbound file transfers
- Access to sensitive directories

Potential Log Sources:
- VSFTPD logs
- Authentication logs
- File access monitoring

---

## Sensitive File Access Visibility

### Credential File Retrieval Activity

Sensitive Linux authentication files were accessed remotely.

Files:
- `/etc/passwd`
- `/etc/shadow`

Related Screenshots:
- `03-passwd-file-download.png`
- `04-shadow-file-download.png`

### Detection Opportunities

Monitor for:
- Access to sensitive system files
- Unusual file transfer activity
- Privileged file access
- Data exfiltration behavior

Potential Detection Sources:
- Auditd logs
- File integrity monitoring
- EDR telemetry
- Linux security logs

---

## Password Cracking Activity

### Offline Credential Cracking

Password hashes were reviewed and cracked offline.

Related Screenshots:
- `05-shadow-hash-review.png`
- `06-john-password-cracking-results.png`

### Detection Considerations

Offline cracking activity itself may not generate direct logs on the victim system.

However, defenders should monitor for:
- Shadow file access attempts
- Credential dumping activity
- Unusual archive or transfer operations
- Authentication anomalies after compromise

---

## Remote Access Detection

### Root SSH Authentication

Direct root SSH authentication was successfully validated.

Related Screenshot:
- `07-root-ssh-access-validation.png`

### Detection Opportunities

Monitor for:
- Root SSH logins
- Remote privileged authentication
- Abnormal login times
- Geographic anomalies
- Brute-force attempts

Potential Detection Sources:
- `/var/log/auth.log`
- SSH daemon logs
- SIEM authentication correlation

---

### Telnet Authentication Exposure

Telnet permitted insecure plaintext authentication.

Related Screenshot:
- `08-telnet-insecure-login.png`

### Detection Opportunities

Monitor for:
- Telnet session establishment
- Plaintext credential exposure
- Legacy protocol usage
- Unencrypted remote administration activity

Potential Detection Sources:
- Network IDS signatures
- Firewall telemetry
- Packet capture analysis

---

## SMB Detection Opportunities

### SMB Enumeration and Write Access

SMB shares permitted unauthorized enumeration and file upload activity.

Related Screenshots:
- `10-anonymous-smb-share-enumeration.png`
- `11-unauthorized-smb-file-write.png`

### Detection Opportunities

Monitor for:
- Anonymous SMB access
- Unexpected SMB write operations
- File upload activity
- Suspicious share enumeration

Potential Detection Sources:
- Samba logs
- File integrity monitoring
- Windows event logs
- EDR telemetry

---

## Privileged Account Detection

### Duplicate UID 0 Account

A duplicate root-equivalent account existed on the system.

Related Screenshot:
- `12-duplicate-uid-zero-account-review.png`

### Detection Opportunities

Monitor for:
- Multiple UID 0 accounts
- Unauthorized account creation
- Privileged account modifications
- Changes to `/etc/passwd`

Potential Detection Sources:
- Auditd
- Linux account monitoring
- File integrity tools
- Privileged access monitoring

---

## Hardening Validation Detection

### Service Removal Validation

Hardening activities removed several unnecessary services.

Removed Services:
- VSFTPD
- Telnet
- Apache HTTP Server

Related Screenshots:
- `14-vsftpd-service-removal.png`
- `15-telnet-service-removal.png`
- `16-apache-service-removal.png`

### Post-Hardening Validation

SMB access restrictions successfully reduced exposure.

Related Screenshot:
- `18-post-hardening-smb-access-denied.png`

---

## Overall Detection Assessment

The environment demonstrated several high-risk detection opportunities involving:

- Weak authentication controls
- Insecure legacy protocols
- Sensitive file exposure
- Privileged account misuse
- Anonymous network access
- Excessive service exposure

The remediation activities improved defensive visibility and reduced opportunities for unauthorized access and lateral movement.
