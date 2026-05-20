# Enterprise Active Directory Policy Hardening

## Overview

This project documents an Active Directory security administration and Group Policy hardening workflow performed within a Windows Server enterprise domain environment.

The assessment focused on organizational unit (OU) administration, domain user provisioning, password policy enforcement, Group Policy Object (GPO) management, and restriction validation activities designed to improve administrative control and reduce insecure user behavior across domain-managed systems.

The workflow demonstrates practical Windows enterprise administration and security policy management operations commonly associated with identity management and defensive system hardening.

---

## Investigation Scope

The assessment focused on the following administrative and security areas:

- Active Directory Users and Computers (ADUC) administration
- Organizational Unit (OU) creation
- Domain user provisioning workflows
- Default Domain Policy review
- Password policy hardening
- Group Policy Object (GPO) administration
- User restriction enforcement
- Policy propagation validation
- Administrative group assignment review

---

## Tools Used

| Tool | Purpose |
|------|----------|
| Active Directory Users and Computers (ADUC) | Domain user and OU administration |
| Group Policy Management Console (GPMC) | Enterprise policy management |
| Windows Server 2008 | Domain controller environment |
| Command Prompt | Administrative validation and policy refresh |
| Group Policy Editor | Security policy configuration |

---

## Analysis Areas

### Active Directory Administration

The environment was reviewed through Active Directory Users and Computers (ADUC) to validate domain visibility and organizational management workflows.

#### ADUC Console Launch

![ADUC Console](screenshots/01-aduc-console-launch.png)

---

### Organizational Unit Management

An Organizational Unit (OU) structure was created to support policy separation and administrative grouping of managed domain users.

#### Organizational Unit Creation

![OU Creation](screenshots/02-organizational-unit-creation.png)

---

### Domain User Provisioning

Multiple domain users were provisioned within the managed OU structure to simulate enterprise identity administration workflows.

#### Creeper User Creation

![Creeper User](screenshots/03-ad-user-creation-creeper.png)

#### Zombie User Creation

![Zombie User](screenshots/04-ad-user-creation-zombie.png)

#### Steve User Creation

![Steve User](screenshots/05-ad-user-creation-steve.png)

---

### Group Policy Management

The Group Policy Management Console (GPMC) was used to review and modify domain-level policy configurations.

#### Group Policy Management Console

![GPMC](screenshots/06-group-policy-management-console.png)

#### Default Domain Policy Editing

![Default Domain Policy](screenshots/07-default-domain-policy-editing.png)

---

### Password Policy Hardening

Password security controls were reviewed and strengthened through domain password policy configuration.

#### Password Policy Review

![Password Policy Review](screenshots/08-password-policy-review.png)

#### Minimum Password Enforcement

![Password Enforcement](screenshots/09-minimum-password-policy-enforcement.png)

---

### Organizational Unit Policy Restrictions

A dedicated OU-level policy was created to restrict Control Panel access for managed users within the OU scope.

#### OU Group Policy Creation

![OU GPO Creation](screenshots/10-ou-group-policy-creation.png)

#### Control Panel Policy Review

![Control Panel Policy](screenshots/11-control-panel-policy-review.png)

#### Restriction Policy Enabled

![Restriction Policy](screenshots/12-control-panel-restriction-policy-enabled.png)

---

### Policy Propagation Validation

Policy refresh operations were performed to validate successful GPO propagation across managed systems.

#### Group Policy Refresh Validation

![GPUpdate Validation](screenshots/13-group-policy-refresh-validation.png)

---

### Administrative Group Assignment Review

Domain user group assignments were reviewed and modified to validate administrative permission workflows.

#### Backup Operators Assignment

![Backup Operators](screenshots/14-backup-operators-group-assignment.png)

---

### Restriction Enforcement Validation

Restriction enforcement was validated through controlled user interaction with restricted operating system functionality.

#### Control Panel Restriction Enforcement

![Restriction Enforcement](screenshots/15-control-panel-restriction-enforcement.png)

---

## Key Findings

- Successfully created and managed Organizational Units (OU)
- Provisioned multiple domain-managed user accounts
- Reviewed and modified domain password security policies
- Enforced minimum password length requirements
- Created OU-level Group Policy restrictions
- Validated successful Group Policy propagation
- Confirmed Control Panel restriction enforcement
- Reviewed administrative group assignment workflows

---

## Defensive Value

This project demonstrates practical enterprise administration and defensive hardening workflows associated with:

- Active Directory administration
- Group Policy management
- Password security enforcement
- Identity and access management
- Organizational policy segmentation
- Administrative control validation
- User restriction enforcement
- Enterprise Windows hardening

---

## Environment Details

| Component | Details |
|-----------|---------|
| Operating System | Windows Server 2008 |
| Environment Type | Active Directory Domain |
| Management Platform | Group Policy Management |
| Authentication Model | Domain-Based Authentication |
| Investigation Type | Enterprise Policy Hardening |

---

## Analyst Assessment

The assessment demonstrated how centralized Group Policy administration can improve enterprise security visibility and enforce consistent user restrictions across managed systems.

The workflow also highlighted the operational importance of password hardening, policy propagation validation, organizational segmentation, and administrative access management within enterprise Windows environments.
