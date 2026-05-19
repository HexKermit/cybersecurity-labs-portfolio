# Investigation Findings

## Windows Authentication Findings

The assessment reviewed local Windows authentication enforcement settings to validate whether interactive logon protections were properly configured.

The review identified the importance of enforcing credential-based authentication workflows to reduce unauthorized local access exposure.

![Netplwiz Enforcement](../screenshots/01-netplwiz-login-enforcement.png)

---

## Local Security Policy Findings

Windows Local Security Policy configurations were reviewed to assess authentication visibility, local security settings, and interactive logon configuration exposure.

The assessment demonstrated how local policy configuration directly impacts:

- Authentication security
- User interaction controls
- Audit visibility
- System hardening posture

![Security Policy Navigation](../screenshots/02-local-security-policy-navigation.png)

---

## Interactive Logon Findings

Interactive logon policy settings were reviewed to validate authentication messaging and user notification visibility during login workflows.

The review confirmed that authentication warning banners can improve:

- User awareness
- Security policy visibility
- Acceptable use notification
- Administrative compliance visibility

![Interactive Logon Policy](../screenshots/03-interactive-logon-policy-review.png)

---

## Warning Banner Configuration Findings

A warning banner was successfully configured through Local Security Policy settings.

The configuration demonstrated implementation of user-facing authentication notices commonly used to reinforce acceptable use policies within enterprise environments.

![Warning Banner Configuration](../screenshots/04-warning-banner-configuration.png)

---

## Logon Warning Validation Findings

Authentication workflows successfully displayed the configured warning banner during login validation activities.

The validation confirmed successful implementation of interactive logon notification controls.

![Login Warning Banner](../screenshots/05-login-warning-banner.png)

---

## Audit Policy Findings

Audit failure policies were enabled to improve failed authentication visibility within Windows security logs.

The assessment highlighted the operational importance of enabling audit logging for:

- Failed authentication attempts
- Credential validation visibility
- Security monitoring
- Incident investigation support

![Audit Failure Policy](../screenshots/06-audit-failure-policy-enabled.png)

---

## Event Viewer Findings

Windows Event Viewer logs successfully captured failed authentication activity after audit policy configuration.

The review confirmed visibility into:

- Failed authentication attempts
- Account validation activity
- Security event logging
- Audit event generation

![Event Viewer Audit Failures](../screenshots/07-event-viewer-audit-failures.png)

---

## Linux Exposure Findings

Initial Linux network enumeration identified multiple exposed services prior to hardening activities.

The assessment confirmed externally visible network exposure conditions associated with insecure service configurations.

![Initial Port Exposure](../screenshots/08-zenmap-initial-open-ports.png)

---

## Telnet Exposure Findings

The assessment confirmed insecure Telnet authentication exposure within the Linux environment.

Observed risks included:

- Plaintext authentication exposure
- Insecure remote administration
- Credential interception risk
- Legacy protocol exposure

The review reinforced the importance of replacing insecure legacy protocols with encrypted alternatives.

![Telnet Access Review](../screenshots/09-telnet-insecure-login.png)

---

## Linux User Validation Findings

Linux account creation and identity validation activities were successfully reviewed using local account enumeration workflows.

The assessment demonstrated visibility into:

- Local user management
- Account creation validation
- User identity verification
- Authentication management workflows

![Linux User Validation](../screenshots/10-linux-user-creation-validation.png)

---

## Authentication Log Findings

Linux authentication logs were reviewed to validate authentication activity visibility and account-related event logging.

The review confirmed that authentication logs provide valuable visibility into:

- Account activity
- Authentication events
- User management actions
- Administrative operations

![Authentication Log Review](../screenshots/11-auth-log-review.png)

---

## Firewall Hardening Findings

iptables firewall configurations were implemented to reduce exposed services and restrict inbound network access.

The assessment confirmed:

- Reduced attack surface visibility
- Improved inbound access restrictions
- Enhanced network filtering controls
- Improved service exposure management

### Default DROP Policy

![Default DROP Policy](../screenshots/12-iptables-default-drop-policy.png)

### HTTP Allow Rule

![HTTP Allow Rule](../screenshots/13-iptables-http-allow-rule.png)

---

## Post-Hardening Verification Findings

Post-remediation network rescanning confirmed reduced port exposure visibility after firewall hardening activities.

The reassessment validated successful exposure reduction and improved network restriction enforcement.

![Post-Hardening Port Scan](../screenshots/14-post-hardening-port-scan.png)

---

## Investigation Summary

The assessment successfully demonstrated:

- Windows authentication security review
- Local security policy analysis
- Authentication audit logging
- Event visibility validation
- Linux exposure enumeration
- Insecure protocol review
- Firewall hardening implementation
- Post-remediation verification workflows

The assessment also reinforced the operational importance of reducing attack surface visibility, improving audit monitoring, and validating remediation effectiveness during defensive security operations.
