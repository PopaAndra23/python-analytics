# Operational Analytics & Product Portfolio Management (Python)

## 📌 Project Overview
This project establishes a data cleaning and exploratory data analysis (EDA) pipeline using Python to evaluate product performance and inventory transaction patterns for **AdventureWorks**. Moving away from theoretical exercises, the analysis is structured around real-world business tickets simulated from cross-department requests (Finance, Operations, Strategy, and Product Management).

---

## 🛠️ Tech Stack & Libraries Used
* **Programming Language:** Python
* **Data Manipulation:** `pandas`
* **Data Visualization:** `matplotlib`
* **Environment:** Jupyter Notebook (`.ipynb`)

---

## 🔧 Operational Pipeline & Data Architecture

### 1. Data Cleaning & Standardization (Mandatory Layer)
* Inspected dataset shapes, data types, and structural gaps across retail sheets (`products_aw.csv` and `transactions_aw.csv`).
* Implemented structural data cleanups: handled missing values, removed trailing and leading spaces from text columns (`.str.strip()`), and re-mapped system codes into descriptive names (e.g., transforming product lines into *Road, Mountain, Standard, Touring*).
* Parsed date strings into active `datetime` objects to ensure precise time-series calculations.

### 2. Analytical Modules & Departmental Reports

* **Product Portfolio Matrix (Product Management Ticket - PE01):** Filtered the inventory dataset to isolate completed finished goods with valid retail pricing tiers. Computed median prices and evaluated price variance across product categories to optimize catalog distribution.
* **Gross Margin & Profitability Audit (Finance Ticket - PE02):** Created custom reusable functions to calculate Gross Profit Margin (%) across categories. Isolated margin trends and performed anomaly detection to flag high-volume items with critical profit margins under 10%.
* **Transaction Velocity Analysis (Operations Ticket - PE03):** Aggregated operational transaction types (Sales - S, Purchases - P, Work orders/Production - W) to determine their percentage distribution. Identified and ranked the Top 10 high-velocity products based on transaction volume.
* **Time-Series Horizon Trends (Strategy & Planning Ticket - PE04):** Extracted granular time components (months and days of the week) from transaction records. Converted numerical days into proper calendar day names (Monday, Tuesday...) to locate peak operational capacity and supply chain spikes.

---

## 💡 Engineering Best Practices Applied
* **DRY Principle (Don't Repeat Yourself):** All financial metrics, margins, and time-series conversions are wrapped inside clean, reusable Python functions (`def`) adhering to custom corporate naming conventions (`EXX_functionName`).
* **Business-Driven Interpretations:** Rather than just outputting raw code blocks, every visual chart generated in the notebook is accompanied by Markdown cells translating the statistical data into actionable economic insights for management.
