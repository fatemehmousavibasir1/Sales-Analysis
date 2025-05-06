
#  Sales Data Analysis for Company

The Company is a leading Iranian exporter of products to various countries. This project is part of a data-driven initiative to enhance commercial performance by analyzing sales records over recent years.

This repository contains the code and documentation for a five-phase data analysis process, working solely with `numpy`, `pandas`, `matplotlib`, and `seaborn`, based on data provided in an Excel file named `sales.xlsx`.

---

##  Dataset Overview

The dataset is stored in a file named `sales.xlsx` and contains detailed records of customer purchases. Here's a brief overview of the columns:

| Column Name      | Description |
|------------------|-------------|
| `InvoiceNumber`  | A unique 6-digit invoice number. If it starts with "C", the invoice was canceled. |
| `ProductCode`    | A unique 5-digit code identifying each product type. |
| `ProductName`    | Name of the product. |
| `Quantity`       | Number of units sold in each invoice. |
| `InvoiceDate`    | Date of the invoice. |
| `UnitPrice`      | Price per unit of the product. |
| `CusotmerId`     | A unique 5-digit code representing each customer. *(Note: typo in column name preserved from original)* |
| `Country`        | Country of residence of the customer. |

---

##  Project Goals

The analysis is broken down into five major steps:

### 1.  Data Preprocessing

- **Read and inspect** the Excel file.
- Handle **missing or incorrect values**.
- Remove **canceled invoices** (invoices starting with "C").
- Convert `InvoiceDate` to datetime format.
- Create new columns such as `TotalPrice = Quantity × UnitPrice`.

### 2.  Exploratory Data Analysis (EDA)

- Understand **overall sales trends**.
- Find **top-selling products** and **peak sales periods**.
- Analyze **average basket size** per transaction.
- Plot revenue distribution using histograms and boxplots.

### 3.  Market Analysis

- Compare **customer counts vs revenue** per country.
- Identify **underperforming markets** (countries with many customers but low revenue).
- Visualize geographical distribution of customers and sales.

### 4.  Customer Segmentation with RFM

Using **Recency, Frequency, Monetary** analysis:
- Score each customer based on:
  - **Recency**: Days since last purchase.
  - **Frequency**: Number of transactions.
  - **Monetary**: Total revenue from the customer.
- Assign customers to one of **7 meaningful segments**:
  - Champions
  - Loyal Customers
  - Potential Loyalists
  - New Customers
  - At Risk
  - Can't Lose Them
  - Hibernating

### 5.  Customer Retention Analysis

- Track how many customers **returned for repeat purchases** in subsequent months.
- Analyze **retention curves** and customer lifetime behavior.
- Visualize churn and loyalty rates over time.

---

##  Visualizations

The project includes a variety of visual insights such as:

- Line charts for **monthly revenue trends**
- Bar charts for **country-level comparisons**
- Heatmaps for **RFM segmentation**
- Retention matrices and customer flow

All visualizations are built using `matplotlib` and `seaborn` to maintain compatibility with project requirements.

---

##  Tech Stack

This project is built using:

- `Python 3.13`
- `pandas` – Data manipulation
- `numpy` – Numerical operations
- `matplotlib` – Static plotting
- `seaborn` – Enhanced statistical visualization

---

##  Project Structure

```
sales-analysis/
│
├── sales.xlsx               # Raw dataset
├── README.md                # Project documentation
├── Sib_Company_1_preprocessing.ipynb   # Step 1: Data cleaning & feature creation
├── Sib_Company_2_exploration.ipynb            # Step 2: Exploratory data analysis
├── Sib_Company_3_market_study.ipynb # Step 3: Country-level performance
├── Sib_Company_4_rfm.ipynb # Step 4: Customer segmentation
├── Sib_Company_5_Retention_analysis.ipynb # Step 5: Retention tracking
```

---

##  How to Run the Project

1. Clone this repository:
```bash
git clone https://github.com/fatemehmousavibasir1/Sales-Analysis.git
```

2. Install required packages (optional if using JupyterLab/Colab):
```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

3. Start from `Sib_Company_1_preprocessing.ipynb` and run each notebook sequentially.

---
