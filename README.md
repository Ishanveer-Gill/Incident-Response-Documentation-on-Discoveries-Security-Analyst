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

On March 26, 2024, at 20:32:48 Eastern Time, Malware was found on the computer "windows-vm," which could harm the system and its data.

**Initial Response Actions**

- Confirm if the alert or report is valid.
- Find the main user account of the affected system, if relevent.
- Inform people who are affected and show them how to protect themselves.
- Scan the whole system with updated antivirus software to find and delete any malware.
- If the malware can't be removed or if there's big damage, turn off the computer and disconnect it from the internet.

**Containment and Recovery**

- Separate the infected computer and any others that might be affected.
- Reset the computer to a known clean state using system imaging or clean installation
- Enhance security protocols to stop more malware attacks in the future.



