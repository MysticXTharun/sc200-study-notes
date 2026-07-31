# Day 2 – Microsoft Defender for Endpoint

## Section 1 – Introduction to Microsoft Defender for Endpoint

### What is Microsoft Defender for Endpoint?

Microsoft Defender for Endpoint (MDE) is Microsoft’s enterprise endpoint security platform.

It provides:

* Next-Generation Antivirus (NGAV)
* Endpoint Detection and Response (EDR)
* Threat and Vulnerability Management
* Automated Investigation and Response
* Threat intelligence
* Endpoint response actions

MDE helps organizations prevent, detect, investigate, and respond to threats targeting endpoint devices.

---

## What is an Endpoint?

An endpoint is a device connected to or used to access an organization’s network and resources.

Examples:

* Windows laptop
* Windows desktop
* Windows Server
* Linux server
* macOS device
* Mobile device

---

## MDE Security Lifecycle

```text
Prevent
   ↓
Detect
   ↓
Investigate
   ↓
Respond
```

### Prevent

MDE prevents attacks using:

* Microsoft Defender Antivirus
* Attack Surface Reduction rules
* Web protection
* Device control
* Cloud-delivered protection

### Detect

MDE detects suspicious activity such as:

* Malware execution
* PowerShell abuse
* Credential theft
* Suspicious logons
* Ransomware behavior
* Malicious network connections

### Investigate

SOC analysts investigate endpoint activity using:

* Alerts
* Incidents
* Process trees
* Device timelines
* Investigation graphs
* Advanced Hunting

### Respond

MDE response actions include:

* Isolate device
* Run antivirus scan
* Quarantine file
* Stop process
* Collect investigation package
* Live Response
* Automated remediation

---

## Microsoft Defender Antivirus vs Microsoft Defender for Endpoint

| Microsoft Defender Antivirus                  | Microsoft Defender for Endpoint                                                  |
| --------------------------------------------- | -------------------------------------------------------------------------------- |
| Provides antivirus and antimalware protection | Provides complete endpoint security                                              |
| Primarily detects malware                     | Detects malware and suspicious behavior                                          |
| Uses signatures and cloud protection          | Uses signatures, telemetry, analytics, threat intelligence, and machine learning |
| Provides malware detections                   | Provides alerts, incidents, investigation, and response                          |
| Focuses on prevention                         | Covers prevention, detection, investigation, and response                        |

Microsoft Defender Antivirus is one protection component within the wider Microsoft Defender for Endpoint platform.

---

## Defender Sensor

The Defender for Endpoint sensor continuously collects endpoint telemetry.

Examples include:

* Process creation
* Process termination
* File activity
* Registry changes
* User logons
* Network connections
* Service activity
* Scheduled tasks
* Device information

The sensor collects activity continuously, even when no malware alert has been generated.

---

## Cloud-Based Analysis

Endpoint telemetry is sent to the Microsoft Defender cloud.

Microsoft analyzes the telemetry using:

* Behavioral analytics
* Machine learning
* Threat intelligence
* Detection rules
* Cloud security analytics

Cloud analysis helps identify known malware, unknown threats, suspicious behavior, and attack patterns across multiple devices.

---

## MDE Architecture

```text
Endpoint Device
      ↓
Microsoft Defender Antivirus
      ↓
Defender for Endpoint Sensor
      ↓
Endpoint Telemetry
      ↓
Microsoft Defender Cloud
      ↓
Analytics + Machine Learning + Threat Intelligence
      ↓
Microsoft Defender XDR Portal
      ↓
SOC Analyst
```

### Architecture Explanation

1. Microsoft Defender Antivirus provides malware prevention and protection.
2. The Defender sensor continuously collects endpoint telemetry.
3. Telemetry is sent securely to the Microsoft Defender cloud.
4. Microsoft analyzes the activity using analytics, machine learning, and threat intelligence.
5. Alerts and related activities are correlated into incidents.
6. SOC analysts review and investigate them in the Microsoft Defender XDR portal.
7. Analysts or automated capabilities perform response actions.

---

## MDE vs Traditional Antivirus

| Traditional Antivirus       | Microsoft Defender for Endpoint                 |
| --------------------------- | ----------------------------------------------- |
| Mainly signature-based      | Signature and behavior-based                    |
| Focuses on known malware    | Detects known and unknown threats               |
| Limited endpoint visibility | Rich endpoint telemetry                         |
| Mainly local detection      | Cloud-assisted analysis                         |
| Basic remediation           | Investigation and advanced response actions     |
| Limited attack context      | Process tree, timeline, incidents, and evidence |

---

## CrowdStrike and MDE Comparison

| CrowdStrike Falcon | Microsoft Defender for Endpoint     |
| ------------------ | ----------------------------------- |
| Falcon Sensor      | Defender for Endpoint Sensor        |
| Falcon Console     | Microsoft Defender XDR Portal       |
| Detection          | Alert                               |
| Real Time Response | Live Response                       |
| Host Containment   | Device Isolation                    |
| Falcon Spotlight   | Threat and Vulnerability Management |
| IOC Management     | Indicators                          |

