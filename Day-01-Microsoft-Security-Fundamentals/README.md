# Day 1: Microsoft Security Fundamentals

## Overview

Day 1 introduces the SC-200 certification, the role of a Security Operations Analyst, and the Microsoft security ecosystem.

The main focus is understanding how Microsoft Sentinel and Microsoft Defender XDR help security teams detect, investigate, and respond to threats.

## Learning Objectives

By the end of Day 1, I should be able to:

- Explain the purpose of the SC-200 certification
- Describe the role of a Security Operations Analyst
- Understand the Microsoft security ecosystem
- Explain the purpose of Microsoft Defender XDR
- Navigate the Microsoft Defender portal
- Differentiate between events, alerts, and incidents
- Identify common security entities
- Understand the basic purpose of Microsoft Sentinel
- Write simple KQL queries

## 1. SC-200 Certification Overview

The SC-200 certification is designed for Security Operations Analysts who use Microsoft security technologies to:

- Monitor security environments
- Detect suspicious activities
- Investigate alerts and incidents
- Respond to security threats
- Perform threat hunting
- Improve security detections
- Automate incident-response activities

The primary technologies covered in SC-200 are:

- Microsoft Sentinel
- Microsoft Defender XDR
- Microsoft Defender for Endpoint
- Microsoft Defender for Office 365
- Microsoft Defender for Identity
- Microsoft Defender for Cloud Apps
- Microsoft Entra ID Protection
- Kusto Query Language

## 2. Security Operations Analyst Role

A Security Operations Analyst is responsible for protecting an organisation by monitoring, detecting, investigating, and responding to security threats.

### Common Responsibilities

- Monitor security alerts
- Perform initial alert triage
- Investigate suspicious activities
- Analyse endpoint, identity, email, and cloud data
- Determine whether an alert is malicious or benign
- Assign incident severity
- Contain affected users and devices
- Escalate confirmed incidents
- Document investigation findings
- Perform proactive threat hunting
- Tune detection rules
- Reduce false-positive alerts

## 3. Microsoft Security Ecosystem

The Microsoft security ecosystem provides security visibility across identities, endpoints, email, applications, cloud resources, and network activity.

| Technology | Main Purpose |
|---|---|
| Microsoft Sentinel | Cloud-native SIEM and security orchestration platform |
| Microsoft Defender XDR | Correlates security data across multiple Defender products |
| Defender for Endpoint | Protects and monitors endpoint devices |
| Defender for Identity | Detects identity-based threats |
| Defender for Office 365 | Protects email and collaboration services |
| Defender for Cloud Apps | Provides visibility and control over cloud applications |
| Defender for Cloud | Protects cloud workloads and resources |
| Entra ID Protection | Detects risky users and sign-in activity |

## 4. Microsoft Sentinel

Microsoft Sentinel is a cloud-native SIEM and SOAR platform.

### SIEM

SIEM stands for Security Information and Event Management.

A SIEM platform helps security teams:

- Collect logs from different sources
- Store and analyse security data
- Detect suspicious activities
- Generate alerts
- Correlate related events
- Create security incidents
- Support threat hunting and investigation

### SOAR

SOAR stands for Security Orchestration, Automation, and Response.

SOAR capabilities help security teams:

- Automate repetitive tasks
- Enrich alerts with additional information
- Assign incidents automatically
- Notify analysts
- Block malicious indicators
- Run incident-response playbooks

### Important Sentinel Components

- Log Analytics workspace
- Data connectors
- Analytics rules
- Alerts
- Incidents
- Entities
- Hunting queries
- Workbooks
- Watchlists
- Automation rules
- Playbooks

## 5. Microsoft Defender XDR

Microsoft Defender XDR is an extended detection and response platform.

It combines security information from multiple Microsoft Defender products to provide a unified view of attacks.

### Defender XDR Data Sources

- Endpoints
- User identities
- Email messages
- Microsoft 365 applications
- Cloud applications

### Main Capabilities

- Centralised alert monitoring
- Automatic alert correlation
- Incident creation
- Cross-domain investigation
- Automated investigation and response
- Advanced hunting
- Threat analytics
- Security reports

## 6. Microsoft Defender Portal

Microsoft Defender XDR is accessed through the Microsoft Defender portal.

Portal address:

```text
https://security.microsoft.com