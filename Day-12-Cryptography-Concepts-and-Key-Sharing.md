# Day 12 — Cryptography Concepts and Key Sharing

**Date:** 9 July 2026  
**Training Topic:** Cryptography Concepts and Key Sharing

## 1.Introduction

Cryptography is an important part of cybersecurity. It uses mathematical techniques to protect information during storage and transmission. It helps maintain confidentiality, integrity, and authenticity.

During this session, I studied different encryption methods and understood how cryptographic keys are used to protect data.

## 2. Symmetric Encryption

Symmetric encryption uses the same secret key for both encryption and decryption.

The sender encrypts the original message using a secret key. The receiver uses the same key to decrypt the message and recover the original information.

**Example:** AES (Advanced Encryption Standard).

**Advantages:**
- It is generally fast and efficient.
- It is suitable for encrypting large amounts of data.
- It is widely used to protect files and communications.

**Limitation:**
- The sender and receiver must share the secret key securely.
- If an unauthorised person obtains the key, they may be able to decrypt the protected data.

## 3. Asymmetric Encryption

Asymmetric encryption uses a pair of mathematically related keys:

- **Public key:** Can be shared with others.
- **Private key:** Must be kept secret by its owner.

In a common public-key encryption arrangement, a sender encrypts information using the receiver's public key. The receiver then uses their private key to decrypt it.

**Example:** RSA.

**Advantages:**
- It helps establish secure communication without first sharing the same secret encryption key.
- The public key can be distributed openly.
- Public-key cryptography can also support digital signatures, which help verify authenticity and integrity.

**Limitation:**
- Public-key operations are generally slower than symmetric encryption for large amounts of data.
- Private keys must be protected carefully.


## 4. Secure Key Sharing

Secure key sharing means transferring or establishing cryptographic keys in a way that prevents unauthorised people from obtaining them.

Key sharing is important because encryption is only effective when the required keys remain protected.

Some methods include:

1. **Secure communication channels:** Using an appropriately protected channel to transfer keys.
2. **Public-key cryptography:** Using public-key techniques to establish or protect a secret key.
3. **Key exchange protocols:** Using protocols such as Diffie–Hellman to establish a shared secret over an insecure network.
4. **Key management:** Storing keys securely, restricting access, and replacing compromised keys.

## 5. Real-Life Applications

Cryptography and secure key management are used in:

- Online banking and digital payments.
- HTTPS connections between browsers and websites.
- Secure messaging applications.
- Protection of sensitive files.
- Authentication and digital signatures.
- Secure communication between computer systems.

## 6. Learning Platforms and References

I referred to online educational resources to improve my understanding of cryptography, encryption techniques, and secure key sharing.

### 1. Google Cloud
I explored educational material about encryption and learned how encryption helps protect sensitive information.

**Resource:** https://cloud.google.com/learn/what-is-encryption

### 2. Microsoft Learn
I referred to Microsoft documentation to learn more about cryptography, encryption, hashing, and cryptographic key management.

**Resource:** https://learn.microsoft.com/en-us/windows/security/operating-system-security/system-security/cryptography-certificate-mgmt

### 3. NIST
I referred to the National Institute of Standards and Technology (NIST) resource to understand the Advanced Encryption Standard (AES).

**Resource:** https://www.nist.gov/publications/advanced-encryption-standard-aes

