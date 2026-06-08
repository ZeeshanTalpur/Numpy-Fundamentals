 🐍 Python Lists vs NumPy Arrays

A Jupyter Notebook exploring the key differences between Python's built-in Lists and NumPy Arrays — with real benchmarks on speed and memory to back it all up.

 📋 About

One of the most important things to understand early in your Data Science journey is why NumPy exists and what it actually buys you over regular Python lists. This notebook answers that question with hands-on code and actual measured results — not just theory.

 🔍 What's Covered

 1. Creating a List vs an Array
- How a Python list is created natively
- How a NumPy array is created using `np.array()`
- The difference in their types (`list` vs `numpy.ndarray`)

 2. ⚡ Speed Comparison
Multiplying 400,000 elements by 2:

| Structure | Time Taken |
|---|---|
| Python List | ~0.106 seconds |
| NumPy Array | ~0.009 seconds |

> NumPy is ~12x faster in this benchmark — and the gap grows massively with larger data.

 3. 🗄️ Memory Comparison
Storing 1,000,000 integers:

| Structure | Memory Used |
|---|---|
| Python List | 34.33 MB |
| NumPy Array | 7.63 MB |

> NumPy uses more than 4x less memory than a Python List for the same data.

 📊 Final Verdict

| Feature | Python List | NumPy Array |
|---|---|---|
| Import required | ❌ No | ✅ Yes (`numpy`) |
| Speed | ~100x slower | ⚡ Much faster |
| Math operations | Needs loops | Vectorized (no loops!) |
| Memory usage | ~4x more | Compact & efficient |
| Data types | Mixed (heterogeneous) | Same type (homogeneous) |

 🚀 How to Run

Make sure you have Jupyter and NumPy installed:

```bash
pip install notebook numpy
```

Then launch the notebook:

```bash
jupyter notebook Lists_vs_Array.ipynb
```

 🛠️ Built With

- Python 3
- NumPy
- Jupyter Notebook
- `time` and `sys` modules (for benchmarking)

 📁 File Structure

```
Python-Lists-vs-Numpy-Arrays/
└── Lists_vs_Array.ipynb
```

 💡 Concepts Used

- NumPy array creation with `np.array()`
- Speed benchmarking with `time.time()`
- Memory measurement with `sys.getsizeof()` and `ndarray.nbytes`
- Vectorized operations vs explicit loops

 🆚 What's Different About This Project

This is the first Data Science-focused notebook in the repo — a shift from Python programming projects to actual data analysis territory. No terminal prompts, no game loops — just clean, documented Jupyter cells exploring how and why NumPy is a cornerstone of Data Science in Python.

---
Part of my Data Science learning journey 📊🐍
