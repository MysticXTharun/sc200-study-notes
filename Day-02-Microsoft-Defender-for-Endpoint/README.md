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

# Day 2 – Microsoft Defender for Endpoint

# Section 2 – Microsoft Defender for Endpoint Architecture (Deep Dive)

## Architecture Overview

Microsoft Defender for Endpoint combines multiple security components to provide end-to-end endpoint protection.

Its architecture consists of:

- Microsoft Defender Antivirus (NGAV)
- Defender for Endpoint Sensor
- Microsoft Defender Cloud
- Behavioral Analytics
- Threat Intelligence
- Machine Learning
- Attack Surface Reduction (ASR)
- Microsoft Defender SmartScreen
- Device Control
- Microsoft Defender XDR

Together, these components help prevent, detect, investigate, and respond to endpoint threats.

---

## Microsoft Defender Architecture

```text
                     Microsoft Defender XDR
                               ▲
                               │
                    Alerts and Incidents
                               ▲
                               │
                Microsoft Defender Cloud
      ┌─────────────────────────────────────────┐
      │ • Machine Learning                      │
      │ • Behavioral Analytics                  │
      │ • Threat Intelligence                   │
      │ • Global Threat Signals                 │
      └─────────────────────────────────────────┘
                               ▲
                               │
                  Endpoint Telemetry
                               ▲
                               │
                  Defender for Endpoint Sensor
                               ▲
                               │
      ┌─────────────────────────────────────────┐
      │ Endpoint Device                         │
      │ • Defender Antivirus                    │
      │ • ASR Rules                             │
      │ • SmartScreen                           │
      │ • Device Control                        │
      └─────────────────────────────────────────┘
```

---

# Microsoft Defender Antivirus (NGAV)

Microsoft Defender Antivirus is Microsoft's Next-Generation Antivirus solution.

Its primary responsibilities include:

- Malware prevention
- Signature-based detection
- Heuristic analysis
- Cloud-delivered protection
- File quarantine
- Scheduled scans
- Real-time protection

Example:

```text
User downloads Trojan.exe
        ↓
Defender Antivirus scans file
        ↓
Malicious signature detected
        ↓
File quarantined
        ↓
Alert generated
```

---

# Defender for Endpoint Sensor

The Defender Sensor is the EDR component of Microsoft Defender for Endpoint.

Unlike an antivirus engine, the sensor continuously collects endpoint telemetry even when no malware is detected.

Examples of collected telemetry include:

- Process creation
- Process termination
- Parent-child process relationships
- Command-line arguments
- File creation and deletion
- Registry modifications
- Network connections
- User logons
- Services
- Scheduled tasks

Example:

```text
powershell.exe -EncodedCommand
```

The sensor records:

- Parent process
- Command line
- User
- Timestamp
- Network activity
- Related events

This telemetry is securely transmitted to Microsoft Defender Cloud for further analysis.

---

# Microsoft Defender Cloud

The Microsoft Defender Cloud receives endpoint telemetry from Defender Sensors deployed across managed devices.

The cloud analyzes telemetry using:

- Behavioral Analytics
- Machine Learning
- Threat Intelligence
- Detection Rules
- Global Threat Signals

Unlike traditional antivirus solutions, Microsoft analyzes telemetry collected from millions of devices worldwide to identify suspicious behavior and emerging threats.

---

# Behavioral Monitoring

Behavioral monitoring focuses on identifying malicious actions instead of relying only on malware signatures.

Examples include:

- Credential dumping
- PowerShell abuse
- Office spawning PowerShell
- LSASS access
- Shadow copy deletion
- Mass file encryption
- WMI abuse

Behavioral monitoring enables Microsoft Defender to detect fileless and previously unknown attacks.

---

# Attack Surface Reduction (ASR)

Attack Surface Reduction (ASR) rules are Microsoft-provided security rules designed to block risky attack techniques before they become security incidents.

Common ASR rules include:

- Block Office applications from creating child processes
- Block executable content from email
- Block credential stealing from LSASS
- Block JavaScript or VBScript from launching executables
- Block ransomware behavior

