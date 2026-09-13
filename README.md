# Wazuh SIEM Home Lab

## Project Overview

This project demonstrates the deployment and use of a Wazuh SIEM environment to monitor a Windows endpoint and investigate security events.

I configured a Wazuh manager in a virtualized lab environment, connected my Windows endpoint using the Wazuh agent, and analyzed Windows Event Logs through the Wazuh dashboard.

The lab focuses on practical SOC analyst skills including log analysis, authentication monitoring, event correlation, and security event investigation.

## Lab Environment

- Wazuh SIEM
- Wazuh Manager
- Wazuh Dashboard
- Windows Endpoint
- Wazuh Agent
- VMware Workstation
- Windows Event Logs

## Skills Demonstrated

- SIEM monitoring
- Windows Event Log analysis
- Authentication event investigation
- Log filtering and correlation
- Endpoint monitoring
- Wazuh agent deployment
- Security alert analysis
- MITRE ATT&CK interpretation

## Windows Authentication Investigation

During the investigation, I analyzed Windows Security Event ID **4624**, which represents a successful account logon.

Using Wazuh Discover, I filtered the collected Windows events by:

`data.win.system.eventID: 4624`

I then used the **Target Logon ID** to correlate activity associated with a specific Windows logon session.

This reduced the results from multiple authentication events to a single relevant event and demonstrated how analysts can pivot between fields to investigate endpoint activity.

## Key Findings

The investigation identified:

- Windows Security Event ID **4624**
- Successful workstation logon activity
- Authentication package: **Negotiate**
- Windows Security EventChannel logs
- Correlated activity using the Target Logon ID
- Wazuh rules associated with Windows authentication activity

The event was classified by Wazuh as:

**Windows Workstation Logon Success**

## MITRE ATT&CK Mapping

Wazuh also provided MITRE ATT&CK information associated with the observed event.

This demonstrated how SIEM platforms enrich raw endpoint telemetry with security context that analysts can use during investigations.

## What I Learned

This lab helped me gain hands-on experience with the workflow of a SOC analyst:

**Collect → Filter → Investigate → Correlate → Document**

Rather than reviewing individual logs in isolation, I learned how SIEM fields such as Event ID and Logon ID can be used to narrow large datasets and reconstruct relevant endpoint activity.

## Screenshots

Screenshots documenting the Wazuh deployment and investigation will be added to this repository.

## Disclaimer

This project was completed in a controlled home lab environment for educational and cybersecurity training purposes.
