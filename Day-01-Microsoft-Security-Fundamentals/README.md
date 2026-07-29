# Day 1 – Microsoft Security Fundamentals

## Objectives

* Understand the purpose of the SC-200 certification.
* Learn the Microsoft Security ecosystem.
* Understand the role of Microsoft Defender XDR.
* Differentiate between incidents and alerts.
* Learn about assets, identities, devices, and mailboxes.
* Get introduced to Kusto Query Language (KQL).

---

# Section 1 – SC-200 Overview

## What is SC-200?

SC-200 is the Microsoft Security Operations Analyst certification that validates the skills required to detect, investigate, respond to, and remediate cyber threats using Microsoft security solutions such as Microsoft Defender XDR and Microsoft Sentinel.

---

## Who Should Take SC-200?

This certification is designed for:

* Security Operations Center (SOC) Analysts
* Cybersecurity Analysts
* Incident Responders
* Threat Hunters
* Security Engineers working with Microsoft security technologies

It is ideal for professionals who want to build or advance their careers in Microsoft-based Security Operations.

---

## Major Microsoft Security Products Covered

The SC-200 certification focuses on the following Microsoft security solutions:

* Microsoft Sentinel
* Microsoft Defender XDR
* Microsoft Defender for Endpoint
* Microsoft Defender for Office 365
* Microsoft Defender for Identity
* Microsoft Defender for Cloud Apps

These products work together to provide threat detection, investigation, response, and threat hunting capabilities across an organization's environment.

---

## Skills Measured

The SC-200 certification develops the skills required to:

* Monitor security alerts and incidents
* Perform alert triage and investigations
* Respond to and remediate security incidents
* Perform threat hunting using Kusto Query Language (KQL)
* Analyze threats across Microsoft security products
* Automate security operations using Microsoft technologies

---

## Why is SC-200 Important?

Organizations using Microsoft security solutions require analysts who can effectively investigate and respond to cyber threats. SC-200 demonstrates practical knowledge of Microsoft Defender XDR, Microsoft Sentinel, KQL, and modern Security Operations Center (SOC) workflows.

---

## Microsoft Security Products Covered

| Product                           | Purpose                                                                                                           |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Microsoft Sentinel                | Cloud-native SIEM and SOAR platform used for monitoring, threat detection, investigation, and response.           |
| Microsoft Defender XDR            | Unified Extended Detection and Response (XDR) platform that correlates alerts across Microsoft security products. |
| Microsoft Defender for Endpoint   | Endpoint Detection and Response (EDR) solution for protecting Windows, Linux, macOS, Android, and iOS devices.    |
| Microsoft Defender for Office 365 | Protects email, Teams, SharePoint, and OneDrive from phishing, malware, and malicious links.                      |
| Microsoft Defender for Identity   | Detects identity-based attacks such as Pass-the-Hash, Kerberoasting, and lateral movement in Active Directory.    |
| Microsoft Defender for Cloud Apps | Provides Cloud Access Security Broker (CASB) capabilities to monitor and secure cloud applications.               |

---

## Key Takeaways

* SC-200 is Microsoft's Security Operations Analyst certification.
* Microsoft Sentinel is Microsoft's SIEM and SOAR platform.
* Microsoft Defender XDR provides unified threat detection and response.
* KQL is the primary language used for threat hunting and log analysis.
* SC-200 focuses on practical SOC operations using Microsoft security technologies.

---

## Interview Questions

### 1. What is SC-200?

SC-200 is a Microsoft certification that validates the skills required to detect, investigate, respond to, and remediate cyber threats using Microsoft security solutions.

### 2. Who should take SC-200?

SOC Analysts, Cybersecurity Analysts, Incident Responders, Threat Hunters, and professionals working with Microsoft security technologies.

### 3. What Microsoft products are covered in SC-200?

* Microsoft Sentinel
* Microsoft Defender XDR
* Microsoft Defender for Endpoint
* Microsoft Defender for Office 365
* Microsoft Defender for Identity
* Microsoft Defender for Cloud Apps

### 4. What skills are measured?

* Security monitoring
* Alert triage
* Incident investigation
* Threat hunting using KQL
* Threat response
* Security automation

---

# Section 2 – Microsoft Security Ecosystem

## Microsoft Entra ID

Microsoft Entra ID (formerly Azure Active Directory) is Microsoft's cloud-based Identity and Access Management (IAM) service. It manages users, groups, devices, authentication, and authorization across cloud and on-premises resources. It provides security capabilities such as Multi-Factor Authentication (MFA), Single Sign-On (SSO), Conditional Access, and Identity Protection.

---

## Microsoft Defender XDR

Microsoft Defender XDR (Extended Detection and Response) is Microsoft's unified detection and response platform. It correlates security signals from endpoints, identities, email, cloud applications, and other Microsoft security services into a single incident, enabling SOC analysts to investigate and respond efficiently.

### Key Features

* Cross-domain threat correlation
* Unified incident management
* Automated investigation and response
* Attack timeline visualization

---

## Microsoft Sentinel

Microsoft Sentinel is Microsoft's cloud-native SIEM and SOAR platform. It collects security telemetry from Microsoft products, third-party security tools, cloud services, and on-premises infrastructure. It provides centralized monitoring, threat detection, threat hunting using KQL, investigation, and automated response through playbooks.

### Key Features

