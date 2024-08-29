**Cyber Kill Chain | TryHackMe — WriteUp**


In this session, we'll explore the Cyber Kill Chain—a framework designed to detect and thwart network intrusions. You’ll gain insight into the steps adversaries take to achieve their objectives, helping you stay a step ahead.


### Task 1: Overview

The concept of a kill chain originates from the military, where it outlines the steps of an attack: identifying the target, making the decision to attack, and finally, destroying the target.

In 2011, Lockheed Martin, a global leader in security and aerospace, adapted this concept to cybersecurity by developing the Cyber Kill Chain® framework. This framework outlines the stages a malicious actor must go through to execute a successful cyber attack. By understanding these stages, you can better defend against various threats.

**Why is it essential to grasp the Cyber Kill Chain?**

Understanding the Cyber Kill Chain is crucial for defending against ransomware, security breaches, and Advanced Persistent Threats (APTs). By applying this framework, you can assess your network’s security, pinpoint gaps, and reinforce weak spots.

For SOC Analysts, Security Researchers, Threat Hunters, or Incident Responders, mastering the Kill Chain enables you to detect intrusion attempts and comprehend an attacker’s goals.

In this room, we’ll explore the following attack phases:

- Reconnaissance
- Weaponization
- Delivery
- Exploitation
- Installation
- Command & Control
- Actions on Objectives

**Learning Objectives:** This room will deepen your understanding of each phase of the Cyber Kill Chain, including its strengths and limitations.

**Outcome:** By the end, you'll be equipped to identify and disrupt various stages of an attack, effectively breaking the “kill chain.”

**Question Section:** 
No response required.

### Task 2: Reconnaissance

Let’s begin by defining reconnaissance from an attacker’s viewpoint. Reconnaissance involves gathering information about a system or a victim, serving as the initial planning stage for an adversary.

Open-Source Intelligence (OSINT) is a crucial component of this phase, allowing attackers to gather information from publicly available sources. This might include details about a company’s size, employee contact information, or other relevant data that can aid in targeting.

For example, let’s consider an attacker who calls himself “Megatron.” He plans a sophisticated attack and starts with reconnaissance. During this stage, Megatron might engage in email harvesting—a method of gathering email addresses for use in phishing attacks. 

Here are some tools that might be used during this phase:

- **theHarvester**: This tool collects emails, names, subdomains, IPs, and URLs from various public data sources.
- **Hunter.io**: A tool for finding contact information associated with a domain.
- **OSINT Framework**: A collection of OSINT tools organized by category.

Attackers also exploit social media platforms like LinkedIn, Facebook, and Twitter to gather additional information on potential targets.

**Questions:**
1. What is the name of the Intel Gathering Tool that is a web-based interface to the common tools and resources for open-source intelligence?  
   **Answer:** OSINT Framework

2. What is the term for the process of gathering email addresses during the reconnaissance stage?  
   **Answer:** Email harvesting

### Task 3: Weaponization

Weaponization involves creating malicious software or documents that can be used to exploit a system. For instance, an attacker might create an infected Microsoft Office document with a malicious macro or Visual Basic for Applications (VBA) scripts.

Attackers may also create payloads or worms, embed them into USB drives, and distribute these in public. Additionally, they might use Command and Control (C2) techniques to remotely execute commands on a victim’s machine.

**Questions:**
1. What term refers to a group of commands designed to perform specific tasks, which can be exploited for malicious purposes in Microsoft Office documents?  
   **Answer:** Macro

### Task 4: Delivery

In the Delivery phase, the attacker selects the method to transmit the payload. Common methods include:

- **Phishing emails**: Crafting emails that appear legitimate but contain malicious payloads.
- **Infected USB drives**: Distributing USB drives laced with malware in public places.
- **Watering hole attacks**: Compromising a website frequented by a specific group and using it to deliver malware.

**Questions:**
1. What is the term for an attack that targets a specific group by infecting a website they regularly visit?  
   **Answer:** Watering hole attack

### Task 5: Exploitation

To gain access, an attacker must exploit a vulnerability. This could involve phishing emails, exploiting software vulnerabilities, or using zero-day exploits, which are vulnerabilities unknown to software vendors or antivirus solutions.

**Questions:**
1. What is the term for an attack that targets an unknown software vulnerability?  
   **Answer:** Zero-day

### Task 6: Installation

After exploiting a system, an attacker might install a backdoor to maintain access. Persistence techniques might include:

- Installing web shells on servers.
- Modifying Windows services or registry keys to execute malicious payloads on startup.
- Timestomping to alter file timestamps and avoid detection.

**Questions:**
1. What technique is used to modify file time attributes to conceal changes?  
   **Answer:** Timestomping

2. What is the name of the malicious script that an attacker might plant on a web server to maintain access?  
   **Answer:** Web shell

### Task 7: Command & Control

Once access is established, the attacker sets up a C2 channel to control the compromised system. Common C2 channels include:

- **HTTP/HTTPS**: Using common web protocols to blend malicious traffic with legitimate traffic.
- **DNS tunneling**: Using DNS requests to communicate with a C2 server.

**Questions:**
1. What is the name of the C2 communication technique where the victim makes regular DNS requests to an attacker-controlled server?  
   **Answer:** DNS tunneling

### Task 8: Actions on Objectives

Finally, the attacker achieves their goals, which might involve exfiltrating data, escalating privileges, or causing disruption.

**Questions:**
1. What is the name of the Microsoft technology that allows the creation of backup copies or snapshots of files or volumes?  
   **Answer:** Shadow Copy

### Task 9: Practice Analysis

Let’s apply what you’ve learned to a real-world scenario: the infamous 2013 Target data breach, which resulted in the theft of millions of credit and debit card records. Use the Static Site Lab provided to map this breach to the Cyber Kill Chain.

**Questions:**
1. What is the flag after you complete the static site?  
   **Answer:** THM{7HR347_1N73L_12_4w35om3}

### Task 10: Conclusion

The Cyber Kill Chain is a valuable framework for improving network defenses, but it’s not perfect. Since its last update in 2011, cyber threats have evolved, and relying solely on the traditional Kill Chain can leave gaps in your defenses. Combining this framework with others, like MITRE ATT&CK and Unified Kill Chain, provides a more comprehensive approach to cybersecurity.

Thanks for following along in this walkthrough. Stay tuned for the next guide on the “Unified Kill Chain.”