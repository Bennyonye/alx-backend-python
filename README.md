# 0x00. Python - Variable Annotations

## Description

This project introduces variable annotations in Python, focusing on specifying function signatures and variable types. It covers the use of type annotations for more readable and maintainable code and introduces tools like `mypy` for validating the correctness of your type annotations.

## Learning Objectives

By the end of this project, you should be able to:

- Understand type annotations in Python 3.
- Use type annotations to specify function signatures and variable types.
- Explain the concept of Duck Typing in Python.
- Validate your code with `mypy`.

## Resources

To complete this project, you can refer to the following resources:

- [Python 3 Typing Documentation](https://docs.python.org/3/library/typing.html)
- [MyPy Cheat Sheet](https://mypy.readthedocs.io/en/latest/cheat_sheet_py3.html)

## Project Requirements

### General

- Allowed editors: `vi`, `vim`, `emacs`.
- All your files will be interpreted/compiled on **Ubuntu 18.04 LTS** using `python3` (version 3.7).
- All your files should end with a new line.
- The first line of all your files should be exactly `#!/usr/bin/env python3`.
- A `README.md` file, at the root of the folder of the project, is mandatory.
- Your code should use the **pycodestyle** style (version `2.5.`).
- All your files must be executable.
- The length of your files will be tested using `wc`.
- All your modules should have a documentation string (run `python3 -c 'print(__import__("my_module").__doc__)'` to test).
- All your classes should have a documentation string (run `python3 -c 'print(__import__("my_module").MyClass.__doc__)'` to test).
- All your functions (inside and outside a class) should have a documentation string (run `python3 -c 'print(__import__("my_module").my_function.__doc__)'` and `python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'` to test).
- A documentation is not a simple word. It’s a real sentence explaining the purpose of the module, class, or method (the length of it will be verified).

## Installation and Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/<username>/0x00-python-variable_annotations.git
   cd 0x00-python-variable_annotations
   ```

2. **Install `mypy`** for type validation:
   ```bash
   pip install mypy
   ```

3. **Run the `mypy` validator** on your code:
   ```bash
   mypy <filename>.py
   ```

4. **Run Python scripts**:
   ```bash
   ./<filename>.py
   ```

## Tasks Overview

### 0. Basic Annotations
- **Task**: Write a function `def add(a: float, b: float) -> float:` that takes two float arguments and returns their sum as a float.

### 1. Concatenate Strings
- **Task**: Write a function `def concat(str1: str, str2: str) -> str:` that takes two strings and returns a concatenated string.

### 2. Type Checking
- **Task**: Write a function `def to_str(n: float) -> str:` that takes a float and returns its string representation.

### 3. Multiple Variable Annotations
- **Task**: Write a function `def sum_list(input_list: List[float]) -> float:` that takes a list of floats and returns their sum as a float.

### 4. Typed Arguments and Return Values
- **Task**: Write a function `def element_length(lst: Iterable[Sequence]) -> List[Tuple[Sequence, int]]:` that takes an iterable of sequences and returns a list of tuples containing the sequence and its length.

## How to Run the Code

1. Make sure the scripts are executable:
   ```bash
   chmod +x <filename>.py
   ```

2. Run the script:
   ```bash
   ./<filename>.py
   ```

3. Validate the script using `mypy`:
   ```bash
   mypy <filename>.py
   ```

## Author
**BennyOnye**
