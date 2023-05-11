# Designing a Honeynet in Azure with Incident Response
![HoneyNet-2](https://i.imgur.com/4ItmMCq.jpg)
## Summary

In this project, Microsoft Azure is used to construct a honeynet that produces authentic cyber-attacks from random hackers around the globe.  
## Objective
The main objective of this project is to build skills and develop knowledge in a SOC (Security Operations Center) environment on how to respond and mitigate network attacks. The honeynet is deployed with vulnerabilities to attract attackers and allow analysis of their methods. Thereafter, incident response procedures are executed to harden the environment using custom security controls and NIST standards. 

## Platform and Technologies Utilized

- Microsoft Azure
  - Azure Sentinel
  - Azure Virtual Machines (2 Windows, 1 Linux)
  - Blob Storage Account
  - Key Vault
  - Kusto Query Language (KQL)
  - Log Analytics Workspace
  - Microsoft Defender for Cloud
  - Network Security Groups (NSGs)
  - Resource Groups
  
- Additional Items
  - Analytics Rules (Custom Incident Triggers) 
  - Built a Watchlist (Monitor Network Traffic)
  - Created Workbooks (Custom Queries via KQL) 

- Incident Response Procedures
  - NIST SP 800-53 (Security Controls)
  - NIST SP 800-61 (Incident Handling) 
## Part 1: Network Design Minus Security Controls
![Network Exposed](https://i.imgur.com/XuL4age.jpg)

In this phase, the network is void of proper security and vulnerable to various attack types such as Ransomware, Brute Force, DDoS, SQL Injection, XSS(Cross-site Scripting), Phishing, etc.

Some of the configurations used to accomplish this include: 

-	Created (3) VMs to allow ingress/egress traffic.
-	Disabled the firewalls rules on each machine.
- The network is left in this state for 3-4 day period. 
<br/>
<b>VM Creation</b>

![vm-1](https://i.imgur.com/mY5K0dR.jpg)


## Attacker Map - Exposed Network
<b>The following showcases the global map and geo location of attacks against the network in its vulnerable state.
<br/>
<br/>
<b>Windows Machine Traffic
  
![0 Windows](https://i.imgur.com/AkJei4G.jpg)
<br/>
<br/>

<b>Linux Machine Traffic
  
![0 Linux](https://i.imgur.com/031X03K.jpg)
<br/>
<br/>

<b>Microsoft SQL Server Traffic
  
![0 SecurityAlerts](https://i.imgur.com/M9N6OAh.jpg)
<br/>
<br/>

<b>Sentinel NSG (Network Security Group) Traffic
  
![0 Sentinel](https://i.imgur.com/GFyOqMP.jpg)
<br/>
<br/>
## Attacks Metrics – Pre-Security
The figures below highlight the number of attacks logged against the network in the vulnerable state over a 3-4 day period.
  
![stats-1](https://i.imgur.com/j6AZHt4.jpg)

## Part 2: Network Design Post Security Controls
![Network Secured](https://i.imgur.com/5FPEDlL.jpg)

In this phase, security controls have been applied to eliminate known vulnerabilities and limited potential attacks. 
The network is monitored for a 24-hour period to analyze the impact of the controls applied. Some of the mitigation efforts in this phase include:
- Security Controls Implemented
  - Configured Firewall Rules
  - Network Security Groups (NSGs)
  - Automated Log Ingestion
  - Log Analytics Workspace (Custom Logs with KQL)
  - Configured Azure Sentinel as SIEM
  - NIST Framework

- Incident Response Procedures
  - Responded to Incidents
  - Analyzed Legitimacy (True-Positive or False-Positive)
  - Assigned Ownership
  - Contained and Investigated
  - Applied Solutions
  - Documented Incident


<b>Configuring Log Analytics Workspace - Custom Queries
  
![logs-1](https://i.imgur.com/1Ax4EIZ.jpg)
<br/>
<br/>
  
<b>Diagnostic Settings
  
![logs-2](https://i.imgur.com/5LG3gzI.jpg)
<br/>
<br/>
  
<b>Creating Sentinel Workbooks
  
![logs-5](https://i.imgur.com/m3CZGQQ.jpg)
<br/>
<br/>
  
<b>Incident Tracking - Investigating Log Alerts
  
![logs-6](https://i.imgur.com/rqPQFU1.jpg)
<br/>
<br/>
  
## Attacks Metrics – Post-Security
The figures below highlight the “reduced” number of attacks logged against the network after security controls were applied. 
The environment was monitored over a 24-hour timeframe.
  
![stats-2](https://i.imgur.com/4I8zWWp.jpg)

## Percentage Decrease 
   
The figures displays the decreased percentages after the security controls were applied.
  
![stats-3](https://i.imgur.com/y7W1fwR.jpg)

## Conclusion

This project helped showcase the valuable role SOC analysts play in the defense of network security and DLP (Data Loss Prevention). Using Azure cloud, I was able to develop a deeper understanding of how a SOC environment operates and execute some of the skills necessary (analyzing logs, conducting incident response, applying security controls) to minimize threats and protect data. 

Thanks for viewing! 
And a big thanks to <a href="https://www.youtube.com/@JoshMadakor">Josh Madakor</a> for instructing this lab. 
