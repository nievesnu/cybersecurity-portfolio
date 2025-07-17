## Module 2: Attacks, Concepts and Techniques

## Types of Malware

* **Spyware**: Tracks and logs your activity (keystrokes, data, online behavior). Often bundled with legitimate software or trojans.
* **Adware**: Displays unwanted ads, usually in browsers. Often paired with spyware.
* **Backdoor**: Bypasses normal authentication to give remote access to a system. Hard to detect.
* **Ransomware**: Encrypts your data and demands payment to restore access. Spread via phishing or system vulnerabilities.
* **Scareware**: Uses fake warnings to trick users into installing malware.
* **Rootkit**: Alters OS to allow remote access. Very stealthy, often requires full system reinstall.
* **Virus**: Replicates and attaches to files. Needs user interaction. Can be destructive or harmless. Often spreads via USB, email, or network shares.
* **Trojan Horse**: Disguises as legit software. Doesn’t self-replicate but opens a door for malware.
* **Worms**: Self-replicate and spread independently. Don’t need user interaction. Used in major historical attacks like Code Red (2001).

---

## Infiltration Techniques

* **Social Engineering**: Human manipulation to gain access (e.g., tailgating, quid pro quo).
* **DoS (Denial-of-Service)**: Overwhelms target with traffic or malformed packets.
* **DDoS (Distributed DoS)**: Same as DoS but from multiple sources.
* **Botnet**: Network of infected machines controlled via a C\&C server.
* **On-Path Attacks**: Intercept or alter communications (Man-in-the-Middle/Mobile).
* **SEO Poisoning**: Ranks malicious sites higher using search optimization.
* **Wi-Fi Password Cracking**
* **Password Attacks**:

  * **Password Spraying**: Tries common passwords on many users.
  * **Dictionary Attack**: Uses lists of common passwords.
  * **Brute Force**: Tries every combination.
  * **Rainbow Table**: Uses precomputed hash tables.
  * **Traffic Interception**: Reads passwords stored or transmitted in plain text.
* **APT (Advanced Persistent Threats)**: Long-term, stealthy, highly targeted attacks, often nation-state sponsored.

---

## Hardware Vulnerabilities

* Result from design flaws in specific device models.
* **Example**: *SYNful Knock* on Cisco IOS (2015) allowed attackers to gain control of enterprise-grade routers, such as the legacy Cisco ISR routers, from which they could monitor all network communication and infect other network devices. This vulnerability was introduced into the system when an altered IOS version was installed on the routers.
* **Prevention**: Verify firmware integrity and restrict physical access. Verify the integrity of the downloaded IOS image and limit the physical access of such equipment to authorized personnel only.

---

## Categorizing Software Vulnerabilities

* **Buffer Overflow**: Writes data beyond buffer limits, can cause crashes or privilege escalation.
* **Non-Validated Input**: Malicious data input exploits program behavior (e.g., malformed image files).
* **Race Conditions**: Execution timing flaws can create vulnerabilities.
* **Weak Security Practices**: Avoid using custom security code. Use proven libraries.
* **Access Control Issues**:

  * Improper access settings can be exploited.
  * Physical access can override software protections — use encryption.

---

## Cryptocurrency & Cryptojacking

* **Cryptocurrency**: Digital money secured via encryption.
* **Cryptojacking**: Malware mines crypto using your device's resources without your consent.

---

## Module 2 Quiz Result

![Module 2 Quiz Result](https://github.com/user-attachments/assets/6769f98a-7808-4fd7-a0c0-92c2eedf76ef)

---
