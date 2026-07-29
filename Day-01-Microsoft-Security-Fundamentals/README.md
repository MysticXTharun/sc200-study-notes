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

# Section 3 – Microsoft Defender XDR Architecture

## What is Microsoft Defender XDR Architecture?

Microsoft Defender XDR is Microsoft's unified Extended Detection and Response platform. It integrates security signals from endpoints, identities, email, cloud applications, and other Microsoft security services.

It collects and correlates related alerts into a single incident and provides SOC analysts with a centralized platform for investigation, threat hunting, automated response, and attack disruption.

Microsoft Defender XDR can be considered the central brain of the Microsoft security ecosystem because it connects security data from multiple Defender products.

---

## Main Microsoft Defender XDR Products

### Microsoft Defender for Endpoint

Microsoft Defender for Endpoint protects endpoint devices and operating systems, including:

* Windows
* Linux
* macOS
* Android
* iOS

It collects endpoint telemetry such as:

* Process executions
* File activity
* Network connections
* Registry changes
* Malware detections
* Device vulnerabilities

It can also perform response actions such as isolating a device, running an antivirus scan, collecting an investigation package, and initiating live response.

---

### Microsoft Defender for Office 365

Microsoft Defender for Office 365 protects Microsoft 365 communication and collaboration services, including:

* Exchange Online
* Outlook
* Microsoft Teams
* SharePoint
* OneDrive

It detects threats such as:

* Phishing emails
* Malicious attachments
* Malicious links
* Business Email Compromise
* Spam
* Account compromise attempts

---

### Microsoft Defender for Identity

Microsoft Defender for Identity protects on-premises and hybrid identity environments, including:

* Active Directory
* Domain Controllers
* Hybrid identities

It detects identity-based attacks such as:

* Credential theft
* Pass-the-Hash
* Pass-the-Ticket
* Kerberoasting
* Suspicious authentication
* Lateral movement
* Domain reconnaissance

---

### Microsoft Defender for Cloud Apps

Microsoft Defender for Cloud Apps protects Software as a Service and cloud applications.

It helps identify:

* Shadow IT
* Impossible travel
* Suspicious cloud activity
* OAuth application abuse
* Unusual downloads
* Data exfiltration
* Risky cloud applications

---

## Defender XDR Data Flow

```text
User or System Activity
          ↓
Security Event
          ↓
Microsoft Defender Product
          ↓
Alert Generated
          ↓
Microsoft Defender XDR
          ↓
Alert Correlation
          ↓
Single Incident
          ↓
SOC Investigation
          ↓
Containment and Remediation
```

A user or system activity generates security telemetry. The relevant Microsoft Defender product analyzes the activity and generates an alert when suspicious or malicious behavior is detected.

Microsoft Defender XDR collects related alerts from different security domains and correlates them into a single incident representing the complete attack chain.

---

## How Incidents are Created

Microsoft Defender XDR uses its correlation engine to identify relationships between alerts.

It considers information such as:

* Affected users
* Affected devices
* Email messages
* IP addresses
* Processes
* Files
* Attack techniques
* Time of activity

Related alerts are grouped into one incident, allowing analysts to investigate the complete attack rather than reviewing every alert separately.

---

## Example Attack Correlation

```text
Phishing Email
      ↓
Defender for Office 365 Alert
      ↓
Credentials Stolen
      ↓
Defender for Identity Alert
      ↓
Malware Executed
      ↓
Defender for Endpoint Alert
      ↓
Microsoft Defender XDR
      ↓
One Correlated Incident
```

---

## Why Defender XDR Reduces Analyst Workload

Microsoft Defender XDR reduces SOC analyst workload by:

* Correlating related alerts automatically
* Reducing alert fatigue
* Providing a unified attack timeline
* Collecting evidence automatically
* Displaying affected users and devices
* Providing recommended response actions
* Supporting automated investigation
* Supporting automatic attack disruption

Instead of reviewing several unrelated alerts individually, analysts can investigate the complete attack from a single incident.

---

## Interview Questions

### What is Microsoft Defender XDR architecture?

