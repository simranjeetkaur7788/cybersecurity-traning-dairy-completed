# Day 17 — Conditional Statements in Python

**Date:** 15 July 2026  
**Training Topic:** Conditional Statements

## 1. Objective
The objective of this session was to learn how Python programs make decisions using `if`, `elif`, and `else`.

## 2. Introduction
Conditional statements allow a program to execute different instructions depending on whether a condition is true or false.

## 3. The `if` Statement

```python
number = 10

if number > 0:
    print("The number is positive.")
```

The code inside the `if` block runs when the condition is true.

## 4. The `if-else` Statement

```python
number = int(input("Enter a number: "))

if number % 2 == 0:
    print("The number is even.")
else:
    print("The number is odd.")
```

This program checks whether a number is even or odd.

## 5. The `if-elif-else` Statement

```python
score = int(input("Enter a score from 0 to 100: "))

if score >= 80:
    print("High score")
elif score >= 50:
    print("Passing score")
else:
    print("Below passing score")
```

The `elif` keyword checks another condition when the earlier condition is false.

## 6. Logical Operators in Conditions

```python
password_length = 14
has_number = True

if password_length >= 12 and has_number:
    print("Both conditions are satisfied.")
else:
    print("One or more conditions are not satisfied.")
```

This example demonstrates logical conditions; it is not a complete password-strength assessment.

## 7. Practical Exercise
I practised checking whether numbers were positive, negative, even, or odd. I also used `if`, `elif`, and `else` to produce different outputs based on user input.

Conditional statements can validate input, classify log events, check program settings, and display warnings when certain conditions are met.

