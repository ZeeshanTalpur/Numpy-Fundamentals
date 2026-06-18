 🛠️ Advanced NumPy Toolkit — Data Cleaning & Logic

Part of my NumPy Learning Series — the toolkit every Data Scientist actually reaches for on messy, real-world data. Forget means and reshapes. This one is about filtering bad data, handling missing values, making decisions on arrays, and cleaning a dataset end to end. 🔥

---

 📒 About This Notebook

In real datasets, the problem isn't calculating means — it's dealing with missing values, filtering bad rows, labeling data conditionally, and extracting only what matters. This notebook covers the full data-cleaning toolkit in NumPy with a real industry pipeline at the end.

---

 🧠 What's Covered

 1. 🎭 Boolean Masking (Conditional Selection)
Filter arrays based on conditions — no loops needed.
```python
data = np.array([10, 25, 30, 45, 50])

data > 30               → [False, False, False, True, True]
data[data > 30]         → [45, 50]
```

 2. ⚡ Multiple Conditions
Always wrap each condition in parentheses. Use NumPy operators, not Python keywords.

| Want | Use | Not |
|---|---|---|
| AND | `&` | `and` |
| OR | `\|` | `or` |
| NOT | `~` | `not` |

```python
data[(data > 20) & (data < 50)]    AND → [25, 30, 45]
data[(data > 20) | (data < 50)]    OR  → all values
data[~(data > 30)]                 NOT → [10, 25, 30]
```

 3. 🔀 np.where() — The Decision Engine
If-else logic for entire arrays in one line.
```python
ages = np.array([17, 14, 21, 12, 23, 62])
np.where(ages >= 18, "Adult", "child")
 → ['child','child','Adult','child','Adult','Adult']
```

 4. 🧩 np.select() — Multi-Condition Logic
When you have more than two outcomes.
```python
conditions = [ages < 18, (ages >= 18) & (ages <= 60), ages > 60]
choices    = ["child", "adult", "retired"]
np.select(conditions, choices, default="")
 → ['child','child','adult','child','adult','retired']
```

 5. 🕳️ Handling Missing Data (NaN)

Create, detect, and remove:
```python
data = np.array([10, np.nan, 30, np.nan, 50])

np.isnan(data)          detect  → [False, True, False, True, False]
data[~np.isnan(data)]   remove  → [10., 30., 50.]
```

 6. 🛡️ NaN-Safe Statistics
Normal functions break silently with NaN values.
```python
np.mean(data)       → may return NaN ❌

np.nanmean(data)    → 30.0  ✓
np.nanmedian(data)  → 30.0  ✓
np.nanstd(data)     → 16.33 ✓
```

 7. ✂️ np.clip() — Value Control
Limit values to a range. Outlier handling in one line.
```python
data = np.array([10, 20, 30, 40, 50])
np.clip(data, 20, 40)    → [20, 20, 30, 40, 40]
```
> Values below 20 become 20. Values above 40 become 40.

 8. 📍 argmax & argmin
Find the index of the highest or lowest value.
```python
data = np.array([10, 50, 30])
np.argmax(data)    → 1  (index of 50)
np.argmin(data)    → 0  (index of 10)
```

 9. 🔢 argsort()
Sort, but return indices instead of values.
```python
data = np.array([40, 10, 30])
np.argsort(data)    → [1, 2, 0]  (10 is at idx 1, 30 at idx 2, 40 at idx 0)
```

 10. 🔍 np.unique()
Find distinct values — with optional counts.
```python
data = np.array([1, 1, 2, 2, 3, 3, 3])
np.unique(data)                           → [1, 2, 3]
np.unique(data, return_counts=True)       → ([1,2,3], [2,2,3])
```

 11. ✅ Logical Reductions — any() & all()
```python
np.any(data > 40)    True if ANY value passes  → True
np.all(data > 0)     True if ALL values pass   → True
```

---

 🏭 Real Industry Pipeline (Everything Combined)

```python
data = np.array([10, 25, np.nan, 45, 60, np.nan])

 Step 1: Remove NaNs
clean = data[~np.isnan(data)]

 Step 2: Clip extreme values
clean = np.clip(clean, 20, 50)

 Step 3: Label data
labels = np.where(clean > 40, "High", "Low")

 Step 4: NaN-safe statistics
np.nanmean(clean)    → 35.0
np.nanstd(clean)     → 12.75
```

This 4-step pattern runs constantly in real data preprocessing pipelines. 🔥

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook Advanced_NumPy_Toolkit.ipynb
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
| 05 | Vectorization Mathematics |
| 06 | Broadcasting |
| 07 | Statistical Computing |
| 08 | Practice Set (Ep 05–08) |
| 09 | Linear Algebra |
| 10 | Random Numbers, Probability & Simulation |
| 11 | Advanced NumPy Toolkit ← You are here |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
