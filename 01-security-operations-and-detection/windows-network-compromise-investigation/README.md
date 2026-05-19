# Windows Network Compromise Investigation and Persistence Analysis

![Status](https://img.shields.io/badge/Status-Complete-green)
![Focus](https://img.shields.io/badge/Focus-DFIR%20%7C%20Incident%20Response-blue)
![Tools](https://img.shields.io/badge/Tools-Volatility%20%7C%20Autoruns%20%7C%20DumpIt%20%7C%20Windows-orange)

## Overview

This investigation focused on analyzing indicators of compromise (IOCs), persistence mechanisms, suspicious services, and volatile evidence within a compromised Windows environment.

The lab simulated a defensive incident response workflow involving:
- volatile data collection
- memory acquisition
- persistence investigation
- suspicious service analysis
- startup artifact review
- scheduled task analysis
- network connection investigation

Several suspicious artifacts were identified, including:
- fake Windows binaries
- suspicious scheduled tasks
- unknown Windows services
- startup persistence files
- suspicious outbound network connections

The investigation also demonstrated how memory forensics and persistence analysis can improve threat visibility and support defensive investigation workflows.

---

## Objectives

- Perform volatile data collection
- Capture system memory for forensic analysis
- Investigate suspicious established network connections
- Identify persistence mechanisms
- Analyze suspicious Windows services
- Review startup folder artifacts
- Investigate scheduled task persistence
- Correlate suspicious indicators across multiple artifacts

---

## Tools Used

| Tool | Purpose |
|---|---|
| DumpIt | Volatile memory acquisition |
| Volatility Framework | Memory forensic analysis |
| Autoruns | Persistence artifact investigation |
| Windows Task Scheduler | Scheduled task analysis |
| MSConfig | Service investigation |
| Netstat | Network connection review |
| Windows Explorer | File system investigation |

---

## Investigation Workflow

### 1. Local Administrator Review

Local administrator membership and privileged access visibility were reviewed during the investigation process.

![Local Administrator Review](screenshots/account-analysis/local-administrator-group-review.png)

---

### 2. Volatile Data Collection

Established network connections were reviewed to identify suspicious communication activity and potential suspicious communication indicators.

![Volatile Data Connections](screenshots/volatile-data-analysis/volatile-data-established-connections.png)

---

### 3. Memory Acquisition

System memory was captured using DumpIt to preserve volatile evidence for forensic investigation.

![DumpIt Memory Acquisition](screenshots/memory-analysis/dumpit-memory-acquisition.png)

---

### 4. Memory Forensic Analysis

Volatility netscan analysis identified suspicious established connections associated with unusual executables and remote communication activity.

![Volatility Netscan](screenshots/memory-analysis/volatility-netscan-established-connections.png)

---

### 5. Scheduled Task Persistence Analysis

Suspicious scheduled tasks were reviewed to identify persistence behavior and unauthorized automatic execution activity.

#### Explora Persistence Task

![Explora Persistence](screenshots/task-scheduler-analysis/task-scheduler-explora-persistence.png)

#### Svchost Persistence Task

![Svchost Persistence](screenshots/task-scheduler-analysis/task-scheduler-svchost-persistence.png)

---

### 6. Startup Folder Artifact Analysis

Startup folder contents were reviewed to identify suspicious executables and batch file persistence artifacts.

![Startup Folder Analysis](screenshots/file-system-analysis/startup-folder-suspicious-files.png)

---

### 7. Batch File Persistence Investigation

A suspicious batch file containing remote command execution behavior and external communication indicators was identified during the investigation.

![Batch File Persistence](screenshots/file-system-analysis/batch-file-winhelper-persistence.png)

---

### 8. Suspicious Binary Analysis

Suspicious executables located within the Windows System32 directory were identified and reviewed during file system analysis.

![Suspicious System32 Binaries](screenshots/file-system-analysis/system32-suspicious-binaries.png)

---

### 9. Service Persistence Investigation

Persistence artifacts associated with suspicious Windows services were investigated using Autoruns and service configuration analysis tools.

#### Autoruns Persistence Review

![Autoruns Persistence](screenshots/persistence-analysis/autoruns-suspicious-service-persistence.png)

#### Unknown Service Manufacturer

![MSConfig Service Analysis](screenshots/service-analysis/msconfig-unknown-service-manufacturer.png)

#### Suspicious Service Executable Path

![Suspicious Service Path](screenshots/service-analysis/suspicious-service-executable-path.png)

---

## Key Findings

- Multiple persistence mechanisms were identified across the compromised system
- Suspicious scheduled tasks were configured for automatic execution
- Fake Windows-style executables were identified within sensitive directories
- Suspicious outbound network connections were observed during memory analysis
- Startup folder artifacts indicated unauthorized execution behavior
- Unknown Windows services demonstrated persistence-related indicators
- Memory forensic analysis improved visibility into suspicious process activity

---

## Indicators of Compromise (IOCs)

| IOC Type | Observation |
|---|---|
| Suspicious Binary | svch0st.exe |
| Suspicious Binary | explora.exe |
| Suspicious Binary | winhelper.EXE |
| Suspicious Network Activity | External connections over port 2222 |
| Persistence Mechanism | Scheduled tasks |
| Persistence Mechanism | Startup folder batch files |
| Persistence Mechanism | Suspicious Windows services |

---

## Skills Demonstrated

- Windows incident response
- Volatile data collection
- Memory forensic analysis
- IOC correlation
- Persistence analysis
- Scheduled task investigation
- Service analysis
- Startup artifact investigation
- Defensive investigation workflows
- DFIR documentation

---

## MITRE ATT&CK Mapping

| Technique | ID | Tactic |
|---|---|---|
| Scheduled Task/Job | T1053 | Persistence |
| Boot or Logon Autostart Execution | T1547 | Persistence |
| Windows Service | T1543 | Persistence |
| Masquerading | T1036 | Defense Evasion |
| Command and Scripting Interpreter | T1059 | Execution |
| System Owner/User Discovery | T1033 | Discovery |

---

## Ethical Notice

This investigation was conducted in a controlled lab environment for defensive security training, incident response education, and DFIR skill development purposes only.
