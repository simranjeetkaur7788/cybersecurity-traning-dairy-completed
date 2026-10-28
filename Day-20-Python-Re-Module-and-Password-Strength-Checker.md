# Day 20 — Python `re` Module and Password Strength Checker

**Date:** 18 July 2026  
**Training Topic:** Regular Expressions and Password Strength Checking

## 1. Objective
The objective of this session was to learn the basics of Python's `re` module, practise regular expressions, and understand how pattern matching can support a simple password-strength checker.

## 2. Introduction
Regular expressions, often called regex, are patterns used to search for or match text. Python's built-in `re` module provides functions for working with these patterns.

Regex can help validate input formats, search logs, and detect text patterns.

## 3. Importing the `re` Module

```python
import re
```

## 4. Searching for a Pattern

```python
import re

text = "Cybersecurity training with Python"
result = re.search("Python", text)

if result:
    print("Pattern found.")
else:
    print("Pattern not found.")
```

`re.search()` searches text for a matching pattern.

## 5. Finding All Matches

```python
import re

text = "There are 12 alerts and 5 warnings."
numbers = re.findall(r"\d+", text)
print(numbers)
```

The pattern `\d+` matches one or more digits.

## 6. Replacing Text

```python
import re

text = "user123 logged in"
updated_text = re.sub(r"\d+", "[NUMBER]", text)
print(updated_text)
```

`re.sub()` replaces matching text.

## 7. Simple Password-Strength Checker

The following beginner program checks length and whether the password contains uppercase letters, lowercase letters, digits, and special characters. It is a learning exercise, not a complete security assessment.

```python
import re

password = input("Enter a password to check: ")

checks = {
    "At least 12 characters": len(password) >= 12,
    "Uppercase letter": bool(re.search(r"[A-Z]", password)),
    "Lowercase letter": bool(re.search(r"[a-z]", password)),
    "Number": bool(re.search(r"\d", password)),
    "Special character": bool(re.search(r"[^A-Za-z0-9]", password))
}

for description, passed in checks.items():
    print(f"{description}: {'Yes' if passed else 'No'}")

score = sum(checks.values())

if score == 5:
    print("Result: Meets all checks in this simple exercise.")
elif score >= 3:
    print("Result: Meets some checks; consider improving it.")
else:
    print("Result: Does not meet most checks.")
```

A real password-strength assessment should also consider length, common or breached passwords, predictability, and the system's password policy. Passwords should not be logged or stored in plaintext by this exercise.

## 8. Practical Exercise
I practised importing `re`, searching for text, finding numeric patterns, replacing matching text, and using regular expressions in a basic password-checking program.

This session improved my understanding of Python regular expressions and their practical uses. It also showed how Python can be used to build beginner-level security tools.
