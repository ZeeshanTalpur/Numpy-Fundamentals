 🔧 NumPy Array Manipulation

Part of my NumPy Learning Series — where I break down core concepts one notebook at a time! This one dives into reshaping, combining, splitting, and transforming arrays. 📐

---

 📒 About This Notebook

This notebook explores the most important array manipulation techniques in NumPy. No fluff — just clean examples, clear explanations, and hands-on practice challenges at the end.

---

 🧠 What's Covered

 1. 🔄 Reshape
Change the shape of an array without touching the data.
- Reshape into any `(rows, columns)` combo
- Use `-1` to let NumPy auto-calculate a dimension

 2. 📉 Flatten
Collapse a multi-dimensional array into 1D.
- `flatten()` — always returns a copy
- `ravel()` — usually returns a view (memory-efficient!)

 3. 🔃 Transpose
Swap rows and columns using `.T` — super useful in linear algebra and ML pipelines.

 4. ➕ Adding Dimensions
Turn a 1D array into a row vector or column vector using `np.newaxis`.
- Row vector → `arr[np.newaxis, :]`
- Column vector → `arr[:, np.newaxis]`

 5. 🔗 Combining Arrays
Four ways to join arrays:
| Method | What it does |
|---|---|
| `np.concatenate()` | Appends arrays |
| `np.vstack()` | Stacks vertically (row-wise) |
| `np.hstack()` | Stacks horizontally (column-wise) |
| `np.stack()` | Stacks along a new axis |

 6. ✂️ Splitting Arrays
The opposite of stacking:
| Method | What it does |
|---|---|
| `np.split()` | Splits into equal parts |
| `np.hsplit()` | Splits columns |
| `np.vsplit()` | Splits rows |

---

 🏋️ Practice Challenges

5 challenges to test your understanding — all solved in the notebook!

|  | Challenge |
|---|---|
| 1 | Reshape `np.arange(24)` into 4 rows × 6 columns |
| 2 | Reshape a 2×3 array into 3×2 without typing values manually |
| 3 | Stack 3 monthly sales arrays into a 3×3 matrix |
| 4 | Convert a 1D array into a column vector for ML |
| 5 | Reshape 12 sales values into 4 quarters × 3 months |

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook 5__Array_Manipulation.ipynb
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
| 04 | (coming soon) |
| 05 | Array Manipulation ← You are here |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱  
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
