# Day 18 — For and While Loops in Python

**Date:** 16 July 2026  
**Training Topic:** For Loops and While Loops

## 1. Objective
The objective of this session was to learn how loops repeat instructions and how to use `for` and `while` loops in Python.

## 2. Introduction
Loops reduce repeated code by allowing a program to perform the same action multiple times.

## 3. The `for` Loop
A `for` loop can process items in a collection or repeat an operation over a sequence.

```python
tools = ["Nmap", "Wireshark", "Python"]

for tool in tools:
    print(tool)
```

The loop displays each item in the list.

The `range()` function generates a sequence of numbers:

```python
for number in range(1, 6):
    print(number)
```

This program prints numbers from 1 through 5.

## 4. The `while` Loop
A `while` loop repeats its block while the condition remains true.

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

The counter increases during each iteration so that the condition eventually becomes false.

## 5. Difference Between `for` and `while`

| For Loop | While Loop |
|---|---|
| Commonly processes items in a collection or a known range. | Repeats while a condition is true. |
| Often used when the sequence is known. | Often used when repetition depends on a condition. |
| Example: visiting each list item. | Example: repeating until a counter reaches a limit. |

## 6. Loop Control
Python provides `break` and `continue`.

- `break` stops the loop.
- `continue` skips the rest of the current iteration and moves to the next one.

```python
for number in range(1, 6):
    if number == 3:
        continue
    print(number)
```

This program skips printing the number 3.

## 7. Practical Exercise
I practised displaying sequences of numbers, processing list items, repeating instructions with a counter, and controlling loops with conditions.
