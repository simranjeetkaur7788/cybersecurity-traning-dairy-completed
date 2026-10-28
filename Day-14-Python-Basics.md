# Day 14 — Python Basics

**Date:** 11 July 2026  
**Training Topic:** Introduction to Python Programming

## 1. Objective

The objective of this training session was to learn the fundamentals of Python programming and understand how Python can be used to perform basic tasks. I practised simple Python programs and learned how programming skills can support cybersecurity activities.

## 2. Introduction

Python is a high-level programming language known for its simple syntax and readability. It is widely used in software development, automation, data analysis, and cybersecurity.

During this session, I learned basic Python syntax, variables, data types, input and output, and simple operations.

## 3. Introduction to Python

Python allows programmers to write instructions that a computer can execute.

Some important features of Python are:

- Simple and readable syntax.
- Support for procedural and object-oriented programming.
- A large collection of built-in functions and libraries.
- Cross-platform support.
- Use in scripting and automation.

## 4. Variables

A variable is a name used to store a value in a program.

Example:

```python
name = "Simran"
age = 19
course = "Cyber Security"

print(name)
print(age)
print(course)
```

In this example, the variables store a name, age, and course. The `print()` function displays their values.

## 5. Basic Data Types

Python provides several built-in data types.

| Data Type | Description | Example |
|---|---|---|
| `int` | Stores whole numbers | `age = 19` |
| `float` | Stores decimal numbers | `price = 25.5` |
| `str` | Stores text | `name = "Python"` |
| `bool` | Stores `True` or `False` | `is_valid = True` |
| `list` | Stores an ordered collection | `numbers = [1, 2, 3]` |

Example:

```python
number = 10
percentage = 85.5
language = "Python"
is_learning = True

print(type(number))
print(type(percentage))
print(type(language))
print(type(is_learning))
```

The `type()` function displays the data type of a value.

## 6. Input and Output

The `input()` function accepts information from the user, while `print()` displays output.

Example:

```python
name = input("Enter your name: ")
print("Welcome", name)
```

This program accepts a name and displays a welcome message.

## 7. Operators in Python

Operators perform calculations and comparisons.

### Arithmetic Operators

| Operator | Purpose | Example |
|---|---|---|
| `+` | Addition | `5 + 2` |
| `-` | Subtraction | `5 - 2` |
| `*` | Multiplication | `5 * 2` |
| `/` | Division | `5 / 2` |
| `//` | Floor division | `5 // 2` |
| `%` | Remainder | `5 % 2` |
| `**` | Exponentiation | `5 ** 2` |

Example:

```python
a = 10
b = 3

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Remainder:", a % b)
```

## 8. Conditional Statements

Conditional statements allow a program to make decisions based on conditions.

Example:

```python
password_length = int(input("Enter password length: "))

if password_length >= 12:
    print("The password meets the minimum length target.")
else:
    print("The password is shorter than the minimum length target.")
```

This program checks the length entered by the user. It demonstrates a basic condition, not a complete password-strength assessment.

## 9. Loops in Python

Loops repeat a set of instructions.

Example using a `for` loop:

```python
for number in range(1, 6):
    print(number)
```

This program displays the numbers from 1 to 5.

## 10. Practical Exercises

During this session, I practised basic Python programming tasks:

1. Displaying messages using `print()`.
2. Storing values in variables.
3. Identifying different data types.
4. Accepting user input.
5. Performing arithmetic operations.
6. Using conditional statements.
7. Repeating instructions using loops.

These exercises helped me understand the basic structure of a Python program.

