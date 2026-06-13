 ⚡ Vectorization Mathematics

Part of my NumPy Learning Series — applying operations to entire arrays at once, no loops needed. This notebook covers the math backbone of NumPy that makes Data Science fast. 🚀

---

 📒 About This Notebook

NumPy's real power isn't just storing data — it's doing math on entire arrays in one shot. This notebook breaks down every major category of vectorized operations with clean examples and a real-world sales dataset for aggregations.

---

 🧠 What's Covered

 1. ➕ Vectorized Arithmetic Operations
Apply scalar operations element-wise across the whole array — no loops!

| Operation | Symbol | Example |
|---|---|---|
| Addition | `+` | `arr + 5` |
| Subtraction | `-` | `arr - 5` |
| Multiplication | `` | `arr  2` |
| Division | `/` | `arr / 10` |
| Exponent | `` | `arr  2` |
| Floor Division | `//` | `arr // 3` |
| Modulus | `%` | `arr % 3` |

 2. 🔗 Inter-Array Operations
Two arrays, one operation — element-wise, positional, instant.
- `a + b`, `a - b`, `a  b`, `a / b`

 3. ⚖️ Comparison Operations
Returns a boolean array — the foundation of filtering and masking.
```python
ages = np.array([12, 18, 25, 30, 15])
ages > 18    → [False False  True  True False]
ages < 18    → [ True False False False  True]
ages == 25   → [False False  True False False]
```

 4. 🔢 Universal Functions (ufuncs)
Pre-built math functions that run fast on entire arrays.

| Function | What it does |
|---|---|
| `np.sqrt(arr)` | Square root of each element |
| `np.abs(arr)` | Absolute value |
| `np.exp(arr)` | Exponential `eˣ` |
| `np.log(arr)` | Natural logarithm |

 5. 📐 Trigonometric Functions
```python
np.sin(np.pi / 6)    → 0.5
np.cos(np.pi / 6)    → 0.866
np.tan(np.pi / 3)    → 1.732
```

 6. 📊 Aggregation Functions
Summarize an entire array in one call.

```python
sales = np.array([100, 200, 300, 400])

np.sum(sales)    → 1000
np.mean(sales)   → 250.0
np.min(sales)    → 100
np.max(sales)    → 400
np.std(sales)    → 111.8
np.var(sales)    → 12500.0
```

 7. 🧭 Axis-Wise Operations
Control which direction the aggregation runs on 2D arrays.

```python
 axis=0 → column-wise (down each column)
np.sum(sales, axis=0)

 axis=1 → row-wise (across each row)
np.sum(sales, axis=1)
```

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook Vectorization_Mathematics.ipynb
```

Requirements: Python 3.x · NumPy · Jupyter Notebook

```bash
pip install numpy jupyter
```

---

 📚 Part of the NumPy Series

| Notebook | Topic |
|---|---|
| 01 | NumPy Basics & Array Creation |
| 02 | Array Attributes |
| 03 | Indexing & Slicing |
| 04 | Array Manipulation |
| 05 | Vectorization Mathematics ← You are here |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱  
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
