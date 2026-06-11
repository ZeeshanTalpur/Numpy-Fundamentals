 🔢 NumPy Problem Set (1–4) — Indexing, Slicing & Boolean Masking

A hands-on NumPy practice notebook with 20 real-world problems across 4 difficulty levels. Each problem simulates a genuine data scenario — from website analytics to fraud detection — to build practical intuition for NumPy's core features.

---

 📚 What's Covered

- NumPy array creation
- Array indexing (basic, fancy, and boolean)
- Array slicing (1D and 2D)
- Array attributes: `.shape`, `.ndim`, `.size`, `.dtype`
- Conditional filtering on 2D arrays
- Modifying array values in-place

---

 🏆 Difficulty Levels

 ⚡ Level 1 — Junior Data Analyst (Easy)

|  | Problem | Dataset |
|---|---------|---------|
| 1 | Daily Website Visitors | `visitors = np.array([120, 145, 132, 167, 189, 210, 195])` |
| 2 | Product Prices | `prices = np.array([100, 250, 80, 120, 400, 60])` |
| 3 | Temperature Monitoring | `temps = np.array([32, 34, 35, 38, 40, 42, 37])` |
| 4 | Employee IDs | `employee_ids = np.array([101,102,103,104,105,106,107,108])` |
| 5 | Sales Data | `sales = np.array([5000, 7000, 6500, 9000, 12000, 11000])` |

<details>
<summary>📋 View Tasks</summary>

Problem 1 — Daily Website Visitors
- Get the first day's visitors
- Get the last day's visitors
- Get visitors for the first 3 days
- Get visitors for the weekend (last 2 days)

Problem 2 — Product Prices
- Extract all products costing more than 100
- Extract all products costing less than 100
- Extract the 2nd, 4th, and 6th products using fancy indexing

Problem 3 — Temperature Monitoring
- Get temperatures above 37
- Get temperatures below 35
- Reverse the dataset

Problem 4 — Employee IDs
- Extract IDs from position 2 to 6
- Extract every second ID
- Extract IDs at positions 1, 3, and 7

Problem 5 — Sales Data
- Find all sales above 8000
- Replace sales below 7000 with 0
- Verify the shape, ndim, size and dtype

</details>

---

 🔧 Level 2 — Data Cleaning Tasks (Intermediate)

|  | Problem | Dataset |
|---|---------|---------|
| 6 | Customer Ages | 1D array of ages |
| 7 | E-commerce Orders | 2D array — `OrderID \| Amount` |
| 8 | Student Scores | 2D array — 4 students × 3 subjects |
| 9 | Hospital Patients | 2D array — `PatientID \| Age` |
| 10 | Manufacturing Defects | 1D daily defect counts |

<details>
<summary>📋 View Tasks</summary>

Problem 6 — Customer Ages
`ages = np.array([15,22,34,18,17,45,29,13,50])`
- Extract all adults (18+)
- Extract all minors
- Count how many adults remain after filtering

Problem 7 — E-commerce Orders
```
orders = np.array([
    [101, 500],
    [102, 1500],
    [103, 800],
    [104, 2500],
    [105, 300]
])   Columns: OrderID | Amount
```
- Extract all order amounts
- Extract orders with amount > 1000
- Extract only the order IDs of high-value orders

Problem 8 — Student Scores
```
scores = np.array([
    [78, 85, 90],
    [45, 50, 55],
    [88, 92, 95],
    [60, 65, 70]
])
```
- Extract first student's scores
- Extract Maths scores (column 0)
- Extract students whose Maths score is above 70

Problem 9 — Hospital Patients
```
patients = np.array([
    [1, 25],
    [2, 67],
    [3, 43],
    [4, 80],
    [5, 15]
])   Columns: PatientID | Age
```
- Extract senior citizens (60+)
- Extract patient IDs of seniors
- Extract minors

Problem 10 — Manufacturing Defects
`defects = np.array([2,5,0,1,8,3,0])`
- Extract days with defects
- Extract days with zero defects
- Extract every alternate day

</details>

---

 📊 Level 3 — Real Dataset Manipulation (Upper Intermediate)

|  | Problem | Dataset |
|---|---------|---------|
| 11 | Customer Dataset | 2D array — `Name \| Age \| Salary` |
| 12 | Mobile App Analytics | 2D array — 3 apps × 4 quarters |
| 13 | Logistics Tracking | 2D array — `DeliveryID \| DelayDays` |
| 14 | Marketing Campaign | 2D array — `CampaignID \| Leads` |
| 15 | Sensor Data | `np.arange(1, 101)` |

