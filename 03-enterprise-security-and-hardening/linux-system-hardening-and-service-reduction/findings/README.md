# Findings

## Critical Findings

### Anonymous FTP Access Enabled

The FTP service permitted anonymous authentication access, allowing unauthorized users to interact with exposed files on the target system.

#### Risk
- Unauthorized file access
- Sensitive data exposure
- Information disclosure
- Potential malware upload opportunities

#### Evidence
- Successful anonymous FTP authentication
- Accessible file listing visibility
- Remote file retrieval operations

Related Screenshots:
- `02-anonymous-ftp-login.png`
- `03-passwd-file-download.png`
- `04-shadow-file-download.png`

---

### Sensitive Credential File Exposure

Sensitive Linux authentication files were retrievable through exposed services.

#### Exposed Files
- `/etc/passwd`
- `/etc/shadow`

#### Risk
- Offline password cracking
- Credential disclosure
- Privilege escalation preparation
- Authentication compromise

Related Screenshots:
- `03-passwd-file-download.png`
- `04-shadow-file-download.png`
- `05-shadow-hash-review.png`

---

### Weak Password Detection

Extracted password hashes were successfully cracked using offline password attacks.

#### Risk
- Unauthorized authentication access
- Credential reuse exposure
- Lateral movement risk
- Privileged account compromise

#### Validation
Password cracking activity identified weak passwords through John the Ripper.

Related Screenshot:
- `06-john-password-cracking-results.png`

---

### Root SSH Authentication Exposure

The system allowed direct root account authentication through SSH.

#### Risk
- Full system compromise
- Remote administrative abuse
- Increased brute-force attack exposure
- Privilege escalation simplification

Related Screenshot:
- `07-root-ssh-access-validation.png`

---

### Telnet Service Exposure

The Telnet service permitted plaintext authentication access.

#### Risk
- Credential interception
- Session hijacking
- Insecure remote administration
- Lack of encrypted communication

Related Screenshot:
- `08-telnet-insecure-login.png`

---

### Default Apache Web Exposure

The Apache HTTP service remained publicly accessible with default configuration visibility.

#### Risk
- Web service reconnaissance
- Version disclosure
- Additional attack surface exposure
- Misconfiguration visibility

Related Screenshot:
- `09-default-apache-web-page.png`

---

### SMB Share Misconfiguration

SMB shares allowed unauthorized enumeration and file write activity.

#### Risk
- Unauthorized file access
- Malware staging
- Lateral movement opportunities
- Data manipulation

#### Validation
SMB shares allowed remote visibility and unauthorized file write operations.

Related Screenshots:
- `10-anonymous-smb-share-enumeration.png`
- `11-unauthorized-smb-file-write.png`

---

### Duplicate UID 0 Account Presence

An unauthorized account was configured with UID 0 privileges.

#### Risk
- Hidden root-equivalent access
- Persistence mechanism abuse
- Privilege escalation
- Administrative bypass

Related Screenshot:
- `12-duplicate-uid-zero-account-review.png`

---

## Post-Remediation Findings

### Service Exposure Reduction

Several unnecessary services were removed during remediation activities.

Removed Services:
- VSFTPD
- Telnet
- Apache HTTP Server

Related Screenshots:
- `14-vsftpd-service-removal.png`
- `15-telnet-service-removal.png`
- `16-apache-service-removal.png`

---

### Improved SMB Access Restrictions

Post-hardening validation confirmed reduced SMB accessibility.

Related Screenshot:
- `18-post-hardening-smb-access-denied.png`

---

## Overall Assessment

The system initially contained multiple high-risk security weaknesses involving:

- Weak service exposure
- Sensitive credential disclosure
- Weak authentication controls
- Excessive remote access exposure
- Insecure legacy protocols
- Privilege escalation risks

Hardening activities significantly reduced attack surface exposure and improved the overall defensive posture of the Linux environment.
