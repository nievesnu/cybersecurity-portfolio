# Search Skills — TryHackMe  
I just completed [Search Skills](https://tryhackme.com/room/searchskillscS?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=linkedin&sharerId=687937a5488df707cc460ae1) on TryHackMe!

Finds:  
- Tools: Shodan, VirusTotal, CVE databases, ExploitDB, GitHub PoCs, Linux MAN pages.  
- Understood how Shodan fingerprints exposed services and devices.  
- Practiced filtering by country, port, org, hostname.  
- Used VirusTotal to check malicious files across 70+ engines.  
- Queried CVEs and reviewed CVSS scoring.  
- Used MAN pages to understand command syntax.  
- Identified PoC scripts in GitHub repositories.

<details>
<summary>Shodan Filters (Tabla Simplificada)</summary>

<br>

| Filtro | Descripción | Ejemplo |
|--------|-------------|---------|
| country | Limitar por país | `country:IE` |
| port | Filtrar por puerto o rango | `port:22` |
| org | Organización / ASN | `org:AS7224` |
| hostname | Coincidir dominio/host | `hostname:fakebank.thm` |

<br>

</details>

---

<details>
<summary> Answers</summary>

What domain is associated with IP `185.243.115.47`? → tryhackme.thm
How many security vendors flagged the file as dangerous? → 52
CVE-2026-1337 — What CVSS classification did it get? → 10
Example command to open a connection to host.example.com on port 42: nc host.example.com 42
Name of the script demonstrating the vulnerability: exploit.py

</details>
