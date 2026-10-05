# What is Networking — TryHackMe

Pre Security → Network Fundamentals
Room: What is Networking

Finds: 

- The World Wide Web (WWW) was invented by Tim Berners-Lee.
- The Web allows information and resources to be accessed through the Internet using technologies such as HTTP/HTTPS, URLs, web servers, and web browsers.
- An IP address is used to identify a device on a network. An IPv4 address is made up of four sections, separated by periods. Each section is called an octet.
- IPv4 addresses contain four octets and provide approximately 4.3 billion possible addresses. The increasing number of Internet-connected devices created a shortage of available IPv4 addresses.
- IPv6 is the newer version of the Internet Protocol addressing system. It supports: 2^128 possible addresses, providing a vastly larger address space than IPv4. IPv6 also introduces more efficient methods for handling network addressing.
- A MAC address is a hardware-level identifier associated with a network interface. MAC stands for: Media Access Control.


<details> <summary>Answers</summary>

What does IP stand for?: Internet Protocol
What is each section of an IP address called?: Octet
How many sections does an IPv4 address have?: 4

</details>

MAC Address Spoofing

In the interactive lab, I used the provided environment to spoof the MAC address and gain access to the site. The purpose of the exercise was to demonstrate that network access controls based solely on a MAC address can potentially be bypassed if the address can be changed.

<details> <summary>🚩 Flag</summary>

THM{YOU_GOT_ON_TRYHACKME}

</details>

Ping and ICMP

The ping command is used to test connectivity between a device and another host.
It works using the ICMP (Internet Control Message Protocol).
A basic ping request looks like:
ping 10.10.10.10
The destination host responds if it is reachable and configured to respond to ICMP requests.

I used ping against: 8.8.8.8
The exercise returned a flag.

<details> <summary>🚩 Flag</summary>

THM{I_PINGED_THE_SERVER}

</details>
