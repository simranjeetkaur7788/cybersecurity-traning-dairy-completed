# Day 22 — Comparing and Storing File Hashes

**Date:** 21 July 2026  
**Training Topic:** File Integrity Checking Using Hashes

## 1. Objective
The objective of this session was to understand how file hashes can be stored and compared to check whether a file has changed.

## 2. Introduction
File integrity checking helps detect unexpected changes in data. A cryptographic hash function generates a digest from file contents. Comparing a newly calculated digest with a previously trusted digest can help identify whether the contents have changed.

The original hash must be stored or obtained from a trusted source. If an attacker can change both the file and its stored reference hash, a simple comparison may not detect tampering.

## 3. Why Compare Hashes?
A file may change because it has been edited, corrupted, or modified without permission.

- If the hashes match, the file contents are consistent with the reference at the time of comparison.
- If the hashes differ, the file contents or the hashing process may have changed.

## 4. Python Program to Calculate a File Hash

```python
import hashlib

def calculate_sha256(file_path):
    digest = hashlib.sha256()

    with open(file_path, "rb") as file:
        for chunk in iter(lambda: file.read(4096), b""):
            digest.update(chunk)

    return digest.hexdigest()

file_path = "example.txt"
print("Current SHA-256:", calculate_sha256(file_path))
```

Make sure `example.txt` exists in the same working directory, or provide the correct path.

## 5. Compare Two Files

```python
import hashlib

def calculate_sha256(file_path):
    digest = hashlib.sha256()

    with open(file_path, "rb") as file:
        for chunk in iter(lambda: file.read(4096), b""):
            digest.update(chunk)

    return digest.hexdigest()

original_hash = calculate_sha256("original.txt")
new_hash = calculate_sha256("new.txt")

print("Original file hash:", original_hash)
print("New file hash:", new_hash)

if original_hash == new_hash:
    print("The file contents match.")
else:
    print("The file contents differ.")
```

Create `original.txt` and `new.txt` before running the program. The result depends on whether their contents match.

## 6. Storing a Hash in a Text File

```python
import hashlib

def calculate_sha256(file_path):
    digest = hashlib.sha256()

    with open(file_path, "rb") as file:
        for chunk in iter(lambda: file.read(4096), b""):
            digest.update(chunk)

    return digest.hexdigest()

file_hash = calculate_sha256("original.txt")

with open("hash_record.txt", "w", encoding="utf-8") as record:
    record.write(file_hash + "\n")

print("Reference hash saved.")
```

The reference digest should be protected from unauthorised modification. For stronger assurance, store or authenticate the reference separately.

## 7. Practical Exercise
I practised calculating SHA-256 digests, comparing hashes, and saving a reference hash to a text file. I learned that even a small change in a file will usually produce a different SHA-256 digest.

 my understanding of file integrity checking. Comparing cryptographic hashes is a practical way to detect changes in files and is useful when developing basic cybersecurity tools.
