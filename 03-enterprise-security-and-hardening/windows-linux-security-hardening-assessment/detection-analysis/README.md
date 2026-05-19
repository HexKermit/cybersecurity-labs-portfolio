# Detection Analysis

## Detection Visibility Overview

This assessment focused on improving defensive visibility across Windows and Linux environments through authentication monitoring, audit policy review, network exposure analysis, and firewall hardening validation.

The workflow demonstrated how security configuration reviews and post-remediation verification activities improve operational visibility and reduce exposed attack surface conditions.

---

## Windows Authentication Visibility

Authentication enforcement settings were reviewed to validate secure login requirements and reduce unauthorized local access exposure.

Authentication controls are operationally important because weak local login protections may increase:

- Unauthorized workstation access
- Shared credential abuse
- Local privilege misuse
- Authentication bypass risk

![Netplwiz Enforcement](../screenshots/01-netplwiz-login-enforcement.png)

---

## Local Security Policy Visibility

Windows Local Security Policy configurations were reviewed to assess visibility into authentication-related controls and system hardening posture.

The review demonstrated how policy visibility supports:

- Security baseline validation
- Authentication enforcement
- Local hardening review
- Administrative configuration auditing

![Security Policy Navigation](../screenshots/02-local-security-policy-navigation.png)

---

## Interactive Logon Monitoring

Interactive logon policy settings were reviewed to validate user notification visibility during authentication workflows.

Security warning banners help improve:

- User awareness
- Acceptable use visibility
- Administrative policy communication
- Login event consistency

![Interactive Logon Policy](../screenshots/03-interactive-logon-policy-review.png)

---

## Authentication Banner Validation

The configured login warning banner was validated during authentication workflows to confirm successful policy implementation.

This demonstrated visibility into:

- Authentication policy enforcement
- User notification controls
- Security messaging workflows

![Login Warning Banner](../screenshots/05-login-warning-banner.png)

---

## Audit Logging Visibility

Audit failure policies were enabled to improve authentication monitoring visibility within Windows security logs.

Audit logging provides defensive value through visibility into:

- Failed authentication attempts
- Credential validation activity
- Unauthorized access attempts
- Security investigation workflows

![Audit Failure Policy](../screenshots/06-audit-failure-policy-enabled.png)

---

## Event Viewer Security Analysis

Windows Event Viewer logs successfully captured failed authentication activity after audit configuration changes.

The review confirmed visibility into:

- Authentication failures
- Security event generation
- Account validation activity
- Login-related events

Detection opportunities include:

- Failed login alerting
- Brute-force attempt monitoring
- Authentication anomaly detection
- User activity correlation

![Event Viewer Audit Failures](../screenshots/07-event-viewer-audit-failures.png)

---

## Linux Exposure Visibility

Initial Linux network enumeration identified exposed services prior to firewall hardening activities.

The assessment demonstrated how exposed legacy services increase:

- External visibility
- Unauthorized access opportunities
- Remote attack surface exposure
- Operational security risk

![Initial Port Exposure](../screenshots/08-zenmap-initial-open-ports.png)

---

## Telnet Exposure Analysis

The Linux environment exposed Telnet authentication services using plaintext credential transmission.

This exposure created elevated risk associated with:

- Credential interception
- Insecure remote administration
- Legacy protocol exposure
- Unencrypted authentication traffic

Detection opportunities include:

- Telnet traffic monitoring
- Legacy protocol detection
- Plaintext authentication alerts
- Remote access auditing

![Telnet Access Review](../screenshots/09-telnet-insecure-login.png)

---

## Linux Account Activity Visibility

Linux account creation and user validation activities were reviewed to assess local account management visibility.

Authentication logs and user validation workflows provide operational value through:

- User activity visibility
- Administrative auditing
- Account lifecycle monitoring
- Authentication tracking

![Linux User Validation](../screenshots/10-linux-user-creation-validation.png)

---

## Authentication Log Monitoring

Linux authentication logs were reviewed to validate account activity visibility and administrative event monitoring.

Authentication logs improve defensive visibility into:

- User authentication events
- Account modifications
- Administrative actions
- Privileged activity tracking

![Authentication Log Review](../screenshots/11-auth-log-review.png)

---

## Firewall Hardening Analysis

iptables firewall rules were implemented to reduce unnecessary inbound access visibility and improve network filtering controls.

The firewall configuration demonstrated:

- Reduced exposed service visibility
- Improved inbound filtering
- Access restriction enforcement
- Network segmentation concepts

### Default DROP Policy

![Default DROP Policy](../screenshots/12-iptables-default-drop-policy.png)

### HTTP Allow Rule

![HTTP Allow Rule](../screenshots/13-iptables-http-allow-rule.png)

---

## Post-Hardening Exposure Verification

Post-remediation rescanning confirmed successful reduction of exposed services after firewall hardening implementation.

The reassessment validated:

- Reduced attack surface visibility
- Improved filtering effectiveness
- Successful remediation enforcement
- Exposure reduction verification

![Post-Hardening Port Scan](../screenshots/14-post-hardening-port-scan.png)

---

## Security Operations Relevance

This assessment demonstrated several defensive security concepts associated with:

- Authentication monitoring
- Audit visibility
- Windows policy review
- Legacy protocol exposure analysis
- Linux authentication logging
- Firewall hardening
- Exposure reduction validation
- Post-remediation reassessment workflows

These workflows are operationally relevant during:

- Security operations reviews
- Hardening initiatives
- Exposure management assessments
- Defensive monitoring activities
- Post-remediation validation procedures

---

## Detection Assessment

The assessment demonstrated how authentication monitoring, audit logging, exposure reduction, and firewall hardening workflows improve defensive visibility across Windows and Linux systems.

The investigation also reinforced the operational importance of continuous reassessment, audit visibility, and network exposure management during defensive security operations.
