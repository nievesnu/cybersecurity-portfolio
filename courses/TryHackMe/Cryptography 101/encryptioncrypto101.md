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

Why Cryptography Matters: Cryptography protects confidentiality, integrity, and authenticity of data.

Used in: HTTPS, SSH, VPNs, password hashing, secure messaging, sigital signatures,
In CTFs, crypto challenges often test: weak encryption, misconfigurations, poor randomness, small key sizes, incorrect RSA usage  

---

Symmetric vs Asymmetric Encryption  

Symmetric Encryption: one key for encrypting and decrypting. Fast and used for bulk data.
Asymmetric Encryption: uses public key + private key. Slower but enables secure communication without sharing a secret key.

RSA Fundamentals: is based on the difficulty of factoring large prime numbers.
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

Key Exchange Methods  
- Diffie–Hellman (DH): allows two parties to derive a shared secret over an insecure channel.
- RSA Key Exchange: encrypts a symmetric key using the recipient’s public RSA key.  Used in older TLS versions.

---

Quantum computers threaten RSA and ECC due to Shor’s algorithm.

Expected changes:
- Migration to post‑quantum cryptography (PQC)  
- Lattice‑based algorithms (Kyber, Dilithium)  
- Hybrid encryption (classical + PQC)  

---
<details>
<summary><strong>Task 1–7 — Questions & Answers</strong></summary>

Task 1 — Introduction  
Q1) I’m ready to start learning about cryptography!: No answer needed  

Task 2 — Importance of Cryptography  
Q2) What is the standard required for handling credit card information?: PCI DSS  

Task 3 — Plaintext to Ciphertext  
Q3) What do you call the encrypted plaintext?: ciphertext  
Q4) What do you call the process that returns the plaintext?: decryption  

Task 4 — Historical Ciphers  
Q5) Knowing that *XRPCTCRGNEI* was encrypted using Caesar Cipher, what is the original plaintext?: ICANENCRYPT  

Task 5 — Types of Encryption  
Q6) Should you trust DES?: Nay  
Q7) When was AES adopted as an encryption standard?: 2001  

Task 6 — Basic Math  
Q8) What’s `1001 ⊕ 1010`?: 0011  
Q9) What’s `118613842 % 9091`?: 3565  
Q10) What’s `60 % 12`?: 0  

</details>

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
