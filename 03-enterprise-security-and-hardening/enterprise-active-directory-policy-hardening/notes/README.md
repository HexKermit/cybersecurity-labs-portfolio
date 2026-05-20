# Investigation Notes

## Assessment Context

This assessment focused on enterprise Active Directory administration and Group Policy hardening activities performed within a Windows domain environment.

The workflow emphasized centralized identity management, password policy enforcement, Organizational Unit (OU) segmentation, and user restriction validation using native Windows enterprise administration tools.

The investigation simulated administrative workflows commonly associated with enterprise Windows infrastructure management and defensive system hardening operations.

---

## Assessment Methodology

The assessment followed a structured administrative workflow consisting of:

1. Active Directory administration review
2. Organizational Unit (OU) creation
3. Domain user provisioning
4. Group Policy review
5. Password policy hardening
6. OU-level policy deployment
7. Group Policy propagation validation
8. Restriction enforcement testing
9. Administrative group assignment review

The methodology prioritized centralized policy enforcement and enterprise administrative visibility rather than offensive security testing.

---

## Active Directory Administration Notes

The environment was reviewed through Active Directory Users and Computers (ADUC) to validate domain administration visibility and enterprise object management workflows.

Observed administration areas included:

- Domain hierarchy visibility
- Organizational Unit structure
- User administration workflows
- Centralized identity management

#### ADUC Console Visibility

![ADUC Console](../screenshots/01-aduc-console-launch.png)

---

## Organizational Unit Notes

An Organizational Unit (OU) was created to provide administrative segmentation and Group Policy targeting capability within the domain environment.

The OU structure demonstrated:

- Administrative organization
- Policy inheritance scoping
- User grouping workflows
- Enterprise segmentation capability

#### Organizational Unit Creation

![OU Creation](../screenshots/02-organizational-unit-creation.png)

---

## User Provisioning Notes

Multiple domain users were provisioned within the OU structure to simulate enterprise identity administration operations.

The workflow demonstrated visibility into:

- Domain account provisioning
- User creation workflows
- Identity management operations
- Enterprise authentication administration

### Creeper User Provisioning

![Creeper User](../screenshots/03-ad-user-creation-creeper.png)

### Zombie User Provisioning

![Zombie User](../screenshots/04-ad-user-creation-zombie.png)

### Steve User Provisioning

![Steve User](../screenshots/05-ad-user-creation-steve.png)

---

## Group Policy Administration Notes

The Group Policy Management Console (GPMC) was used to review and modify enterprise security policies within the Active Directory environment.

The workflow demonstrated visibility into:

- Domain-level policy administration
- Centralized security configuration
- Enterprise hardening management
- Administrative policy deployment

### Group Policy Management Console

![GPMC](../screenshots/06-group-policy-management-console.png)

### Default Domain Policy Editing

![Default Domain Policy](../screenshots/07-default-domain-policy-editing.png)

---

## Password Policy Notes

Password security settings were reviewed and strengthened through domain-level password policy configuration.

The assessment reinforced the importance of:

- Minimum password requirements
- Centralized authentication controls
- Consistent password enforcement
- Enterprise security baselines

### Password Policy Review

![Password Policy Review](../screenshots/08-password-policy-review.png)

### Password Enforcement Validation

![Password Enforcement](../screenshots/09-minimum-password-policy-enforcement.png)

---

## Organizational Restriction Notes

An OU-level Group Policy Object (GPO) was created to restrict access to Control Panel functionality for managed users.

The restriction workflow demonstrated:

- User behavior control
- Administrative enforcement capability
- Centralized configuration restrictions
- Policy inheritance validation

### OU Group Policy Creation

![OU GPO Creation](../screenshots/10-ou-group-policy-creation.png)

### Control Panel Policy Review

![Control Panel Policy](../screenshots/11-control-panel-policy-review.png)

### Restriction Policy Enabled

![Restriction Policy](../screenshots/12-control-panel-restriction-policy-enabled.png)

---

## Policy Propagation Notes

Group Policy refresh operations were used to validate successful policy synchronization and enforcement across managed systems.

The workflow demonstrated visibility into:

- GPO propagation
- Enterprise configuration synchronization
- Administrative deployment validation
- Policy refresh operations

### Group Policy Refresh Validation

![GPUpdate Validation](../screenshots/13-group-policy-refresh-validation.png)

---

## Administrative Group Notes

Administrative group assignments were reviewed and modified to validate permission management workflows within the enterprise environment.

The review demonstrated visibility into:

- Delegated permissions
- Administrative role assignment
- Privileged group management
- Access governance workflows

### Backup Operators Assignment

![Backup Operators](../screenshots/14-backup-operators-group-assignment.png)

---

## Restriction Enforcement Notes

OU-level restrictions were validated through controlled user interaction testing against restricted operating system functionality.

The assessment confirmed successful:

- Restriction inheritance
- Policy enforcement
- User limitation workflows
- Administrative control validation

### Restriction Enforcement Validation

![Restriction Enforcement](../screenshots/15-control-panel-restriction-enforcement.png)

---

## Tooling Observations

The assessment demonstrated how native Windows administration tools provide centralized visibility into:

- Identity management
- Enterprise authentication
- Group Policy administration
- Organizational segmentation
- Restriction enforcement
- Administrative permissions
- Security baseline management

The workflow also demonstrated the operational value of combining:

- Active Directory administration
- Group Policy management
- Password hardening
- Restriction validation
- Policy propagation testing

within enterprise Windows security operations.

---

## Assessment Limitations

This assessment focused on administrative hardening and enterprise policy management activities within a controlled lab environment.

The assessment did not include:

- Enterprise SIEM integration
- Kerberos attack simulation
- Active Directory threat hunting
- Domain controller forensics
- PowerShell attack analysis
- Privilege escalation testing
- Large-scale enterprise infrastructure management

---

## Analyst Notes

The assessment demonstrated how centralized Active Directory administration and Group Policy enforcement improve enterprise security consistency, authentication visibility, and administrative control across Windows domain environments.

The workflow also reinforced the operational importance of password hardening, policy inheritance validation, restriction enforcement, and enterprise identity management during defensive security operations.
