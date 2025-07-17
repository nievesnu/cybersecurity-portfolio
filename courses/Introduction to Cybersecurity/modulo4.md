## Module 4: Protecting the Organization

### Security Appliances

Security appliances can be standalone devices (e.g., routers) or software tools that run on a network device. They are generally categorized as follows:

#### Routers

Primarily used to connect network segments. They also offer basic traffic filtering, helping control communication between different segments.

#### Firewalls

Firewalls inspect network traffic for malicious behavior and apply security policies to allow or block traffic. Types include:

* **Network layer firewall**: Filters by IP addresses.
* **Transport layer firewall**: Filters by data ports and connection states.
* **Application layer firewall**: Filters by applications or services.
* **Context-aware layer firewall**: Filters by user, device, role, and threat profile.
* **Proxy server**: Filters web content requests.
* **Reverse proxy server**: Protects and manages access to web servers.
* **NAT firewall**: Hides internal IP addresses.
* **Host-based firewall**: Filters traffic on individual systems.

#### Intrusion Prevention Systems (IPS)

Use traffic signatures to detect and block malicious activities in real-time.

#### Virtual Private Networks (VPNs)

Create secure encrypted tunnels for remote access and interconnect branch offices securely.

#### Antimalware/Antivirus

Identify and block malicious code using signature and behavior-based analysis.

#### Other Security Devices

Include web/email security appliances, decryption tools, access control servers, and management systems.

---

### Port Scanning

Each application uses a port number for communication. Port scanning probes for open ports, which can:

* Reveal running services and the OS (used in attacks)
* Help network admins verify firewall configurations

Example using Nmap:

```
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
```

---

### IDS vs IPS

* **Intrusion Detection System (IDS)**: Monitors and alerts on suspicious traffic.
* **Intrusion Prevention System (IPS)**: Monitors and actively blocks malicious traffic.

Image: Cisco's Threat Grid <img width="1054" height="563" alt="image" src="https://github.com/user-attachments/assets/468dbc24-3cc8-48ce-80c0-0223c24ca88a" />

#### Teams Involved

* **SOC team**: Secure Operations Center collects actionable security data.
* **Incident Response team**:  has access to forensically sound information then analyzes behavior for faster mitigation.
* **Threat Intelligence team**: enhances defense through analysis, improving the organization’s security infrastructure..
* **Engineering team**:  is able to consume and act on threat information faster, often in an automated way.
---

### Security Best Practices

* **Risk assessment**: Identify valuable assets and risks.
* **Security policies**: Define rules, roles, and responsibilities.
* **Physical security**: Restrict access to equipment.
* **HR security**: Perform background checks.
* **Backups**: Regularly back up and test data recovery.
* **Patching**: Keep systems updated.
* **Access control**: Use role-based permissions and strong authentication.
* **Incident response**: Employ and drill response teams.
* **Monitoring tools**: Use integrated analytics tools.
* **Network security devices**: Use next-gen routers/firewalls.
* **Endpoint security**: Use enterprise antimalware.
* **User education**: Train staff on security.
* **Data encryption**: Encrypt all sensitive data.

---

### Behavior-Based Security

* **Honeypots**: Decoy systems that trap attackers and log their behavior.
* **Cisco Cyber Threat Defense**: Uses behavior-based detection to identify the who/what/when/where/how of attacks.
<img width="508" height="398" alt="image" src="https://github.com/user-attachments/assets/92049cfd-1073-4d02-8ed6-b9d7ac0a3da4" />

#### NetFlow Technology

Collects metadata about network traffic, showing who, when, and how devices access the network.
<img width="531" height="426" alt="image" src="https://github.com/user-attachments/assets/6e320fe0-7872-4e45-9083-ca28d6d58174" />

---

### Penetration Testing

A controlled attack to identify and fix vulnerabilities:

1. **Planning**: Information gathering and footprinting.
2. **Scanning**: Port/vulnerability scanning and enumeration.
3. **Gaining Access**: Exploiting systems via payloads, social engineering, or misconfigurations.
4. **Maintaining Access**: Staying undetected using backdoors, Trojans, and rootkits.
5. **Reporting**: Share findings to improve defenses.

---

### Impact Reduction

* **Communicate**: Internally and externally, be transparent.
* **Accountability**: Own up and respond sincerely.
* **Details**: Disclose what happened and what was compromised.
* **Cause**: Investigate and identify the breach vector.
* **Apply Lessons**: Improve systems based on findings.
* **Recheck**: Ensure no backdoors remain.
* **Educate**: Train staff and stakeholders.

---

### Risk Management

Risk management is the formal process of continuously identifying and assessing risk in an effort to reduce the impact of threats and vulnerabilities. You cannot eliminate risk completely but you can determine acceptable levels by weighing up the impact of a threat with the cost of implementing controls to mitigate it. The cost of a control should never be more than the value of the asset you are protecting.

1. **Frame the risk**: Identify the threats that increase risk. Threats may include processes, products, attacks, potential failure or disruption of services, negative perception of an organization’s reputation, potential legal liability or loss of intellectual property.
2. **Assess the risk**: Determine the severity that each threat poses. For example, some threats may have the potential to bring an entire organization to a standstill, while other threats may be only minor inconveniences. Risk can be prioritized by assessing financial impact (a quantitative analysis) or scaled impact on an organization's operation (a qualitative analysis).
3. **Respond to the risk**: Develop an action plan to reduce overall organization risk exposure, detailing where risk can be eliminated, mitigated, transferred or accepted.
4. **Monitor the risk**: Continuously review any risk reduced through elimination, mitigation or transfer actions. Remember, not all risks can be eliminated, so you will need to closely monitor any threats that have been accepted.

---

### Cisco CSIRT

Cisco’s Computer Security Incident Response Team works with global partners (FIRST, NSIE, DSIE, DNS-OARC) to stay updated on threats.

#### Security Tools & Practices:

* **Playbooks**: Provide case-based response guides.
* **Detection/Prevention**: Use tools like SIEM and DLP.
* **Cisco Identity Services Engine (ISE)/TrustSec**: Enforce role-based access to resources.

---


* An IPS can block or deny traffic based on a positive rule or signature match.
* An IDS scans data against a database of rules or attack signatures, looking for malicious traffic.
* A DLP system is designed to stop sensitive data from being stolen from or escaping a network. 
* A SIEM system collects and analyzes security alerts, logs and other real-time and historical data from security devices on the network.

---
### Exam Result

<img width="917" height="619" alt="image" src="https://github.com/user-attachments/assets/8454898c-79ba-49d5-8796-b703fda84672" />

---
