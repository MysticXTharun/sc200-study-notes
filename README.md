# Microsoft SC-200 Study Notes

## About This Repository

This repository documents my preparation for the **Microsoft SC-200: Security Operations Analyst Associate** certification.

It serves as both:

* A structured SC-200 study tracker
* A collection of revision notes
* A record of hands-on Microsoft security labs
* A cybersecurity portfolio demonstrating practical SOC skills

## Exam Information

| Item               | Details                                         |
| ------------------ | ----------------------------------------------- |
| Certification      | Microsoft Security Operations Analyst Associate |
| Exam               | SC-200                                          |
| Exam Date          | 14 August 2026                                  |
| Preparation Period | 28 July 2026 – 13 August 2026                   |
| Current Status     | In Progress                                     |

## Background

I have approximately **1.5 years of Security Operations Center experience** involving:

* SIEM alert monitoring and triage
* Security incident investigation
* Threat hunting
* Root-cause analysis
* Detection-rule development and tuning
* False-positive reduction
* MITRE ATT&CK mapping
* Incident documentation and reporting

My previous experience includes tools such as:

* IBM QRadar
* Splunk
* Wazuh
* Elastic Stack
* Microsoft Defender for Endpoint
* CrowdStrike Falcon
* Palo Alto firewall logs
* Windows Event Logs
* Linux authentication logs

This study plan focuses on expanding my experience into the Microsoft security ecosystem, particularly **Microsoft Sentinel, Microsoft Defender XDR, and Kusto Query Language**.

## Study Objectives

The main objectives of this study plan are to:

* Understand the Microsoft security ecosystem
* Configure and manage Microsoft Sentinel
* Understand Microsoft Defender XDR components
* Investigate alerts and incidents
* Write KQL queries for log analysis
* Perform proactive threat hunting
* Use threat intelligence during investigations
* Create and tune analytics rules
* Understand automation rules and playbooks
* Prepare for scenario-based SC-200 exam questions

## Microsoft Security Technologies Covered

* Microsoft Sentinel
* Microsoft Defender XDR
* Microsoft Defender for Endpoint
* Microsoft Defender for Office 365
* Microsoft Defender for Identity
* Microsoft Defender for Cloud Apps
* Microsoft Defender for Cloud
* Microsoft Entra ID Protection
* Kusto Query Language
* Azure Logic Apps
* Microsoft Security Copilot fundamentals

## Study Plan

|  Day | Date      | Main Topic                                 | Practical Work                                                               | Status      |
| ---: | --------- | ------------------------------------------ | ---------------------------------------------------------------------------- | ----------- |
|    1 | 28 July   | SC-200 and Microsoft Security Fundamentals | Explore Microsoft Defender portal and write basic KQL queries                | Completed   |
|    2 | 29 July   | Microsoft Sentinel Fundamentals            | Create or explore a Sentinel workspace and understand its architecture       | In Progress |
|    3 | 30 July   | Data Collection and Connectors             | Study data connectors, tables, agents, DCRs and ingestion methods            | Not Started |
|    4 | 31 July   | KQL Fundamentals                           | Practise `search`, `where`, `project`, `sort`, `take` and `distinct`         | Not Started |
|    5 | 1 August  | Intermediate KQL                           | Practise `summarize`, `extend`, `parse`, `join`, `union` and time filters    | Not Started |
|    6 | 2 August  | Sentinel Analytics and Incidents           | Study analytics rules, entity mapping, alert grouping and incident creation  | Not Started |
|    7 | 3 August  | Microsoft Defender XDR                     | Explore alerts, incidents, assets, identities, devices and mailboxes         | Not Started |
|    8 | 4 August  | Microsoft Defender for Endpoint            | Study device onboarding, alert investigation, timelines and response actions | Not Started |
|    9 | 5 August  | Defender for Office 365 and Identity       | Investigate phishing, malicious email and identity-related alerts            | Not Started |
|   10 | 6 August  | Defender for Cloud Apps and Cloud          | Study cloud-app discovery, risky activities and cloud workload protection    | Not Started |
|   11 | 7 August  | Incident Investigation and Response        | Investigate a complete incident and document the response process            | Not Started |
|   12 | 8 August  | Threat Hunting                             | Create hunting queries and map suspicious activity to MITRE ATT&CK           | Not Started |
|   13 | 9 August  | Threat Intelligence                        | Work with indicators, watchlists, enrichment and IOC investigation           | Not Started |
|   14 | 10 August | Automation and Playbooks                   | Study automation rules, Logic Apps, triggers and response actions            | Not Started |
|   15 | 11 August | Hands-on Practice                          | Complete Sentinel, Defender XDR and KQL investigation scenarios              | Not Started |
|   16 | 12 August | Practice Assessment                        | Complete a mock exam and review incorrect answers                            | Not Started |
|   17 | 13 August | Final Revision                             | Revise weak areas, important KQL commands and investigation workflows        | Not Started |
| Exam | 14 August | SC-200 Certification Exam                  | Final exam                                                                   | Scheduled   |

## Day 1 Topics

Day 1 covers the foundation required for the remaining study plan:

