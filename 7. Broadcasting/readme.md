 📡 NumPy Broadcasting

> "Don't loop what NumPy can expand." — the whole point of this notebook.

Broadcasting is NumPy's superpower that lets you do arithmetic between arrays of different shapes — without writing a single loop. NumPy automatically stretches the smaller array to match the larger one, keeping your code clean and fast.

---

 📖 What's Covered

 Core Rules
| Rule | Description |
|------|-------------|
| Rule 1 | Compare dimensions from the right |
| Rule 2 | Dimensions are compatible if they're equal OR one of them is 1 |

 Broadcasting Types

| Type | Shape Example | What Happens |
|------|--------------|--------------|
| Scalar | `(2,3)` + `()` | Scalar expands to fill the entire array |
| Row Vector | `(2,3)` + `(3,)` | Row repeats downward across all rows |
| Column Vector | `(2,3)` + `(2,1)` | Column repeats sideways across all columns |

---

 🔬 Real Data Science Examples

 Example 1 — Sensor Calibration
A 3-city temperature grid where each city's thermometer has a different calibration offset. A `(3,1)` correction vector broadcasts across all 3 days automatically.

 Example 2 — Feature Scaling (Mean Centering)
A dataset with Age and Salary columns. Subtracting a `(2,)` means vector centers each column — this exact pattern is used in every ML preprocessing pipeline.

---

 🏋️ Challenge Set

|  | Task | Concept Practiced |
|---|------|-------------------|
| 1 | Add scalar bonus to 3×4 sales matrix | Scalar broadcasting |
| 2 | Add row vector `(3,)` to a 4×3 matrix | Row broadcasting |
| 3 | Add column vector `(4,1)` to a 4×3 matrix | Column broadcasting |
| 4 | Convert 1D ages array → column vector | `reshape(-1, 1)` |
| 5 | Mean-center a feature matrix | Real ML preprocessing |

All 5 challenges solved ✅

---

 🧠 Professional Uses

Broadcasting powers these everyday DS/ML operations:

- `X - mean` → Feature Centering
- `(X - mean) / std` → Normalization / Standardization
- `image  factor` → Image Processing
- `sensor_data + correction` → Sensor Calibration
- `revenue  tax_rates` → Financial Modeling
- `X @ W + b` → Neural Network Forward Pass (the `+ b` is broadcasting!)

---

 🛠️ Tools Used

![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat-square&logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Broadcasting-blue?style=flat-square&logo=numpy)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)

---

 🗂️ Part of My NumPy Series

| Notebook | Topic |
|----------|-------|
| 01 | Array Creation |
| 02 | Array Attributes |
| 03 | Indexing & Slicing |
| 04 | Broadcasting ← you are here |

---

More learning, more building, more data coming up! ✨
