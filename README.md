# Tata Motors Financial Analysis – Power BI Dashboard
An interactive Power BI report that analyzes the financial performance of **Tata Motors**. It turns annual profit and loss and balance sheet data into KPI cards, trend charts, composition charts and a decomposition tree, so growth, profitability and balance sheet strength can be understood at a glance.

📄 **[Read the full project report (PDF)](TATA_Motors_Analysis_Report.pdf)**
![Overview Dashboard](images/page1-dashboard.png)
---
## Key Features
- 5-page Power BI report: overview dashboard, data tables, margin analysis, loan-grade chart and decomposition tree
- KPI cards, gauge and combo (column + line) charts for Reserves, Investments and Equity Capital
- Donut, pie and treemap charts for asset composition
- Year slicer for interactive filtering
- Decomposition tree for drill-down analysis
- Custom DAX calculated column and measures for profit margin

## Report Pages
| Page | Content |
|------|---------|
| Page 1 | Main dashboard with combo charts, KPI cards, gauge, donut, pie, treemap, line chart and Year slicer |
| Page 2 | Quarterly results table (Sep 2024, Jun 2025, Sep 2025) |
| Page 3 | Profit margin table and notes on calculated column vs measure |
| Page 4 | Loan amount by loan grade (credit-risk dataset) |
| Page 5 | Decomposition tree |

## Data Model
| Table | Description |
|-------|-------------|
| `final` | Annual profit and loss, Mar 2014 to Mar 2025, plus TTM |
| `Table 8` | Annual balance sheet, Mar 2014 to Mar 2025 |
| `Table 2` | Quarterly results |
| `creditriskdata` | Loan applicant sample (30 rows) |

## DAX Used
**Calculated column**
Rowmargincoloumn = DIVIDE('final'[Net Profit +], 'final'[Sales +])
**Measures**
Total Profit = SUM(Income_Source[Profit_for_the_year_EUR_m])
Total Sales = SUM(Income_Source[Revenues_EUR_m])
RowProfitMargin = DIVIDE([Total Profit], [Total Sales])
A **calculated column** is computed row by row and stored in the model. A **measure** is evaluated at query time and responds to slicers and filters.

## Key Insights
- **Strong growth:** sales grew from Rs. 232,834 crore (FY2014) to Rs. 439,695 crore (FY2025), about **5.9% a year**.
- **Profit recovery:** after losses from FY2019 to FY2022, net profit returned to Rs. 31,807 crore in FY2024 and Rs. 28,149 crore in FY2025.
- **Stable operating margin:** 13% in FY2024 and FY2025, up from 7% to 9% in the weaker years.
- **Lower interest burden:** interest cost fell from Rs. 10,225 crore (FY2023) to Rs. 5,083 crore (FY2025).
- **Leverage:** borrowings to net worth improved to 0.66x in FY2022 and stood at 1.04x in FY2025.
- **Capacity investment:** capital work in progress grew from Rs. 22,046 crore (FY2022) to Rs. 41,622 crore (FY2025).

## Tools Used
- Microsoft Power BI Desktop
- DAX

## How to Open
1. Download `TATA_Motors_Analysis.pbix` from this repository.
2. Open it in **Power BI Desktop** (Windows). The `.pbix` file cannot be opened directly on GitHub.

## Repository Structure
tata-motors-financial-analysis-powerbi/
├── TATA_Motors_Analysis.pbix
├── TATA_Motors_Analysis_Report.pdf
├── README.md
└── images/
    └── page1-dashboard.png
## Author
**Nitin Nayan**
