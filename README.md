# 📐 NumPy Fundamentals

A complete, from-scratch NumPy learning series — built notebook by notebook, documented thoroughly, and shared publicly as I learned. This repository covers everything from basic array creation to a full industry-style data science capstone project — using **NumPy only**. 🚀

> **Stack:** Python · NumPy · Jupyter Notebook
> **Duration:** 13 episodes + 2 practice sets + 1 capstone project
> **Goal:** Master NumPy as both a data analysis tool and the mathematical engine behind Machine Learning.

---

## 🗂️ Repository Structure

```
Numpy-Fundamentals/
│
├── 1.  Lists vs Array
├── 2.  Creating Arrays
├── 3.  Array Attributes
├── 4.  Indexing and Slicing
├── Problem Set (1-4)              ← Practice: Episodes 1–4
│
├── 5.  Array Manipulation
├── 6.  Vectorization Mathematics
├── 7.  Broadcasting
├── 8.  Statistical Computing
├── Problem Set (5-8)              ← 20 Problems across 4 difficulty levels
│
├── 9.  Linear Algebra
├── 10. Random Numbers, Probability and Simulation
├── 11. Advanced NumPy Toolkit
├── 12. Common Data Science Workflows
│
└── 13. Capstone Project           ← Retail Customer Intelligence Analysis 🏆
```

Each folder contains a Jupyter notebook and its own dedicated README.

---

## 📚 Complete Episode Guide

### 🟢 Phase 1 — Foundations (Episodes 1–4)

| # | Topic | What You Learn |
|---|---|---|
| 1 | **Lists vs Array** | Why NumPy exists, performance gap, when to use each |
| 2 | **Creating Arrays** | `np.array`, `np.zeros`, `np.ones`, `np.arange`, `np.linspace`, `np.eye`, `np.random` |
| 3 | **Array Attributes** | `.shape`, `.ndim`, `.dtype`, `.size`, `.itemsize`, `.nbytes` |
| 4 | **Indexing & Slicing** | 1D/2D indexing, negative indexing, step slicing, fancy indexing |
| — | **Problem Set (1–4)** | Challenges covering all Phase 1 concepts end-to-end |

---

### 🟡 Phase 2 — Core Operations (Episodes 5–8)

| # | Topic | What You Learn |
|---|---|---|
| 5 | **Array Manipulation** | `reshape`, `flatten`, `ravel`, `.T`, `vstack`, `hstack`, `stack`, `split` |
| 6 | **Vectorization Mathematics** | Arithmetic ops, comparison ops, ufuncs (`sqrt`, `abs`, `exp`, `log`), trig, axis-wise aggregations |
| 7 | **Broadcasting** | Scalar, row & column broadcasting, the 2 rules, real DS examples, professional uses (`X @ W + b`) |
| 8 | **Statistical Computing** | Mean, median, std, variance, percentiles, quartiles, IQR, outlier detection, correlation |
| — | **Problem Set (5–8)** | 20 problems across 4 levels — Beginner → Advanced. Sales, salaries, sensors, ML feature centering, all solved with pure NumPy |

---

### 🔵 Phase 3 — Advanced & Applied (Episodes 9–12)

| # | Topic | What You Learn |
|---|---|---|
| 9 | **Linear Algebra** | Dot product, matrix multiplication (`@`), transpose, identity matrix, inverse, determinant, solving equations, norms — and how `X @ W + b` is the skeleton of ML |
| 10 | **Random Numbers, Probability & Simulation** | `random`, `randint`, seeds for reproducibility, `choice`, `shuffle`, `permutation`, uniform & normal distributions, Monte Carlo simulation |
| 11 | **Advanced NumPy Toolkit** | Boolean masking (`&`, `\|`, `~`), `np.where`, `np.select`, NaN detection & removal, NaN-safe stats, `np.clip`, `argmax`, `argsort`, `unique` |
| 12 | **Common Data Science Workflows** | 10 real business workflows: customer segmentation, outlier detection, correlation analysis, missing data investigation, product ranking, survey analytics, probability estimation, feature engineering |

---

### 🏆 Phase 4 — Capstone Project (Episode 13)

**Retail Customer Intelligence Analysis**

> **Scenario:** You've joined a retail analytics team as a Junior Data Scientist. The company wants a complete customer intelligence report. One rule: **NumPy only. No Pandas. No Scikit-learn.**