* Overview of the SC-200 certification
* Role of a Security Operations Analyst
* Microsoft security ecosystem
* Microsoft Defender XDR
* Microsoft Defender portal
* Difference between events, alerts and incidents
* Security entities and assets
* Users and identities
* Devices and endpoints
* Email and mailboxes
* Introduction to Microsoft Sentinel
* Introduction to Kusto Query Language

## Daily Study Routine

| Activity                           | Recommended Time |
| ---------------------------------- | ---------------: |
| Theory and Microsoft Learn modules |          2 hours |
| Practical lab                      |        1–2 hours |
| KQL practice                       |           1 hour |
| Notes and GitHub documentation     |    30–45 minutes |
| Practice questions and revision    |    30–45 minutes |

## Repository Structure

```text
sc200-study-notes/
├── README.md
├── Day-01-Security-Fundamentals/
├── Day-02-Microsoft-Sentinel/
├── Day-03-Data-Connectors/
├── Day-04-KQL-Fundamentals/
├── Day-05-Intermediate-KQL/
├── Day-06-Analytics-and-Incidents/
├── Day-07-Defender-XDR/
├── Day-08-Defender-for-Endpoint/
├── Day-09-Office-365-and-Identity/
├── Day-10-Cloud-Apps-and-Cloud/
├── Day-11-Incident-Response/
├── Day-12-Threat-Hunting/
├── Day-13-Threat-Intelligence/
├── Day-14-Automation-and-Playbooks/
├── Day-15-Hands-on-Labs/
├── Day-16-Practice-Assessment/
├── Day-17-Final-Revision/
├── KQL-Queries/
├── Practice-Questions/
└── Screenshots/
```

## KQL Topics

The following KQL concepts will be practised during the preparation:

### Basic Operators

* `search`
* `where`
* `project`
* `project-away`
* `take`
* `limit`
* `sort`
* `distinct`

### Data Analysis

* `summarize`
* `count`
* `countif`
* `dcount`
* `extend`
* `case`
* `iff`

### Data Correlation

* `join`
* `union`
* `lookup`
* `let`

### Time and String Operations

* `ago()`
* `between`
* `bin()`
* `contains`
* `has`
* `startswith`
* `endswith`
* `parse`
* `extract`

## Hands-on Lab Goals

During this study plan, I aim to complete the following practical activities:

* Explore the Microsoft Defender portal
* Configure or explore a Microsoft Sentinel workspace
* Understand Log Analytics tables
* Connect security data sources
* Investigate Microsoft Sentinel incidents
* Investigate Defender XDR incidents
* Analyse endpoint and identity alerts
* Investigate phishing emails
* Write KQL detection queries
* Create scheduled analytics rules
* Perform threat hunting
* Enrich indicators of compromise
* Map detections to MITRE ATT&CK
* Create automation rules
* Understand incident-response playbooks

## Incident Investigation Workflow

For each practical incident, I will follow this investigation process:

1. Review the alert name and description.
2. Identify the affected user, host, IP address or mailbox.
3. Review the incident timeline.
4. Analyse the relevant logs.
5. Validate the indicators of compromise.
6. Correlate related alerts and entities.
7. Determine whether the activity is malicious or benign.
8. Map the activity to MITRE ATT&CK.
9. Assign severity and classification.
10. Recommend containment and remediation actions.
11. Document the investigation findings.
12. Close or escalate the incident.

## Documentation Format

Each study-day folder will contain:

* Topic overview
* Important concepts
* Investigation workflow
* KQL queries
* Practical lab steps
* Screenshots
* Key exam points
* Interview-related questions
* Daily revision summary

## Progress Summary

| Category                        | Progress    |
| ------------------------------- | ----------- |
| Microsoft Security Fundamentals | Completed   |
| Microsoft Sentinel              | Not Started |
| Microsoft Defender XDR          | Not Started |
| KQL                             | Not Started |
| Incident Investigation          | Not Started |
| Threat Hunting                  | Not Started |
| Threat Intelligence             | Not Started |
| Automation                      | Not Started |
| Practice Assessments            | Not Started |

## Related Cybersecurity Projects

My practical cybersecurity portfolio also includes:

* Wazuh SIEM Detection Engineering Lab
* Windows Threat-Hunting Dashboard
* Ransomware Early-Warning Dashboard
* Phishing Email Investigation Dashboard
* IOC Enrichment Tool
* MITRE ATT&CK Coverage Dashboard

These projects support my SC-200 preparation by strengthening my knowledge of log analysis, incident investigation, threat detection, IOC enrichment and security automation.

## Expected Outcome

By completing this study plan, I aim to:

* Pass the Microsoft SC-200 certification exam
* Improve my Microsoft Sentinel and Defender XDR skills
* Strengthen my KQL knowledge
* Perform structured security investigations
* Build practical Microsoft security projects
* Prepare for SOC Analyst and Microsoft Security Operations roles

## Author

**Sai Tharun**

* GitHub: [MysticXTharun](https://github.com/MysticXTharun)
* Career Focus: SOC Operations, SIEM, Microsoft Sentinel, Threat Hunting and Incident Response
* Certification Status: Microsoft SC-200 — In Progress
