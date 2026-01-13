## Honeypot SOC Lab

 VM Honeypot made with Azure and Microsoft Sentinel 
![image](https://raw.githubusercontent.com/Gabriel-Ponce/windows-honeypot-sentinel-soc-lab/refs/heads/main/Screenshot%202026-01-12%20202715.png)

## Lab Setup & Architecture

### Cloud Environment
- Microsoft Azure subscription
- Dedicated Resource Group for isolation and management

### Network Configuration
- Azure Virtual Network created to host the honeypot
- Network Security Group intentionally configured to allow all inbound traffic (any protocol, any port) to simulate a highly exposed system

### Endpoint Deployment
- Windows 10 virtual machine deployed as an internet-facing honeypot
- Public IP assigned to allow unsolicited external connections

### Logging & SIEM Integration
- Azure Log Analytics Workspace created for centralized log ingestion
- Windows security and event logs forwarded from the VM to Log Analytics
- Microsoft Sentinel enabled and connected to the workspace for SIEM capabilities

![image](https://raw.githubusercontent.com/Gabriel-Ponce/windows-honeypot-sentinel-soc-lab/refs/heads/main/Screenshot%202026-01-12%20192246.png)

### Monitoring & Visualization
- Azure Workbook created in Microsoft Sentinel
- Attacker source IP addresses enriched with geolocation data
- World map visualization used to display global attack activity against the honeypot

## Purpose of the Lab

This lab was designed to simulate how Security Operations Center (SOC) teams monitor and analyze attacks against exposed systems. By intentionally deploying a vulnerable, internet-facing Windows host, the lab demonstrates how quickly automated attacks occur and how SIEM tools like Microsoft Sentinel are used to detect, analyze, and visualize malicious activity.