**13 professional stages delivered:**

| Stage | Deliverable |
|---|---|
| 01 | Dataset Understanding Report |
| 02 | Data Quality Assessment |
| 03 | Missing Value Treatment |
| 04 | Descriptive Analytics — Customer Profile |
| 05 | Customer Ranking Report |
| 06 | Outlier Investigation (IQR Method) |
| 07 | Customer Segmentation (Low / Medium / High) |
| 08 | VIP Customer Detection |
| 09 | Correlation Matrix Analysis |
| 10 | Feature Engineering — 3 new columns created |
| 11 | Min-Max Normalization + Z-Score Standardization |
| 12 | Train/Test Split — ML-Ready Dataset |
| 13 | Executive Summary Report |

**Final output:** 12 customers → 0 missing values → 7 features → outliers flagged → VIPs identified → fully ML-ready. 🔥

---

## 🛠️ Complete Skills Index

### Array Fundamentals
- Array creation: `np.array`, `np.zeros`, `np.ones`, `np.arange`, `np.linspace`, `np.eye`
- Attributes: `.shape`, `.ndim`, `.dtype`, `.size`, `.nbytes`
- Indexing, slicing, fancy indexing, boolean indexing

### Core Operations
- Reshape, flatten, ravel, transpose
- Stack (`vstack`, `hstack`, `stack`) and split
- Vectorized arithmetic — no loops
- Broadcasting (scalar, row, column)
- Axis-wise operations (`axis=0` vs `axis=1`)

### Statistical Computing
- Mean, median, mode, std, variance, min, max, range
- Percentiles, quartiles, IQR
- Outlier detection (industry-standard IQR method)
- Correlation and covariance

### Linear Algebra
- Dot product, matrix multiplication
- Transpose, identity matrix
- Inverse (`linalg.inv`), determinant (`linalg.det`)
- Solving systems of equations (`linalg.solve`)
- Vector norms (`linalg.norm`)

### Randomness & Simulation
- Random floats, integers, seeds
- Choice, shuffle, permutation
- Uniform and normal distributions
- Monte Carlo simulation

### Data Cleaning & Logic
- Boolean masking with `&`, `|`, `~`
- `np.where()` and `np.select()` for conditional logic
- NaN detection (`isnan`), removal, and safe statistics (`nanmean`, `nanstd`, `nanmedian`)
- `np.clip()`, `argmax`, `argmin`, `argsort`, `unique`

### Machine Learning Foundations
- Feature matrix (X) and target vector (y)
- Train/test split
- Min-max normalization
- Z-score standardization
- Euclidean distance, cosine similarity
- Feature engineering (ratios, products, flags)
- Mean Squared Error (MSE)

---

## 🚀 Getting Started

```bash
git clone https://github.com/ZeeshanTalpur/Numpy-Fundamentals.git
cd Numpy-Fundamentals
jupyter notebook
```

**Requirements:**

```bash
pip install numpy jupyter
```

---

## 📖 How to Use This Repo

| You are... | Start here |
|---|---|
| Complete beginner | Folder `1. Lists vs Array` — work through in order |
| Know Python basics | Folder `2. Creating Arrays` |
| Comfortable with basics | Folder `5. Array Manipulation` (Phase 2) |
| Want applied practice | `Problem Set (1-4)` or `Problem Set (5-8)` |
| Prepping for ML | Folder `9. Linear Algebra` onwards |
| Want a challenge | Folder `13. Capstone Project` — try each stage yourself first |

---

## 🗺️ What's Next

With NumPy complete, the journey continues into:

- 🐼 **Pandas** — data manipulation on real datasets
- 📊 **Data Visualization** — Matplotlib & Seaborn
- 🤖 **Machine Learning** — Scikit-learn

---

## 🙋 About Me

I'm **Zeeshan**, a Software Engineering student at Mehran University of Engineering & Technology (MUET), Jamshoro — learning Data Science and AI in public, one notebook at a time. 🌱

Every episode in this repository was documented and shared publicly on LinkedIn and GitHub as I built it. This isn't a course. It's a learning log.

📎 [LinkedIn](https://linkedin.com/in/zeeshan-talpur-4277b4252) · [GitHub](https://github.com/ZeeshanTalpur)

---

More learning, more building, more data coming up! ✨
