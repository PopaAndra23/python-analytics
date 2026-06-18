## 📌 Project Overview
The goal of this project was to analyze data from two files: `products_aw.csv` (product catalog) and `transactions_aw.csv` (stock transactions). 

Instead of just doing abstract exercises, the project simulates real business requests (called "Tickets") from different store departments like Finance, Operations, Strategy, and Product Management.

---

## 🛠️ Tools Used
* **Language:** Python
* **Data Libraries:** `pandas` and `numpy`
* **Charts:** `matplotlib`
* **Environment:** Jupyter Notebook (`.ipynb`)

---

##  What I Did in This Project

### 1. Preparing and Cleaning the Data
* Checked the dataset sizes and looked at the data types to make sure everything was correct.
* Fixed string columns by removing unnecessary empty spaces using `.str.strip()`.
* Converted date text columns into proper Python `datetime` objects so I could do time-based analysis.
* Mapped system abbreviations into friendly names (like changing product codes into *Road, Mountain, Standard, or Touring*).

### 2. Answering Business Requests (Tickets)
* **Product Catalog (Ticket PE01):** Filtered the data to look only at active finished goods. I calculated the median prices and checked how prices vary across different product categories.
* **Profit & Finance (Ticket PE02):** Created custom Python functions (`def`) to automatically calculate the Gross Profit Margin (%). I also searched for products that have a critical profit margin of less than 10%.
* **Transactions & Sales (Ticket PE03):** Grouped data by transaction types (Sales, Purchases, Production) to see their percentages. I also found the Top 10 most active products with the highest transaction counts.
* **Time Trends (Ticket PE04):** Extracted the months and days of the week from dates. I converted day numbers into actual names (Monday, Tuesday...) and found out which months and weekdays have the most activity.

---

## 💡 Good Practices Applied
* **Reusable Code:** I used standard Python functions (`def`) for calculations so I didn't have to rewrite the same code multiple times (following the DRY - Don't Repeat Yourself principle).
* **Business Conclusions:** Inside the notebook, every chart and calculation is followed by a short note written in Markdown explaining what the data actually means for a manager.

---

## 📂 Repository Structure
* `Proiect_Python_AdventureWorks.ipynb`: The complete Jupyter Notebook with all my Python code, generated charts, and text explanations visible.