* Centralized log collection
* Threat detection and analytics
* KQL-based threat hunting
* Automated response using Playbooks
* Integration with Microsoft and third-party security solutions

---

# Security Concepts

## SIEM vs XDR

| SIEM                                     | XDR                                                           |
| ---------------------------------------- | ------------------------------------------------------------- |
| Collects logs from multiple data sources | Collects security telemetry from integrated security products |
| Provides centralized visibility          | Provides cross-domain threat correlation                      |
| Detects suspicious activities            | Automatically correlates related attacks                      |
| Supports long-term investigations        | Focuses on rapid detection and response                       |

---

## SIEM vs SOAR

| SIEM                                     | SOAR                                 |
| ---------------------------------------- | ------------------------------------ |
| Collects and analyzes security logs      | Automates investigation and response |
| Generates alerts                         | Executes predefined playbooks        |
| Supports threat detection                | Reduces manual analyst effort        |
| Provides visibility into security events | Performs automated remediation       |

---

## EDR vs XDR

| EDR                              | XDR                                                                                |
| -------------------------------- | ---------------------------------------------------------------------------------- |
| Protects endpoint devices        | Protects endpoints, identities, email, cloud apps, and integrated security sources |
| Endpoint-focused detection       | Cross-domain threat detection                                                      |
| Investigates endpoint activities | Correlates attacks across multiple security domains                                |
| Limited to endpoints             | Provides organization-wide visibility                                              |

---

## Alert

An **alert** is a notification generated by a security product when suspicious or malicious activity is detected based on predefined detection rules or analytics.

---

## Incident

An **incident** is a collection of one or more related alerts that together represent a single security attack or campaign requiring investigation and response.

---

# Attack Flow Example

```text
Phishing Email
      │
      ▼
Microsoft Defender for Office 365
      │
      ▼
Alert Generated
      │
      ▼
User Clicks Malicious Link
      │
      ▼
Credential Theft
      │
      ▼
Microsoft Defender for Identity
      │
      ▼
Alert Generated
      │
      ▼
Malware Executes on Endpoint
      │
      ▼
Microsoft Defender for Endpoint
      │
      ▼
Alert Generated
      │
      ▼
Microsoft Defender XDR
      │
      ▼
Correlates Multiple Alerts
      │
      ▼
Single Incident
      │
      ▼
Microsoft Sentinel
      │
      ▼
Threat Hunting • Analytics • Automation • Incident Response
```

---

## Key Learnings

* Microsoft Entra ID manages identities and access.
* Microsoft Defender XDR correlates related alerts into a single incident.
* Microsoft Sentinel provides enterprise-wide SIEM and SOAR capabilities.
* Alerts represent individual detections, while incidents group related alerts into one investigation.
* Defender XDR focuses on real-time detection and response, while Microsoft Sentinel provides centralized monitoring, long-term analytics, threat hunting, and automation.

---

## Interview Questions

### 1. What is Microsoft Entra ID?

Microsoft Entra ID is Microsoft's cloud-based Identity and Access Management (IAM) service that manages identities, authentication, authorization, and secure access to applications and resources.

### 2. What is Microsoft Defender XDR?

Microsoft Defender XDR is Microsoft's unified Extended Detection and Response platform that correlates security signals from multiple Microsoft security products into a single incident for efficient investigation and response.

### 3. What is Microsoft Sentinel?

Microsoft Sentinel is Microsoft's cloud-native SIEM and SOAR platform that collects security data, detects threats, supports threat hunting using KQL, and automates incident response.

### 4. What is the difference between SIEM and XDR?

SIEM centralizes log collection and analysis from multiple sources, while XDR correlates security telemetry across integrated security products to provide faster detection and response.

### 5. What is the difference between SIEM and SOAR?

SIEM focuses on collecting, analyzing, and detecting threats from security logs, whereas SOAR automates investigation, orchestration, and response using predefined playbooks.

### 6. What is the difference between EDR and XDR?

EDR protects endpoint devices by detecting and responding to endpoint threats. XDR extends protection across endpoints, identities, email, cloud applications, and other integrated security domains.

### 7. What is an Alert?

An alert is a notification generated by a security product when suspicious or malicious activity is detected.

### 8. What is an Incident?

An incident is a collection of related alerts that together represent a single security attack requiring investigation and response.

### 9. How does a phishing email become an alert?

A phishing email is analyzed by Microsoft Defender for Office 365. If malicious content is detected, an alert is generated. If the attack progresses, additional alerts may be generated by Defender for Identity and Defender for Endpoint. Microsoft Defender XDR correlates these related alerts into a single incident.

### 10. Why do organizations use both Microsoft Defender XDR and Microsoft Sentinel?

Organizations use Microsoft Defender XDR for real-time detection, investigation, and automated response across Microsoft security products. Microsoft Sentinel complements Defender XDR by providing centralized SIEM and SOAR capabilities, long-term log retention, threat hunting, analytics, third-party integrations, and automation.

---

## References

* Microsoft Learn – SC-200 Learning Path
* Microsoft Defender XDR Documentation
* Microsoft Sentinel Documentation
* Microsoft Learn – Kusto Query Language (KQL)

---

# Status

* ✅ Section 1 – SC-200 Overview
* ✅ Section 2 – Microsoft Security Ecosystem
* ⏳ Section 3 – Microsoft Defender XDR Architecture (Next)
