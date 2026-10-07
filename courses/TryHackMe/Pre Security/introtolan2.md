# Intro to LAN — TryHackMe  
I just completed [Intro to LAN](https://tryhackme.com/room/introtolan) on TryHackMe!

Finds:  
- Concepts: LAN, routing, switching, topologies, subnetting, ARP, DHCP.  
- Understood how routers forward traffic between networks (routing).  
- Reviewed how switches interconnect devices and forward frames.  
- Compared network topologies: bus, star, pros & cons.  
- Practiced subnetting basics: masks, ranges, network/host addresses.  
- Learned ARP flow and DHCP packet sequence.

---

<details>
<summary>Answers & Flag</summary>

THM{TOPOLOGY_FLAWS}

What does LAN stand for? → Local Area Network  
Verb for the job routers perform → Routing  
Device that centrally connects multiple devices → Switch  
Cost‑efficient topology → Bus Topology  
Expensive topology → Star Topology  
Lab flag → THM{TOPOLOGY_FLAWS}

Dividing a network into smaller pieces → Subnetting  
Bits in a subnet mask → 32  
Range of an octet → 0–255  
Address identifying start of a network → Network Address  
Address identifying devices → Host Address  
Device responsible for sending data to another network → Default Gateway

ARP stands for → Address Resolution Protocol  
Packet asking if a device has a specific IP → Request  
Physical identifier → MAC Address  
Logical identifier → IP Address

Packet used to retrieve an IP → DHCP Discover  
Packet sent after receiving an offer → DHCP Request  
Final packet sent by DHCP server → DHCP ACK

</details>

---

This room covered: LAN fundamentals, routing vs switching, network topologies, subnetting basics, ARP resolution, and DHCP negotiation sequence.

---

Si quieres, sigo con DNS in Detail o el siguiente room que estés haciendo.
