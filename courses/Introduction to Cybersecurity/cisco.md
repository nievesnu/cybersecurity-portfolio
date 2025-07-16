# 🌐 Cisco – Introduction to Cybersecurity


### My Knowledge Check Result
<img width="1605" height="647" alt="Captura de pantalla 2025-07-14 192625" src="https://github.com/user-attachments/assets/2d069a19-f041-430b-8327-9604ef56b15d" />

> Before completing the course, I answered the initial questions to check my current knowledge at the time.
> I did this to be able to compare it with the final exam and measure the skills I gained during the course.

---

## Module 1: Introduction to Cybersecurity

### What is Cybersecurity?

> An ongoing effort to protect individuals, organizations, and governments from digital attacks.

- How can hackers access your personal data? Through Medical records, Educational records & Employment and financial records.

### What do hackers want?

**Example (Phishing Attack):**  
A phishing scam targeted users of an online bank. Victims received an email that looked like a real notification warning of "suspicious activity" and asked them to click a link to verify their identity.  
The link led to a **fake login page**. When users entered their credentials, attackers stole the data and accessed their accounts.

### Identity Theft (is not a joke, Jim):
- Used to incur high medical bills (especially in systems without universal healthcare).
- Used to steal money or take out loans under another person’s name.

### Who else wants my data?
- **ISPs (Internet Service Providers):** Track your online activity and may sell it to advertisers.
- **Advertisers:** Use online habits and preferences for targeted ads.
- **Search engines & social media:** Collect gender, location, phone number, ideologies, etc.
- **Websites:** Use cookies to track and sell user data trails.

---
### Types of Organizational Data

- **Traditional:** Transactional data, intellectual property, financial data  
- **IoT:** Devices connected to the internet that collect and share data  

### The Security Cube (3D Framework)

#### CIA Triad – Core Principles of Cybersecurity:

- **Confidentiality:** Encryption, identity proofing, two-factor authentication  
- **Integrity:** Use of hash functions or checksums  
- **Availability:** Hardware maintenance, updates, backups  

#### Data States:

- **Data in process:** Actively being used (e.g., updating a database)  
- **Data at rest:** Stored on disk or memory  
- **Data in transit:** Moving between systems or networks  

### Protection Measures:

- **People:** Awareness, training, education  
- **Technology:** Firewalls, antivirus, secure hardware  
- **Policies and Procedures:** Rules and frameworks to govern access and response
---

### Data Security Breaches – Examples

- **Persirai Botnet:** Exploited IoT cameras via open ports for DDoS attacks  
- **Equifax Breach:** US credit reporting agency compromised due to web exploit  

### Consequences of Security Breaches

- **Reputational Damage:** Loss of trust, compensation, slow recovery  
- **Vandalism:** Inserting false info (e.g., fake phone number on website)  
- **Theft:** Personal data used for fraud or identity theft  
- **Loss of Revenue:** Direct financial impact and business disruption  
- **Damaged Intellectual Property:** Leaked trade secrets hurt competitiveness  

---

**Practical Case 1**: 
- Data: Massive data breach in an hotel chain the hackers couldn´t access account or financial info.
- Vulnerability: hackers gained access via customer database by using employees login details
- Result: The hackers stole the personal information of over three million hotel guests. This included their names, email addresses and phone numbers.
**Practical Case 2**: 
- Data: bad management of clients information - can be used for phising malware and fraud
- Vulnerability: leaving it at the public site - bad security practice (control your access via 2fa or smt!)
- Result: Hackers are targeting the increasing numbers of organizations who are migrating to the cloud or using cloud-based services and resources. In this scenario, hackers were able to take advantage of an organization’s poor security practices. Unsecured cloud databases left exposed on the Internet present a huge vulnerability and one that attackers will seek to exploit to gain easy access to valuable organizational data.  

In both cases, the organizations need to invest in improved security practices.

This might include:

- investing in cybersecurity training for all staff so that they are aware of and able to spot a cyber attack
- enforcing two factor authentication for employees accessing files and applications that contain sensitive data
- maintaining log files and ongoing monitoring to identify anomalous behavior that might indicate a data breach
- storing the passwords of customers using a combination of salting and robust hashing algorithms
- separating cloud-based resources from the public Internet into an isolated private network segment
- granting employee access to personal data and internal systems only via a secure VPN connection.