---

## Quick Revision

### What is MDE?

Microsoft Defender for Endpoint is Microsoft’s enterprise endpoint security platform that combines NGAV, EDR, threat intelligence, automated investigation, vulnerability management, and response capabilities.

### What does the Defender sensor do?

It continuously collects endpoint telemetry such as process, file, logon, registry, and network activity.

### Why is cloud analysis important?

It enables Microsoft to correlate telemetry and detect threats using analytics, machine learning, and threat intelligence.

### What are the four phases of MDE?

* Prevent
* Detect
* Investigate
* Respond

### What is the MDE equivalent of CrowdStrike RTR?

Live Response.

### What is the MDE equivalent of CrowdStrike Host Containment?

Device Isolation.

---

## Interview Answer

Microsoft Defender for Endpoint is Microsoft’s enterprise endpoint security platform. It combines Next-Generation Antivirus, Endpoint Detection and Response, Threat and Vulnerability Management, threat intelligence, and automated investigation and response. The Defender sensor continuously collects endpoint telemetry and sends it to Microsoft’s cloud, where analytics, machine learning, and threat intelligence detect suspicious behavior. SOC analysts investigate alerts and incidents in the Microsoft Defender XDR portal and perform actions such as device isolation, antivirus scanning, file quarantine, and Live Response.

---

# Section 2 – Microsoft Defender for Endpoint Architecture

## Overview

Microsoft Defender for Endpoint (MDE) uses multiple security components that work together to protect endpoint devices from cyber threats.

Unlike traditional antivirus solutions that rely mainly on signatures, MDE combines endpoint telemetry, cloud analytics, machine learning, behavioral analysis, and Microsoft threat intelligence to detect both known and unknown threats.

---

## Microsoft Defender for Endpoint Architecture

```text
Endpoint Device
      ↓
Microsoft Defender Antivirus (NGAV)
      ↓
Microsoft Defender Sensor
      ↓
Endpoint Telemetry
      ↓
Microsoft Defender Cloud
      ↓
Behavior Analytics
Machine Learning
Threat Intelligence
Detection Rules
      ↓
Alerts
      ↓
Incidents
      ↓
Microsoft Defender XDR Portal
      ↓
SOC Analyst
      ↓
Response Actions
```

---

## Components of the Architecture

### Endpoint Device

The protected endpoint can be:

- Windows
- Windows Server
- Linux
- macOS
- Mobile devices

The endpoint generates security events continuously.

---

### Microsoft Defender Antivirus (NGAV)

Provides prevention against malware using:

- Signature detection
- Heuristics
- Cloud-delivered protection
- Exploit protection
- Real-time protection

Its primary goal is to stop malware before execution.

---

### Defender for Endpoint Sensor

The Defender sensor continuously collects endpoint telemetry.

Examples include:

- Process creation
- Process termination
- File creation
- Registry changes
- Network connections
- User logons
- Scheduled tasks
- Services
- Device information

The sensor collects activity regardless of whether malware is detected.

---

### Endpoint Telemetry

Telemetry is the security data collected from endpoint devices.

Examples include:

- Process events
- File events
- Registry events
- Network events
- Authentication events
- Device health information

Telemetry is securely transmitted to the Microsoft Defender cloud.

---

### Microsoft Defender Cloud

Telemetry is analyzed in Microsoft's cloud using:

- Behavioral analytics
- Machine learning
- Threat intelligence
- Global threat signals
- Detection logic

The cloud correlates activities across multiple devices and users to identify sophisticated attacks.

---

### Behavioral Analytics

Behavioral analytics detects suspicious activities based on attacker behavior rather than malware signatures.

Examples:

- Credential dumping
- PowerShell abuse
- Mass file encryption
- Backup deletion
- Suspicious process chains

---

### Machine Learning

Machine learning identifies malicious activity by analyzing patterns collected from millions of devices worldwide.

It helps detect:

- Unknown malware
- Zero-day attacks
- Fileless attacks
- Suspicious behavior

---

### Threat Intelligence

Microsoft Threat Intelligence provides information about:

- Malicious IP addresses
- Malicious domains
- Malicious URLs
- File hashes
- Threat actors
- Known attack techniques

Threat intelligence improves detection accuracy.

---

### Detection Rules

Detection rules combine:

- Telemetry
- Behavioral analytics
- Machine learning
- Threat intelligence

to generate alerts for suspicious activities.

---

### Alerts

An alert represents a suspicious activity detected on an endpoint.

Examples:

- PowerShell execution
- Ransomware activity
- Credential theft
- Malware detection

---

### Incidents

Multiple related alerts are automatically correlated into an incident.

An incident provides the complete attack story.

---

### Microsoft Defender XDR Portal

SOC analysts use the Defender XDR portal to:

