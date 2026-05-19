# Investigation Notes

## Assessment Context

This assessment focused on reviewing Windows and Linux security configurations to identify insecure authentication settings, exposed legacy services, weak firewall configurations, and insufficient audit visibility across multiple operating systems.

The workflow emphasized authentication hardening, audit monitoring, exposure reduction, and post-remediation verification activities commonly associated with defensive security operations.

---

## Assessment Methodology

The assessment followed a structured workflow consisting of:

1. Windows authentication review
2. Local security policy analysis
3. Interactive logon configuration review
4. Audit logging validation
5. Linux exposure enumeration
6. Telnet exposure validation
7. Account management review
8. Firewall hardening implementation
9. Post-remediation verification

The methodology prioritized defensive visibility and remediation validation rather than offensive exploitation activities.

---

## Windows Authentication Notes

Windows authentication controls were reviewed using local authentication enforcement settings and interactive logon configuration analysis.

Observed review areas included:

- Credential enforcement visibility
- Interactive logon configuration
- Local policy accessibility
- Authentication workflow visibility

The assessment reinforced the importance of enforcing secure local authentication controls within Windows environments.

![Netplwiz Enforcement](../screenshots/01-netplwiz-login-enforcement.png)

---

## Local Security Policy Notes

Windows Local Security Policy settings were reviewed to assess authentication-related configurations and hardening visibility.

The review demonstrated visibility into:

- Security configuration management
- Local authentication settings
- Interactive logon controls
- Administrative policy visibility

![Security Policy Navigation](../screenshots/02-local-security-policy-navigation.png)

---

## Interactive Logon Notes

Interactive logon settings were reviewed to validate authentication messaging and user notification visibility.

A warning banner was configured to reinforce acceptable use awareness and improve login workflow visibility.

### Interactive Logon Policy Review

![Interactive Logon Policy](../screenshots/03-interactive-logon-policy-review.png)

### Warning Banner Configuration

![Warning Banner Configuration](../screenshots/04-warning-banner-configuration.png)

### Login Warning Validation

![Login Warning Banner](../screenshots/05-login-warning-banner.png)

---

## Audit Logging Notes

Audit failure logging policies were enabled to improve authentication monitoring visibility within Windows Event Viewer logs.

The assessment demonstrated how authentication auditing improves visibility into:

- Failed login activity
- Unauthorized access attempts
- Account validation behavior
- Security event generation

### Audit Failure Policy

![Audit Failure Policy](../screenshots/06-audit-failure-policy-enabled.png)

### Event Viewer Visibility

![Event Viewer Audit Failures](../screenshots/07-event-viewer-audit-failures.png)

---

## Linux Exposure Notes

Initial Linux enumeration identified multiple exposed services prior to hardening activities.

The assessment highlighted the operational risks associated with:

- Legacy services
- Plaintext authentication protocols
- Excessive exposed ports
- Insecure remote administration methods

![Initial Port Exposure](../screenshots/08-zenmap-initial-open-ports.png)

---

## Telnet Exposure Notes

The Linux environment exposed Telnet services using insecure plaintext authentication transmission.

The assessment demonstrated how Telnet exposure increases risk associated with:

- Credential interception
- Unencrypted traffic visibility
- Unauthorized remote access
- Legacy protocol exploitation

The workflow reinforced the importance of replacing Telnet with encrypted remote administration protocols such as SSH.

![Telnet Access Review](../screenshots/09-telnet-insecure-login.png)

---

## Linux Account Management Notes

Linux user account creation and identity validation activities were reviewed using local account management workflows.

Observed administrative review areas included:

- User creation validation
- Account visibility
- Local identity management
- Administrative account monitoring

![Linux User Validation](../screenshots/10-linux-user-creation-validation.png)

---

## Authentication Log Review Notes

Linux authentication logs were reviewed to validate visibility into account-related activities and authentication events.

The review demonstrated how authentication logs improve visibility into:

- User activity
- Administrative actions
- Login events
- Account modifications

![Authentication Log Review](../screenshots/11-auth-log-review.png)

---

## Firewall Hardening Notes

iptables firewall rules were implemented to reduce exposed network services and restrict unnecessary inbound access visibility.

The hardening workflow applied:

- Default deny filtering
- Service-specific allow rules
- Exposure reduction controls
- Inbound traffic restrictions

### Default DROP Policy

![Default DROP Policy](../screenshots/12-iptables-default-drop-policy.png)

### HTTP Allow Rule

![HTTP Allow Rule](../screenshots/13-iptables-http-allow-rule.png)

---

## Post-Remediation Verification Notes

Post-hardening network rescanning confirmed reduced exposure visibility after firewall configuration changes.

The reassessment validated:

- Reduced exposed ports
- Improved network filtering
- Successful remediation enforcement
- Reduced attack surface visibility

![Post-Hardening Port Scan](../screenshots/14-post-hardening-port-scan.png)

---

## Tooling Observations

The assessment demonstrated how common administrative and security tools provide visibility into:

- Authentication controls
- Audit logging
- Exposed services
- Firewall behavior
- Account activity
- Exposure reduction verification

The workflow also demonstrated the operational value of combining:

- Enumeration
- Configuration review
- Hardening
- Logging validation
- Reassessment

within defensive security operations.

---

## Assessment Limitations

This assessment focused on authentication security, audit visibility, and firewall hardening activities within a controlled lab environment.

The assessment did not include:

- Enterprise SIEM integration
- Endpoint detection engineering
- Malware analysis
- Memory forensics
- Threat hunting
- Large-scale infrastructure management
- Cloud security monitoring

---

## Analyst Notes

The assessment demonstrated how weak authentication controls, insecure legacy services, and insufficient firewall restrictions can increase attack surface visibility across Windows and Linux systems.

The workflow also reinforced the operational importance of audit visibility, exposure reduction, authentication monitoring, and post-remediation validation during defensive security operations.
