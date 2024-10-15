# 0x00. Async Comprehension

This project focuses on learning and implementing asynchronous comprehensions in Python, an important technique to handle asynchronous operations with better efficiency and clarity.

## Concepts

- **Async Generators**: Generate values asynchronously.
- **Async Comprehensions**: Collect values from an async generator using list comprehensions.
- **Concurrency**: Execute multiple async tasks simultaneously for better performance.

## Tasks To Complete

### 0. Async Generator

In **0-async_generator.py**, you need to create an asynchronous coroutine called `async_generator` that meets the following requirements:

- **Behavior**: The coroutine loops 10 times. Each time, it asynchronously waits for 1 second before yielding a random number between 0 and 10.
- **Key Module**: Use Python’s `random` module to generate the random number.

**Usage Example**:

```python
import asyncio
from 0-async_generator import async_generator

async def main():
    async for number in async_generator():
        print(number)

asyncio.run(main())
```

### 1. Async Comprehensions

In **1-async_comprehension.py**, you need to write a coroutine called `async_comprehension` that:

- Imports the `async_generator` from the previous task.
- Uses an async comprehension to collect 10 random numbers from the generator.
- Returns the list of the 10 random numbers.

**Usage Example**:

```python
import asyncio
from 1-async_comprehension import async_comprehension

async def main():
    numbers = await async_comprehension()
    print(numbers)

asyncio.run(main())
```

### 2. Run Time for Four Parallel Comprehensions

In **2-measure_runtime.py**, the goal is to measure the runtime of executing multiple asynchronous comprehensions concurrently:

- Import the `async_comprehension` from the previous file.
- Write a coroutine called `measure_runtime` that runs `async_comprehension` four times in parallel using `asyncio.gather`.
- Measure and return the total runtime of the concurrent executions.

**Usage Example**:

```python
import asyncio
from 2-measure_runtime import measure_runtime

async def main():
    total_time = await measure_runtime()
    print(f"Total runtime: {total_time} seconds")

asyncio.run(main())
```

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/YourUsername/alx-async-comprehension.git
   ```

2. Run the scripts using Python 3.7+:

   ```bash
   python3 0-async_generator.py
   python3 1-async_comprehension.py
   python3 2-measure_runtime.py
   ```

   Ensure that **asyncio** is available, as it is required to run asynchronous coroutines.

## Key Concepts

- **Asynchronous Programming**: Allows the program to perform other operations while waiting for time-consuming tasks to complete.
- **Concurrency**: Executing multiple tasks simultaneously, particularly useful when dealing with I/O-bound tasks (e.g., API calls, file reading, etc.).
- **Async Generators**: Like regular generators, but work asynchronously.
- **Async Comprehensions**: Allow async iterations inside comprehensions (e.g., list comprehensions) for more efficient handling of asynchronous operations.

## Resources

- [AsyncIO Documentation](https://docs.python.org/3/library/asyncio.html)
- [PEP 530 – Asynchronous Comprehensions](https://www.python.org/dev/peps/pep-0530/)
- [Concurrency in Python](https://realpython.com/python-concurrency/)

## Author
This project is developed and maintained by **BennyOnye**.