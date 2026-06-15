 📊 Statistical Computing

Part of my NumPy Learning Series — turning raw numbers into meaningful insights. This notebook covers the core statistical toolkit every Data Scientist reaches for during EDA. 🧠

---

 📒 About This Notebook

Looking at raw numbers tells you very little — statistics summarizes data into meaningful information. This notebook walks through every essential statistical measure in NumPy, why each one matters, and wraps up with the professional EDA workflow Data Scientists follow on any new dataset.


 🧠 What's Covered

 1. 📍 Mean
The central value of the dataset.
```python
np.mean(arr)
```

 2. 📐 Median
The middle value after sorting — less sensitive to outliers than the mean.
```python
np.median(arr)
```

Mean vs Median: When outliers are present, median better represents the "typical" value. Example in the notebook: an array with one extreme outlier (`500`) shows Mean = `120.0` vs Median = `30.0`.

 3. ⬆️⬇️ Minimum & Maximum
```python
np.max(arr)    or arr.max()
np.min(arr)    or arr.min()
```

 4. 📏 Range
```python
arr.max() - arr.min()
```

 5. 📈 Variance
How spread out the data is.

$$\text{Var}(X) = \frac{1}{n}\sum_{i=1}^{n}(x_i - \bar{x})^2$$

```python
np.var(arr)
```
> Squaring the differences prevents positive and negative deviations from cancelling out.

 6. 📉 Standard Deviation
Same idea as variance, but easier to interpret (same units as the data).

$$\sigma = \sqrt{\text{Var}(X)}$$

```python
np.std(arr)
```

 7. 🎯 Percentiles
The value below which a given percentage of observations fall.
```python
np.percentile(results, 50)   50% of values fall below this
```

 8. 🧩 Quartiles
Special percentiles that divide data into 4 parts:

| Quartile | Percentile |
|---|---|
| Q1 | 25th |
| Q2 | 50th |
| Q3 | 75th |

 9. 📦 Interquartile Range (IQR)
```python
iqr = q3 - q1
```
Used heavily in outlier detection.

 10. 🚨 Outlier Detection
Industry-standard rule using IQR bounds:

$$\text{Lower Bound} = Q_1 - 1.5 \times IQR$$
$$\text{Upper Bound} = Q_3 + 1.5 \times IQR$$

Any value outside these bounds is a potential outlier.
```python
outliers = arr[(arr < lower_bound) | (arr > upper_bound)]
```

 11. 🔗 Correlation
Measures interdependence between two variables.
```python
np.corrcoef(hours_studied, scores)
```

| Value | Meaning |
|---|---|
| `+1` | Strong positive relationship |
| `0` | No relationship |
| `-1` | Strong negative relationship |

---

 🧭 Professional Data Scientist Workflow

A 7-step checklist applied to any new dataset during EDA:

| Step | What to check |
|---|---|
| 1 | `shape`, `dtype` |
| 2 | `min`, `max` |
| 3 | `mean`, `median` |
| 4 | `std`, `var` |
| 5 | percentiles |
| 6 | outlier detection |
| 7 | correlation analysis |

This workflow runs constantly in Exploratory Data Analysis (EDA).

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook Statistical_Computing.ipynb
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
| 07 | Statistical Computing ← You are here |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱  
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
