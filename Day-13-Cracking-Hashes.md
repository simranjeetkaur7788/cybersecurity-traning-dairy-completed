# Day 13 — Cracking Hashes

**Date:** 10 July 2026  
**Training Topic:** Hash Cracking and Password Security  
**Learning Area:** Cybersecurity and Cryptography

## 1. Objective

The objective of this training session was to understand hash functions, identify common hash types, and learn how hash-cracking techniques work in an authorised practice environment. I also learned how to use Kali Linux tools to test password hashes and understand the importance of password security.

## 2. Introduction

Hashing is an important concept in cybersecurity. A hash function takes input data and produces a fixed-length output called a hash value or digest.

Hashing is commonly used to check file integrity and verify passwords. Unlike encryption, hashing is designed as a one-way process, meaning that the original input should not be practically recoverable from a secure hash alone.

Hash cracking involves attempting to discover an input, such as a password, that produces a particular hash value.

## 3. What Is a Hash?

A hash is a fixed-length value generated from input data using a hash function.

Important characteristics of hashing include:

- **Fixed-length output:** The output length is determined by the algorithm.
- **Deterministic results:** The same input produces the same hash when the same algorithm and settings are used.
- **One-way design:** Secure hash functions are designed to make it impractical to recover the original input from the hash.
- **Integrity verification:** Hash values can help identify changes in files.

## 4. Common Hashing Algorithms

| Algorithm | Description |
|---|---|
| MD5 | Produces a 128-bit hash but is no longer considered secure for collision-resistant applications. |
| SHA-1 | Produces a 160-bit hash and is no longer recommended for security-sensitive collision-resistant applications. |
| SHA-256 | A member of the SHA-2 family that produces a 256-bit hash. |
| SHA-512 | A member of the SHA-2 family that produces a 512-bit hash. |

Hash formats can sometimes be recognised by their length and appearance. However, different algorithms may produce values with similar appearances, so length alone is not always enough to identify a hash correctly.

## 5. What Is Hash Cracking?

Hash cracking is the process of testing possible inputs to discover one that matches a target hash.

In an authorised security laboratory, this process helps demonstrate why weak passwords can be vulnerable even when systems store password hashes instead of plaintext passwords.

Hash cracking does not decrypt a hash. Instead, a tool generates candidate passwords, hashes them using the appropriate method, and compares the results with the target hash.

## 6. Common Hash-Cracking Techniques

### A. Dictionary Attack

A dictionary attack tests possible passwords from a prepared list called a wordlist.

The tool checks whether any candidate password produces a matching hash.

### B. Brute-Force Attack

A brute-force attack systematically tests possible character combinations until a matching result is found or the search space is exhausted.

The time required depends on password length, character set, hardware, and hashing method.

### C. Rule-Based Attack

A rule-based attack modifies candidate words according to specified patterns, such as adding numbers or symbols.

These techniques should only be practised on authorised lab data or systems for which permission has been granted.

## 7. Tools Used for Hash Cracking

### Hashcat

Hashcat is a password recovery and auditing tool that supports many hash formats and attack strategies.

### Hash Identification Tools

Hash-identification tools help narrow down the possible algorithm associated with a hash value. The results are not always conclusive, so additional verification may be necessary.

## 8. Step-by-Step Practical Using Kali Linux
**Room Link:** [Open my completed Crack the Hash room](https://tryhackme.com/room/crackthehash?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

**The following commands demonstrate how to test a hash from an authorised practice lab. The exact hash format depends on the challenge.**

### Step 1: Check John the Ripper

Open the Kali Linux terminal and enter:

```bash
john --version
```

This command checks whether John the Ripper is installed and displays its version.

If it is not installed, use:

```bash
sudo apt update
sudo apt install john
```

### Step 2: Create a Hash File

Create a file to store the hash provided in your authorised practice lab:

```bash
nano hash.txt
```

Paste the lab hash into the file.

To save the file:
1. Press `Ctrl + O`.
2. Press `Enter`.
3. Press `Ctrl + X`.

Check the contents:

```bash
cat hash.txt
```

### Step 3: Identify the Possible Hash Type

If the `hashid` utility is installed, run:

```bash
hashid 'PASTE_YOUR_LAB_HASH_HERE'
```

Replace the example text with your lab hash.

The tool may suggest several possible algorithms. Confirm the correct format using the challenge instructions because different algorithms can produce similar-looking hash values.

### Step 4: Check Available Wordlists

Enter:

```bash
ls /usr/share/wordlists/
```

This command lists the available wordlists.

If `rockyou.txt.gz` is present, extract it using:

```bash
sudo gzip -dk /usr/share/wordlists/rockyou.txt.gz
```

The `-k` option keeps the original compressed file.

### Step 5: Test the Hash with John the Ripper

For a supported hash format, use:

```bash
john --format=HASH_FORMAT --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```

Replace `HASH_FORMAT` with the correct format for your lab hash.

This command tests candidate passwords from the wordlist against the hash.

### Step 6: Display Recovered Results

Enter:

```bash
john --show hash.txt
```

This command displays any recovered password associated with the hashes John recognises in the file.

If no password is found, it does not necessarily mean the password is strong. The candidate may not be present in the wordlist, or the hash format may be incorrect.

### Step 7: Record the Results

After completing the authorised exercise, record:

- The hash type identified.
- The tool used.
- The wordlist used.
- Whether a matching password was found.
- What the result taught you about password security.

**Practical learning:** I learned how to prepare a hash file, check available wordlists, use a password-auditing tool, and display the results of a password-testing exercise.

**Important:** Use these commands only with authorised practice hashes. The correct format and procedure depend on the lab challenge.

## 9. Why Are Weak Passwords Easier to Crack?

Weak passwords are easier to guess because they may be short, common, predictable, or based on familiar words and patterns.

Password security can be improved by:

1. Using long and unique passwords.
2. Avoiding common words and predictable patterns.
3. Using a password manager.
4. Enabling multifactor authentication.
5. Avoiding password reuse across different accounts.

## 10. How Password Hashing Improves Security

Websites should not store user passwords in plaintext. Instead, they should use suitable password-hashing methods designed to resist password-guessing attacks.

Secure password storage commonly uses algorithms such as Argon2id, scrypt, bcrypt, or PBKDF2, with appropriate settings and a unique salt for each
