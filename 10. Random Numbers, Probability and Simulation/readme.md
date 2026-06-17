 🎲 Random Numbers, Probability & Simulation

Part of my NumPy Learning Series — where math meets the real world. This notebook covers how Data Scientists generate synthetic data, run probability experiments, and simulate real-world scenarios — all without collecting a single data point. 🧪

---

 📒 About This Notebook

You don't always have enough data. Sometimes you need 100,000 fraud cases but only have 1,000. That's where simulation comes in. This notebook walks through every randomness tool in NumPy — from basic random floats to Monte Carlo simulations — and wraps up with a full industry mini-project: 1,000 synthetic customers analyzed end to end.

---

 🧠 What's Covered

 1. 🎰 Random Floats
Generate random numbers between 0 and 1.
```python
np.random.random()         single float
np.random.random(3)        1D array
np.random.random((2,3))    2D matrix
```
Used for: initializing ML weights, simulating sensor noise, testing algorithms.

 2. 🔢 Random Integers
```python
np.random.randint(1, 5)          one integer
np.random.randint(1, 10, 5)      1D array
np.random.randint(1, 5, (3,4))   2D matrix
```
Industry example:
```python
ages = np.random.randint(18, 65, 1000)   1000 synthetic customers
```

 3. 🔒 Reproducibility (Seeds)
Without a seed — different result every run. Bad for science.
```python
np.random.seed(42)
np.random.randint(1, 10, 5)    always the same output
```
> If your model hits 92% accuracy, your teammate should be able to reproduce it. Seeds make that possible.

 4. 🎯 Random Choice
Pick random elements from existing data.
```python
np.random.choice(fruits, 3)                     with replacement
np.random.choice(fruits, 3, replace=False)      without replacement
```
Industry usage:
```python
sample = np.random.choice(customer_ids, size=100, replace=False)
```

 5. 🔀 Shuffle vs Permutation

| Method | Behaviour |
|---|---|
| `np.random.shuffle(arr)` | Modifies original array in-place |
| `np.random.permutation(arr)` | Returns new shuffled array, original unchanged |

 6. 📊 Distributions

Uniform — values spread evenly between bounds:
```python
np.random.uniform(50, 100, 10)
```

Normal — bell curve, the shape of real-world data:
```python
np.random.normal(loc=50, scale=10, size=100)
 loc = mean, scale = std dev
```
Used for: heights, IQ scores, exam marks, measurement errors. Many ML assumptions depend on approximately normal data.

 7. 🧪 Data Sampling
Survey 500 people out of 10,000 — in one line:
```python
population = np.arange(10000)
sample = np.random.choice(population, size=500, replace=False)
```

 8. 🪙 Probability Simulation
Estimate probability of heads in 10,000 coin tosses:
```python
tosses = np.random.choice(["H","T"], size=10000)
np.mean(tosses == "H")    → ~0.5
```

 9. 🎰 Monte Carlo Simulation
Estimate probability of rolling a 6 — without any math:
```python
dice = np.random.randint(1, 7, 100000)
np.mean(dice == 6)    → ~0.1667
```
> Instead of solving P(event) mathematically, simulate millions of experiments. That's Monte Carlo.

 10. 🏭 Industry Mini Project
Build 1,000 synthetic customers with age, salary, and spending score:
```python
age      = np.random.randint(16, 60, 1000)
salary   = np.random.normal(50000, 3000, 1000)
spending = np.random.randint(1, 6, 1000)
customers = np.column_stack((age, salary, spending))
```
Then: compute means, stds, correlation matrix, sample 100 customers, shuffle, find probability of salary > 80,000, and probability of age < 25.

This resembles the first step of many real-world analytics pipelines. 🔥

---

 🚀 How to Run

```bash
git clone https://github.com/ZeeshanTalpur/<repo-name>.git
cd <repo-name>
jupyter notebook Random_Probability_and_Simulation.ipynb
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
| 10 | Random Numbers, Probability & Simulation ← You are here |

---

 🙋 About Me

I'm Zeeshan, a Data Science & AI enthusiast learning in public. 🌱
Follow my journey → [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/ZeeshanTalpur)

More learning, more building, more data coming up! ✨
