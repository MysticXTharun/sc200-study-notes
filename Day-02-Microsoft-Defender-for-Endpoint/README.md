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

## Day 2 Progress

* ✅ Section 1 – Introduction to Microsoft Defender for Endpoint
* 🔄 Section 2 – MDE Architecture Deep Dive
* ⬜ Section 3 – Endpoint Onboarding
* ⬜ Section 4 – Device Inventory
* ⬜ Section 5 – Device Timeline
* ⬜ Section 6 – Machine Actions
* ⬜ Section 7 – Indicators
* ⬜ Section 8 – Threat and Vulnerability Management
* ⬜ Section 9 – Custom Detection Rules
* ⬜ Section 10 – Live Response and Advanced Hunting
* ⬜ Section 11 – Revision and Mock Exam
