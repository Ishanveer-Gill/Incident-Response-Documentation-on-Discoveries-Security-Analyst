# Incident Response Documentation on my Findings: Security Analyst

<p align="center">
<img src="https://github.com/Ishanveer-Gill/Incident-Response-Documentation-on-Discoveries-Security-Analyst/assets/66128498/c5fb4e1e-646b-4807-a8fa-ada5a941b3ba" height="80%" width="80%" alt="9"/><br />

## Introduction
During the Azure HoneyNet simulation, I took on the responsibility of a Cyber Incident Responder within my Security Operations Center (SOC), diligently investigating and resolving three security incidents. This document acts as a summary of my learning experience, demonstrating the effectiveness of the incident response procedures I deployed to mitigate possible threats.

## Scope
The document includes summaries, evaluations of outcomes, actions taken in response, and categorizations (if relevant), for the incidents listed below.
- Incident ID: 2 - Brute Force ATTEMPT - MS SQL Server
- Incident ID: 3 - Malware Detected
- Incident ID: 4 - Possible Privilege Escalation (Azure Key Vault Critical Credential Retrieval or Update)

## Incident ID: 2 - Brute Force ATTEMPT - MS SQL Server

<p align="center">
<img src="https://github.com/Ishanveer-Gill/Incident-Response-Documentation-on-Discoveries-Security-Analyst/assets/66128498/1840af46-278d-4daa-b971-d3c1b99d700b" height="80%" width="80%" alt="9"/><br />
  <p align="center">
<img src="https://github.com/Ishanveer-Gill/Incident-Response-Documentation-on-Discoveries-Security-Analyst/assets/66128498/0a13275c-4b87-4c13-9f30-24d8ad717ce8" height="30%" width="30%" alt="9"/><br />

**Incident Summary**

On March 26, 2024, at 21:21:11 Eastern Time, Azure Sentinel detected a brute force attack attempt on a MS SQL Server located inside of my "windows-vm". The attackera, identified as 2 IP addresses 182.200.7.72 and 20.240.208.141, attempted to brute force inside the SQL server with no success. This incident shows someone trying to break into a system and get more control than they should have.

**Impact Assessment**

The incident has been classified as a confirmed security breach due to the IP addresses originating from locations outside the USA, and these attackers are linked to other alerts and incidents.

**Initial Response Actions**

- Check if the alert is valid.
- Separate the "windows-vm" and MS SQL system right away and change passwords for affected users.
- Find out where and how the attack started.
- Figure out when and how the attack happened.
- Look at other Network Security Groups (NSGs) to see if they're attacked too.
- Review logs for anything suspicious.
- Look into accounts with special access and make sure sensitive data is safe.

**Containment and Recovery**

- Block the attacker from reaching other systems by creating a temporary network barrier.
- Restrict unnecessary traffic to the "windows-vm" system by adjusting NSG settings.
- Change passwords for affected users and make sure they're strong.
- Add extra security by enabling multi-factor authentication (MFA) for all users.
- Scan the "windows-vm" and SQL server/system thoroughly for malware.
- Keep an eye on the system for any more strange activity to ensure it stays safe.

## Incident ID: 3 - Malware Detected

<p align="center">
<img src="https://github.com/Ishanveer-Gill/Incident-Response-Documentation-on-Discoveries-Security-Analyst/assets/66128498/af212cde-74b5-4b94-bab3-eabbbde47923" height="80%" width="80%" alt="9"/><br />
  <p align="center">
<img src="https://github.com/Ishanveer-Gill/Incident-Response-Documentation-on-Discoveries-Security-Analyst/assets/66128498/4b4f8e68-9f1a-45cc-be17-df8bdef0a0c0" height="30%" width="30%" alt="9"/><br />

**Incident Summary**

On January 5, 2024, at 18:05:12 UTC, Malware was detected on workstation “windows-vm01”, potentially compromising the confidentiality, integrity, availability of the system and data.

**Initial Response Actions**

1. Verify the authenticity of the alert or report.
2. Identify the primary user account of the affected system, if applicable.
3. Notify affected stakeholders and provide guidance on how to protect themselves.
4. Run a full system scan using an up-to-date antivirus software to identify and remove the malware.
5. If the malware cannot be removed or significant damage is suspected, shut down the workstation and disconnect it from the network.

**Containment and Recovery**

1. Quarantine the infected workstation and any other potentially impacted systems.
2. Restore the workstation to a known clean state through system imaging or clean installation.
3. Strengthen security measures to prevent future malware incidents.




