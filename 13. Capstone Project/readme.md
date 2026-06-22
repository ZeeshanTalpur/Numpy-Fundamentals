 🏆 NumPy Capstone Project — Retail Customer Intelligence Analysis

The final project of my NumPy Learning Series. No Pandas. No Scikit-learn. No shortcuts. Just NumPy — applied to a real business scenario across 13 professional stages. 💪

---

 📒 The Scenario

> You have joined a retail analytics team as a Junior Data Scientist. The company has provided a customer dataset and wants you to prepare a complete intelligence report for management.
>
> Rules: NumPy only. No Pandas. No Scikit-learn.

---

 🗂️ The Dataset

```python
data = np.array([
    [1,  22, 50000,  45, 1],
    [2,  25, 70000,  60, 2],
    [3,  30, 90000,  80, 5],
    [4,  21, 45000,  40, 1],
    [5,  35, 120000, 90, 8],
    [6,  42, 150000, 95, 10],
    [7,  28, np.nan, 70, 3],    ← missing value
    [8,  31, 85000,  75, 4],
    [9,  29, 78000,  65, 3],
    [10, 60, 250000, 20, 20],   ← suspected outlier
    [11, 24, 52000,  55, 2],
    [12, 27, 68000,  62, 3]
])
```

Columns: CustomerID · Age · Salary · SpendingScore · YearsAsCustomer

---

 🧠 The 13 Stages

 Stage 1 — Dataset Understanding
Shape, dtypes, column extraction. Know your data before you touch it.
```python
rows, columns = data.shape        (12, 5)
age     = data[:, 1]
salary  = data[:, 2]
spending_score = data[:, 3]
years   = data[:, 4]
```

 Stage 2 — Data Quality Assessment
```python
np.sum(np.isnan(data))                          1 missing value
np.where(np.isnan(data))                        row 7, column 3 (Salary)
(np.sum(np.isnan(data)) / data.size)  100      → 0.69% missing
```

 Stage 3 — Missing Value Treatment
Replaced with median salary — not mean, because the $250,000 outlier would skew it.
```python
data[np.where(np.isnan(data))] = np.nanmedian(data[:, 2])
```

 Stage 4 — Descriptive Analytics
Mean, median, std, min, max for every feature → built the "typical customer" profile.
```python
np.mean(data[:, 1])     avg age
np.median(data[:, 2])   median salary
np.std(data[:, 3])      spending score spread
```

 Stage 5 — Customer Ranking
```python
data[data[:, 2] == data[:, 2].max()]    highest salary
data[data[:, 3] == data[:, 3].max()]    highest spending score
```

 Stage 6 — Outlier Investigation (IQR Method)
```python
q1 = np.percentile(salary, 25)
q3 = np.percentile(salary, 75)
iqr = q3 - q1
lower = q1 - 1.5  iqr
upper = q3 + 1.5  iqr
outliers = data[(data[:, 2] < lower) | (data[:, 2] > upper)]
```
Finding: Customer 10 — salary of $250,000 — flagged as a potential outlier. 3× the next highest earner. Could be a VIP, executive, or data entry error. Needs investigation.

 Stage 7 — Customer Segmentation
```python
conditions = (
    salary <= 60000,
    (salary > 60000) & (salary <= 100000),
    salary > 100000
)
choices = ["Low income", "Medium income", "High income"]
segments = np.select(conditions, choices, default="")
```

 Stage 8 — High-Value Customer Detection (VIP)
Definition: Salary above average AND Spending Score above average.
```python
vip = data[(data[:, 2] > np.mean(data[:, 2])) & (data[:, 3] > np.mean(data[:, 3]))]
```
These customers should be prioritized for retention campaigns.

 Stage 9 — Correlation Analysis
```python
matrix = np.corrcoef(data, rowvar=False)
```
Findings:
- Strongest positive: Higher salary → higher spending
- Longer tenure → higher customer value
- Weakest: Age shows the least linear relationship with other features

 Stage 10 — Feature Engineering
Three new features created to enrich the dataset:

| Feature | Formula | Why |
|---|---|---|
| Value Score | `salary × spending` | Combined measure of customer worth |
| Loyalty Score | `years × spending` | Long-term engagement signal |
| Spending Efficiency | `spending / salary` | Who spends the most relative to income |

```python
X = np.column_stack((age, salary, spending, years,
                     value_score, loyalty_score, spending_ratio))
```

 Stage 11 — Normalization & Standardization
```python
 Min-Max Normalization → [0, 1]
normalized = (arr - arr.min()) / (arr.max() - arr.min())

 Z-Score Standardization → mean=0, std=1
standardized = (arr - np.mean(arr)) / np.std(arr)
```
Verified: all normalized values in [0,1]. All standardized means ≈ 0, stds ≈ 1. ✅

 Stage 12 — Train/Test Split
```python
y = (spending_score > 70).astype(int)          target: High Spender
indices = np.random.permutation(len(x_std))
split = int(0.8  len(x_std))                  80/20 split

X_train = x_std[train_idx]    (9, 4)
X_test  = x_std[test_idx]     (3, 4)
y_train = y[train_idx]         (9,)
y_test  = y[test_idx]          (3,)
```

 Stage 13 — Executive Summary
Complete management report covering:
- Data quality findings
- Customer profile
- Outlier flags and explanations
- Segmentation breakdown
- VIP customer list
- Correlation insights
- ML readiness confirmation

---

 📊 Final Results

| Metric | Value |
|---|---|
| Total Customers | 12 |
| Original Features | 4 |
| Engineered Features | 3 |
| Final Feature Count | 7 |
| Missing Values (before) | 1 |
| Missing Values (after) | 0 |
| Outliers Flagged | 1 (Customer 10) |
| VIP Customers | Identified ✅ |
| ML-Ready | ✅ |

---

 🛠️ Skills Applied

✅ Array slicing & column extraction  
✅ NaN detection & imputation  
✅ Descriptive statistics  
✅ Boolean masking & filtering  
✅ IQR-based outlier detection  
✅ `np.select()` for multi-condition segmentation  
✅ Correlation matrix (`np.corrcoef`)  
✅ Feature engineering  
✅ Min-Max normalization  
✅ Z-score standardization  
✅ Train/test split with `np.random.permutation`  
✅ Target variable creation  

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook NumPy_Capstone.ipynb
```

Requirements: Python 3.x · NumPy · Jupyter Notebook

```bash
pip install numpy jupyter
```

---

 📚 NumPy Series — Complete

|  | Topic |
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
| 11 | Advanced NumPy Toolkit |
| 12 | Real Data Science Workflows |
| 13 | NumPy for Machine Learning Foundations |
| 14 | Capstone Project ← You are here 🏆 |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱  
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
