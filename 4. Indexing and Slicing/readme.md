 📊 NumPy Indexing and Slicing

A beginner-friendly Jupyter Notebook covering how to extract specific pieces of data from NumPy arrays — a fundamental skill for any Data Science workflow.

---

 📂 File

`Indexing_and_Slicing.ipynb`

---

 🧠 What This Notebook Covers

 🔹 Indexing
- Positive Indexing — accessing elements left to right (`arr[2]`)
- Negative Indexing — accessing elements right to left (`arr[-2]`)

 🔹 Slicing — `arr[start : stop : step]`
- `start` — where to begin
- `stop` — where to end (exclusive)
- `step` — how many positions to jump
- Reversing an array using `arr[::-1]`

 🔹 2D Array Slicing (Rows & Columns)
Working with a dataset of names, ages, and salaries:
- Slice all ages → `arr[:, 0]`
- Slice all salaries → `arr[:, 1]`
- Slice first N records → `arr[:2, ]`
- Combine row + column slicing → `arr[:2, 0]`

 🔹 Boolean Indexing
- Filter data using conditions instead of positions
- Example: `ages >= 18` returns a boolean mask — no loops needed!

 🔹 Fancy Indexing
- Pick specific rows or columns using index lists
- `arr[[1, 2]]` — select rows 1 and 2
- `arr[:, [0]]` — select only column 0

---

 🛠️ Tech Used

- Python 3.13
- NumPy
- Jupyter Notebook

---

 🔗 Part of My NumPy Learning Series

This notebook is part of my ongoing NumPy fundamentals journey.  
Check out the full series → [github.com/ZeeshanTalpur](https://github.com/ZeeshanTalpur)

---

More learning, more building, more data coming up! 🚀