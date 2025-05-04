# Computational Theory

This repository contains solutions to a multi-part programming and theory assignment based on the **SHA-256 specification (FIPS 180-4)** and foundational computer science concepts such as hashing, Turing Machines, and computational complexity.

## Research & Workflow

- Each task in this assignment is accompanied by **research notes** written directly in the Jupyter notebook as Markdown cells. These notes explain the theory, algorithms, or standards behind each implementation.
- Where relevant, external references are included.

## Project Management

- Task progress and milestones were **tracked using GitHub Issues**.
- Each issue corresponds to a specific task, allowing for clear breakdowns, discussion, and status updates.
- This workflow helped structure the development process and document task completion efficiently.

## Contents

| Task | Title | Brief Description |
|------|-------|-------------------|
| 1 | Binary Representations | Python implementations of basic bitwise operations used in SHA-256 |
| 2 | Hash Functions | Porting and analyzing a C hash function by Kernighan & Ritchie |
| 3 | SHA-256 Padding | Implementation of SHA-256-compliant message padding |
| 4 | Prime Numbers | Two algorithms to compute the first 100 primes |
| 5 | Roots | Extracting the fractional bits of square roots of primes |
| 6 | Proof of Work | Finding dictionary words with most SHA-256 leading zero bits |
| 7 | Turing Machine | Simulated Turing Machine that adds 1 to a binary number |
| 8 | Computational Complexity | Bubble sort analysis across all permutations of a 5-element list |

---

## Task Summaries

### Task 1: Binary Representations
Implemented the following functions:
- `rotl(x, n=1)`: Left bitwise rotation on a 32-bit integer.
- `rotr(x, n=1)`: Right bitwise rotation.
- `ch(x, y, z)`: The SHA-256 choose function.
- `maj(x, y, z)`: The SHA-256 majority function.

### Task 2: Hash Functions
Converted a hash function from C to Python. It multiplies a rolling hash by `31` and takes modulo `101`. Explained why `31` (a small prime) and `101` (also prime) are good choices to reduce hash collisions.

### Task 3: SHA-256 Padding
Wrote a function that:
- Calculates and prints the padding for any file.
- Follows FIPS 180-4 rules: append `1` bit, followed by `0`s, and finally a 64-bit length field.

### Task 4: Prime Numbers
Implemented:
- **Trial division** algorithm.
- **Sieve of Eratosthenes** for efficient prime generation.

Compared performance and explained algorithmic logic.

### Task 5: Roots
Calculated the first 32 bits of the **fractional part** of the square roots of the first 100 prime numbers. These values are commonly used in SHA-256 constants.

### Task 6: Proof of Work
- Loaded a dictionary of English words.
- Calculated SHA-256 hashes and counted **leading zero bits**.
- Found the word(s) with the **most leading zero bits** and provided dictionary-based proof of validity.

### Task 7: Turing Machines
Simulated a Turing Machine in Python that:
- Starts at the leftmost symbol of a binary string.
- Adds `1` to the binary number using proper state transitions and tape simulation.
- Modeled carry logic using formal Turing rules.

### Task 8: Computational Complexity
- Implemented **bubble sort** with a counter for comparisons.
- Ran it on all **120 permutations** of `[1, 2, 3, 4, 5]`.
- Printed the number of comparisons needed for each permutation to observe performance variations.

## Research & Workflow

- Each task in this assignment is accompanied by **research notes** written directly in the Jupyter notebook as Markdown cells. These notes explain the theory, algorithms, or standards (e.g., FIPS 180-4) behind each implementation.
- Where relevant, external references are included (e.g., Turing Machine definitions, SHA-256 specification).
- This documentation ensures the work is both **transparent** and **educationally grounded**.

## Project Management

- Task progress and milestones were **tracked using GitHub Issues**.
- Each issue corresponds to a specific task, allowing for clear breakdowns, discussion, and status updates.
- This workflow helped structure the development process and document task completion efficiently.

## How to Run the Tasks Notebook

To run the tasks and view the research, code, and outputs interactively, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/CormacM22/computationaltheory.git
cd computationaltheory
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook
```
Then open the notebook file (e.g., tasks.ipynb) from the Jupyter interface.

#### Notes

- All tasks are contained and documented within a single notebook.

- Each section includes research, code, and outputs.

- Make sure to use Python 3.8+ for full compatibility.


