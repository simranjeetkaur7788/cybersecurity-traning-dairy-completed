# Day 19 — Python OS Module

**Date:** 17 July 2026  
**Training Topic:** Introduction to the `os` Module

## 1. Objective
The objective of this session was to learn how Python's built-in `os` module interacts with operating-system features and supports basic file and directory tasks.

## 2. Introduction
The `os` module provides functions for interacting with the operating system. It can help inspect the current working directory, list directory contents, create folders, and check paths.

## 3. Importing the Module

```python
import os
```

This makes the module's functions available in the program.

## 4. Checking the Current Working Directory

```python
import os

print(os.getcwd())
```

`os.getcwd()` displays the current working directory of the running program.

## 5. Listing Directory Contents

```python
import os

items = os.listdir(".")
print(items)
```

`os.listdir()` lists files and directories in the specified location. The dot (`.`) represents the current directory.

## 6. Checking Whether a Path Exists

```python
import os

path = "example.txt"

if os.path.exists(path):
    print("The path exists.")
else:
    print("The path does not exist.")
```

This program checks whether the specified path exists.

## 7. Creating a Directory

```python
import os

folder_name = "practice_folder"

if not os.path.exists(folder_name):
    os.mkdir(folder_name)
    print("Folder created.")
else:
    print("Folder already exists.")
```

This creates a folder only if it does not already exist.

## 8. Practical Exercise
I practised importing the `os` module, displaying the working directory, listing files and folders, checking paths, and creating a practice directory.


## 12. Conclusion
This session introduced me to Python's `os` module and its role in automation. These skills can be useful when developing simple scripts and cybersecurity utilities.
