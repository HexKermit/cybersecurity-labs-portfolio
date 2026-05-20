# Investigation Findings

## Active Directory Administration Findings

The assessment validated successful access to the Active Directory Users and Computers (ADUC) management environment used for centralized domain administration.

The review confirmed visibility into:

- Domain objects
- Organizational Units (OU)
- User management workflows
- Administrative hierarchy structure

#### ADUC Console Visibility

![ADUC Console](../screenshots/01-aduc-console-launch.png)

---

## Organizational Unit Findings

An Organizational Unit (OU) named for administrative grouping was successfully created within the Active Directory domain structure.

The OU implementation demonstrated:

- Administrative segmentation
- Policy scoping capability
- User grouping management
- Delegated administration structure

#### Organizational Unit Creation

![OU Creation](../screenshots/02-organizational-unit-creation.png)

---

## Domain User Provisioning Findings

Multiple domain users were provisioned within the managed OU structure to simulate enterprise identity management workflows.

The assessment validated successful:

- User object creation
- Domain account provisioning
- OU-based account placement
- Identity administration workflows

### Creeper User Provisioning

![Creeper User](../screenshots/03-ad-user-creation-creeper.png)

### Zombie User Provisioning

![Zombie User](../screenshots/04-ad-user-creation-zombie.png)

### Steve User Provisioning

![Steve User](../screenshots/05-ad-user-creation-steve.png)

---

## Group Policy Management Findings

The Group Policy Management Console (GPMC) was successfully used to review and modify enterprise policy configurations.

The assessment demonstrated visibility into:

- Domain-level policy management
- Enterprise policy inheritance
- Administrative configuration workflows
- Security policy administration

### Group Policy Management Console

![GPMC](../screenshots/06-group-policy-management-console.png)

### Default Domain Policy Editing

![Default Domain Policy](../screenshots/07-default-domain-policy-editing.png)

---

## Password Policy Findings

The Default Domain Policy was modified to enforce stronger password security requirements across domain-managed systems.

The assessment confirmed:

- Increased minimum password length
- Domain-wide password enforcement
- Improved authentication hardening
- Centralized password policy management

### Password Policy Review

![Password Policy Review](../screenshots/08-password-policy-review.png)

### Minimum Password Enforcement

![Password Enforcement](../screenshots/09-minimum-password-policy-enforcement.png)

---

## Organizational Unit Policy Findings

An OU-level Group Policy Object (GPO) was created and linked to the Organizational Unit structure.

The policy restricted user access to Control Panel functionality.

The assessment demonstrated:

- OU-specific policy enforcement
- Administrative restriction workflows
- Centralized configuration management
- User behavior restriction capability

### OU Group Policy Creation

![OU GPO Creation](../screenshots/10-ou-group-policy-creation.png)

### Control Panel Policy Review

![Control Panel Policy](../screenshots/11-control-panel-policy-review.png)

### Restriction Policy Enabled

![Restriction Policy](../screenshots/12-control-panel-restriction-policy-enabled.png)

---

## Group Policy Propagation Findings

Policy refresh operations successfully propagated updated Group Policy settings across managed systems.

The assessment validated:

- Successful GPO propagation
- Policy refresh operations
- Updated configuration enforcement
- Administrative policy deployment

### Group Policy Refresh Validation

![GPUpdate Validation](../screenshots/13-group-policy-refresh-validation.png)

---

## Administrative Group Assignment Findings

Domain group assignments were reviewed and modified to validate administrative permission workflows.

The assessment demonstrated visibility into:

- Privileged group assignment
- Administrative delegation
- Access management workflows
- Domain permission structures

### Backup Operators Assignment

![Backup Operators](../screenshots/14-backup-operators-group-assignment.png)

---

## Restriction Enforcement Findings

The configured OU-level policy successfully restricted user access to Control Panel functionality during validation activities.

The enforcement demonstrated:

- Successful GPO application
- User restriction enforcement
- Administrative control effectiveness
- Policy inheritance validation

### Restriction Enforcement Validation

![Restriction Enforcement](../screenshots/15-control-panel-restriction-enforcement.png)

---

## Investigation Summary

The assessment successfully demonstrated:

- Active Directory administration
- Organizational Unit management
- Enterprise user provisioning
- Group Policy administration
- Password hardening enforcement
- OU-level policy restrictions
- Administrative permission workflows
- Policy propagation validation

The investigation also reinforced the operational importance of centralized policy management, identity administration, and enterprise security enforcement within Active Directory environments.
