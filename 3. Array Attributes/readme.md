 📐 NumPy Fundamentals — Array Attributes

A Jupyter Notebook covering the 6 essential attributes of NumPy arrays, demonstrated across 1D, 2D, and 3D arrays — with fun facts that show how these attributes connect to each other.

 📋 About

This is part of my NumPy Fundamentals series. After learning how to create arrays, the next step is understanding what you can know about them. This notebook covers every key attribute you'll use constantly while working with NumPy in Data Science.

 📚 What's Covered

Three arrays are created upfront and used throughout the entire notebook:

```python
arr1d = np.array([2, 3, 4, 5])                           1D — shape (4,)
arr2d = np.array([[1,2,3], [2,3,4]])                      2D — shape (2,3)
arr3d = np.array([[[1,2,3],[4,5,6]], [[2,4,6],[8,10,12]]])  3D — shape (2,2,3)
```

---

 1. `.shape` — Size in each dimension

Returns a tuple describing the array's structure.

| Array | Shape |
|---|---|
| 1D | `(4,)` — 4 elements |
| 2D | `(2, 3)` — 2 rows, 3 columns |
| 3D | `(2, 2, 3)` — 2 blocks, 2 rows, 3 columns |

---

 2. `.ndim` — Number of dimensions

```python
arr1d.ndim   → 1
arr2d.ndim   → 2
arr3d.ndim   → 3
```

---

 3. `.size` — Total number of elements

```python
arr1d.size   → 4
arr2d.size   → 6
arr3d.size   → 12
```

> 💡 Fun fact: `size` = product of all values in `shape`
> `arr3d.shape` = `(2, 2, 3)` → `2 × 2 × 3 = 12`

---

 4. `.dtype` — Data type of elements

```python
arr1d.dtype   → int64
arr2d.dtype   → int64
arr3d.dtype   → int64
```

All three arrays contain integers, so NumPy assigns `int64` by default.

---

 5. `.itemsize` — Memory per element (bytes)

```python
arr1d.itemsize   → 8 bytes (int64 = 64 bits = 8 bytes)
arr2d.itemsize   → 8 bytes
arr3d.itemsize   → 8 bytes
```

---

 6. `.nbytes` — Total memory used (bytes)

```python
arr1d.nbytes   → 32
arr2d.nbytes   → 48
arr3d.nbytes   → 96
```

> 💡 Fun fact: `nbytes` = `size × itemsize`
> `arr3d`: `12 elements × 8 bytes = 96 bytes`

---

 🗂️ Quick Reference

From the notebook's own tips section:

| Question | Attribute |
|---|---|
| How many dimensions? | `.ndim` |
| How many rows/columns? | `.shape` |
| How many total values? | `.size` |
| What type of values? | `.dtype` |
| Memory per value? | `.itemsize` |
| Total memory used? | `.nbytes` |

 🚀 How to Run

```bash
pip install notebook numpy
jupyter notebook Array_Attributes.ipynb
```

 🛠️ Built With

- Python 3
- NumPy
- Jupyter Notebook

 📁 File Structure

```
Numpy-Fundamentals/
└── 3. Array attributes/
    └── Array_Attributes.ipynb
```

 💡 Key Relationships

```
size    = product of shape values       → (2,2,3) = 12
nbytes  = size × itemsize              → 12 × 8  = 96
```

---
Part of my NumPy Fundamentals series 📊🐍