Microsoft Defender XDR is Microsoft's unified Extended Detection and Response architecture. It integrates signals from Defender for Endpoint, Defender for Office 365, Defender for Identity, and Defender for Cloud Apps. It correlates related alerts into a single incident and provides centralized investigation, threat hunting, automated response, and attack disruption capabilities.

### How are incidents created in Microsoft Defender XDR?

Microsoft Defender XDR analyzes relationships between alerts, users, devices, files, processes, emails, IP addresses, and attack techniques. It then correlates related alerts into a single incident representing one attack or campaign.

### Why does Microsoft Defender XDR reduce analyst workload?

It automatically correlates alerts, gathers evidence, provides an attack timeline, identifies affected assets, and recommends response actions. This reduces manual investigation time and helps analysts respond within the required SLA.

---

# Section 4 – Microsoft Defender Portal

## What is the Microsoft Defender Portal?

The Microsoft Defender Portal is a centralized web-based security console where SOC analysts monitor, investigate, hunt, respond to, and remediate security threats across an organization's Microsoft environment.

The portal can be accessed through:

```text
https://security.microsoft.com
```

It provides a single interface for endpoints, identities, email, cloud applications, alerts, incidents, hunting, and response actions.

---

## Major Defender Portal Sections

### Home

The Home page provides a high-level overview of the organization's security environment.

It may display:

* Active incidents
* Active alerts
* Devices at risk
* Security recommendations
* Recent security activities
* Security posture information

---

### Incidents

The Incidents page contains correlated security investigations.

An incident may include:

* One or more related alerts
* Affected users
* Affected devices
* Email messages
* Files
* Processes
* Attack timeline
* Evidence
* MITRE ATT&CK techniques
* Recommended actions

Incidents are generally prioritized because they provide the complete context of an attack.

---

### Alerts

The Alerts page displays individual security detections generated by Microsoft Defender products.

Examples include:

* Suspicious PowerShell activity
* Malware detection
* Phishing email
* Impossible travel
* Credential theft
* Malicious attachment
* Lateral movement

One or more related alerts may be grouped into a single incident.

---

### Assets

The Assets section provides information about entities involved in security activity.

Examples include:

* Devices
* Users
* Identities
* Mailboxes
* IP addresses

Analysts can use asset pages to review risk, alerts, incidents, timelines, logged-on users, software, and other related information.

---

### Action Center

The Action Center displays security response actions performed manually or automatically.

It may include:

* Device isolation
* File quarantine
* Antivirus scans
* User containment
* Investigation actions
* Pending actions
* Completed actions
* Failed actions
* Actions awaiting approval

The Action Center helps analysts verify that containment and remediation actions were successfully completed.

---

### Email and Collaboration

This section is powered by Microsoft Defender for Office 365.

It is used to investigate:

* Phishing emails
* Malicious attachments
* Malicious URLs
* Email campaigns
* Business Email Compromise
* Teams-related threats

---

### Endpoints

This section is powered by Microsoft Defender for Endpoint.

It provides:

* Device inventory
* Device risk information
* Device timelines
* Vulnerability information
* Antivirus status
* Running processes
* Logged-on users
* Response actions

---

### Identity

This section is powered by Microsoft Defender for Identity.

It provides information about:

* User identities
* Domain Controllers
* Authentication activities
* Credential theft
* Lateral movement
* Identity-related alerts

---

### Cloud Apps

This section is powered by Microsoft Defender for Cloud Apps.

It helps monitor:

* SaaS applications
* Cloud activities
* OAuth applications
* Shadow IT
* Suspicious downloads
* Impossible travel
* Data exfiltration

---

### Hunting

The Hunting section is used for proactive threat hunting using Kusto Query Language.

Analysts can search for:

* Suspicious processes
* Failed authentication
* PowerShell abuse
* Malware activity
* Malicious network connections
* Credential theft
* Ransomware behavior

Threat hunting helps identify hidden or previously undetected threats.

---

### Reports

The Reports section provides security metrics and trends, including:

