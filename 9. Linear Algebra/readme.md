# 📐 Linear Algebra for Data Science & Machine Learning

Part of my **NumPy Learning Series** — the math backbone behind every ML model you've ever used. This notebook covers 10 core concepts from scalars to solving equations, and connects it all back to the real ML formula: `X @ W + b`. 🧠

---

## 📒 About This Notebook

You don't need a math degree to understand linear algebra — you just need the right lens. This notebook builds every concept from scratch using NumPy, explains the *why* behind each operation, and ends with the insight that ties it all together: how matrix multiplication and broadcasting power machine learning models.

---

## 🧠 What's Covered

### Part 1 — Scalars, Vectors & Matrices
The three building blocks of linear algebra:
- **Scalar** → just a number
- **Vector** → a 1D array
- **Matrix** → an nD array where n > 1. Represents datasets, images, transformations, feature tables.

### Part 2 — Vector Operations
```python
a + b   # addition   → [5, 7, 9]
a - b   # subtraction → [-3,-3,-3]
a * 10  # scalar multiplication → [10, 20, 30]
```

### Part 3 — Dot Product
Multiply corresponding elements and sum them up.

$$a \cdot b = \sum_{i=1}^{n} a_i b_i$$

```python
np.dot(a, b)   # [1,2,3]·[4,5,6] = 4+10+18 = 32
```

### Part 4 — Matrix Multiplication
```python
A @ B            # the clean way
np.matmul(A, B)  # same result
```
> ⚠️ `A * B` is element-wise, NOT matrix multiplication.

**Shape Rule:** `(m,n) × (n,p) → (m,p)`
**Eligibility Rule:** columns of A must equal rows of B.

Each element `[i][j]` in the result = dot product of row `i` from A and column `j` from B.

### Part 5 — Transpose
```python
A.T   # (2,3) → (3,2)
```
Swaps rows and columns. Used constantly to align shapes before matrix multiplication.

### Part 6 — Identity Matrix
```python
I = np.eye(3)   # 3×3 identity matrix
A @ I == A      # always true — behaves like multiplying by 1
```

### Part 7 — Matrix Inverse
```python
np.linalg.inv(A)       # inverse of A
A @ np.linalg.inv(A)   # → Identity matrix (I)
```
Only possible when the determinant ≠ 0.

### Part 8 — Determinant
```python
np.linalg.det(A)
```
Tells you if a matrix is invertible:
- `det = 0` → **singular** (not invertible)
- `det ≠ 0` → **non-singular** (invertible)

### Part 9 — Solving Systems of Equations
Turn algebra problems into matrix problems:
```
x + y = 5
2x + y = 8
```
```python
A = np.array([[1,1],[2,1]])
b = np.array([5, 8])
np.linalg.solve(A, b)   # → [3., 2.]  → x=3, y=2
```

### Part 10 — Norms
The length (magnitude) of a vector — measured from the origin.

$$\|v\| = \sqrt{x^2 + y^2}$$

```python
v = np.array([3, 4])
np.linalg.norm(v)   # → 5.0
```

---

## ⚡ Industry Insight — The ML Equation

```python
prediction = X @ W + b
```

| Symbol | Meaning |
|---|---|
| `X` | Data matrix (features) |
| `W` | Model weights |
| `b` | Bias term |
| `@` | Matrix multiplication |
| `+ b` | Broadcasting |

This is the skeleton of most machine learning models. Now you know exactly what every symbol means. 🧠

---

## 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook Linear_Algebra.ipynb
```

**Requirements:** Python 3.x · NumPy · Jupyter Notebook

```bash
pip install numpy jupyter
```

---

## 📚 Part of the NumPy Series

| Notebook | Topic |
|---|---|
| 01 | NumPy Basics & Array Creation |
| 02 | Array Attributes |
| 03 | Indexing & Slicing |
| 04 | Array Manipulation |
| 05 | Vectorization Mathematics |
| 06 | Broadcasting |
| 07 | Statistical Computing |
| 08 | Practice Set (Ep 05–08) |
| **09** | **Linear Algebra ← You are here** |

---

## 🙋 About Me

I'm **Zeeshan**, a Data Science & AI enthusiast learning in public. 🌱
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
