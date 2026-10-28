# Day 10: Introduction to Hydra and Cryptography

**Date:** 7 July 2026

## 1. Objective

The objective of this day was to learn about Hydra, understand basic networking concepts, and study the fundamentals of cryptography, including symmetric encryption, asymmetric encryption, and hashing.

## 2. Introduction to Hydra

Hydra is a password-testing tool used in authorised security assessments to check the strength of authentication systems. It supports different protocols and services.

Security professionals may use Hydra in a controlled lab to understand password security and identify weak authentication practices.
**Room Link:** [Open my completed Hydra room](https://tryhackme.com/room/hydra?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)


 ### Key Points

- Hydra can test authentication against supported services.
- Weak and reused passwords can increase security risks.
- Strong passwords help protect user accounts.
- Testing must only be performed on systems for which permission has been granted.

## 3. Introduction to Cryptography

Cryptography is the practice of protecting information using mathematical techniques. It helps keep information confidential and protects data during storage and communication.
**Room Link:** [Open my completed Cryptography for Dummies room](https://tryhackme.com/room/cryptographyfordummies?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)
**Room Link:** [Open my completed Cryptography Basics room](https://tryhackme.com/room/cryptographybasics?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

### Importance of Cryptography

- Protects sensitive information.
- Helps maintain confidentiality.
- Supports data integrity.
- Helps verify identity through cryptographic authentication methods.
- Supports secure communication over networks.

### Important Terms

**Plaintext:** The original readable information.

**Ciphertext:** Information transformed into an unreadable form through encryption.

**Encryption:** The process of converting plaintext into ciphertext.

**Decryption:** The process of converting ciphertext back into plaintext using the appropriate key.

**Key:** Information used by a cryptographic algorithm to encrypt or decrypt data.

## 4. Symmetric Encryption

Symmetric encryption uses the same secret key for encryption and decryption.

The sender encrypts the original information using a secret key. The receiver uses the same key to decrypt it.

### Working Process

1. The sender prepares the original message.
2. The encryption algorithm uses a secret key to transform the message.
3. The encrypted message is sent to the receiver.
4. The receiver uses the same secret key to decrypt the message.
5. The original information becomes readable again.

### Example

AES (Advanced Encryption Standard) is a widely used symmetric encryption algorithm.

### Advantages

- Fast for encrypting large amounts of data.
- Suitable for file and disk encryption.
- Efficient for protecting stored information.

### Limitation

The secret key must be shared securely. If an unauthorised person obtains the key, they may be able to decrypt the protected information.

## 5. Asymmetric Encryption

Asymmetric encryption uses a pair of mathematically related keys:

- **Public key:** Can be shared with others.
- **Private key:** Must be kept secret by its owner.

In a common public-key encryption process, a sender encrypts information using the receiver's public key. The receiver then uses their private key to decrypt it.

### Working Process

1. The receiver generates a public and private key pair.
2. The receiver shares the public key.
3. The sender uses the public key to encrypt the message.
4. The receiver uses the corresponding private key to decrypt it.

### Example

RSA is a well-known public-key cryptographic algorithm.

### Advantages

- Helps protect information without directly sharing the private key.
- Supports secure key establishment and other cryptographic applications.
- Can be used in digital signature systems.

### Limitation

Public-key operations are generally slower than symmetric encryption for large amounts of data. Real-world secure systems often combine symmetric and asymmetric cryptography.


## 6. Introduction to Hashing

Hashing converts input data into a fixed-length output called a hash or message digest.

Unlike encryption, hashing is designed to be a one-way process. A hash is not normally decrypted to recover the original data.

### Uses of Hashing

- Checking file integrity.
- Detecting changes in data.
- Supporting password verification when implemented with suitable password-hashing methods.
- Verifying that downloaded files match an expected hash.

### Example: SHA-256

SHA-256 is a cryptographic hash function that produces a 256-bit hash value.

For example, Linux provides the `sha256sum` command to calculate the SHA-256 hash of a file.

```bash
sha256sum filename.txt
```

If the file changes, its hash will usually change as well.

### Important Note

A hash function is not an encryption algorithm. Encryption is designed to be reversible with the correct key, whereas cryptographic hashing is designed to be one-way.

## 7. Password Security

Passwords are an important part of account security. Weak or reused passwords can make accounts more vulnerable to unauthorised access.

Good password practices include:

- Using long, unique passwords.
- Avoiding predictable personal information.
- Not reusing the same password across multiple accounts.
- Using a password manager.
- Enabling multi-factor authentication where available.

For secure password storage, systems should use specialised password-hashing algorithms such as Argon2id, scrypt, or bcrypt rather than storing plaintext passwords or relying on a fast hash alone.