* Incident trends
* Alert trends
* Device exposure
* Security posture
* Threat statistics
* Response performance

---

## Defender Portal Investigation Workflow

```text
Alert Generated
      ↓
Incident Created
      ↓
SOC Analyst Opens Incident
      ↓
Reviews Alerts and Timeline
      ↓
Identifies Affected Assets
      ↓
Investigates Email, Identity and Endpoint
      ↓
Contains the Threat
      ↓
Remediates the Environment
      ↓
Verifies Actions in Action Center
      ↓
Closes the Incident
```

---

## Defender Portal Product Mapping

| Portal Section          | Microsoft Product                    |
| ----------------------- | ------------------------------------ |
| Incidents               | Microsoft Defender XDR               |
| Alerts                  | Microsoft Defender security products |
| Endpoints               | Microsoft Defender for Endpoint      |
| Identity                | Microsoft Defender for Identity      |
| Email and Collaboration | Microsoft Defender for Office 365    |
| Cloud Apps              | Microsoft Defender for Cloud Apps    |
| Hunting                 | Microsoft Defender XDR               |
| Action Center           | Microsoft Defender XDR               |

---

## Interview Questions

### What is the Microsoft Defender Portal?

The Microsoft Defender Portal is a centralized web-based security console where SOC analysts monitor incidents, investigate alerts, hunt threats, respond to attacks, isolate devices, and perform remediation across Microsoft security products.

### Why is the Incidents page more important than the Alerts page?

The Incidents page provides the complete attack context by grouping related alerts, users, devices, emails, files, and evidence into one investigation. The Alerts page displays individual detections, while the Incidents page shows the broader attack chain.

### What information is available in the Assets section?

The Assets section contains information about devices, users, identities, mailboxes, and IP addresses. Analysts can review their risk level, related alerts, incidents, timeline, software, and other security information.

### What is the purpose of the Action Center?

The Action Center displays automated and manual response actions. It allows analysts to review pending, completed, failed, and approved actions such as device isolation, file quarantine, antivirus scans, and investigation activities.

### Which section is used for proactive threat hunting?

The Hunting section is used to proactively search for hidden or undetected threats using Kusto Query Language.

---

# Section 5 – Incidents and Alerts

## What is an Alert?

An **alert** is a notification generated by a Microsoft Defender product when suspicious or malicious activity is detected.

Examples:

* Malware detected
* Phishing email
* Suspicious PowerShell
* Impossible travel
* Failed authentication

---

## What is an Incident?

An **incident** is a collection of one or more related alerts that together represent a single attack or attack campaign.

Microsoft Defender XDR automatically correlates related alerts into one incident for easier investigation.

---

## Alert vs Incident

| Alert                                 | Incident                             |
| ------------------------------------- | ------------------------------------ |
| Single security detection             | Collection of related alerts         |
| Generated by Defender product         | Correlated by Microsoft Defender XDR |
| Limited context                       | Complete attack context              |
| Investigated individually if required | Main investigation object            |

---

## Alert Severity

* Informational
* Low
* Medium
* High
* Critical

---

## Alert Status

* New
* In Progress
* Resolved
* False Positive

---

## Incident Lifecycle

```text
Security Event
      ↓
Alert
      ↓
Incident
      ↓
Triage
      ↓
Investigation
      ↓
Containment
      ↓
Eradication
      ↓
Recovery
      ↓
Lessons Learned
      ↓
Closure
```

---

## Investigation Concepts

### Evidence

Artifacts collected during investigation.

Examples:

* Files
* Processes
* URLs
* Domains
* IP Addresses
* Registry changes
* Email messages

### Entities

Objects involved during an investigation.

Examples:

* User
* Device
* IP Address
* URL
* Domain
* File
* Process
* Mailbox

---

## MITRE ATT&CK

MITRE ATT&CK is a knowledge base that maps attacker tactics and techniques, helping analysts understand the attack lifecycle and improve detection and response.

---

## Interview Questions (Quick Revision)

### What is an alert?

A notification generated when suspicious or malicious activity is detected.

### What is an incident?