https://www.netacad.com/content/i2cs/7.1/courses/content/m1/en-US/assets/m1-lab-what-was-taken.pdf
-> https://github.com/nievesnu/cybersecurity-portfolio/courses/Introduction to Cybersecurity/breach-examples.md
---
## Types of Attackers

- Script kiddies: amateurs
- White hat: breaks in prior permission to look for vulnerabilities to improve the security of a network or system
- Grey hat: similar to white but biased can published vulnerabilities they found or report to the owner
- Black hat: takes advantage of vulnerability for gain
- Organized hackers (Anonymus): have cyber criminals, hacktivists(awareness about issues) terrorist and state sponsored hackers (pigs, commits sabotage on behalf of their government, well funded)

**Internal Threats**: Employees => clumsy
**External Threats**: Outsiders => have to gain access

**Stuxnet malware** was designed not just to hijack targeted computers but to actually cause physical damage to equipment controlled by computers
Non-Trivial distribution, Sophistication, Modular coding, Unique Target(patience), Motive.
**The Purpose of Cyberwarfare** gain advantage over adversaries via compromised info via espionage = disruption & chaos.

Module 1 Quiz Result: <img width="902" height="635" alt="image" src="https://github.com/user-attachments/assets/6a555e94-0d77-4399-8700-50ffbf9dfdc8" />


---

## Module 2: Attacks, Concepts and Techniques

## Types of Malware:
Spyware: designed to track and spy on you, spyware monitors your online activity and can log every key you press on your keyboard, as well as capture almost any of your data, including sensitive personal information such as your online banking details. Spyware does this by modifying the security settings on your devices. It often bundles itself with legitimate software or Trojan horses.
Adware: is often installed with some versions of software and is designed to automatically deliver advertisements to a user, most often on a web browser. You know it when you see it! It’s hard to ignore when you’re faced with constant pop-up ads on your screen. It is common for adware to come with spyware.
Backdoor: is used to gain unauthorized access by bypassing the normal authentication procedures to access a system. As a result, hackers can gain remote access to resources within an application and issue remote system commands. A backdoor works in the background and is difficult to detect.
Ransomware: is designed to hold a computer system or the data it contains captive until a payment is made. Ransomware usually works by encrypting your data so that you can’t access it.
Some versions of ransomware can take advantage of specific system vulnerabilities to lock it down. Ransomware is often spread through phishing emails that encourage you to download a malicious attachment or through a software vulnerability.
Scareware: uses 'scare’ tactics to trick you into taking a specific action. Scareware mainly consists of operating system style windows that pop up to warn you that your system is at risk and needs to run a specific program for it to return to normal operation. If you agree to execute the specific program, your system will become infected with malware.
Rootkit: is designed to modify the operating system to create a backdoor, which attackers can then use to access your computer remotely. Most rootkits take advantage of software vulnerabilities to gain access to resources that normally shouldn’t be accessible (privilege escalation) and modify system files. Rootkits can also modify system forensics and monitoring tools, making them very hard to detect. In most cases, a computer infected by a rootkit has to be wiped and any required software reinstalled.
Virus: is a type of computer program that, when executed, replicates and attaches itself to other executable files, such as a document, by inserting its own code. Most viruses require end-user interaction to initiate activation and can be written to act on a specific date or time. Viruses can be relatively harmless, such as those that display a funny image. Or they can be destructive, such as those that modify or delete data.
Viruses can also be programmed to mutate in order to avoid detection. Most viruses are spread by USB drives, optical disks, network shares or email.
Trojan horse: carries out malicious operations by masking its true intent. It might appear legitimate but is, in fact, very dangerous. Trojans exploit your user privileges and are most often found in image files, audio files or games. Unlike viruses, Trojans do not self-replicate but act as a decoy to sneak malicious software past unsuspecting users.
Worms: replicates itself in order to spread from one computer to another. Unlike a virus, which requires a host program to run, worms can run by themselves. Other than the initial infection of the host, they do not require user participation and can spread very quickly over the network. Worms share similar patterns: They exploit system vulnerabilities, they have a way to propagate themselves, and they all contain malicious code (payload) to cause damage to computer systems or networks. Worms are responsible for some of the most devastating attacks on the Internet. In 2001, the Code Red worm had infected over 300,000 servers in just 19 hours.

