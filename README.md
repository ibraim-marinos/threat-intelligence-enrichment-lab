# Threat Intelligence Enrichment Lab

This project documents a Threat Intelligence Enrichment investigation performed during a Home SOC Lab exercise.

The investigation began after a suspicious PowerShell download alert was identified. Multiple Indicators of Compromise (IOCs) were extracted and enriched using multiple open-source threat intelligence platforms to determine whether the activity was associated with known malicious infrastructure.

---

# Project Overview

This investigation demonstrates how multiple Threat Intelligence platforms can be used together to enrich Indicators of Compromise (IOCs), validate findings, correlate intelligence, and support analyst decision-making.

The investigation focuses on three primary IOC types:

- IP Address
- Domain
- SHA256 File Hash

Threat intelligence was gathered from multiple public intelligence platforms and correlated to produce a final analyst assessment.

---

# Objectives

- Investigate suspicious Indicators of Compromise (IOCs)
- Perform Threat Intelligence enrichment
- Correlate findings from multiple intelligence sources
- Validate IP, domain and file hash reputation
- Assess overall security risk
- Document investigation findings
- Simulate a SOC Tier 1 investigation workflow

---

# Technologies Used

- Splunk SIEM
- Windows Event Logs
- PowerShell Operational Logs
- VirusTotal
- AbuseIPDB
- URLHaus
- MalwareBazaar

---

# Investigation Workflow

```text
Alert Detection
        │
IOC Extraction
        │
IP Reputation Analysis
        │
Domain Reputation Analysis
        │
File Hash Analysis
        │
Threat Intelligence Correlation
        │
Risk Assessment
        │
Final Verdict
```

---

# Key Findings

## IP Analysis

- VirusTotal reported no malicious detections.
- AbuseIPDB reported no abuse reports.
- Overall assessment: **Low Risk**

---

## Domain Analysis

- VirusTotal identified multiple detections.
- URLHaus listed the domain as malware infrastructure.
- Overall assessment: **High Risk**

---

## File Hash Analysis

- VirusTotal detected the sample as malicious.
- Associated with the Mamont Android Banking Trojan family.
- Overall assessment: **Malicious**

---

## MalwareBazaar

- No matching records were found.
- No malware family information was available.
- This did not change the overall investigation outcome.

---

# Evidence Collected

The investigation combined evidence from multiple Threat Intelligence sources.

| Indicator | Evidence Summary | Screenshot |
|-----------|------------------|------------|
| IP | VirusTotal reputation analysis | TI-01_VirusTotal_IP |
| IP | AbuseIPDB abuse validation | TI-02_AbuseIPDB_IP |
| Domain | VirusTotal domain reputation | TI-03_VirusTotal_Domain |
| Domain | URLHaus malware infrastructure validation | TI-04_URLHaus_Domain |
| Hash | VirusTotal malware analysis | TI-05_VirusTotal_Hash |
| Hash | MalwareBazaar lookup (No matching records) | TI-06_MalwareBazaar_Hash |

---

# Skills Demonstrated

- Threat Intelligence Enrichment
- IOC Analysis
- Threat Hunting Methodology
- Security Investigation
- Threat Correlation
- Malware Research
- Risk Assessment
- Security Reporting
- SOC Tier 1 Investigation Workflow

---

# Repository Structure

```text
threat-intelligence-enrichment-lab/
│
├── investigation/
│   └── investigation-summary.md
│
├── iocs/
│   └── ioc-list.md
│
├── screenshots/
│   ├── README.md
│   ├── TI-01_VirusTotal_IP.png
│   ├── TI-02_AbuseIPDB_IP.png
│   ├── TI-03_VirusTotal_Domain.png
│   ├── TI-04_URLHaus_Domain.png
│   ├── TI-05_VirusTotal_Hash.png
│   └── TI-06_MalwareBazaar_Hash.png
│
├── README.md
└── threat-intelligence-enrichment-lab.pdf
```

---

# Related Documentation

### Investigation Summary

Contains a high-level summary of the investigation findings.

➡️ investigation/investigation-summary.md

---

### IOC List

Contains all Indicators of Compromise identified during the investigation.

➡️ iocs/ioc-list.md

---

### Investigation Screenshots

Evidence collected during the investigation.

- VirusTotal IP Analysis
- AbuseIPDB IP Validation
- VirusTotal Domain Analysis
- URLHaus Domain Validation
- VirusTotal Hash Analysis
- MalwareBazaar Hash Lookup

➡️ screenshots/

---

# Full Investigation Report

📄 **Download Full Investigation Report (PDF)**

➡️ [Threat Intelligence Enrichment Report](threat-intelligence-enrichment-lab.pdf)

The PDF contains the complete investigation, screenshots, analyst notes, IOC enrichment process, and final assessment.

---

# Final Verdict

After correlating all Threat Intelligence sources, the identified domain and file hash were assessed as malicious and consistent with known malware infrastructure.

Although MalwareBazaar returned no matching records for the file hash, VirusTotal provided sufficient evidence linking the sample to the Mamont Android Banking Trojan.

This investigation demonstrates how multiple Threat Intelligence platforms can be combined to validate Indicators of Compromise, improve confidence in analyst findings, and support evidence-based security investigations.
