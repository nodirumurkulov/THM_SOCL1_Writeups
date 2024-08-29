
**Diamond Model | TryHackMe — Walkthrough**

Learn about the four core features of the Diamond Model of Intrusion Analysis: adversary, infrastructure, capability, and victim.

### Task 1: Introduction
**What is the Diamond Model?**

The Diamond Model of Intrusion Analysis was developed in 2013 by cybersecurity professionals Sergio Caltagirone, Andrew Pendergast, and Christopher Betz.

The model is built around four core features: adversary, infrastructure, capability, and victim. These components form the fundamental elements of any intrusion activity. You may also come across two additional components—Social-Political and Technology—which will be discussed later in this room. The model is named the “Diamond Model” because these four core features are interconnected at the edges, forming a diamond shape.

The Diamond Model encapsulates the essential concepts of intrusion analysis and adversary operations, while also offering flexibility to adapt to new ideas. It allows for real-time integration of intelligence for network defense, automated event correlation, classification of adversary campaigns, and the ability to forecast adversary operations and plan mitigation strategies.

**Why should you learn about the Diamond Model?**

The Diamond Model helps you identify the elements of an intrusion. By the end of this room, you’ll be able to construct a Diamond Model for various events, such as breaches or attacks, and analyze Advanced Persistent Threats (APTs). Additionally, the model can help explain events to non-technical audiences, providing valuable insights into the actions of malicious threat actors.

**Questions:**

1. Read the above.  
   **Answer:** No answer needed

### Task 2: Adversary
**Who is an Adversary?**

An adversary, also known as an attacker, enemy, cyber threat actor, or hacker, is the person or group behind a cyberattack. According to the creators of the Diamond Model, an adversary is an actor or organization responsible for utilizing a capability against a victim to achieve their goals. Often, identifying the adversary during the early stages of a cyberattack is difficult, but gathering data from the incident can help in determining who the adversary might be.

It’s important to distinguish between an adversary operator and an adversary customer:

- **Adversary Operator:** The individual or group conducting the intrusion activities.
- **Adversary Customer:** The entity that benefits from the activities. This could be the same person as the operator or a separate group.

For example, an adversary customer might control multiple operators, each with its own capabilities and infrastructure.

**Questions:**

1. What is the term for a person or group with the intention to perform malicious actions against cyber resources?  
   **Answer:** Adversary Operator

2. What is the term for the person or group that benefits from the cyberattacks?  
   **Answer:** Adversary Customer

### Task 3: Victim
**Victim** refers to the target of the adversary, which could be an organization, individual, target email address, IP address, domain, etc. It’s crucial to understand the difference between victim personae and victim assets:

- **Victim Personae:** The people or organizations targeted by the adversary.
- **Victim Assets:** The systems, networks, email addresses, and other resources that the adversary targets.

For example, in a spear-phishing attack, the victim is the individual who clicks on a malicious link, making them the target of the adversary’s interest.

**Questions:**

1. What is the term in the Diamond Model for organizations or people being targeted?  
   **Answer:** Victim Personae

### Task 4: Capability
**Capability** refers to the skills, tools, and techniques used by the adversary in an event. It includes everything from basic techniques like manual password guessing to more sophisticated methods like developing malware.

- **Capability Capacity:** The vulnerabilities and exposures that a particular capability can exploit.
- **Adversary Arsenal:** The complete set of tools and capabilities that an adversary possesses.

An adversary must have the necessary capabilities or access to such capabilities, whether that involves malware development skills or acquiring ransomware as a service.

**Questions:**

1. What is the term for the set of tools or capabilities that belong to an adversary?  
   **Answer:** Adversary Arsenal

### Task 5: Infrastructure
**Infrastructure** refers to the physical or logical interconnections that an adversary uses to deliver capabilities or maintain control. This can include IP addresses, domain names, email addresses, or even malicious USB devices.

- **Type 1 Infrastructure:** Infrastructure controlled or owned by the adversary.
- **Type 2 Infrastructure:** Infrastructure controlled by an intermediary, which the victim perceives as the adversary’s infrastructure. This type is often used to obfuscate the true source of an attack.

**Questions:**

1. To which type of infrastructure do malicious domains and compromised email accounts belong?  
   **Answer:** Type 2 Infrastructure

2. What type of infrastructure is most likely owned by an adversary?  
   **Answer:** Type 1 Infrastructure

### Task 6: Event Meta-Features
The Diamond Model includes six possible meta-features that can add valuable information:

- **Timestamp:** The date and time of the event, helping to identify patterns and group activities.
- **Phase:** The stages of an intrusion, such as reconnaissance, weaponization, and exploitation.
- **Result:** The outcome of the adversary’s operations, such as success, failure, or unknown, and its impact on the CIA (Confidentiality, Integrity, and Availability) triad.
- **Direction:** Describes the direction of the intrusion, whether it’s victim-to-infrastructure, infrastructure-to-victim, etc.
- **Methodology:** The general classification of the intrusion, such as phishing, DDoS, or breach.
- **Resources:** External resources needed for the intrusion, such as software, hardware, funds, or knowledge.

**Questions:**

1. What meta-feature does the axiom "Every malicious activity contains two or more phases which must be successfully executed in succession to achieve the desired result" belong to?  
   **Answer:** Phase

2. You can label the event results as "success," "failure," or "unknown." Which meta-feature is this related to?  
   **Answer:** Result

3. To what meta-feature does this phrase apply: "Every intrusion event requires one or more external resources to be satisfied prior to success"?  
   **Answer:** Resources

### Task 7: Social-Political Component
The social-political component describes the motivations and intent of the adversary, such as financial gain, gaining acceptance in the hacker community, hacktivism, or espionage.

For instance, a victim might provide resources, such as computing power for a botnet used in cryptocurrency mining, while the adversary gains financially.

### Task 8: Technology Component
The technology component highlights the relationship between capability and infrastructure, showing how the adversary operates and communicates. An example could be a watering-hole attack, where the adversary compromises a legitimate website that their targeted victims are likely to visit.

### Task 9: Practice Analysis
Ready to create your own Diamond Model? Deploy the static site attached to this task and explore the case study to extract the information needed for your Diamond Model.

**Questions:**

1. Complete all eight areas of the diamond. What is the flag that is displayed to you?  
   **Answer:** THM{DIAMOND_MODEL_ATTACK_CHAIN}

### Task 10: Conclusion
We hope you found this room helpful and that you can apply the Diamond Model concepts to disrupt threat activity. The Diamond Model is a scientific approach to improving the efficiency and accuracy of intrusion analysis. With this tool in your arsenal, you’ll be better equipped to leverage real-time intelligence for network defense and predict adversary operations.