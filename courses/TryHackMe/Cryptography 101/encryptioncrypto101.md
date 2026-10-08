# Encryption Crypto 101 — TryHackMe  
I just completed the Encryption Crypto 101 room on TryHackMe!  
This room introduces core cryptography concepts essential for cybersecurity, CTFs, and real‑world security engineering.

---
This room covers:

- Why cryptography matters  
- Symmetric vs asymmetric encryption  
- RSA fundamentals  
- Key exchange methods  
- Quantum computing impact  
- Practical exercises using basic crypto tools  

---

## 1. Why Cryptography Matters  
Cryptography protects confidentiality, integrity, and authenticity of data.

Used in:
- HTTPS  
- SSH  
- VPNs  
- Password hashing  
- Secure messaging  
- Digital signatures  

In CTFs, crypto challenges often test:
- Weak encryption  
- Misconfigurations  
- Poor randomness  
- Small key sizes  
- Incorrect RSA usage  

---

## 2. Symmetric vs Asymmetric Encryption  

### Symmetric Encryption  
One key for encrypting and decrypting.  
Fast and used for bulk data.

Examples:
- AES  
- DES (deprecated)  
- ChaCha20  

### Asymmetric Encryption  
Uses public key + private key.  
Slower but enables secure communication without sharing a secret key.

Examples:
- RSA  
- ECC  
- ElGamal  

---

## 3. RSA Fundamentals  
RSA is based on the difficulty of factoring large prime numbers.

Key concepts:
- Public key → encrypt / verify  
- Private key → decrypt / sign  
- Key sizes: 2048–4096 bits  
- Vulnerabilities: reused primes, weak randomness, small exponents  

Common uses:
- Secure key exchange  
- Digital signatures  
- Authentication  

Tools often used:
- `openssl`  
- `rsactftool`  
- CyberChef  

---

## 4. Key Exchange Methods  

### Diffie–Hellman (DH)  
Allows two parties to derive a shared secret over an insecure channel.

### RSA Key Exchange  
Encrypts a symmetric key using the recipient’s public RSA key.  
Used in older TLS versions.

---

## 5. Quantum Computing & The Future  
Quantum computers threaten RSA and ECC due to Shor’s algorithm.

Expected changes:
- Migration to post‑quantum cryptography (PQC)  
- Lattice‑based algorithms (Kyber, Dilithium)  
- Hybrid encryption (classical + PQC)  

---

## Practical Notes  
Tools used in this room:
- CyberChef  
- OpenSSL  
- Online RSA utilities  
- Basic Python scripts  

Example commands:

```bash
openssl rsa -in key.pem -text
openssl pkey -pubin -in pubkey.pem -text
openssl rsautl -decrypt -inkey private.pem -in ciphertext.bin