---
## Infiltration
**Social Engineering** = manipulation of people in an attempt to gain access to privileged data then tailgating and quid pro quo.
**Denial-of-Service Attack** Overwhelming  quantity of traffic vs Maliciously formatted packets
**Distributed Denial-of-Service Attack** similar to DoS but coordinated between multiple sources.
**Botnet** is a group of bots, connected through the Internet, that can be controlled by a malicious individual or group, typically controlled through a command and control server.
Infected bots try to communicate with a command and control host on the Internet.
The Cisco Firewall botnet filter is a feature that detects traffic coming from devices infected with the malicious botnet code.
The cloud-based Cisco Security Intelligence Operations (SIO) service pushes down updated filters to the firewall that match traffic from new known botnets.
Alerts go out to Cisco’s internal security team to notify them about the infected devices that are generating malicious traffic so that they can prevent, mitigate and remedy these.
**On-Path Attacks** intercept or modify communications between two devices man-in-the-middle or man-in-the-mobile attack.
**SEO Poisoning** attackers take advantage of popular search terms and use SEO to push malicious sites higher up the ranks of search results. The most common goal is to increase traffic to malicious sites that may host malware or attempt social engineering.
**Wi-Fi Password Cracking** 
**Password Attacks** .
Password spraying attempts to gain access to a system by ‘spraying’ a few commonly used passwords across a large number of accounts. For example, a cybercriminal uses 'Password123' with many usernames before trying again with a second commonly-used password, such as ‘qwerty.’ This technique allows the perpetrator to remain undetected as they avoid frequent account lockouts.
Dictionary attacks A hacker systematically tries every word in a dictionary or a list of commonly used words as a password in an attempt to break into a password-protected account.
Brute-force attacks simplest and most commonly used way of gaining access to a password-protected site, brute-force attacks see an attacker using all possible combinations of letters, numbers and symbols in the password space until they get it right.
Rainbow attacks Passwords in a computer system are not stored as plain text, but as hashed values (numerical values that uniquely identify data). A rainbow table is a large dictionary of precomputed hashes and the passwords from which they were calculated. Unlike a brute-force attack that has to calculate each hash, a rainbow attack compares the hash of a password with those stored in the rainbow table. When an attacker finds a match, they identify the password used to create the hash.
Traffic interception If you store a password in clear, anyone who has access to your account or device can read it.
**Advanced Persistent Threats** (APTs) — a multi-phase, long term, stealthy and advanced operation against a specific target. well-funded and typically targets organizations or nations for business or political reasons.

---
## Hardware Vulnerabilities
Most often the result of hardware design flaws. Hardware vulnerabilities are specific to device models and are not generally exploited through random compromising attempts.
SYNful Knock vulnerability discovered in Cisco Internetwork Operating System (IOS) in 2015 allowed attackers to gain control of enterprise-grade routers, such as the legacy Cisco ISR routers, from which they could monitor all network communication and infect other network devices. This vulnerability was introduced into the system when an altered IOS version was installed on the routers. To avoid this, you should always verify the integrity of the downloaded IOS image and limit the physical access of such equipment to authorized personnel only.
**Categorizing Software Vulnerabilities** 
Buffer overflow: Buffers are memory areas allocated to an application. A vulnerability occurs when data is written beyond the limits of a buffer. By changing data beyond the boundaries of a buffer, the application can access memory allocated to other processes. This can lead to a system crash or data compromise, or provide escalation of privileges.
Non-validated input: Programs often require data input, but this incoming data could have malicious content, designed to force the program to behave in an unintended way.
For example, consider a program that receives an image for processing. A malicious user could craft an image file with invalid image dimensions. The maliciously crafted dimensions could force the program to allocate buffers of incorrect and unexpected sizes.
Race conditions: the output of an event depends on ordered or timed outputs. A race condition becomes a source of vulnerability when the required ordered or timed events do not occur in the correct order or proper time.
Weaknesses in security practices: 
Systems and sensitive data can be protected through techniques such as authentication, authorization and encryption. Developers should stick to using security techniques and libraries that have already been created, tested and verified and should not attempt to create their own security algorithms. These will only likely introduce new vulnerabilities.
Access control problems
Access control is the process of controlling who does what and ranges from managing physical access to equipment to dictating who has access to a resource, such as a file, and what they can do with it, such as read or change the file. Many security vulnerabilities are created by the improper use of access controls.
Nearly all access controls and security practices can be overcome if an attacker has physical access to target equipment. For example, no matter the permission settings on a file, a hacker can bypass the operating system and read the data directly off the disk. Therefore, to protect the machine and the data it contains, physical access must be restricted, and encryption techniques must be used to protect data from being stolen or corrupted.

