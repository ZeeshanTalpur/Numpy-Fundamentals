 🔢 NumPy Fundamentals — Creating Arrays

A Jupyter Notebook covering 9 different ways to create NumPy arrays, from basic 1D/2D arrays to random arrays and identity matrices — with clean examples and outputs for each.

 📋 About

This is part of my NumPy Fundamentals series, documenting my hands-on learning of NumPy one topic at a time. This notebook focuses entirely on array creation — the very first thing you need to master before doing anything in Data Science with NumPy.

 📚 What's Covered

 1. 📝 From a Python List
Creating 1D and 2D arrays directly from nested Python lists using `np.array()`.

```python
arr = np.array([1, 2, 3, 4, 5])              1D
arr = np.array([[1,2,3], [2,4,6], [3,6,9]])  2D
```

 2. ⬜ Array of Zeros
Creating arrays pre-filled with `0.0` using `np.zeros()`.

```python
np.zeros(5)       1D → [0. 0. 0. 0. 0.]
np.zeros((3,3))   2D → 3×3 matrix of zeros
```

 3. 🟦 Array of Ones
Creating arrays pre-filled with `1.0` using `np.ones()`.

```python
np.ones(5)       1D → [1. 1. 1. 1. 1.]
np.ones((3,2))   2D → 3×2 matrix of ones
```

 4. 🕳️ Empty Array
Creating an uninitialized array with `np.empty()` — faster than zeros/ones when you plan to fill values yourself.

```python
np.empty(5)   Values are whatever was already in memory
```

 5. 🔢 Array with a Specific Value
Filling an entire array with one custom value using `np.full()`.

```python
np.full(5, 68)       1D → [68 68 68 68 68]
np.full((2,3), 5)    2D → 2×3 matrix of 5s
```

 6. 📈 Sequence Array (`arange`)
Creating a range-based sequence with `np.arange()` — like Python's `range()` but returns an array.

```python
np.arange(10)        [0 1 2 3 ... 9]
np.arange(1, 23)     [1 2 3 ... 22]
np.arange(0, 10, 2)  [0 2 4 6 8]  ← with step
```

 7. 📊 Evenly Spaced Numbers (`linspace`)
Creating a fixed number of evenly spaced values between two points using `np.linspace()`.

```python
np.linspace(0, 10, 5)   [ 0.  2.5  5.  7.5  10.]
 start=0, stop=10, num=5
```

> 💡 Key difference from `arange`: you control how many values, not the step size.

 8. 🔲 Identity Matrix
Creating an N×N identity matrix (1s on the diagonal, 0s elsewhere) using `np.eye()`.

```python
np.eye(3)
 [[1. 0. 0.]
  [0. 1. 0.]
  [0. 0. 1.]]
```

 9. 🎲 Random Arrays
Creating arrays with random values using `np.random`.

```python
np.random.random(5)          floats between 0 and 1
np.random.randint(0, 100, 5)  integers between 0 and 99
 start=0, stop=100, size=5
```

 🚀 How to Run

Make sure you have Jupyter and NumPy installed:

```bash
pip install notebook numpy
```

Then launch the notebook:

```bash
jupyter notebook creating_arrays.ipynb
```

 🛠️ Built With

- Python 3
- NumPy
- Jupyter Notebook

 📁 File Structure

```
Numpy-Fundamentals/
└── 2. Creating arrays/
    └── creating_arrays.ipynb
```

 💡 Functions Covered

| Function | Purpose |
|---|---|
| `np.array()` | Create array from a list |
| `np.zeros()` | Array filled with 0s |
| `np.ones()` | Array filled with 1s |
| `np.empty()` | Uninitialized array |
| `np.full()` | Array filled with a custom value |
| `np.arange()` | Range-based sequence |
| `np.linspace()` | Evenly spaced values |
| `np.eye()` | Identity matrix |
| `np.random.random()` | Random floats (0–1) |
| `np.random.randint()` | Random integers in a range |

---
Part of my NumPy Fundamentals series 📊🐍
