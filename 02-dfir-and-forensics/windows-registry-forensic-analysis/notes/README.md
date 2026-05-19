# Investigation Notes

## Investigation Context

This investigation focused on offline Windows Registry forensic analysis within a controlled DFIR lab environment.

The investigation analyzed:
- registry hive acquisition workflows
- SAM account artifacts
- startup-related registry entries
- operating system configuration data
- TCP/IP-related registry artifacts
- user-specific registry activity
- shell folder configuration artifacts
- registry validation workflows

Cross-hive registry analysis significantly improved forensic visibility into operating system behavior, startup execution activity, and user-related configuration artifacts.

---

# Environment Details

| Component | Details |
|---|---|
| Operating System | Windows 10 |
| Investigation Type | DFIR / Registry Forensics |
| Acquisition Tool | FTK Imager |
| Registry Analysis Tool | Windows Registry Recovery (WRR) |
| Validation Tool | Regedit |
| Investigation Environment | Controlled Security Lab |

---

# Analyst Observations

Multiple registry-based forensic artifacts were identified during the investigation process.

Observed artifacts included:
- local account registry data
- SID-related account information
- startup application entries
- services and drivers configuration
- TCP/IP registry artifacts
- shell folder configuration data
- user-specific startup behavior

The investigation demonstrated how Windows Registry analysis can significantly improve visibility into operating system behavior and profile-level forensic evidence.

---

# Registry Acquisition Notes

Offline registry acquisition workflows successfully obtained:
- SAM hive
- SOFTWARE hive
- SYSTEM hive
- SECURITY hive
- NTUSER.DAT user hive

Offline acquisition improved forensic preservation and enabled structured registry analysis without dependence on live-system interaction.

---

# SAM Analysis Notes

SAM analysis identified:
- built-in Windows accounts
- local account enumeration artifacts
- SID-related registry entries
- account-linked forensic evidence

The investigation reinforced the importance of SAM analysis during account-related DFIR investigations and authentication artifact review.

---

# SOFTWARE Hive Notes

SOFTWARE hive analysis improved visibility into:
- Windows installation metadata
- installed application information
- startup-related application entries
- operating system configuration artifacts

Startup application analysis strengthened visibility into automatic execution behavior and registry-linked startup activity.

---

# SYSTEM Hive Notes

SYSTEM hive analysis identified:
- services configuration artifacts
- driver-related registry entries
- network adapter configuration
- TCP/IP-related registry artifacts
- DHCP-related configuration behavior

The investigation improved visibility into system-level operating system configuration and network-related forensic evidence.

---

# NTUSER.DAT Analysis Notes

NTUSER.DAT analysis identified:
- shell folder registry paths
- user startup application entries
- profile-specific configuration artifacts
- user-level registry behavior

User hive analysis significantly improved visibility into profile-related operating system activity and startup-related forensic evidence.

---

# Registry Validation Notes

Validation analysis compared offline registry findings against live registry structures using Regedit.

Validation workflows confirmed:
- registry path consistency
- locale-related registry values
- network interface registry artifacts
- registry structure visibility

Validation analysis improved confidence in registry artifact interpretation and forensic consistency.

---

# Defensive Investigation Insights

The investigation highlighted the importance of:
- offline registry acquisition
- cross-hive forensic correlation
- startup registry visibility
- account-related artifact review
- system configuration analysis
- user hive investigation
- registry validation workflows

Layered registry forensic analysis significantly improves DFIR operational visibility and investigative accuracy.

---

# Operational Considerations

This investigation was performed within a controlled security lab environment for DFIR research and defensive forensic training purposes.

The investigation did not include:
- enterprise SIEM integration
- EDR telemetry correlation
- enterprise-scale incident response infrastructure
- malware reverse engineering
- production threat intelligence enrichment

---

# Analyst Assessment

The investigation reinforced the importance of correlating multiple registry hives rather than relying on isolated registry artifacts alone.

Combining SAM analysis, SOFTWARE review, SYSTEM investigation, NTUSER.DAT analysis, and validation workflows significantly improved visibility into:
- operating system behavior
- startup execution activity
- account-related artifacts
- user configuration behavior
- network-related registry evidence
- profile-level forensic artifacts

Layered registry forensic analysis significantly strengthened investigative context and DFIR operational visibility.
