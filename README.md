# AtliQ Hardwares - Sales Analytics Report (Excel)

A comprehensive sales analytics project built in Microsoft Excel for **AtliQ Hardwares**, a fictional consumer electronics hardware company. The workbook consolidates sales, P&L, market performance, and product data across fiscal years 2019-2021 using Power Query, Power Pivot, and DAX-based pivot tables.

---

## Project Objective

The goal of this project is to empower business stakeholders with clear, data-driven answers to key questions:

- Which customers are growing fastest, and by how much?
- Are we hitting our market targets - and where are we falling short?
- How is gross margin trending across fiscal years and quarters?
- Which products and divisions are driving revenue growth?
- What new products launched in 2021, and how did they perform?

---

## Repository Structure

```
AtliQ_Hardwares_Sales_Report/
│
├── AtliQ_Hardwares_Sales_Report.xlsx   # Main workbook with all pivot tables & data model
│
└── Reports/                            # PDF exports of each report
    ├── Customer_net_sales.pdf
    ├── Division_report.pdf
    ├── Market_performance.pdf
    ├── New_products_2021.pdf
    ├── Top_5_Bottom_5_Products.pdf
    ├── Top_5_Countries.pdf
    └── Top_10_Products.pdf
```

---

## Reports Included

### 1. Customer Net Sales Performance
Tracks net sales (USD) for 16 customers across FY2019, FY2020, and FY2021, with a Year-over-Year (YoY) % growth column. Filtered by region, market (defaulted to India), and division.

**Key Insight:** AtliQ Exclusive grew **~293%** YoY from 2020→2021, the highest among all customers. Amazon remains the highest revenue contributor at **$22.96M** in FY2021.

---

### 2. Market Performance vs. Target
Compares FY2021 actual net sales against targets for **23 countries**, showing the absolute gap and % miss.

**Key Insight:** All markets missed their FY2021 targets. Poland had the largest shortfall at **-18.1%**, while Portugal came closest at **-4.3%**. Grand total net sales reached **$598.9M** against a target gap of **-$54.9M (-9.2%)**.

---

### 3. P&L by Fiscal Years
Monthly and quarterly breakdown of **Net Sales, COGS, Gross Margin, and GM%** across FY2019, FY2020, and FY2021, with YoY net sales comparison ratios (21 vs 20, 20 vs 19).

| Fiscal Year | Net Sales | Gross Margin | GM% |
|-------------|-----------|--------------|-----|
| FY2019 | $87.5M | $36.2M | 41.4% |
| FY2020 | $196.7M | $73.3M | 37.3% |
| FY2021 | $598.9M | $218.2M | 36.4% |

**Key Insight:** Revenue grew **~204% from FY2019 to FY2021**, but GM% compressed by ~5 percentage points, indicating rising cost pressure.

---

### 4. Top 10 Products
Ranks the 10 best-performing products by net sales in FY2021, with FY2020 baseline and YoY growth %.

**Key Insight:** **AQ Mx NB** had the highest YoY growth at **5,523%** (from $25K to $1.44M). **AQ Electron 4 3600 Desktop Processor** was the top revenue product at **$19.4M**.

---

### 5. Division Report
Summarizes FY2020 vs FY2021 net sales and YoY growth by division — N & S (Networking & Storage), P & A (Peripherals & Accessories), and PC.

| Division | FY2021 Sales | YoY Growth |
|----------|-------------|------------|
| PC | $165.8M | +314% |
| P & A | $338.4M | +221% |
| N & S | $94.7M | +84% |

---

### 6. Top 5 & Bottom 5 Products
Highlights the five highest and five lowest performing products by net sales quantity — useful for inventory and portfolio decisions.

---

### 7. New Products 2021
Lists 16 products launched for the first time in FY2021 (zero FY2020 revenue), with their FY2021 net sales. Combined, they generated **$176.2M**, representing a significant share of FY2021 revenue.

**Key Insight:** **AQ Qwerty** was the top new launch at **$21.98M**.

---

### 8. Top 5 Countries 2021
Ranks the top 5 markets by FY2021 net sales revenue.

---

## Tools & Techniques Used

| Tool / Feature | Purpose |
|---|---|
| **Power Query (M)** | Data ingestion, transformation, and cleaning from raw source tables |
| **Power Pivot / Data Model** | Building relationships between fact and dimension tables |
| **DAX Measures** | Calculated metrics — Net Sales, COGS, Gross Margin, GM%, YoY % |
| **Pivot Tables** | Dynamic report slicing by region, market, division, customer |
| **Conditional Formatting** | Visual highlighting of growth rates and performance gaps |

---

## Data Model Overview

The workbook uses a **Star Schema** design:

- **Fact Table:** `fact_sales_monthly` — transaction-level sales data
- **Dimension Tables:** `dim_customer`, `dim_product`, `dim_market`, `dim_date`

Relationships are managed in the Power Pivot data model, enabling cross-table DAX calculations and consistent slicer behaviour across all pivot reports.

---

## How to Use

1. **Download** `AtliQ_Hardwares_Sales_Report.xlsx` and open in **Microsoft Excel 2016 or later** (Power Pivot required).
2. Use the **slicer filters** (Region, Market, Division, Customer) on each sheet to drill into specific segments.
3. The **P&L sheet** contains separate pivot tables per fiscal year — scroll down to see FY2019, FY2020, and FY2021 side by side.
4. PDF exports of each report are available in the `Reports/` folder for quick reference without Excel.

---

## Key Business Questions Answered

| Business Question | Report |
|---|---|
| Which customers grew the most in FY2021? | Customer Net Sales Performance |
| Did we achieve our sales targets by country? | Market Performance vs. Target |
| How is profitability trending over time? | P&L by Fiscal Years |
| Which products should we prioritize or discontinue? | Top 10 / Top 5 & Bottom 5 Products |
| How did our new product launches perform? | New Products 2021 |
| Which divisions are growing fastest? | Division Report |
| Which geographies are our biggest markets? | Top 5 Countries 2021 |

---

## Contact

Built by **Aniruddh Galande** | [LinkedIn](linkedin.com/in/aniruddhgalande) | [GitHub](https://github.com/Aniruddh4980)

> *This project is part of a data analytics portfolio. All data is fictional and used solely for learning purposes.*