A collection of one or more related alerts representing a single attack.

### Why does Defender XDR create incidents?

To correlate related alerts, reduce alert fatigue, provide the complete attack timeline, and simplify investigation.

### Difference between alert severity and incident severity?

* Alert severity is assigned by the individual Defender product.
* Incident severity is determined after Defender XDR correlates all related alerts.

### What is evidence?

Artifacts collected during an investigation, such as files, processes, IPs, URLs, and email messages.

### What are entities?

Objects involved in an investigation, such as users, devices, files, URLs, processes, and IP addresses.

### Examples of containment actions

* Isolate device
* Disable user account
* Block IP
* Quarantine email
* Block malicious URL

### Examples of eradication actions

* Remove malware
* Remove persistence
* Delete malicious files
* Remove attacker tools

### Examples of recovery actions

* Restore normal operations
* Restore files (if needed)
* Verify endpoint health
* Re-enable accounts

---

# Section 6 – Assets and Entities

## What is an Asset?

An **asset** is any valuable resource owned, managed, or protected by an organization.

Examples:

* Windows device
* Linux server
* Azure VM
* User account
* Mailbox
* Database
* Network device

---

## What is an Entity?

An **entity** is any object involved in an alert or incident investigation.

Examples:

* User
* Device
* File
* Process
* URL
* Domain
* IP Address
* Email
* Registry key

---

## Asset vs Entity

| Asset                                | Entity                                        |
| ------------------------------------ | --------------------------------------------- |
| Valuable organizational resource     | Object involved in an investigation           |
| Owned or managed by the organization | May belong to the organization or an attacker |
| Protected by the SOC                 | Used to understand and investigate attacks    |

---

## Key Concept

* Every **asset** involved in an incident becomes an **entity**.
* Not every **entity** is an **asset**.

Example:

| Object             | Asset | Entity |
| ------------------ | :---: | :----: |
| Company Laptop     |   ✅   |    ✅   |
| User Account       |   ✅   |    ✅   |
| PowerShell Process |   ❌   |    ✅   |
| Malicious URL      |   ❌   |    ✅   |
| Attacker IP        |   ❌   |    ✅   |

---

## Common Assets

* Device
* User Account
* Identity
* Mailbox
* Azure VM

---

## Common Entities

* User
* Device
* File
* Process
* URL
* Domain
* IP Address
* Email
* Registry Key

---

## Why Assets Matter

Assets help analysts determine:

* Business impact
* Scope of the attack
* Investigation priority
* Containment strategy

---

## Why Defender XDR Links Entities

Microsoft Defender XDR links entities to:

* Show relationships
* Build the attack timeline
* Simplify investigations
* Provide complete attack context
* Speed up incident response

---

## Interview Questions (Quick Revision)

### What is an asset?

A valuable resource owned, managed, or protected by an organization.

### What is an entity?

Any object involved in an alert or incident investigation.

### Difference between asset and entity?

Assets are organizational resources, whereas entities are investigation objects.

### Can an entity exist without being an asset?

Yes. For example, a malicious IP address or attacker-controlled domain is an entity but not an organizational asset.

### Can an asset become an entity?

Yes. When an organizational asset is involved in an incident, it also becomes an entity in the investigation.

### Why are assets important?

They help analysts determine business impact, prioritize incidents, and identify affected systems.

### Name five assets.

* Device
* User account
* Mailbox
* Identity
* Azure VM

### Name five entities.

* IP Address
* URL
* File
* Process
* Domain

---

# Section 7 – Investigation Graph and Evidence

## What is the Investigation Graph?

The **Investigation Graph** is a visual representation of all related entities and evidence involved in an incident. It helps analysts understand the attack path without manually reviewing every log.

---

## Why is the Investigation Graph Important?

* Visualizes relationships between entities
* Speeds up investigations
* Helps identify the attack path
* Simplifies Root Cause Analysis (RCA)
* Reduces manual log correlation

---

## Common Entities in the Investigation Graph

* User
* Device
* Email
* Process
* File
* URL
* Domain
* IP Address

---

## What is Evidence?