---
## Cryptocurrency & Cryptojacking
Cryptocurrency is digital money that can be used to buy goods and services, using strong encryption techniques to secure online transactions.
Cryptojacking is an emerging threat that hides on a user’s computer, mobile phone, tablet, laptop or server, using that machine’s resources to 'mine’ cryptocurrencies without the user's consent or knowledge.

---

Module 2 Quiz Result: <img width="936" height="644" alt="image" src="https://github.com/user-attachments/assets/6769f98a-7808-4fd7-a0c0-92c2eedf76ef" />

---
##  Module 3: Protecting Your Data and Privacy

Protect computer device: Turn the firewall on - Install antivirus and antispyware - Manage your operating system and browser - Set up password protection
Wireless Network Security at home with WPA2 encryption.
**Password**
1. Do not use dictionary words or names in any lenguages
2. Do not use common misspelling of dictionary words
3. Use special characters
4. Do not use computer names or account names
5. Use a p with >10 characters
*NIST guidelines are stronger

---
**Encryption:** converting information into a form in which unauthorized parties cannot read it
How? -> choose a folder > properties > advanced > Encrypt contents to secure data = EFS encription
**BackupData:** at home, secondary location and in the cloud.
**Delete Data Permanently:** It must be overwritten, to do so we have to use specific tools. Windows: SDelete, Linus Shred, MacOS X empty trash.
The only way to be certain that data or files are not recoverable is to physically destroy the hard drive or storage device.

---
**Data Ownership**
The Terms of Service are a legally binding contract that governs the rules of the relationship between you, the service provider and others who use the service.
Before agreeing to use an online service, read the privacy policy and terms of service to understand how your data will be used. Use strong, unique passwords and enable two-factor authentication (2FA) to protect your account. Avoid sharing sensitive information unless necessary. Regularly update your software and review account activity. Be cautious of phishing attempts and only access services from secure networks.
To protect your data and safeguard your account, you should: always read the Terms of Service when registering for a new service and decide whether the service is worth waiving your rights to your data for
select your privacy settings rather than accepting the default, limit the group of people you share content with, review the service provider’s security policy to understand what they are doing to protect your data,
change your passwords periodically, use a complex password and two factor authentication to secure your account.

---
**Two Factor Authentication** adds an extra layer of security for account logins.
OAuth is an open standard protocol that allows you to use your credentials to access third-party applications without exposing your password.
Social sharing rule: the less the best
Dont get Spoofed
Private browsing = less data of yourself trhough the internet bcs disabled cookies & traces of your roundabouts.

---
Password manager applications can protect passwords by saving them in a secure encrypted form. They enable random passwords to be generated and managed easily, averting the need for users to have the same password for multiple accounts, which presents a security risk.

---
Quiz Module 3 Result: <img width="1022" height="644" alt="image" src="https://github.com/user-attachments/assets/afbd4e1e-c186-46f6-9bfe-02a9af7ba3ab" />

---
## Module 4: Protecting the Organization

**Security Appliances** can be standalone devices like a router or software tools that are run on a network device. They fall into six general categories.
Routers
While routers are primarily used to interconnect various network segments together, they usually also provide basic traffic filtering capabilities. This information can help you define which computers from a given network segment can communicate with which network segments.
Firewalls
Firewalls can look deeper into the network traffic itself and identify malicious behavior that has to be blocked. Firewalls can have sophisticated security policies applied to the traffic that is passing through them.
Intrusion prevention systemsFirewalls
In computer networking, a firewall is designed to control or filter which communications are allowed in and which are allowed out of a device or network. A firewall can be installed on a single computer with the purpose of protecting that one computer (host-based firewall) or it can be a standalone network device that protects an entire network of computers and all of the host devices on that network (network-based firewall).

