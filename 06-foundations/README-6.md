# Course 6 — Sound the Alarm: Detection & Response

**Platform:** Google Cybersecurity Professional Certificate, Coursera  
**Duration:** ~19 hours

---

## What This Course Covers

How to detect security incidents, investigate alerts, and respond using the full incident response lifecycle.

---

## Key Topics

### Incident Response Lifecycle (NIST)

```
Preparation → Detection & Analysis → Containment, Eradication & Recovery → Post-Incident Activity
```

| Phase | Key Actions |
|-------|------------|
| **Preparation** | Build IR team, write playbooks, set up monitoring tools |
| **Detection & Analysis** | Identify alerts, verify real vs false positive, assess scope |
| **Containment** | Isolate affected systems, stop spread |
| **Eradication** | Remove malware, patch vulnerability, close access |
| **Recovery** | Restore from clean backups, return to normal operations |
| **Post-Incident** | Write lessons-learned report, update playbooks |

### SIEM Tools

**SIEM (Security Information and Event Management)** collects logs from all sources and correlates them to detect threats.

- **Splunk** — Industry-leading SIEM; uses SPL (Search Processing Language)
- **Google Chronicle** — Cloud-native SIEM; uses UDM (Unified Data Model)

Example Splunk query:
```spl
index=main sourcetype=auth action=failure
| stats count by src_ip
| where count > 10
| sort -count
```

### Intrusion Detection Systems (IDS)

- **NIDS** (Network IDS) — Monitors network traffic (e.g. Suricata, Snort)
- **HIDS** (Host IDS) — Monitors individual device activity
- **Signature-based** — Matches known attack patterns
- **Anomaly-based** — Flags deviation from baseline behavior

### Incident Handler Journal

During this course, students maintain an Incident Handler Journal — a running log of incidents analyzed, tools used, and lessons learned. Entries cover:

- **Ransomware attack analysis** — Phishing email → malware execution → encryption → ransom demand
- **Unauthorized access investigation** — Reviewing logs to trace attacker path
- **Phishing incident response** — Following playbook from detection to user notification

### Network Traffic Analysis

Using Wireshark and tcpdump to capture and analyze packets:
- Identify unusual outbound connections (data exfiltration indicators)
- Spot port scans (attacker reconnaissance)
- Detect DNS queries to suspicious domains
- Identify brute force login attempts

---

## Skills Gained
`Incident response` `SIEM (Splunk, Chronicle)` `IDS/IPS` `Log analysis` `Wireshark` `tcpdump` `Playbooks` `Threat detection` `Security operations`