<details>
<summary>📋 View Tasks</summary>

Problem 11 — Customer Dataset
```
customers = np.array([
    ["Ali",    22, 50000],
    ["Sara",   25, 70000],
    ["Ahmed",  30, 90000],
    ["Ayesha", 21, 45000],
    ["Bilal",  35, 120000]
], dtype=object)
```
- Extract all names
- Extract all salaries
- Extract customers earning above 60000
- Extract names of customers earning above 60000

Problem 12 — Mobile App Analytics
```
downloads = np.array([
    [1200, 1500, 1800, 2200],
    [1000, 1100, 1400, 1700],
    [2500, 2700, 3000, 3300]
])   Rows = Apps | Columns = Quarters
```
- Extract Q2 downloads
- Extract App 3 downloads
- Extract last two quarters

Problem 13 — Logistics Tracking
```
deliveries = np.array([
    [1, 2],
    [2, 5],
    [3, 1],
    [4, 8],
    [5, 3]
])   Columns: DeliveryID | DelayDays
```
- Find delayed deliveries (> 3 days)
- Extract Delivery IDs with delays
- Extract on-time deliveries

Problem 14 — Marketing Campaign
```
campaign = np.array([
    [101, 500],
    [102, 1200],
    [103, 300],
    [104, 2200],
    [105, 1800]
])   Columns: CampaignID | Leads
```
- Extract campaigns generating > 1000 leads
- Extract their IDs
- Extract campaigns generating < 500 leads

Problem 15 — Sensor Data
`sensor = np.arange(1, 101)`
- Extract first 20 readings
- Extract last 20 readings
- Extract every 5th reading
- Reverse the readings

</details>

---

 🧠 Level 4 — Data Scientist Level (Advanced)

|  | Problem | Dataset |
|---|---------|---------|
| 16 | Fraud Detection Preprocessing | 2D array — `TransactionID \| Amount` |
| 18 | Retail Chain Analysis | 2D array — 4 stores × 3 months |
| 19 | Employee Retention Dataset | 2D array — `EmployeeID \| YearsAtCompany` |
| 20 | Mini Data Science Case Study | 2D array — `EmployeeID \| Age \| Salary` |

<details>
<summary>📋 View Tasks</summary>

Problem 16 — Fraud Detection Preprocessing
```
transactions = np.array([
    [1001, 500],
    [1002, 25000],
    [1003, 700],
    [1004, 50000],
    [1005, 900]
])   Columns: TransactionID | Amount
```
- Flag suspicious transactions (> 10000)
- Extract suspicious IDs
- Extract normal transactions

Problem 18 — Retail Chain Analysis
```
stores = np.array([
    [12000, 15000, 18000],
    [ 8000,  9000,  9500],
    [20000, 22000, 25000],
    [ 5000,  6000,  7000]
])   Rows = Stores | Columns = Months
```
- Extract high-performing stores (Month 1 > 10000)
- Extract all sales data for those stores
- Extract Month 3 sales

Problem 19 — Employee Retention Dataset
```
employees = np.array([
    [1, 2],
    [2, 5],
    [3, 1],
    [4, 8],
    [5, 6]
])   Columns: EmployeeID | YearsAtCompany
```
- Extract employees with tenure ≥ 5
- Extract their IDs
- Extract employees with tenure < 3

Problem 20 — Mini Data Science Case Study ⭐
```
data = np.array([
    [101, 22, 50000],
    [102, 35, 120000],
    [103, 19, 25000],
    [104, 41, 90000],
    [105, 28, 70000],
    [106, 17, 15000]
])   Columns: EmployeeID | Age | Salary
```
Without using any loops, solve:
- Extract all adults (18+)
- Extract employees earning > 60000
- Extract employees aged between 20 and 40
- Extract Employee IDs of high earners
- Extract the Age and Salary columns only
- Extract first 3 records
- Extract last 2 records
- Extract every alternate record
- Reverse the entire dataset
- Verify shape, ndim, size and dtype

</details>

---

 🛠️ Requirements

```bash
pip install numpy jupyter
```

---

 🚀 How to Run

```bash
jupyter notebook "Problem_Set__1_-_4_.ipynb"
```

---

 👨‍💻 Author

Zeeshan Talpur
🔗 [GitHub: ZeeshanTalpur](https://github.com/ZeeshanTalpur)

---

More learning, more building, more data coming up! ✨
