# Tata Motors Financial Analysis Dashboard | Power BI
This project explores Tata Motors' financial performance using Power BI. It brings together annual financial statements, quarterly results, and balance sheet data to understand how the company's revenue, profitability, investments, and borrowings have changed over time.
The report includes interactive charts, KPI cards, financial tables, and a decomposition tree to make the data easier to explore and understand.

## Dashboard Preview
[View the Overview Dashboard](https://github.com/nitinnayan01-creator/tata-motors-financial-analysis-powerbi/blob/main/images/page1-dashboard.png)
[View the Full Project Report (PDF)](https://github.com/nitinnayan01-creator/tata-motors-financial-analysis-powerbi/blob/main/TATA_Motors_Analysis_Report%20%281%29.pdf)


## Project Overview
The report is designed to answer a few important questions:
- How has Tata Motors' revenue changed over the years?
- How has the company recovered from periods of losses?
- What do profit margins tell us about its financial performance?
- How have investments, reserves, and borrowings changed?
- What does the balance sheet indicate about the company's financial position?

## Dashboard Features
- **Financial overview:** KPI cards and charts summarizing key financial figures.
- **Trend analysis:** Year-wise comparisons of sales, profit, reserves, investments, and equity capital.
- **Profitability analysis:** Profit margin calculations using DAX.
- **Balance sheet analysis:** Visual breakdowns of assets and other financial components.
- **Interactive year filter:** Select a year to explore the available financial data.
- **Decomposition tree:** Drill down into financial figures to understand their contributing factors.
- **Additional analysis:** Quarterly results and a loan-grade visualization included in the report.

## Report Pages
| Page | Description |
|---|---|
| 1. Overview | KPI cards, financial trends, composition charts, and year slicer |
| 2. Quarterly Results | Comparison of selected quarterly financial results |
| 3. Profit Margin | Profit margin calculations and supporting notes |
| 4. Loan Grade Analysis | Loan amount grouped by loan grade |
| 5. Decomposition Tree | Interactive drill-down analysis |

## Data Model
The report contains the following tables:
| Table | Purpose |
|---|---|
| `final` | Annual profit and loss data from March 2014 to March 2025, including TTM data |
| `Table 8` | Annual balance sheet data |
| `Table 2` | Quarterly financial results |
| `creditriskdata` | Sample credit-risk data used for the loan-grade analysis |

## DAX Calculations
### Calculated Column
Rowmargincoloumn =
DIVIDE(
    'final'[Net Profit +],
    'final'[Sales +]
)
### Profit Margin Measure
Total Profit =
SUM('final'[Net Profit +])
Total Sales =
SUM('final'[Sales +])
RowProfitMargin =
DIVIDE(
    [Total Profit],
    [Total Sales]
)
The calculated column stores a result for each row, whereas a measure calculates its result according to the current filter context, including the selected year.

## Key Financial Insights
Based on the figures used in this analysis:
- **Revenue growth:** Sales increased from ₹232,834 crore in FY2014 to ₹439,695 crore in FY2025.
- **Profit recovery:** After reporting losses during FY2019–FY2022, Tata Motors recorded a net profit of ₹31,807 crore in FY2024 and ₹28,149 crore in FY2025.
- **Operating margin:** The reported operating margin was approximately 13% in both FY2024 and FY2025.
- **Interest costs:** Interest expenses declined from ₹10,225 crore in FY2023 to ₹5,083 crore in FY2025.
- **Borrowings:** The borrowings-to-net-worth ratio was reported at 1.04x in FY2025.
- **Capital investment:** Capital work in progress increased from ₹22,046 crore in FY2022 to ₹41,622 crore in FY2025.
These observations describe the figures included in the project and should be checked against the original financial statements before being used in formal reporting.

## Tools Used
- Microsoft Power BI Desktop
- DAX (Data Analysis Expressions)
- Power BI visualizations and interactive slicers

## How to Open the Project
1. Open the repository on GitHub.
2. Download `TATA_Motors_Analysis.pbix`.
3. Open the downloaded file using Power BI Desktop on Windows.
4. Explore the report pages and use the year slicer to filter the available data.
The `.pbix` file is intended for use with Power BI Desktop. The dashboard image and PDF provide static previews for anyone who cannot open the report interactively.

## Repository Structure
tata-motors-financial-analysis-powerbi/
├── TATA_Motors_Analysis.pbix
├── TATA_Motors_Analysis_Report(1).pdf
├── README.md
└── images/
    └── page1-dashboard.png
    
## Author
**Nitin Nayan**