- Review alerts
- Investigate incidents
- Analyze device timelines
- View process trees
- Perform Advanced Hunting
- Execute response actions

---

## Additional Protection Features

### Attack Surface Reduction (ASR)

ASR rules prevent risky behaviors before they become incidents.

Examples:

- Block Office applications from creating child processes
- Block credential stealing
- Block executable content from email

---

### Microsoft Defender SmartScreen

SmartScreen protects users against:

- Malicious websites
- Phishing websites
- Malicious downloads
- Untrusted applications

---

### Device Control

Device Control allows administrators to manage removable storage devices.

Examples:

- Block USB devices
- Allow approved USB devices
- Read-only access
- Audit removable media usage

---

## Detection Flow

```text
PowerShell Execution
        ↓
Defender Sensor
        ↓
Endpoint Telemetry
        ↓
Microsoft Defender Cloud
        ↓
Behavior Analytics
Machine Learning
Threat Intelligence
        ↓
Alert
        ↓
Incident
        ↓
Microsoft Defender XDR
        ↓
SOC Analyst
        ↓
Response Action
```

---

## Behavioral Detection vs Signature Detection

| Signature Detection | Behavioral Detection |
|---------------------|----------------------|
| Detects known malware | Detects suspicious behavior |
| Signature-based | Behavior-based |
| Requires known signatures | Can detect unknown threats |
| Stops known malware | Detects fileless attacks and zero-day attacks |

---

## Quick Revision

### What is endpoint telemetry?

Security data collected from endpoint devices such as process, file, registry, network and logon events.

---

### What is behavioral analytics?

Behavioral analytics detects suspicious attacker behavior instead of relying only on malware signatures.

---

### What is Microsoft Threat Intelligence?

It provides reputation information about malicious IPs, domains, URLs, hashes and threat actors.

---

### What is the purpose of ASR rules?

Attack Surface Reduction rules block risky behaviors before they become security incidents.

---

### What is SmartScreen?

SmartScreen protects users against phishing websites, malicious downloads and unsafe applications.

---

### What is Device Control?

Device Control manages removable media such as USB devices by allowing, blocking, auditing or restricting access.

---

## Interview Questions

### 1. What is the difference between NGAV and EDR?

**Answer:**

NGAV focuses on preventing malware using signatures, heuristics and cloud protection. EDR continuously collects endpoint telemetry, detects suspicious behavior, investigates incidents and enables response actions.

---

### 2. What is endpoint telemetry?

**Answer:**

Endpoint telemetry is security data collected by the Defender sensor, including process, file, registry, network and authentication events. It is sent to the Microsoft Defender cloud for analysis.

---

### 3. What does the Defender sensor do?

**Answer:**

The Defender sensor continuously collects endpoint activity and sends telemetry to Microsoft Defender for cloud-based analysis. It enables behavioral detection, investigation and response.

---

### 4. What is cloud-delivered protection?

**Answer:**

Cloud-delivered protection sends endpoint telemetry to Microsoft Defender Cloud, where behavioral analytics, machine learning and threat intelligence detect known and unknown threats.

---

### 5. What is behavioral analytics?

**Answer:**

Behavioral analytics identifies suspicious attacker behavior such as credential dumping, PowerShell abuse and ransomware activity without relying only on signatures.

---

### 6. What are ASR rules?

**Answer:**

Attack Surface Reduction rules block risky behaviors like Office spawning PowerShell or credential stealing before they can compromise a device.

---

### 7. What is Microsoft Defender SmartScreen?

**Answer:**

SmartScreen protects users from phishing websites, malicious downloads and untrusted applications by checking Microsoft's reputation services.

---

### 8. What is Device Control?

**Answer:**

Device Control allows administrators to manage removable storage devices by blocking, allowing, auditing or restricting USB access.

---

### 9. What is the difference between an alert and an incident?

**Answer:**

An alert represents a single suspicious activity. Multiple related alerts are automatically correlated into an incident that provides the complete attack story.

---

### 10. Explain the Microsoft Defender for Endpoint architecture.

**Answer:**

The endpoint generates telemetry that is collected by the Defender sensor and sent to Microsoft Defender Cloud. The cloud analyzes it using behavioral analytics, machine learning and threat intelligence to generate alerts and incidents, which SOC analysts investigate in the Microsoft Defender XDR portal before taking response actions.

---

## Day 2 Progress

- ✅ Section 1 – Introduction to Microsoft Defender for Endpoint
- ✅ Section 2 – Microsoft Defender for Endpoint Architecture
- 🔄 Section 3 – Endpoint Onboarding
- ⬜ Section 4 – Device Inventory
- ⬜ Section 5 – Device Timeline
- ⬜ Section 6 – Machine Actions
- ⬜ Section 7 – Indicators
- ⬜ Section 8 – Threat and Vulnerability Management
- ⬜ Section 9 – Custom Detection Rules
- ⬜ Section 10 – Live Response and Advanced Hunting
- ⬜ Section 11 – Revision and Mock Exam