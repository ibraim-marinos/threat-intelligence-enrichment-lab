# Threat Intelligence Enrichment Lab

## Project Overview

This project documents a threat intelligence enrichment investigation performed during a Home SOC Lab exercise.

The investigation began after a suspicious PowerShell download alert was identified. Multiple indicators were extracted and enriched using open-source threat intelligence platforms to determine whether the activity was associated with known malicious infrastructure.

## Objectives

* Investigate suspicious indicators of compromise (IOCs)
* Perform threat intelligence enrichment
* Correlate findings from multiple intelligence sources
* Assess risk and document conclusions
* Simulate a real SOC Tier 1 investigation workflow

## Technologies Used

* Splunk
* VirusTotal
* AbuseIPDB
* URLHaus
* MalwareBazaar
* Windows Event Logs
* PowerShell Logs

## Investigation Workflow

```text
Alert Detection
      ↓
IOC Extraction
      ↓
IP Reputation Analysis
      ↓
Domain Reputation Analysis
      ↓
File Hash Analysis
      ↓
Threat Intelligence Correlation
      ↓
Risk Assessment
      ↓
Final Verdict
```

## Key Findings

### IP Analysis

* VirusTotal: No malicious detections
* AbuseIPDB: No abuse reports identified
* Assessment: Low risk

### Domain Analysis

* VirusTotal: Multiple vendor detections
* URLHaus: Listed as malware distribution infrastructure
* Assessment: High risk

### File Hash Analysis

* VirusTotal: 19/66 detections
* Identified as Android banking trojan activity
* Associated with Mamont malware family
* Assessment: Malicious

### MalwareBazaar

* No matching sample found
* Findings did not change overall assessment

## Investigation Screenshots

| Source        | Evidence                          |
| ------------- | --------------------------------- |
| VirusTotal    | IP reputation analysis            |
| AbuseIPDB     | Community abuse validation        |
| VirusTotal    | Domain reputation analysis        |
| URLHaus       | Malware infrastructure validation |
| VirusTotal    | File hash investigation           |
| MalwareBazaar | Malware repository validation     |

## Skills Demonstrated

* Threat Intelligence Enrichment
* IOC Analysis
* Security Investigation
* Malware Research
* Threat Correlation
* Risk Assessment
* Security Reporting
* SOC Analyst Workflow

## Repository Structure

```text
screenshots/
investigation/
report/
README.md
```

## Final Verdict

After correlating all intelligence sources, the indicators were assessed as malicious and consistent with malware delivery activity.

The investigation demonstrates how multiple threat intelligence platforms can be used together to support evidence-based security decisions.
