# Cryptography Concepts — TryHackMe
I just completed [Cryptography Concepts](https://tryhackme.com/room/cryptographyconcepts?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=linkedin&sharerId=687937a5488df707cc460ae1) room on TryHackMe! 

Cryptography Concepts: Pre Security → Attacks and Defenses → Cryptography Concepts

<details> <summary> Answers & Flag</summary>

Flag from the Secret Message Rescue game: THM{CAESAR_CIPHER_MASTER_2026}
Caesar cipher — CYBER with key 5: HDGJW
Decoded message: SIMPLE CAESAR CIPHER

</details>

Finds:
- Plaintext is a message that can be read normally.
- Ciphertext is the scrambled version of the plaintext.
- A key is the secret value that controls how the encryption and decryption works.
- An algorithm is the public set of steps used with the key to encrypt or decrypt data.
- The algorithm does not need to be secret. The security comes from keeping the key secret.
- Symmetric encryption uses the same key to encrypt and decrypt a message, they are fast, efficient and good for encrypting large amounts of data
The main problem is the key distribution problem. Both people need the same secret key, but securely sharing that key in the first place can be difficult.
```
Plaintext + Encryption Algorithm + Key → Ciphertext
Ciphertext + Decryption Algorithm + Key → Plaintext
```
- Caesar Cipher: is a simple example of symmetric encryption. It works by shifting each letter by a fixed number of positions in the alphabet. To decrypt it, the letters are shifted backwards by the same amount.
The Caesar cipher is not secure enough for real-world use because there are only 25 possible shifts, making it very easy to brute-force.

- Real encryption algorithms such as AES (Advanced Encryption Standard) use much more complex mathematics, but the basic idea of using an algorithm and key remains the same.

<details> <summary>Caesar Cipher Practice</summary>

Using a key of 5: CYBER → HDGJW
The intercepted message: FVZCYR PNRFNE PVCURE was decoded as: SIMPLE CAESAR CIPHER
The Secret Message Rescue Flag was THM{CAESAR_CIPHER_MASTER_2026}

</details>
- Asymmetric encryption uses two mathematically linked keys: Public key, can be shared with anyone, & Private key, must remain secret.
If Alice encrypts a message using Bob's public key, only Bob's private key can decrypt it. This solves the key distribution problem because Alice and Bob do not need to secretly exchange the same key beforehand.

<details> <summary> Answers</summary>

Secret key: private key
Alice using Bob's public key and Bob using his private key to decrypt: Yay
Problem solved: key distribution
Encryption used for bulk data after the HTTPS handshake: symmetric

</details>

- HTTPS: uses both asymmetric and symmetric encryption. When connecting to a website the browser receives the website's public key through a certificate.
Asymmetric encryption is used to securely establish a shared secret. The connection switches to symmetric encryption. Symmetric encryption handles the bulk of the data because it is much faster.
This combination is known as a hybrid approach.

- Certificates: a certificate is a digital document containing information such as: The website's public key, The domain it belongs to, The Certificate Authority (CA) that signed it, Its validity period...
The browser checks whether the certificate was signed by a trusted CA and whether it is still valid.
This helps verify that the website being accessed is actually the website it claims to be.