**Evidence** is the information collected during an investigation that helps determine what happened, when it happened, and how the attack occurred.

### Examples of Evidence

* Process command line
* File hash
* Authentication logs
* Network connection logs
* Registry changes
* Email headers

---

## Entity vs Evidence

| Entity                         | Evidence                                   |
| ------------------------------ | ------------------------------------------ |
| Object involved in an incident | Information collected during investigation |
| User                           | Authentication log                         |
| Device                         | Device timeline                            |
| Process                        | Command line                               |
| File                           | File hash                                  |
| IP Address                     | Network connection record                  |

---

## Automatic Evidence Collection

Microsoft Defender XDR automatically collects investigation data from integrated Defender services, reducing manual effort and helping analysts investigate incidents faster.

Collected information may include:

* Running processes
* File hashes
* Registry changes
* Network connections
* Authentication events
* Email metadata

---

## Process Tree

A **Process Tree** is a hierarchical view showing the parent-child relationship between processes.

Example:

```text
explorer.exe
      ↓
powershell.exe
      ↓
cmd.exe
      ↓
payload.exe
```

The Process Tree helps analysts:

* Identify suspicious process chains
* Find the parent process
* Review command-line arguments
* Detect malware execution
* Trace the attack path

---

## Investigation Timeline

The Investigation Timeline displays events in chronological order, helping analysts reconstruct the attack sequence.

Example:

```text
Email Delivered
      ↓
User Clicked Link
      ↓
PowerShell Started
      ↓
Malware Downloaded
      ↓
Credential Theft
```

---

## Investigation Workflow

```text
Open Incident
      ↓
Review Alerts
      ↓
Open Investigation Graph
      ↓
Review Timeline
      ↓
Analyze Entities
      ↓
Collect Evidence
      ↓
Identify Root Cause
      ↓
Contain
      ↓
Eradicate
      ↓
Recover
      ↓
Close Incident
```

---

## Root Cause Analysis (RCA)

The Investigation Graph helps identify:

* Initial access
* Malware execution
* Persistence
* Lateral movement
* Impact
* Root cause

---

# Interview Questions (Quick Revision)

### What is the Investigation Graph?

A visual representation of entities and evidence connected to an incident.

### Why is the Investigation Graph useful?

It helps analysts quickly understand relationships, identify the attack path, and investigate incidents faster.

### What is evidence?

Information collected during an investigation that helps determine what happened.

### Difference between evidence and an entity?

An **entity** is an object involved in an incident, while **evidence** is the information collected about that object to support the investigation.

### Give five examples of evidence.

* Process command line
* File hash
* Authentication log
* Network connection log
* Registry change

### What is a Process Tree?

A hierarchical view showing the parent-child relationship between processes running on a device.

### Why is the Process Tree important?

It helps identify suspicious process execution, understand process relationships, trace malware execution, and collect evidence.

### What is automatic evidence collection?

Microsoft Defender XDR automatically gathers investigation data from integrated Defender services, reducing manual effort and speeding up investigations.

### How does the Investigation Timeline help analysts?

It presents events in chronological order, helping analysts reconstruct the attack, identify the root cause, and map activities to the MITRE ATT&CK framework.

### How would you investigate a phishing incident using the Investigation Graph?

Review the sender and recipient, verify whether the user clicked the link, analyze the affected device, examine the Process Tree, review collected evidence, identify the root cause, and perform containment and recovery.

---

# Progress

* ✅ Section 1 – SC-200 Overview
* ✅ Section 2 – Microsoft Security Ecosystem
* ✅ Section 3 – Microsoft Defender XDR Architecture
* ✅ Section 4 – Microsoft Defender Portal
* ✅ Section 5 – Incidents and Alerts
* ✅ Section 6 – Assets and Entities
* ✅ Section 7 – Investigation Graph and Evidence
* ⏳ Section 8 – Automated Investigation and Response
* ⬜ Section 9 – Automatic Attack Disruption
* ⬜ Section 10 – KQL Introduction
* ⬜ Section 11 – Day 1 Revision and Quiz