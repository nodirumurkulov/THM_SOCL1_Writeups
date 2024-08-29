**Unified Kill Chain | TryHackMe — Guide**


In this room, we’ll dive into the Unified Kill Chain, a framework designed to outline the stages of a cyber attack and provide a method for identifying and mitigating risks to IT assets.

This room is relatively straightforward, focusing on theory and frameworks. However, as we progress further along this path, the challenges will become increasingly complex.

Link: [Unified Kill Chain Room](https://tryhackme.com/room/unifiedkillchain)

### Task 1: Introduction

Understanding the behaviors, objectives, and methodologies of cyber threats is crucial for establishing a robust cybersecurity defense, also known as a cybersecurity posture.

In this room, you'll be introduced to the Unified Kill Chain (UKC) framework, which is used to understand how cyber attacks unfold.

**Learning Objectives:**

- Grasp why frameworks like the UKC are essential for building a strong cybersecurity posture.
- Use the UKC to comprehend an attacker’s motivations, methodologies, and tactics.
- Understand the various phases of the UKC.
- Discover how the UKC complements other frameworks, such as MITRE ATT&CK.

**Let’s get started!**

### Task 2: What is a “Kill Chain”?

The term “Kill Chain” originates from the military, where it describes the stages of an attack. In cybersecurity, a “Kill Chain” refers to the sequence of steps attackers take to infiltrate a target.

For instance, an attacker might scan for vulnerabilities, exploit them, and escalate privileges—this sequence forms a “Kill Chain.” We’ll delve into these stages in more detail later in this room.

The goal is to understand an attacker’s Kill Chain so that you can implement defensive measures to either preemptively protect a system or disrupt an attacker’s attempts.

**Questions:**

1. Where does the term “Kill Chain” originate from?  
   **Answer:** Military

### Task 3: What is “Threat Modeling”?

Threat modeling in cybersecurity involves a series of steps to enhance the security of a system. Essentially, it’s about identifying risks and involves:

- Identifying which systems and applications need protection and understanding their role in the environment.
- Assessing vulnerabilities and weaknesses in these systems and how they might be exploited.
- Creating a plan to secure these systems against the identified vulnerabilities.
- Implementing policies to prevent these vulnerabilities from recurring, such as through a software development life cycle (SDLC) or employee training on phishing awareness.

Threat modeling is crucial for reducing risk within a system or application, as it provides a high-level overview of an organization’s IT assets (software or hardware) and the steps needed to address vulnerabilities.

The UKC can facilitate threat modeling by helping identify potential attack surfaces and how these systems might be exploited.

**Questions:**

1. What is the technical term for a piece of software or hardware in IT (Information Technology)?  
   **Answer:** Asset

### Task 4: Introducing the Unified Kill Chain

The Unified Kill Chain, published in 2017, complements (rather than competes with) other cybersecurity kill chain frameworks, such as Lockheed Martin’s and MITRE’s ATT&CK.

The UKC outlines 18 phases of an attack, covering everything from reconnaissance to data exfiltration and understanding an attacker’s motives. In this room, these phases are grouped into key areas for simplicity.

**Benefits of the Unified Kill Chain (UKC):**

- **Modern and Updated:** Released in 2017 and updated in 2022, the UKC reflects the current cybersecurity landscape.
- **Comprehensive:** With 18 phases, the UKC offers a detailed view of an attack, unlike other frameworks with fewer stages.
- **Realistic:** The UKC accounts for the fact that attackers often revisit various phases during an attack, providing a more accurate depiction of attack scenarios.

**Questions:**

1. In what year was the Unified Kill Chain framework released?  
   **Answer:** 2017

2. According to the Unified Kill Chain, how many phases are there in an attack?  
   **Answer:** 18

3. What is the name of the attack phase where an attacker uses techniques to evade detection?  
   **Answer:** Defense evasion

4. What is the name of the attack phase where an attacker removes data from a network?  
   **Answer:** Exfiltration

5. What is the name of the attack phase where an attacker achieves their objectives?  
   **Answer:** Objectives

### Task 5: Phase 1 — Initial Foothold

This phase focuses on how an attacker gains access to a system or network.

**Reconnaissance (MITRE Tactic TA0043):**  
Attackers gather information about their target through both passive and active means. This information is crucial for subsequent stages, such as weaponization and exploitation.

**Weaponization (MITRE Tactic TA0001):**  
Attackers set up the necessary infrastructure for the attack, such as command and control servers or systems for catching reverse shells and delivering payloads.

**Social Engineering (MITRE Tactic TA0001):**  
Techniques that manipulate individuals to perform actions that aid the attacker, such as opening malicious attachments or entering credentials on fake websites.

**Exploitation (MITRE Tactic TA0002):**  
Attackers take advantage of vulnerabilities to execute code on the target system, such as uploading a reverse shell or exploiting a web application vulnerability.

**Persistence (MITRE Tactic TA0003):**  
Once access is gained, attackers employ techniques to maintain it, such as creating a service that allows them to regain access or adding the system to a command and control server.

**Defense Evasion (MITRE Tactic TA0005):**  
Attackers use various methods to avoid detection, such as bypassing firewalls, antivirus systems, and intrusion detection systems.

**Command & Control (MITRE Tactic TA0011):**  
Attackers establish communication between their system and the target, allowing them to execute commands, steal data, and pivot to other systems.

**Pivoting (MITRE Tactic TA0008):**  
Attackers use the compromised system as a staging ground to access other systems within the network that are not directly reachable.

**Questions:**

1. What is an example of a tactic to gain a foothold using emails?  
   **Answer:** Phishing

2. Impersonating an employee to request a password reset is a form of what?  
   **Answer:** Social engineering

3. An adversary setting up the command and control server infrastructure is which phase of the Unified Kill Chain?  
   **Answer:** Weaponization

4. Exploiting a vulnerability on a system is which phase of the Unified Kill Chain?  
   **Answer:** Exploitation

5. Leaving behind a malicious service that allows the adversary to log back into the target system is known as what?  
   **Answer:** Persistence

### Task 6: Phase 2 — Network Propagation

After gaining an initial foothold, the attacker seeks to expand their access and privileges within the network.

**Discovery (MITRE Tactic TA0007):**  
Attackers gather information about the network, including user accounts, permissions, applications, and system configurations.

**Privilege Escalation (MITRE Tactic TA0004):**  
Attackers attempt to elevate their privileges, such as gaining SYSTEM/ROOT access, becoming a local administrator, or using a privileged user account.

**Execution (MITRE Tactic TA0002):**  
Attackers deploy their malicious code, using the compromised system as a host for remote trojans, C2 scripts, and other malicious payloads.

**Credential Access (MITRE Tactic TA0006):**  
Attackers steal account credentials, often using keyloggers or credential dumping to gain access to other systems.

**Lateral Movement (MITRE Tactic TA0008):**  
With stolen credentials and elevated privileges, attackers move through the network, targeting additional systems.

**Questions:**

1. As a SOC analyst, you detect numerous failed login attempts from an administrator account. What stage of the kill chain is the attacker attempting to achieve?  
   **Answer:** Privilege escalation

2. Mimikatz, a known attack tool, is detected running on the IT Manager’s computer. What is the tool’s mission?  
   **Answer:** Credential Access

### Task 7: Phase 3 — Action on Objectives

In this final phase, the attacker has achieved significant access and is now working toward their ultimate goal, whether that’s stealing data, disrupting operations, or causing damage.

**Collection (MITRE Tactic TA0009):**  
Attackers gather valuable data, such as files, browser data, audio, video, and emails, for later exfiltration.

**Exfiltration (MITRE Tactic TA0010):**  
Attackers steal data, often using encryption and compression to avoid detection. The data is then sent out through established C2 channels.

**Impact (MITRE Tactic TA0040):**  
Attackers compromise the integrity and availability of data by manipulating, destroying, or encrypting it, often as part of a ransomware attack or to disrupt operations.

**Objectives:**  
Attackers achieve their strategic goals, such as financial gain through ransomware, reputational damage by releasing confidential data, or disrupting business operations.

**Questions:**

1. While monitoring the network as a SOC analyst, you notice a spike in outbound traffic to an unknown IP address. Which stage does this activity describe?  
   **Answer:** Exfiltration

2. Personally identifiable information (PII) has been released to the public by an adversary, and your organization is facing scrutiny for the breach. Which part of the CIA triad is affected by

 this action?  
   **Answer:** Confidentiality

**Final Task:** Deploy the static site attached to this task. Match the various actions of an attacker to the correct phase of the Unified Kill Chain to reveal the flag.

**Answer:** Follow the directions on the static site to complete the quiz and reveal the flag.

**Conclusion**

Congratulations on completing the Unified Kill Chain room! This walkthrough highlights the importance of frameworks like the UKC in identifying risks and mitigating potential attacks by reconstructing the various steps an attacker might take.

The UKC is a modern extension of other frameworks, such as Lockheed Martin’s Cyber Kill Chain. If you’re interested in learning more about cybersecurity frameworks, be sure to check out these rooms on TryHackMe:

- Principles of Security
- Pentesting Fundamentals
- Cyber Kill Chain

This concludes the Unified Kill Chain room. Thanks for following along, and I’ll see you in the next walkthrough on the “Diamond Model.”