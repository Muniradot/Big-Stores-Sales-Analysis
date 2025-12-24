
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



## . Data Sources & Scope

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

- Cardinality: One-to-Many
- Filter Direction: Single (Dimensions → Fact)
- Referential integrity enforced

---

## 7. Data Preparation & Transformation

### Data Cleaning
- Standardized category and sub-category naming
- Removed duplicate order records
- Handled negative profit values explicitly

### Transformations
- Extracted Month and Year from Order Date
- Created Year-Month hierarchy for trend analysis

### Calculations
- **Measures (DAX):**
  - Total Sales
  - Total Profit
- **Calculated Columns:**
  - Order Year
  - Order Month

---

## 8. Metrics & KPIs

| Metric | Definition | Calculation Logic | Example Value | Visual |
|------|-----------|------------------|--------------|--------|
| Total Sales | Total revenue generated | SUM(Sales) | $2.297M | KPI Card |
| Total Profit | Net profit | SUM(Profit) | $286K | KPI Card |
| Technology Sales | Sales from Technology | Category filter | $836K | Bar Chart |
| Furniture Sales | Sales from Furniture | Category filter | $742K | Bar Chart |
| Office Supplies Sales | Sales from Office Supplies | Category filter | $719K | Bar Chart |

---

## 9. Dashboard Analysis

### Sales History (Line Chart)
- Visual Type: Line Chart
- Metric: Monthly Sales
- Timeframe: 2014–2017
- Observation: Sales peak above **$140K/month** during high-performing periods

### Profit History (Line Chart)
- Visual Type: Line Chart
- Metric: Monthly Profit
- Observation: Profit volatility with multiple negative profit months (as low as **–$5K**)

### Sales & Profit by Category (Clustered Bar)
- Technology: **$836K Sales**
- Furniture: **$742K Sales**
- Office Supplies: **$719K Sales**
- Profit margins vary significantly across categories

---

## 10. Key Insights

1. **Technology generates the highest sales at $836K**, accounting for ~36% of total revenue.
2. **Total sales reached $2.297M**, while profit remained relatively low at **$286K**, indicating margin pressure.
3. **Furniture shows high sales ($742K)** but inconsistent profit performance.
4. Several months recorded **negative profit despite stable sales**, suggesting discounting or cost overruns.
5. Sales trends show **seasonal spikes**, particularly mid-year.
6. Office Supplies maintain **steady but lower-margin performance**.
7. Profit growth does not scale proportionally with sales growth.
8. Technology category demonstrates the **best sales-to-profit efficiency**.

---

## 11. Recommendations

1. **Optimize pricing strategies** in Furniture to address profit leakage.
2. Prioritize **Technology category expansion**, given strong revenue contribution.
3. Conduct **cost audits during negative profit months**.
4. Improve **inventory planning around seasonal peaks**.
5. Introduce **profit-based KPIs** alongside sales targets.

---

## 12. Data Quality & Validation

- Cross-validated sales totals against category subtotals
- Confirmed profit aggregation logic across visuals
- Tested slicer interactions (Year, Region, Category)
- Ensured consistent totals across filtered views
- Optimized measures to avoid row-level calculations

---

## 13. Tools & Technologies

| Component | Tool |
|---------|------|
| Visualization | Power BI |
| Data Transformation | Power Query |
| Modeling | Star Schema |
| Analytical Language | DAX |
| File Format | PBIX |

---

## 14. Limitations & Assumptions

- Cost structure details not available
- Customer-level segmentation excluded
- Profit assumed net of standard operating costs
- No external market or competitor data included

---

## 15. Conclusion

This analytics project delivers a comprehensive view of Big Stores’ financial performance, highlighting revenue drivers, profitability risks, and category-level efficiency. The dashboard equips stakeholders with clear, actionable insights to improve margin management, optimize product focus, and strengthen financial decision-making.

---

## 16. Future Enhancements

- Add **customer segmentation analysis**
- Introduce **profit margin and ROI metrics**
- Implement **forecasting and trend projections**
- Drill-down analysis at **sub-category and product SKU level**
- Integrate **inventory and cost data** for deeper margin insights

---

**Project Type:** Business Intelligence & Sales Analytics  
**Use Case:** Portfolio, Academic Review, Executive Presentation

