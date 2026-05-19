# Investigation Findings

## Evidence Source Findings

The forensic image was successfully loaded in E01 format and processed through the Autopsy forensic analysis platform. Evidence metadata validation confirmed filesystem accessibility and sector-level volume visibility during the investigation workflow.

---

## NTFS Volume Observations

The investigation identified an NTFS partition structure containing allocated and unallocated volume space. Volume inspection confirmed sector allocation visibility and accessible filesystem artifact review through the forensic browser interface.

Observed analysis areas included:

- NTFS partition structure
- Sector allocation visibility
- Volume metadata review
- Filesystem navigation accessibility

![NTFS Volume Details](../screenshots/03-ntfs-volume-details.png)

---

## Registry Artifact Findings

Registry hive inspection identified accessible NTUSER.DAT artifacts within the evidence source. The investigation reviewed both parsed and hexadecimal representations of the registry hive to validate low-level artifact visibility and evidence accessibility.

Observed forensic visibility included:

- Registry hive accessibility
- Parsed registry content review
- Hexadecimal artifact inspection
- Raw binary visibility

### Parsed Registry Visibility

![NTUSER.DAT Text Analysis](../screenshots/04-ntuser-dat-text-analysis.png)

### Hexadecimal Artifact Visibility

![NTUSER.DAT Hex Analysis](../screenshots/05-ntuser-dat-hex-analysis.png)

---

## Artifact Categorization Findings

Autopsy successfully parsed and categorized multiple artifact types from the evidence source, including:

- Image artifacts
- Video artifacts
- Office document artifacts

The categorized evidence structure improved investigation visibility and streamlined evidence navigation during analysis activities.

### Image Artifact Visibility

![Image Artifact Review](../screenshots/06-image-artifact-review.png)

### Video Artifact Visibility

![Video Artifact Review](../screenshots/07-video-artifact-analysis.png)

### Office Document Visibility

![Office Document Analysis](../screenshots/08-office-document-analysis.png)

---

## Document Content Findings

Recovered office documents contained accessible parsed text content through Autopsy parsing functionality. The investigation confirmed successful content extraction and readable textual visibility from recovered document artifacts.

![Document Content Review](../screenshots/09-document-content-review.png)

---

## Tagged Evidence Findings

Relevant artifacts were tagged during investigation activities to support reporting workflows and evidence correlation processes.

Tagged evidence handling improved:

- Investigation organization
- Artifact prioritization
- Reporting correlation
- Evidence tracking workflows

![Tagged Evidence Workflow](../screenshots/10-tagged-artifact-workflow.png)

---

## Reporting Findings

The investigation successfully generated structured HTML forensic reporting output from tagged artifacts within the case.

Report generation validated:

- Tagged artifact inclusion
- Evidence reporting workflows
- Structured forensic output generation
- Artifact correlation visibility

### Forensic Report Overview

![Forensic Report Overview](../screenshots/11-forensic-report-overview.png)

### Tagged Evidence Reporting

![Tagged Evidence Report](../screenshots/12-tagged-evidence-report.png)

---

## Investigation Summary

The forensic review successfully demonstrated:

- E01 evidence ingestion workflows
- NTFS filesystem visibility
- Registry artifact accessibility
- Artifact categorization functionality
- Document parsing visibility
- Tagged evidence handling
- Structured forensic reporting workflows

The investigation also demonstrated how forensic tooling can improve evidence navigation, artifact correlation, and reporting efficiency during disk image analysis operations.
