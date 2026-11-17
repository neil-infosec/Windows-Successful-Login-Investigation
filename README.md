# Windows-Successful-Login-Investigation
Investigated Windows successful login events (Event ID 4624) using Windows Event Viewer and Wazuh SIEM. Analyzed Logon Type 2, user authentication details, timestamps, and source IP addresses to understand normal login activity and demonstrate basic SOC Analyst L1 investigation skills.

## 1. Project Overview

**Project Name:** Windows Successful Login Investigation  
**Category:** Security Operations Center (SOC)  
**Tools Used:** Windows Event Viewer, Wazuh SIEM  
**Operating System:** Windows 11  
**Event ID:** 4624  
**Investigation Type:** Authentication Monitoring and Log Analysis  
**Severity:** Informational / Low Risk

### Objective

The objective of this investigation was to identify, analyze, and understand successful Windows authentication events using Windows Event Viewer and Wazuh SIEM.

The investigation focused on identifying the user account, logon type, source address, timestamp, and other relevant authentication details to determine whether the login activity was legitimate or suspicious.

---

## 2. Tools and Technologies

- **Windows 11:** Source endpoint for authentication events.
- **Windows Event Viewer:** Used to collect and investigate Windows Security logs.
- **Wazuh SIEM:** Used to monitor, collect, and analyze security events.
- **Oracle VirtualBox:** Used for the SOC home lab environment.

---

## 3. Investigation Methodology

The investigation was performed using the following steps:

1. Opened Windows Event Viewer.
2. Navigated to Windows Logs → Security.
3. Located successful authentication events using Event ID 4624.
4. Examined the General and Details sections of the event.
5. Identified the account name and logon type.
6. Checked the source network address and timestamp.
7. Verified the collected event in the Wazuh dashboard.
8. Analyzed the event to determine whether the activity was legitimate or suspicious.

---

## 4. Event Analysis

### Windows Security Event Details

| Parameter | Observed Value |
|---|---|
| Event ID | 4624 |
| Event Type | Successful Logon |
| Account Name | SOC-Lab-User |
| Logon Type | 2 |
| Logon Description | Interactive Logon |
| Source Network Address | 127.0.0.1 |
| Timestamp (UTC) | 2026-11-15 06:37:48 |
| Operating System | Windows 11 |

### Understanding Logon Type 2

Logon Type 2 represents an interactive login.

It generally occurs when a user logs into a Windows computer directly using the local keyboard and screen.

This type of authentication is commonly associated with normal workstation usage.

### Understanding Event ID 4624

Windows Security Event ID 4624 is generated when a logon session is successfully created.

Security analysts monitor this event to:

- Track successful authentication attempts.
- Identify user login activity.
- Monitor unusual login patterns.
- Investigate potentially unauthorized access.
- Establish a baseline of normal authentication behavior.

---

## 5. Wazuh SIEM Analysis

The authentication event was also examined through the Wazuh SIEM dashboard.

Wazuh was used to verify that the Windows endpoint successfully generated and forwarded the authentication event to the monitoring platform.

The investigation demonstrated how endpoint security logs can be collected and analyzed centrally using a SIEM solution.

---

## 6. Findings

The investigation identified the following:

1. Windows generated Event ID 4624, indicating successful authentication.
2. The observed logon type was 2, representing an interactive login.
3. The source address was 127.0.0.1, indicating localhost.
4. The event was consistent with normal local workstation authentication.
5. The event was successfully collected and investigated through the SOC monitoring environment.

---

## 7. Security Assessment

**Investigation Result: Benign Activity**

Based on the available event details, the authentication activity was consistent with a normal local interactive login.

No evidence of unauthorized access or external authentication activity was identified from this event alone.

However, a successful login event should not automatically be considered safe. SOC analysts should correlate it with other security events, user activity, login patterns, and endpoint information when investigating potentially suspicious behavior.

---

## 8. Conclusion

This project provided practical experience in investigating Windows successful authentication events using Event Viewer and Wazuh SIEM.

The investigation helped develop an understanding of Windows Security Event ID 4624, logon types, authentication monitoring, endpoint log collection, and basic SIEM analysis.

This project represents a foundational SOC Analyst L1 investigation workflow and demonstrates the importance of monitoring successful authentication activity in identifying potentially unauthorized access.

---

## 9. Skills Demonstrated

- Windows Security Log Analysis
- Event ID Investigation
- Authentication Monitoring
- Logon Type Identification
- Wazuh SIEM Monitoring
- Endpoint Log Collection
- Basic Security Incident Investigation
- Security Event Documentation

---

**Project Status:** Completed

**Disclaimer:** This investigation was conducted in a controlled home lab environment for educational and cybersecurity learning purposes.
