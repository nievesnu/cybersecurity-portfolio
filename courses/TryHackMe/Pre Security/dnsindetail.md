# DNS in Detail — TryHackMe  
I just completed DNS in Detail [(tryhackme.com in Bing)](https://www.bing.com/search?q="https%3A%2F%2Ftryhackme.com%2Froom%2Fdnsindetail") on TryHackMe!

Finds:  
- Concepts: DNS records, zones, resolvers, authoritative servers, recursive queries, caching.  
- Understood how DNS translates domain names into IP addresses.  
- Reviewed common record types: A, AAAA, CNAME, MX, NS, TXT, SOA.  
- Observed DNS query flow: client → resolver → root → TLD → authoritative.  
- Practiced lookups, record inspection, and zone analysis.

<details>
<summary><strong> DNS Record Types </strong></summary>

<br>

| Record | Significado |
|--------|-------------|
| A | IPv4 address |
| AAAA | IPv6 address |
| CNAME | Alias hacia otro dominio |
| MX | Mail Exchange (servidor de correo) |
| NS | Nameserver autoritativo |
| TXT | Información arbitraria (SPF, verificación) |
| SOA | Start of Authority (configuración de zona) |
| PTR | Reverse lookup (IP → dominio) |

<br>

</details>

<details>
<summary>Answer & Flags</summary>
 
- What does DNS stand for? → Domain Name System  
- What port does DNS use? → 53  
- What type of record resolves a domain to an IPv4 address? → A  

DNS Records:  
- MX record points to → mail server  
- CNAME record is → alias  
- TXT record is used for → metadata / verification  

DNS Tools:  
- Command to query DNS → nslookup / dig  
- Querying A record → `dig A example.com`  

Zone & Flow:  
- Root servers → .  
- TLD servers → .com / .net / .org  
- What field specifies how long a DNS record should be cached for? → TTL

DNS Records:  
- CNAME of `shop.website.thm` → shops.myshopify.com  
- TXT record of `website.thm` → THM{7012BBA60997F35A9516C2E16D2944FF}  
- MX record priority → 30  
- A record of `www.website.thm` → 10.10.10.10

</details>

DNS fundamentals, record types, zone hierarchy, recursive resolution, caching behavior, and practical DNS query analysis.
