# 📊 Statistical Engineering & Simulation Project

## 🚀 Project Overview

This project implements a **pure Python statistical engine** from scratch and applies it to real-world data analysis and probabilistic simulation.

The system performs:

* Core statistical analysis (mean, median, mode, variance, standard deviation)
* Outlier detection using standard deviation
* Monte Carlo simulation to model server failures
* Demonstration of the **Law of Large Numbers (LLN)**

No external libraries were used — only Python standard libraries such as `math`, `random`, `json`, and `unittest`.

---

## 🧠 Features

### 1. Statistical Engine (`StatEngine`)

Processes 1D numerical datasets and computes:

#### 🔹 Central Tendency

* Mean
* Median (handles even & odd datasets)
* Mode (supports multimodal distributions)

  * Returns all modes
  * Returns message if all values are unique

#### 🔹 Dispersion

* Variance:

  * Sample Variance (uses **n-1**, Bessel’s correction)
  * Population Variance (uses **n**)
* Standard Deviation

#### 🔹 Outlier Detection

* Identifies values more than `threshold` standard deviations from the mean

#### 🔹 Robust Error Handling

* Prevents empty dataset errors
* Handles invalid data types (raises descriptive errors)

---

### 2. Monte Carlo Simulation

Simulates a startup server crash scenario:

* Daily crash probability: **4.5% (0.045)**
* Function: `simulate_crashes(days)`
* Runs simulations for:

  * 30 days
  * 365 days
  * 10,000 days

---

## 📐 Mathematical Logic

### Variance

* **Population Variance:**

  [
  \sigma^2 = \frac{\sum (x - \mu)^2}{n}
  ]

* **Sample Variance (Bessel’s Correction):**

  [
  s^2 = \frac{\sum (x - \mu)^2}{n - 1}
  ]

### Standard Deviation

[
\sigma = \sqrt{\text{variance}}
]

---

### Median Logic

* **Odd number of elements:** middle value after sorting
* **Even number of elements:** average of two middle values

---

## 📁 Project Structure

```
statistical_engine/
│
├── data/
│   └── sample_salaries.json
│
├── src/
│   ├── stat_engine.py
│   ├── monte_carlo.py
│   └── __init__.py
│
├── tests/
│   ├── test_stat_engine.py
│   └── __init__.py
│
├── main.py
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```
git clone <your-repo-link>
cd statistical_engine
```

### 2. Run the Program

```
python main.py
```

---

## 🧪 Running Tests

Execute unit tests using:

```
python -m unittest discover tests
```

---

## ✅ Acceptance Criteria Checklist

* [x] Handles empty dataset safely
* [x] Handles invalid data types
* [x] Correct mean calculation
* [x] Correct median (even & odd cases)
* [x] Supports multimodal distributions
* [x] Correct sample vs population variance
* [x] Correct standard deviation
* [x] Outlier detection implemented
* [x] Monte Carlo simulation implemented
* [x] Demonstrates Law of Large Numbers

---

## 📊 Statistical Insights

### Outliers in Salary Data

The dataset includes extreme salary values.
Outliers highlight how **mean alone is misleading**, as high salaries skew the average.

Standard deviation provides a clearer picture of **data spread and volatility**.

---

## 🎲 Law of Large Numbers (LLN)

The simulation demonstrates:

* Small samples (30 days) → high variability 
* Large samples (10,000 days) → stable probability close to 0.045 ✅]

### ⚠️ Key Insight

Using a small dataset to predict long-term outcomes is unreliable and risky for decision-making (e.g., server maintenance budgeting).

---
## 📌 Technologies Used

* Python (Standard Library Only)

  * `math`
  * `random`
  * `json`
  * `unittest`