As computer and network attacks have become more sophisticated, new types of firewalls have been developed, which serve different purposes.

Network layer firewall This filters communications based on source and destination IP addresses.
Transport layer firewall Filters communications based on source and destination data ports, as well as connection states.
Application layer firewall Filters communications based on an application, program or service.
Context aware layer firewall Filters communications based on the user, device, role, application type and threat profile.
Proxy server Filters web content requests like URLs, domain names and media types.
Reverse proxy server Placed in front of web servers, reverse proxy servers protect, hide, offload and distribute access to web servers.
Network address translation (NAT) firewall hides or masquerades the private addresses of network hosts.
Host-based firewall Filters ports and system service calls on a single computer operating system.

IPS systems use a set of traffic signatures that match and block malicious traffic and attacks.
Virtual private networks
VPN systems let remote employees use a secure encrypted tunnel from their mobile computer and securely connect back to the organization’s network. VPN systems can also securely interconnect branch offices with the central office network.
Antimalware or antivirus
These systems use signatures or behavioral analysis of applications to identify and block malicious code from being executed.
Other security devices
Other security devices include web and email security appliances, decryption devices, client access control servers and security management systems.

---
**Port Scanning**  each application running on a device is assigned an identifier called a port number. This port number is used on both ends of the transmission so that the right data is passed to the correct application. Port scanning is a process of probing a computer, server or other network host for open ports. It can be used maliciously as a reconnaissance tool to identify the operating system and services running on a computer or host, or it can be used harmlessly by a network administrator to verify network security policies on the network.

Nmap my ip: https://hackertarget.com/nmap-online-port-scanner/
Starting Nmap 7.80 ( https://nmap.org ) at 2025-07-16 10:27 UTC
Nmap scan report for **.***.***.**.dyn.user.ono.com (**.***.***.**)
Host is up (0.12s latency).

PORT     STATE    SERVICE       VERSION
21/tcp   filtered ftp
22/tcp   filtered ssh
23/tcp   closed   telnet
80/tcp   filtered http
110/tcp  closed   pop3
143/tcp  closed   imap
443/tcp  filtered https
3389/tcp closed   ms-wbt-server

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 2.66 seconds

**IDS VS IPS**
Intrusion detection systems (IDSs) and intrusion prevention systems (IPSs) are security measures deployed on a network to detect and prevent malicious activities.
<img width="1054" height="563" alt="image" src="https://github.com/user-attachments/assets/468dbc24-3cc8-48ce-80c0-0223c24ca88a" />
**Cisco's Threat Grid.**

Secure Operations Center team gather more accurate, actionable data.
Incidence Response team  has access to forensically sound information from which it can more quickly analyze and understand suspicious behaviors.
Threat Intelligence team, using this analysis, can proactively improve the organization’s security infrastructure.
Security Infrastructure Engineering team is able to consume and act on threat information faster, often in an automated way.

**Security Best Practices**  .
Perform a risk assessment
Knowing and understanding the value of what you are protecting will help to justify security expenditures.

Create a security policy that clearly outlines the organization’s rules, job roles, and responsibilities and expectations for employees.
Physical security measures Restrict access to networking closets and server locations, as well as fire suppression.
Human resources security measures Background checks should be completed for all employees.
Perform and test backups Back up information regularly and test data recovery from backups.
Maintain security patches and updates Regularly update server, client and network device operating systems and programs.
Employ access controls Configure user roles and privilege levels as well as strong user authentication.
Regularly test incident response Employ an incident response team and test emergency response scenarios.
Implement a network monitoring, analytics and management tool Choose a security monitoring solution that integrates with other technologies.
Implement network security devices Use next generation routers, firewalls and other security appliances.
Implement a comprehensive endpoint security solution Use enterprise level antimalware and antivirus software.
Educate users Provide training to employees in security procedures.
One of the most widely known and respected organizations for cybersecurity training is the SANS Institute. Click here to learn more about SANS and the types of training and certifications they offer.
Encrypt data, all sensitive organizational data, including email.

---

---

---

## Module 5: Will Your Future Be in Cybersecurity?

*()*

---

## Final Exam: Course Completion

*()*

---

### Notes

This Markdown serves as a study log and reference for key cybersecurity principles learned through the Cisco "Introduction to Cybersecurity" course.

