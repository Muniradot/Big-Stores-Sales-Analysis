# Big-Stores-Sales-Analysis
To give a clear and easy-to-understand view of sales across all stores, showing which stores and products perform best, where sales are dropping, and what actions can be taken to improve overall business performance.
# Big Stores Sales & Profit Performance Analytics (2014–2017)

---

## 1. Project Overview

This project delivers an end-to-end Business Intelligence analysis of **Big Stores**, focusing on multi-year **sales and profit performance** across product categories, regions, and sub-categories. The dashboard enables business stakeholders to monitor financial health, identify growth drivers, and detect profitability risks over time.

The analysis spans **four years (2014–2017)** and integrates transactional sales data with product and regional attributes. It provides actionable insights into revenue contribution, profit volatility, and category-level performance patterns, supporting data-driven strategic and operational decisions.

---

## 2. Business Objectives

The analysis addresses the following business objectives:

- Monitor **overall sales and profit trends** over time
- Identify **top-performing product categories**
- Detect **profitability gaps** despite high sales volumes
- Compare **category-level sales vs. profit efficiency**
- Support decisions on **inventory focus, pricing, and category optimization**

Key performance areas monitored:
- Revenue growth
- Profitability
- Category contribution
- Monthly trend stability

---

## 3. Dashboard Preview

![Dashboard Overview](dashboard.png)

The dashboard presents a consolidated view of sales and profit trends, category-level performance, and historical comparisons across multiple years.

---

## 4. Data Sources & Scope

| Aspect | Description |
|------|------------|
| Business Domain | Retail / Big Box Stores |
| Time Range | January 2014 – December 2017 |
| Granularity | Order-level transactional data |
| Geography | Multi-region (Central, East, South, West) |
| Product Coverage | Furniture, Office Supplies, Technology |

### Inferred Tables
- **FactSales**
- **DimDate**
- **DimProduct**
- **DimCategory**
- **DimRegion**

---

## 5. Data Schema & Types

### FactSales Table

| Column Name | Data Type | Example Value | Business Meaning |
|-----------|----------|---------------|------------------|
| Order_Date | Date | 2016-07-15 | Transaction date |
| Sales | Decimal | 1,250.00 | Revenue generated |
| Profit | Decimal | 220.50 | Net profit |
| Category | Text | Technology | Product category |
| Sub_Category | Text | Phones | Product sub-category |
| Region | Text | West | Sales region |

---

## 6. Data Model

**Model Type:** Star Schema  

### Fact Table
- **FactSales**
  - Measures: Total Sales, Total Profit

### Dimension Tables
- **DimDate** → Order Date
- **DimCategory** → Furniture, Office Supplies, Technology
- **DimProduct** → Sub-category level
- **DimRegion** → Central, East, South, West

### Relationships

