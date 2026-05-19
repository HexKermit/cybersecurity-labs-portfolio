# Detection Analysis and Registry Artifact Correlation

## Overview

This section documents the forensic analysis methodologies, registry artifact correlation techniques, and defensive visibility observations identified during the Windows registry forensic investigation.

The investigation focused on correlating:
- offline registry hives
- startup-related registry entries
- SAM account artifacts
- operating system configuration data
- TCP/IP registry artifacts
- services and drivers
- user-specific registry activity

Cross-hive analysis significantly improved forensic visibility into Windows operating system behavior and registry-based forensic evidence.

---

# Detection Analysis Areas

## 1. Registry Acquisition Analysis

Registry acquisition analysis focused on securely obtaining offline Windows registry hives for forensic investigation purposes.

Observed acquisition artifacts included:
- SAM hive acquisition
- SOFTWARE hive acquisition
- SYSTEM hive acquisition
- NTUSER.DAT acquisition
- exported registry file validation

Offline acquisition workflows improved forensic preservation and reduced dependence on live-system registry analysis.

---

## 2. SAM Artifact Analysis

SAM analysis identified multiple account-related registry artifacts associated with local user enumeration.

Observed indicators included:
- local user accounts
- built-in Windows accounts
- SID-related registry data
- account enumeration artifacts

SAM analysis improved visibility into account-related forensic evidence and local authentication structures.

---

## 3. Startup Execution Analysis

Registry analysis identified startup-related execution behavior associated with automatic application launch activity.

Observed indicators included:
- Run registry entries
- startup application paths
- OneDrive startup execution
- user-level startup artifacts

Startup analysis improved visibility into automatic execution behavior and registry-linked startup activity.

---

## 4. Operating System Configuration Analysis

SOFTWARE hive analysis identified operating system configuration artifacts associated with Windows installation and application behavior.

Observed artifacts included:
- Windows installation metadata
- operating system version details
- installed application information
- startup application configuration

The investigation improved visibility into operating system deployment artifacts and software-related registry evidence.

---

## 5. System Configuration Analysis

SYSTEM hive analysis identified:
- services configuration artifacts
- driver-related registry entries
- TCP/IP configuration data
- DHCP-related registry artifacts
- network adapter information

System analysis improved visibility into system-level operating system configuration and network-related forensic evidence.

---

## 6. User Hive Analysis

NTUSER.DAT analysis identified:
- shell folder paths
- startup-related user entries
- user profile configuration artifacts
- profile-level registry behavior

User hive analysis significantly improved visibility into user-specific operating system activity and profile-related forensic evidence.

---

## 7. Registry Validation Analysis

Validation analysis compared offline registry findings against live registry structures using Regedit.

Observed validation areas included:
- locale configuration artifacts
- network interface registry entries
- registry path consistency
- registry structure verification

Validation workflows improved confidence in forensic artifact interpretation and registry consistency analysis.

---

# Artifact Correlation Workflow

The investigation correlated:
- SAM account artifacts
- startup-related registry entries
- SOFTWARE hive configuration data
- SYSTEM hive network artifacts
- NTUSER.DAT user activity
- validation-based registry review

Cross-hive correlation significantly improved investigative visibility into Windows registry behavior and forensic artifact relationships.

---

# Detection Considerations

Defenders should monitor for:
- anomalous startup Run entries
- unexpected user startup applications
- suspicious services configuration
- unusual TCP/IP registry changes
- unauthorized account-related registry activity
- profile-level persistence artifacts
- anomalous registry modification behavior

Combining registry artifact correlation with defensive investigation workflows significantly improves DFIR visibility.

---

# Defensive Investigation Value

This investigation demonstrated how layered registry forensic analysis techniques improve:
- startup artifact visibility
- account investigation workflows
- operating system configuration analysis
- user activity visibility
- network configuration analysis
- registry-based forensic correlation
- DFIR operational workflows

Cross-hive analysis significantly strengthened investigative accuracy and forensic visibility.

---

# Analyst Assessment

The investigation reinforced the importance of correlating multiple registry hives rather than relying on isolated registry artifacts alone.

Combining SAM analysis, SOFTWARE analysis, SYSTEM analysis, NTUSER.DAT review, and registry validation workflows significantly improved forensic visibility into:
- operating system behavior
- startup execution activity
- account-related artifacts
- network configuration evidence
- user-specific registry activity

Layered registry forensic analysis significantly strengthens investigative context during DFIR investigations and incident response operations.
