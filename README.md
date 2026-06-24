# Threat Intelligence Enrichment Lab

## Overview

This project documents a practical threat intelligence enrichment workflow used to investigate suspicious indicators of compromise (IOCs), including hashes, URLs, domains, and IP addresses.

The goal of this lab was to simulate how a SOC Analyst Tier 1 would validate suspicious artifacts using public threat intelligence platforms such as MalwareBazaar, VirusTotal, AbuseIPDB, and URLHaus.

This project focuses on the investigation process, documentation, and decision-making rather than only the final result.

---

## Objective

The main objectives of this lab were to:

* Identify suspicious indicators from a security investigation.
* Validate file hashes using MalwareBazaar and VirusTotal.
* Check IP addresses and URLs against public threat intelligence sources.
* Document findings clearly for incident reporting.
* Practice a SOC-style enrichment workflow.

---

## Tools Used

* MalwareBazaar
* VirusTotal
* URLHaus
* AbuseIPDB
* Splunk
* Windows Event Logs
* Sysmon
* PowerShell Logs

---

## Investigation Workflow

The investigation followed this process:

1. Collected suspicious indicators from lab activity.
2. Checked SHA256 hashes in MalwareBazaar.
3. Verified reputation and detections in VirusTotal.
4. Checked suspicious URLs using URLHaus.
5. Checked IP reputation using AbuseIPDB.
6. Documented whether each indicator was malicious, suspicious, clean, or not found.
7. Summarised findings and lessons learned.

---

## Example Finding

During the investigation, a SHA256 hash was searched in MalwareBazaar using the correct syntax:

```text
sha256:<hash>
```

One sample was identified as related to the Mirai malware family.

The result showed:

* File type: ELF
* Malware family: Mirai
* Tags: elf, mirai

This type of result suggests the file may be associated with Linux-based malware commonly targeting IoT devices such as routers, cameras, or embedded systems.

---

## Key SOC Skills Demonstrated

This project demonstrates:

* IOC enrichment
* Threat intelligence analysis
* Malware reputation checking
* Basic malware family identification
* Evidence-based documentation
* SOC investigation workflow
* Clear reporting for security teams

---

## Lessons Learned

This lab helped reinforce the importance of using the correct search syntax when working with threat intelligence platforms.

For example, MalwareBazaar requires specific prefixes such as:

```text
sha256:<hash>
md5:<hash>
signature:<malware_family>
tag:<tag>
```

A failed search does not always mean an indicator is safe. It may simply mean the indicator is not present in that specific database at the time of analysis.

---

## Conclusion

This project simulates a realistic SOC Tier 1 workflow for enriching suspicious indicators using open-source threat intelligence platforms.

The main value of this lab is not only identifying malicious indicators, but also documenting the investigation process clearly and professionally.
