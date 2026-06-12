# Mini SOC Lab

## Overview

This repository documents my hands-on cybersecurity home lab focused on building practical SOC Analyst skills. The lab uses Wazuh as a SIEM/XDR platform to monitor a Windows endpoint, collect security events, review alerts, and practice incident investigation.

## Lab Objective

The goal of this project is to gain practical experience with:

* SIEM deployment
* Endpoint monitoring
* Windows security event analysis
* Alert triage
* Log investigation
* Incident documentation
* Basic SOC Analyst workflow

## Current Lab Architecture

```text
Windows Host Machine
│
├── Oracle VirtualBox
│   └── Ubuntu VM running Wazuh Server
│
└── Wazuh Agent installed on Windows host
```

## Tools Used

* Oracle VirtualBox
* Ubuntu Linux
* Wazuh Server
* Wazuh Dashboard
* Wazuh Agent for Windows
* Windows Event Logs

## Completed Work

### Wazuh Mini SOC Lab Setup

* Installed Ubuntu in Oracle VirtualBox
* Installed Wazuh server, indexer, and dashboard
* Configured networking between the Windows host and Ubuntu VM
* Installed Wazuh Agent on the Windows host
* Verified that the Windows endpoint appeared as an active monitored agent in Wazuh

### Windows Event Monitoring

- Generated safe Windows authentication events
- Reviewed Windows Event Viewer security logs
- Investigated failed and successful login events in Wazuh
- Practiced basic alert triage and SOC-style documentation

## Next Steps

* Generate safe Windows security events
* Review alerts in Wazuh
* Analyze authentication-related events
* Write SOC-style incident reports
* Expand the lab with additional detection and monitoring scenarios
