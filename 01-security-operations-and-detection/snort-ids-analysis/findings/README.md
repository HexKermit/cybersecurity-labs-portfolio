# Investigation Findings

## Summary

The Snort IDS successfully detected reconnaissance activity generated through an Nmap fast port scan against the target system.

Multiple IDS alerts were triggered and categorized as suspicious scanning behavior, including TCP and UDP-based probe activity.

The investigation demonstrated how IDS platforms can provide visibility into network reconnaissance attempts and support alert triage workflows in SOC environments.

---

## Key Observations

### 1. Reconnaissance Activity Detection

The IDS identified active network scanning behavior generated from the Kali Linux host.

Observed behaviors included:
- Fast TCP scanning
- Port enumeration attempts
- Repeated connection probes

---

### 2. Alert Correlation

Source and destination traffic analysis improved visibility into suspicious communication patterns and reduced investigation ambiguity.

The IDS dashboard allowed alerts to be grouped and reviewed based on:
- Source address
- Destination address
- Protocol type
- Alert signature

---

### 3. Signature-Based Threat Detection

Snort rules successfully generated alerts associated with:
- TCP filtered port scans
- UDP portsweep activity
- Suspicious reconnaissance traffic

This demonstrated the effectiveness of signature-based intrusion detection in identifying common scanning techniques.

---

### 4. Threat Visibility

The BASE alert interface improved visibility into:
- Suspicious traffic behavior
- Repeated alert activity
- Alert occurrence frequency
- Traffic categorization

---

## Security Impact

Unmonitored reconnaissance activity can help attackers:
- Identify exposed services
- Enumerate network infrastructure
- Discover vulnerable systems
- Prepare for future exploitation attempts

Early detection of scanning behavior improves defensive awareness and incident response readiness.

---

## Analyst Notes

This lab reinforced the importance of:
- IDS alert validation
- Network traffic visibility
- Source and destination correlation
- Signature tuning awareness
- Detection workflow analysis

---

## Detection Engineering Insight

This investigation highlighted the importance of combining IDS signatures, traffic analysis, and alert correlation to improve network threat visibility and reduce false positives in SOC environments.
