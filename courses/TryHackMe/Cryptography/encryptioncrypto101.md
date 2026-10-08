# Encryption Crypto 101 — TryHackMe



<details>
<summary><strong>Index</strong></summary>

1. Introduction
2. Symmetric vs Asymmetric Encryption
3. RSA Fundamentals
4. RSA ASCII Flowcharts
5. Key Exchange Methods
6. Diffie–Hellman ASCII Diagrams
7. Digital Signatures and Certificates
8. SSH Authentication
9. Cracking SSH Keys with John
10. GPG / PGP
11. Quantum Computing
12. Tools Used
13. Questions & Answers

</details>

---

Cryptography protects confidentiality, integrity, and authenticity.
It is used in HTTPS, SSH, VPNs, digital signatures, password hashing, secure messaging, and more.

---

### Symmetric Encryption

```
+-------------+
|Plaintext|
+-------------+
 |
 | Encrypt with Key K
 v
+-------------+
| Ciphertext|
+-------------+
 |
 | Decrypt with Key K
 v
+-------------+
|Plaintext|
+-------------+
```

### Asymmetric Encryption

```
Sender Receiver
------ --------
Plaintext ---- Encrypt with ----> Public Key
 |
 v
Ciphertext
 |
 v
Plaintext <--- Decrypt with --- Private Key
```

---

## RSA Fundamentals

RSA relies on the difficulty of factoring large prime numbers.

Key components:

- p, q: prime numbers
- n = p * q
- e: public exponent
- d: private exponent
- m: plaintext
- c: ciphertext

---

## RSA ASCII Flowcharts

### RSA Key Generation

```
 +-------+ +-------+
 | p | | q |
 +-------+ +-------+
\ /
 \ /
\ /
+-----------+
|n = p*q|
+-----------+
 |
 v
 +-----------------------+
 | Choose public exponent|
 | e |
 +-----------------------+
 |
 v
 +-----------------------+
 | Compute private key d |
 +-----------------------+
```

### RSA Encryption

```
Plaintext (m)
 |
 |c = m^e mod n
 v
Ciphertext (c)
```

### RSA Decryption

```
Ciphertext (c)
 |
 |m = c^d mod n
 v
Plaintext (m)
```

---

## Key Exchange Methods

### Diffie–Hellman (DH)

DH allows two parties to derive a shared secret over an insecure channel.

---
### DH Overview

```
Public values: g, p

Alice chooses secret a
Bob chooses secret b
```

### Step-by-step Flowchart

```
+------------------+
| Public g, p|
+------------------+
 |
+------------+------------+
| |
+---------------+ +---------------+
| Alice chooses | | Bob chooses |
| secret a| | secret b|
+---------------+ +---------------+
| |
| A = g^a mod p | B = g^b mod p
| |
+------------+------------+
 |
 v
+------------------+
| Exchange A and B |
+------------------+
 |
+------------+------------+
| |
+----------------------++----------------------+
| Alice computes || Bob computes |
| S = B^a mod p|| S = A^b mod p|
+----------------------++----------------------+
 |
 v
+------------------+
| Shared Secret S|
+------------------+
```

### DH Security Principle

```
Attacker sees: g, p, A, B
Attacker does NOT see: a, b

Computing a or b from A or B requires solving
the discrete logarithm problem (hard).
```

---

## Digital Signatures and Certificates

```
Root CA
 |
 +-- Intermediate CA
 |
 +-- Server Certificate (example.com)
```

Digital signatures verify authenticity using private keys.
Certificates prove server identity using a chain of trust.

---

## SSH Authentication

```
+------------------+
| ssh-keygen |
+------------------+
|
v
+------------------+
| id_rsa (private) |
| id_rsa.pub |
+------------------+
|
v
scp id_rsa.pub --> authorized_keys
```

Permissions:

```
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```

---

## Cracking SSH Keys with John

Convert key:

```
python3 ssh2john.py id_rsa_1593558668558.id_rsa > rsa.hash
```

Crack:

```
john --wordlist=rockyou.txt rsa.hash
```

Show:

```
john --show rsa.hash
```

---

## GPG / PGP

Import key:

```
gpg --import tryhackme.key
```

Decrypt:

```
gpg --output message.txt --decrypt message.gpg
```

---

## Quantum Computing

```
Classical EncryptionQuantum Threat
------------------- -------------------------
RSA (2048)--->Broken by Shor's Algorithm
ECC --->Broken by Shor's Algorithm
AES-128 --->Vulnerable
AES-256 --->Safer
```

Post‑quantum algorithms (Kyber, Dilithium) are being standardized.

---

## 1Tools Used

<details>
<summary><strong>Tools Used in This Room</strong></summary>

### Cryptography Tools
- CyberChef
- OpenSSL
- GPG / PGP
- ssh-keygen

### RSA / Math Tools
- RsaCtfTool
- rsatool
- Python modular arithmetic

### Cracking Tools
- John the Ripper
- ssh2john.py
- rockyou.txt wordlist

### Useful Commands
```
openssl rsa -in key.pem -text
openssl pkey -pubin -in pubkey.pem -text
openssl rsautl -decrypt -inkey private.pem -in ciphertext.bin
```

</details>

---

## Questions & Answers

<details>
<summary>Task 2 — Key Terms</summary>
A: passphrase
</details>

<details>
<summary>Task 3 — Why Encryption Matters</summary>
A: secure shell
A: certificates
A: PCI-DSS
</details>

<details>
<summary>Task 4 — Crucial Crypto Maths</summary>
A: 0
A: 4
A: 3565
</details>

<details>
<summary>Task 5 — Types of Encryption</summary>
A: Nay
A: Triple DES
A: Yea
</details>

<details>
<summary>Task 6 — RSA</summary>
A: 29239669
</details>

<details>
<summary>Task 8 — Certificates</summary>
A: E1
</details>

<details>
<summary>Task 9 — SSH Authentication</summary>
A: RSA
A: delicious
</details>

<details>
<summary>Task 11 — GPG</summary>
A: Pineapple
</details>

---
