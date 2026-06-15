 🏆 NumPy Practice Set — 20 Problems (Episodes 05–08 Recap)

A complete practice set built to apply everything from the last 4 episodes of my NumPy series: Array Manipulation, Vectorization, Broadcasting, and Statistical Computing — all in real-world scenarios. 💪

---

 📒 About This Notebook

20 problems, 4 difficulty levels, zero loops. Every problem is based on a real-world dataset — sales, salaries, sensors, students, stores — and solved using pure NumPy: reshaping, broadcasting, vectorized math, and statistical analysis.

This is the "prove you actually learned it" notebook. 🎯

---

 🧠 Problem Breakdown

 🟢 Level 1 — Beginner

|  | Problem | Concepts Used |
|---|---|---|
| 1 | Monthly Sales — reshape into quarters, find totals & averages | `reshape`, `.T`, `sum`, `mean`, `max`, `min` |
| 2 | Temperature Monitoring — per-city & per-day averages | `mean(axis=0/1)`, `max`, `min` |
| 3 | Employee Bonus — add bonus via vectorization | vectorized `+`, `mean`, `std`, `reshape(-1,1)` |
| 4 | Student Marks — per-student & per-subject stats | `mean(axis)`, `max`, `min`, `flatten` |
| 5 | Website Traffic — reshape into weeks × days | `reshape`, `mean(axis)`, `sum`, `std` |

 🟡 Level 2 — Intermediate

|  | Problem | Concepts Used |
|---|---|---|
| 6 | Retail Stores — 10% sales increase, best store/month | vectorized `%`, `mean(axis)`, boolean indexing |
| 7 | ML Feature Matrix — center data using broadcasting | `mean(axis=0)`, broadcasting subtraction, `std`, `var` |
| 8 | Sensor Calibration — apply correction via broadcasting | column broadcasting, `mean`, `std`, `flatten` |
| 9 | Product Prices — reshape, apply discount, get stats | `reshape`, vectorized `-`, `mean`, `median`, `std` |
| 10 | Quarterly Revenue — stack arrays & transpose | `vstack`, `sum(axis)`, `mean(axis)`, `.T` |

 🟠 Level 3 — Upper Intermediate

|  | Problem | Concepts Used |
|---|---|---|
| 11 | Salary Analytics — detect outliers via IQR | `percentile`, `IQR`, outlier masking |
| 12 | Exam Performance — top student & hardest subject | `mean(axis)`, `std(axis)`, boolean indexing |
| 13 | Correlation Study — correlation & covariance | `corrcoef`, `cov` |
| 14 | Store Performance — add incentives via broadcasting | broadcasting `+`, `mean(axis)`, boolean indexing |
| 15 | Data Transformation Pipeline — reshape → transpose → flatten → reshape | `reshape`, `.T`, `flatten`, `.size` |

 🔴 Level 4 — Advanced

|  | Problem | Concepts Used |
|---|---|---|
| 16 | Customer Spending — correlation between age & spend | `corrcoef`, column slicing |
| 17 | Regional Sales — inflation adjustment via broadcasting | broadcasting `+`, `mean(axis)`, boolean indexing |
| 18 | Quality Control — detect outlier measurement | `mean`, `median`, `std`, `IQR`, outlier detection |
| 19 | Multi-Store Revenue — stack & compare stores | `vstack`, `sum(axis)`, `mean`, boolean indexing |
| 20 | Mini Industry Case Study — full pipeline: mean/median/std per feature, centering, correlation matrix, reshaping & stacking columns | everything combined 🔥 |

---

 🛠️ Skills Demonstrated

✅ Reshaping & Transposing
✅ Flattening & Stacking (`vstack`, `hstack`)
✅ Vectorized Arithmetic (no loops!)
✅ Broadcasting (scalar, row, column)
✅ Aggregations (`mean`, `sum`, `std`, `var`, `median`)
✅ Axis-wise operations (`axis=0` vs `axis=1`)
✅ Percentiles, Quartiles & IQR-based outlier detection
✅ Correlation & Covariance
✅ Boolean masking & conditional indexing

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook Problem_Set__5_-_8_.ipynb
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
| 08 | Practice Set: 20 Problems (Ep 05–08) ← You are here |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
