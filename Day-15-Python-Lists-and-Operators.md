# Day 15 — Python Lists and Operators

**Date:** 13 July 2026  
**Training Topic:** Python Lists and Operators

## 1. Objective
The objective of this session was to understand Python lists and practise using operators to work with values and collections of data.

## 2. Introduction
Python provides several data structures for storing information. A list stores multiple items in one variable, while operators perform calculations, compare values, and combine conditions.

## 3. Python Lists
A list stores an ordered collection of items. Lists are written using square brackets `[]`. List items can be accessed using their index, and the contents can be modified.

```python
tools = ["Nmap", "Wireshark", "Python"]

print(tools)
print(tools[0])
```

Python uses zero-based indexing, so the first item is at index `0`.

### Common List Operations

```python
tools = ["Nmap", "Wireshark"]

tools.append("Python")
print(tools)

tools.remove("Nmap")
print(tools)

print(len(tools))
```

- `append()` adds an item.
- `remove()` removes a matching item.
- `len()` returns the number of items.

## 4. Operators in Python

| Type | Examples | Purpose |
|---|---|---|
| Arithmetic | `+`, `-`, `*`, `/`, `%` | Perform calculations |
| Comparison | `==`, `!=`, `>`, `<` | Compare values |
| Assignment | `=`, `+=`, `-=` | Assign or update values |
| Logical | `and`, `or`, `not` | Combine conditions |
| Membership | `in`, `not in` | Check whether an item exists |

Example:

```python
password_length = 14
has_number = True

print(password_length >= 12)
print(has_number and password_length >= 12)
```

This demonstrates comparison and logical operations.
I practised creating lists, accessing items, adding and removing values, checking list length, and using arithmetic, comparison, logical, and membership operators.

