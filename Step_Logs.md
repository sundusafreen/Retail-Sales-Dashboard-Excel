
# 📘 Step Logs – Retail Sales Insights Excel Project by Sundus Afreen

This document summarizes all the major steps taken during the Excel project, including data preparation, enrichment, and analysis.

---

## ✅ Step 1: Dataset Understanding & Initial Review

**Sheets Reviewed:**
- `Sales_Data`
- `Customer_Info`
- `Product_Info`

**Checklist Covered:**
- Checked for missing values and incorrect formats
- Ensured discount values are between 0 and 0.5
- Verified uniqueness of IDs (Customer and Product)
- Noted all issues and observations in `Step_1_Checklist`

---

## ✅ Step 2: Data Cleaning

**Actions Taken:**
| Column            | Issue Identified             | Action Taken            |
|------------------|------------------------------|--------------------------|
| Order Date        | Format inconsistencies        | Standardized to date format |
| Discount (%)      | Out-of-range values (>0.5)    | Corrected to 0.5 max    |
| Customer ID       | Possible duplicates           | Reviewed & resolved     |
| Unit Price        | Some values = 0               | Replaced with minimum valid values |

Logged in: `Cleaned_Data_Log`

---

## ✅ Step 3: Data Enrichment using XLOOKUP

**Fields Added to Sales_Data:**
| Source Sheet   | Lookup Key     | Fields Added                         |
|----------------|----------------|--------------------------------------|
| Customer_Info  | Customer ID    | Name, Age Group, Gender, Location    |
| Product_Info   | Product ID     | Product Name, Supplier Name          |

Logged in: `Lookup_Log`

---

## ✅ Step 4: Calculated KPIs

**Formulas Created in Sales_Data:**
- `Revenue = Quantity * Unit Price`
- `Profit Margin (%) = Profit / Revenue`
- `Discounted Unit Price = Unit Price * (1 - Discount)`
- `Profit Category = IF(Profit > 500, "High", ...)`

Purpose: To prepare data for PivotTable analysis and KPIs

---

## ✅ Step 5: PivotTable Analysis

Key analyses created:
- Monthly Sales Trend
- Revenue & Profit by Region
- Top 10 Products by Revenue
- Profit by Customer Age Group
- Discount Impact on Profitability

Logged in: `Pivot_Analysis` (and visuals in `Dashboard`)

---

## ✅ Step 6: Dashboard

Interactive dashboard built with:
- KPI cards (Revenue, Profit, Avg. Margin, Orders)
- Slicers: Region, Category, Age Group
- Charts: Line, Column, Bar, Pie

Sheet: `Dashboard`

---

## 🧠 Step 7: Business Insights Summary

7 Key insights noted from the data, e.g.:
- "West region generated highest Q1 revenue"
- "High discounts (>30%) reduce profit sharply"

Logged in: `Insights` sheet

---
