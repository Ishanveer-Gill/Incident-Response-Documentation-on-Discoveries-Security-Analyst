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

On January 6, 2024, at 11:25:48 UTC, Azure Sentinel detected a brute force attack attempt on a Windows system named "windows-vm01". The attacker, identified as IP address 14.192.144.254, made around 15,000 login attempts with no success. The incident suggests a deliberate attempt to gain unauthorized access and elevate privileges on the targeted system.

**Impact Assessment**

The occurrence has been categorized as a verified security breach because of the substantial volume of brute force login attempts and the activation of multiple alerts.

**Initial Response Actions**

1. Verify the authenticity of the alert.
2. Immediately isolate the "windows-vm" system and change the passwords of all affected user accounts.
3. Identify the origin and nature of the attack.
4. Determine the timeframe and method of the attack.
5. Check other Network Security Groups (NSGs) to assess if they are being targeted as well.
6. Conduct a comprehensive review of logs for any other suspicious activities.
7. Review user accounts with elevated privileges and verify the integrity of sensitive data stored on the system.

**Containment and Recovery**

1. Implement temporary network segmentation to prevent the attacker from accessing other systems.
2. Adjust the NSG rules to restrict unnecessary traffic to the "windows-vm" system.
3. Reset the passwords for affected user accounts and enforce strong password policies.
4. Enable multi-factor authentication (MFA) for all user accounts to enhance security.
5. Conduct a full virus scan on the "windows-vm" system to check for malware infections.
6. Monitor the system for any further unusual activity to ensure it remains secure.




