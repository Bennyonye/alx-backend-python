# 0x01. Python - Async

This project is focused on learning and implementing asynchronous code in Python using the `asyncio` module. You'll explore key concepts such as asynchronous coroutines, tasks, and concurrent execution.

## Learning Objectives

By the end of this project, you will understand:

- How to write asynchronous code in Python.
- How to run multiple coroutines concurrently.
- How to manage execution time and measure runtime for async tasks.
- How to use `asyncio.Task` for handling background tasks.

## Tasks To Complete

### 0. The Basics of `async`
File: `0-basic_async_syntax.py`

- Write an asynchronous coroutine `wait_random` that:
  - Takes an integer argument `max_delay` (default value: `10`).
  - Waits for a random delay between `0` and `max_delay` seconds (using the `random` module).
  - Returns the random delay as a `float`.
  
**Example:**
```python
>>> import asyncio
>>> print(asyncio.run(wait_random(5)))
# Output: A random float between 0 and 5.
```

### 1. Let's Execute Multiple Coroutines Concurrently with `async`
File: `1-concurrent_coroutines.py`

- Write an asynchronous function `wait_n` that:
  - Takes two arguments: `n` (number of coroutines to spawn) and `max_delay`.
  - Spawns `n` instances of `wait_random` with the given `max_delay`.
  - Returns a list of all the delays (in ascending order, but **without** using `sort()`).

**Example:**
```python
>>> import asyncio
>>> print(asyncio.run(wait_n(5, 5)))
# Output: A list of random float delays sorted in ascending order.
```

### 2. Measure the Runtime
File: `2-measure_runtime.py`

- Write a `measure_time` function that:
  - Takes two arguments: `n` (number of coroutines) and `max_delay`.
  - Measures the total execution time for calling `wait_n(n, max_delay)`.
  - Returns the average time per coroutine (i.e., `total_time / n`).
  
**Example:**
```python
>>> import asyncio
>>> print(measure_time(5, 5))
# Output: A float representing the average time per coroutine.
```

### 3. Tasks
File: `3-tasks.py`

- Write a function `task_wait_random` that:
  - Takes an integer `max_delay`.
  - Returns an `asyncio.Task` that runs the `wait_random` coroutine.
  
**Example:**
```python
>>> task = task_wait_random(5)
>>> print(task)
# Output: A Task object representing the coroutine.
```

### 4. More Tasks
File: `4-tasks.py`

- Write a function `task_wait_n` that:
  - Takes two arguments: `n` and `max_delay`.
  - Works similarly to `wait_n`, but uses `task_wait_random` to create tasks instead of calling `wait_random` directly.
  
**Example:**
```python
>>> print(asyncio.run(task_wait_n(5, 5)))
# Output: A list of random float delays, sorted in ascending order.
```

---

### Resources
- [Python 3 typing documentation](https://docs.python.org/3/library/typing.html)
- [Asyncio in Python Documentation](https://docs.python.org/3/library/asyncio.html)

### Requirements
- Python 3.7 or higher.
- Code will be checked with `pycodestyle` for style guidelines.
- All files must have a proper documentation string.

## Author
This project is developed and maintained by **BennyOnye**.