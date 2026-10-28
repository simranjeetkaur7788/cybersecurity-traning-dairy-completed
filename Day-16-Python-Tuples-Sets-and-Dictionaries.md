# Day 16 — Python Tuples, Sets, and Dictionaries

**Date:** 14 July 2026  
**Training Topic:** Tuples, Sets, and Dictionaries

## 1. Objective
The objective of this session was to understand three Python data structures: tuples, sets, and dictionaries.

## 2. Introduction
Python data structures help store and organise information. Each structure has different properties and is useful for different purposes.

## 3. Tuples
A tuple stores an ordered collection of items. Tuples are commonly written using parentheses `()` and cannot be changed after creation.

```python
device = ("Laptop", "192.168.1.10", "Online")

print(device)
print(device[0])
```

Tuples are useful for storing a group of values that should remain unchanged.

## 4. Sets
A set stores unique items and does not maintain a fixed positional order.

```python
ports = {22, 80, 443, 80}
print(ports)
```

Repeated values are stored only once.

```python
allowed_ports = {22, 80, 443}
print(22 in allowed_ports)
```

Sets are useful when duplicate values should be removed or membership needs to be checked.

## 5. Dictionaries
A dictionary stores information as key-value pairs.

```python
device = {
    "name": "Laptop",
    "ip_address": "192.168.1.10",
    "status": "Online"
}

print(device["name"])
print(device["ip_address"])
```

A value can be updated using its key:

```python
device["status"] = "Offline"
print(device)
```

## 6. Comparison

| Data Structure | Main Property | Example Use |
|---|---|---|
| Tuple | Ordered and immutable | Fixed device details |
| Set | Stores unique items | Unique port numbers |
| Dictionary | Stores key-value pairs | Device information |

## 7. Practical Exercise
I practised creating tuples, sets, and dictionaries, retrieving values, checking set membership, and updating dictionary entries.


## 11. Conclusion
This session improved my ability to organise data in Python. Choosing an appropriate data structure makes programs easier to understand and maintain.
