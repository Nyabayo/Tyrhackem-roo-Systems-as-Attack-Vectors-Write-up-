# Systems as Attack Vectors Write-up
<img width="392" height="384" alt="image" src="https://github.com/user-attachments/assets/186ab799-79da-45d0-ad2b-d39a9c67ea08" />


## Overview

This repository offers a detailed guide for SOC (Security Operations Center) analysts to understand how attackers exploit vulnerable and misconfigured systems. It covers the significance of systems in the digital world, common attack vectors, and practical defenses to mitigate such risks. The content is aimed at enhancing the skills of SOC analysts to protect systems from various cyber threats.

## Learning Objectives

- Understand the role of systems in modern cybersecurity.
- Explore real-world attack scenarios targeting systems.
- Gain practical experience in defending systems through hands-on practice.

## Prerequisites

Before diving into this guide, ensure the following rooms are completed on TryHackMe:

- [Junior Security Analyst Room](https://tryhackme.com/room/jrsecanalystintrouxo)
- [Humans as Attack Vectors Room](https://tryhackme.com/room/humansattackvectors)

## Table of Contents

1. [Introduction](#introduction)
2. [Definition of Systems](#definition-of-systems)
3. [Attacks on Systems](#attacks-on-systems)
4. [Vulnerabilities](#vulnerabilities)
5. [Misconfigurations](#misconfigurations)
6. [Practice Challenges](#practice-challenges)
7. [Conclusion](#conclusion)
8. [External Resources](#external-resources)

## Introduction

As a SOC analyst, it is important to understand how **systems** serve as attack vectors. Attackers often target systems to steal data, deploy ransomware, or destroy information. This guide will help you learn about common system attacks and the steps you can take to protect your organization.

## Definition of Systems

In cybersecurity, **systems** refer to physical servers, virtual machines, or cloud platforms (e.g., Microsoft 365) where sensitive data is stored. Understanding the value of these systems to attackers is crucial:

| **Breached System**                          | **Attack Value**                                            |
|----------------------------------------------|-------------------------------------------------------------|
| Personal laptop of a school student         | Steal Steam profile and add the PC to a botnet             |
| Senior IT administrator’s bank laptop       | Gain access to internal banking systems                     |
| Mail server of a criminal law firm          | Dump all mailboxes and blackmail victims                    |
| Server in an industrial network             | Encrypt the whole network with ransomware                   |
| Government website management panel         | Damage the website content (defacement/activism)            |

## Attacks on Systems

The first step in most serious attacks is to gain access to the target system. Depending on the attacker’s goal, they may seek to steal data, deploy ransomware, or destroy critical information.

### Human-Led Attacks
Often, attackers exploit human error, such as inserting a malicious USB, downloading malware, or using weak passwords. In fact, **81% of breaches** involve stolen or compromised passwords. Ensure you use strong, unique passwords for each system. Check your passwords with [HaveIBeenPwned](https://haveibeenpwned.com/Passwords).

### Vulnerabilities
Software flaws are common, and in 2024, over **40,000** vulnerabilities were reported. These vulnerabilities are often actively exploited in major attacks. IT administrators sometimes increase the risk by setting weak passwords and failing to restrict access. Learn more about software vulnerabilities here: 
- [2024 Vulnerabilities](https://cyberpress.org/over-40000-cves-published-in-2024/)
- [CISA Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)

### Supply Chain Attacks
Attackers may target trusted software or libraries used by many applications. If an attacker compromises one such software update, all users of that software can be affected. Famous examples include:
- **[SolarWinds](https://attack.mitre.org/campaigns/C0024/#:~:text=Victims%20of%20this%20campaign%20included%20government)**
- **[3CX](https://attack.mitre.org/campaigns/C0024/#:~:text=Victims%20of%20this%20campaign%20included%20government)**

It’s challenging to protect against supply chain attacks, as you don’t have full control over the software. For example, **TryHackMe** once fell victim to a supply chain attack in **Lottie Player**. Learn more about supply chain attacks:
- [TryHackMe Supply Chain Attacks Room](https://tryhackme.com/room/supplychainattacks)

## Vulnerabilities

### Zero-Day Exploits
Some vulnerabilities remain undetected for years, such as **Shellshock** (CVE-2014-6271). A **zero-day vulnerability** is one that attackers exploit before it is publicly discovered. It’s essential to monitor vulnerabilities and apply patches quickly. 

### Responding to Vulnerabilities
Once a vulnerability is discovered, it is assigned a CVE number, and defenders must quickly implement patches. During the waiting period, monitoring for exploitation attempts is crucial.

Learn more about **zero-day vulnerabilities**: 
- [Zero-Day Wikipedia](https://en.wikipedia.org/wiki/Zero-day_vulnerability)

## Misconfigurations

Misconfigurations happen when IT teams set up systems incorrectly, such as using weak passwords like **"123456"**. These mistakes can leave systems open to attacks.

### Examples of Misconfigurations:
- **[McDonald's password misconfiguration](https://www.bleepingcomputer.com/news/security/123456-password-exposed-chats-for-64-million-mcdonalds-job-chatbot-applications/)** exposed chats for 64 million job applications.
- **[Misconfigured AWS cloud](https://www.bleepingcomputer.com/news/security/capital-one-data-breach-affects-106-million-people-suspect-arrested/#:~:text=intrusion%20occurred%20through%20a%20misconfigured%20web%20application%20firewall)** led to the breach of 106 million bank customers.
- **[Smart fridge misconfiguration](https://www.sectigo.com/blog/when-refrigerators-attack-how-cyber-criminals-infect-appliances-and-how-manufacturers-can-stop-them)**: Exposes systems to botnet attacks.

## Practice Challenges

### TryHackMe Challenges
- **[Systems at Risk](https://static-labs.tryhackme.cloud/apps/soc-systemattacks/)**: In this exercise, decide on the best remediation plan for systems at risk. 

### Mitigation Measures

| **Mitigation**              | **Description**                                                              |
|-----------------------------|------------------------------------------------------------------------------|
| **Patch Management**         | Regularly track and apply patches to vulnerable systems.                     |
| **Training for IT**          | Educate IT staff about risks to avoid misconfigurations.                     |
| **Network Protection**       | Restrict access to systems to only trusted IPs and personnel.                |
| **Antivirus Protection**     | Use antivirus software to detect and stop various attacks.                   |

### Remediation Plan
To respond to attacks, SOC analysts must collaborate with the IT team to implement a remediation plan, selecting measures such as patch management, IT training, and network protection.

## Conclusion

While SOC analysts typically don’t manage systems directly, understanding the common attack vectors and working with IT teams is crucial to a strong defense. Stay updated on the latest threats and share knowledge with colleagues.

## External Resources

- **The DFIR Report**: [How Real Intrusions Happen](https://thedfirreport.com/)
- **CISA Known Exploited Vulnerabilities Catalog**: [CISA Vulnerabilities](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
- **BleepingComputer - Supply Chain Attacks**: [Latest Supply Chain Attacks](https://www.bleepingcomputer.com/tag/supply-chain-attack/)
- **CheckPoint Threat Map**: [Interactive Cyber Threat Map](https://threatmap.checkpoint.com/)