ASR reduces the attack surface exposed to attackers and prevents common exploitation techniques.

---

# Microsoft Defender SmartScreen

Microsoft Defender SmartScreen protects users against:

- Malicious websites
- Phishing websites
- Malicious downloads
- Untrusted applications

Example:

```text
User opens fake banking website
        ↓
SmartScreen checks reputation
        ↓
Website identified as phishing
        ↓
Access blocked
```

---

# Device Control

Device Control allows administrators to manage removable storage devices.

Examples:

- USB drives
- External HDDs
- External SSDs

Policies can include:

- Block removable media
- Read-only access
- Allow only approved devices
- Audit device usage

---

# Detection Workflow

```text
PowerShell Execution
        ↓
Defender Sensor
        ↓
Endpoint Telemetry
        ↓
Microsoft Defender Cloud
        ↓
Behavioral Analytics
Machine Learning
Threat Intelligence
        ↓
Alert
        ↓
Microsoft Defender XDR
        ↓
Incident
        ↓
Automated Investigation and Response (AIR)
        ↓
SOC Analyst Investigation
```

For supported high-confidence attacks, Microsoft Defender XDR may also trigger **Automatic Attack Disruption** to contain malicious activity.

---

# NGAV vs EDR

| Next-Generation Antivirus (NGAV) | Endpoint Detection and Response (EDR) |
|----------------------------------|----------------------------------------|
| Prevents malware | Detects, investigates and responds |
| Uses signatures and heuristics | Uses continuous endpoint telemetry |
| Focuses on prevention | Focuses on detection and investigation |
| Quarantines malicious files | Provides timelines, alerts and incidents |
| Local protection with cloud assistance | Cloud-driven detection and response |

NGAV and EDR complement each other to provide comprehensive endpoint security.

---

# Quick Revision

### What is NGAV?

Microsoft Defender Antivirus provides malware prevention through signatures, heuristics and cloud-delivered protection.

### What does the Defender Sensor do?

Continuously collects endpoint telemetry for cloud-based analysis.

### What does Microsoft Defender Cloud do?

Analyzes telemetry using machine learning, behavioral analytics and threat intelligence.

### What is Behavioral Monitoring?

Behavior-based detection that identifies malicious actions instead of relying only on malware signatures.

### What are ASR Rules?

Microsoft security rules that proactively block common attack techniques before they become incidents.

### What does SmartScreen protect against?

- Phishing websites
- Malicious websites
- Malicious downloads
- Untrusted applications

### What is Device Control?

A feature that manages removable storage devices such as USB drives, external HDDs and SSDs through configurable security policies.

---

# Interview Questions

1. Explain the Microsoft Defender for Endpoint architecture.
2. What is the difference between NGAV and EDR?
3. Why does the Defender Sensor continuously collect telemetry?
4. What is cloud-delivered protection?
5. What is behavioral monitoring? Give three examples.
6. What are Attack Surface Reduction (ASR) rules?
7. What does Microsoft Defender SmartScreen protect against?
8. What is Device Control?
9. Explain the complete flow from PowerShell execution to incident creation in Microsoft Defender for Endpoint.
10. Why is behavioral detection more effective than signature-only detection?
11. If a malicious Office document launches `powershell.exe`, which MDE components help detect or prevent the attack, and how?

---

# Day 2 Progress

- ✅ Section 1 – Introduction to Microsoft Defender for Endpoint
- ✅ Section 2 – MDE Architecture (Deep Dive)
- 🔄 Section 3 – Endpoint Onboarding
- ⬜ Section 4 – Device Inventory
- ⬜ Section 5 – Device Timeline
- ⬜ Section 6 – Machine Actions
- ⬜ Section 7 – Indicators
- ⬜ Section 8 – Threat and Vulnerability Management
- ⬜ Section 9 – Custom Detection Rules
- ⬜ Section 10 – Live Response and Advanced Hunting
- ⬜ Section 11 – Revision and Mock Exam
