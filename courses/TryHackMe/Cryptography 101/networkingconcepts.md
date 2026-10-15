# Networking Concepts — TryHackMe  

This document summarizes the **Networking Concepts** room from TryHackMe, part of the Cyber Security 101 learning path.  
It covers foundational networking topics including the OSI model, TCP/IP model, IP addressing, subnets, routing, TCP/UDP, encapsulation, and Telnet.

Room: https://tryhackme.com/room/networkingconcepts  


---

## Task 1 — Introduction

This room introduces core networking concepts essential for cybersecurity and system administration.

---

## Task 2 — OSI Model

The OSI Model is a **7‑layer framework** describing how data moves through a network.

### Q2.1: Which layer connects one application to another?  
**A: Layer 4 (Transport)**

### Q2.2: Which layer routes packets to the proper network?  
**A: Layer 3 (Network)**

### Q2.3: Which layer encodes application data?  
**A: Layer 6 (Presentation)**

### Q2.4: Which layer transfers data between hosts on the same network segment?  
**A: Layer 2 (Data Link)**

---

## Task 3 — TCP/IP Model

The TCP/IP model is a simplified, practical version of the OSI model used in real networks.

### Q3.1: To which layer does HTTP belong?  
**A: Application Layer**

### Q3.2: How many OSI layers does the TCP/IP Application layer cover?  
**A: 3**

---

## Task 4 — IP Addresses and Subnets

IP addresses uniquely identify devices on a network.  
Private IP ranges:

- 10.0.0.0 – 10.255.255.255  
- 172.16.0.0 – 172.31.255.255  
- 192.168.0.0 – 192.168.255.255  

### Q4.1: Which IP address is NOT private?  
Options:  
a) 192.168.250.125  
b) 10.20.141.132  
c) 49.69.147.197  
d) 172.23.182.251  

**A: 49.69.147.197**

### Q4.2: Which IP address is NOT valid?  
Options:  
a) 192.168.250.15  
b) 192.168.254.17  
c) 192.168.305.19  
d) 192.168.199.13  

**A: 192.168.305.19**

---

## Task 5 — UDP and TCP

TCP and UDP are transport‑layer protocols providing end‑to‑end communication.

### Q5.1: Which protocol requires a three‑way handshake?  
**A: TCP**

### Q5.2: Approximate number of port numbers (in thousands)?  
**A: 65**

---

## Task 6 — Encapsulation

Encapsulation is the process of wrapping data with headers/trailers at each layer.

### Q6.1: On WiFi, within what is an IP packet encapsulated?  
**A: Frame**

### Q6.2: What is the UDP data unit that encapsulates application data?  
**A: Datagram**

### Q6.3: What is the TCP data unit that encapsulates application data?  
**A: Segment**

---

## Task 7 — Telnet

Telnet allows connecting to remote ports and interacting with services such as HTTP, SMTP, and echo.

### Q7.1: Use Telnet to connect to the web server on MACHINE_IP. What is the HTTP server name and version?  
**A: lighttpd/1.4.63**

### Q7.2: What flag did you get when viewing the page?  
**A: THM{TELNET_MASTER}**

---

## Task 8 — Conclusion

This room covers essential networking fundamentals including:

- OSI and TCP/IP models  
- IP addressing and private ranges  
- Subnets and routing  
- TCP vs UDP  
- Encapsulation  
- Telnet for service enumeration  

