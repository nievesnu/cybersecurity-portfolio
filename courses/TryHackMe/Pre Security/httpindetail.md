# HTTP in Detail — TryHackMe  
I just completed [HTTP in Detail](https://tryhackme.com/room/httpindetail) on TryHackMe!
And with this earned the webber badge:

<img width="190" height="82" alt="image" src="https://github.com/user-attachments/assets/2680bf18-4bfc-45a0-a8d5-8cd7e4f2278a" />

HTTP in Detail  
Pre Security → Networking → Web Fundamentals  


Finds:  
- Concepts: CRUD, status codes, headers, cookies & certificate validation.  
- Detected invalid certificate on the mock webpage.  
- Reviewed how browsers interpret Content-Length, protocol versions, and secure transport.  
- Identified correct HTTP methods for creation, update, deletion y lectura.  
- Inspected raw request/response structure y metadata esencial.  

<details>
<summary><strong>📘 HTTP Status Codes (Tabla Simplificada)</strong></summary>

<br>

| Código     | Significado                                      |
|------------|--------------------------------------------------|
| 201    | Created — recurso creado correctamente           |
| 404    | Page Not Found — recurso no existe               |
| 503    | Service Unavailable — servidor saturado          |
| 401    | Not Authorised — requiere autenticación          |
| 100–199| Info — continuar petición                        |
| 200–299| Success — todo OK                                |
| 300–399| Redirect — recurso movido                        |
| 400–499| Client Error — error del cliente                 |
| 500–599| Server Error — error del servidor                |
| 200    | OK                                               |
| 301    | Moved Permanently                                |
| 302    | Found (redirect temporal)                        |
| 400    | Bad Request                                      |
| 403    | Forbidden                                        |
| 405    | Method Not Allowed                               |
| 500    | Internal Server Error                            |
| 503    | Service Unavailable                              |

<br>

</details>


<details>
<summary> Answers & Flag</summary>

Device name: THM-HTTP  
Installed RAM: 4.00 GB  
OS Version: Windows Server 2019  
Flag1: THM{INVALID_HTTP_CERT}  
Flag2: THM{INVALID_HTTP_CERT}

HTTP Basics: HTTP stands for → HyperText Transfer Protocol, the S stands for → secure, challenge flag → THM{INVALID_HTTP_CERT}, protocol used → HTTP/1.1, header that tells the browser how much data to expect → Content-Length  
HTTP Methods: create a new user account → POST, update your email address → PUT, remove an uploaded picture → DELETE, view a news article → GET  
Headers: browser being used → User-Agent, type of returned data → Content-Type, website requested → Host, save cookies → Set-Cookie.  

---
### Making Requests  
GET /room → THM{YOU'RE_IN_THE_ROOM}  
URL resultante: `http://tryhackme.com/room`  

GET /blog?id=1 → THM{YOU_FOUND_THE_BLOG}  
URL resultante: `http://tryhackme.com/blog?id=1`  

DELETE /user/1 → THM{USER_IS_DELETED}  
URL resultante: `http://tryhackme.com/user/1`  

PUT /user/2 con username=admin → THM{USER_HAS_UPDATED}  
URL resultante: `http://tryhackme.com/user/2`  

POST /login con username=thm & password=letmein → THM{LOGIN_SUCCESS}  
URL resultante: `http://tryhackme.com/login`  

</details>
This room covered: HTTP fundamentals, CRUD methods, HTTPS validation, certificate errors, headers, cookies, and how clients interpret protocol versions and responses.
---
