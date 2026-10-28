# Day 21 — Python File Handling and Hashing

**Date:** 20 July 2026  
**Training Topic:** File Handling and Hashing Concepts

## 1. Objective
The objective of this session was to learn how Python reads and writes files and to understand how cryptographic hash functions can be used to check data integrity.

## 2. Introduction
File handling allows a program to read information from files and write information to them. In cybersecurity, it can be useful for processing reports, reading logs, and working with sample data.

Hashing is different from encryption. A hash function produces a digest that can help detect changes in data. Hashing does not provide confidentiality and should not be described as encryption.

## 3. Opening and Reading a File

```python
with open("example.txt", "r", encoding="utf-8") as file:
    content = file.read()

print(content)
```

The file must exist in the program's working directory for this example to work.

## 4. Writing to a File

```python
with open("example.txt", "w", encoding="utf-8") as file:
    file.write("This is a Python file-handling exercise.\n")
```

The `"w"` mode replaces existing file content. Use it carefully. Append mode `"a"` can add content to the end of a file.

## 5. Introduction to Hashing
A cryptographic hash function converts data into a fixed-length digest. If a file changes, its digest will usually change as well.

SHA-256 is widely used for integrity checking. A hash alone does not prove who created a file, and it does not encrypt the file.

## 6. Calculating a SHA-256 Hash in Python

```python
import hashlib

data = b"Cybersecurity training"

digest = hashlib.sha256(data).hexdigest()
print("SHA-256:", digest)
```

The `hashlib` module provides access to common hash algorithms. `hexdigest()` displays the digest as hexadecimal text.

## 7. Calculating a Hash for a File

```python
import hashlib

def calculate_sha256(file_path):
    sha256 = hashlib.sha256()

    with open(file_path, "rb") as file:
        for chunk in iter(lambda: file.read(4096), b""):
            sha256.update(chunk)

    return sha256.hexdigest()

print(calculate_sha256("example.txt"))
```

This function reads the file in small binary chunks and calculates its SHA-256 digest
I practised reading and writing text files and learned how to calculate a SHA-256 digest using Python's `hashlib` module. I also learned that file hashing can help identify whether file contents have changed.

andling and hashing concepts. These skills are useful for building tools that process data and verify file integrity.
