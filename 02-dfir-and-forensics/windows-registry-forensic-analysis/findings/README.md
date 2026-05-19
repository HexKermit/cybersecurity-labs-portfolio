# Investigation Findings

## Summary

The investigation identified multiple registry-based forensic artifacts associated with operating system configuration, local account data, startup execution behavior, network configuration, and user-specific registry activity within the Windows environment.

Cross-hive analysis correlated:
- SAM account artifacts
- startup application entries
- services and drivers
- TCP/IP configuration data
- shell folder artifacts
- user-level registry entries

The investigation significantly improved forensic visibility into registry-based operating system artifacts and user-related configuration behavior.

---

# Key Findings

## 1. Registry Hive Acquisition Findings

Registry acquisition successfully collected multiple offline Windows registry hives for forensic analysis.

Acquired artifacts included:
- SAM
- SECURITY
- SOFTWARE
- SYSTEM
- NTUSER.DAT

Offline acquisition improved forensic preservation and reduced dependence on live-system registry analysis.

---

## 2. Local Account Enumeration Findings

SAM analysis identified multiple local accounts and built-in Windows accounts.

Observed artifacts included:
- Administrator account
- Guest account
- user SID information
- account-related registry entries

The investigation improved visibility into local account structure and user-related forensic evidence.

---

## 3. Startup Application Findings

Registry analysis identified startup-related application entries associated with automatic execution behavior.

Observed artifacts included:
- startup Run entries
- OneDrive startup execution
- user-level startup configuration
- registry-linked startup paths

Startup analysis improved visibility into automatic execution behavior and persistence-related registry artifacts.

---

## 4. Operating System Configuration Findings

SOFTWARE hive analysis identified:
- Windows installation information
- operating system metadata
- installation timestamps
- configuration-related registry entries

The investigation improved visibility into operating system deployment artifacts and installation-related forensic evidence.

---

## 5. System Configuration Findings

SYSTEM hive analysis identified:
- services and drivers
- network adapter configuration
- DHCP configuration artifacts
- TCP/IP-related registry entries

The investigation improved visibility into system-level registry configuration and network-related forensic artifacts.

---

## 6. User Hive Findings

NTUSER.DAT analysis identified:
- shell folder paths
- user startup entries
- profile-related configuration artifacts
- user-specific registry behavior

User hive analysis improved forensic visibility into profile-level operating system activity and user configuration behavior.

---

## 7. Registry Validation Findings

Regedit validation analysis confirmed:
- registry path consistency
- locale configuration artifacts
- network interface registry values
- registry structure visibility

Validation analysis improved confidence in offline registry artifact interpretation and forensic consistency.

---

# Artifact Correlation

The investigation correlated:
- SAM account data
- SOFTWARE hive artifacts
- SYSTEM configuration data
- NTUSER.DAT user artifacts
- startup-related registry entries
- network-related registry configuration

Cross-hive correlation significantly improved investigative visibility into Windows operating system behavior and registry-based forensic evidence.

---

# Investigation Impact

The investigation demonstrated how:
- offline registry analysis
- hive correlation
- startup artifact analysis
- account enumeration
- system configuration review
- user hive analysis

can significantly improve forensic visibility during DFIR investigations and incident response workflows.

---

# Analyst Assessment

The investigation reinforced the importance of analyzing multiple registry hives rather than relying on isolated registry artifacts alone.

Combining SAM analysis, SOFTWARE analysis, SYSTEM analysis, and NTUSER.DAT review significantly improved visibility into:
- user accounts
- startup execution behavior
- operating system configuration
- network configuration artifacts
- user profile activity
- registry-based forensic evidence

Layered registry forensic analysis significantly strengthened investigative accuracy and DFIR visibility.
