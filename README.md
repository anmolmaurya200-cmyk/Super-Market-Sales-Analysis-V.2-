# Supermarket Sales Analysis Dashboard (Excel)

An interactive Excel dashboard that helps supermarket management review sales performance across product categories and outlets. It was built as a project for the **Sapphire IQ Data Analytics Internship**.

## Business Problem
Management had sales data only as a raw dataset, which made it hard to identify top-performing products, compare outlets, and see sales patterns. This project turns that data into a single dashboard with metrics, comparisons, and statistical insights.

## Dataset
- **Source:** BlinkIT Grocery Data
- **Size:** 8,523 records (each row is one item in one outlet)
- **Key fields:** Item Type, Item Fat Content, Item Visibility, Outlet Type, Outlet Location Type, Outlet Size, Sales, Rating

## Objectives
1. **Overall sales performance:** total sales, average sales per record, average item visibility
2. **Category and sales comparison:** top 4 category contribution, highest and lowest categories, sales by outlet type
3. **Outlet performance and relationships:** Low Fat vs Regular sales by outlet, visibility vs sales, category mix by outlet type
4. **Statistical analysis:** mean, median, min, max, standard deviation, outliers, and average sales by category, outlet type, and location

## Key Findings
- **Total sales:** 1,201,681, averaging 140.99 per record
- **Top 4 categories** (Fruits and Vegetables, Snack Foods, Household, Frozen Foods) generate **50.6%** of sales
- **Highest category:** Fruits and Vegetables (178,124). **Lowest:** Seafood (9,078)
- **Outlets:** Supermarket Type1 contributes **65.5%** of sales and Type3 the lowest at 10.9%. Average sales per record are nearly identical across outlet types (139.80 to 141.68)
- **Visibility vs sales:** correlation r = **-0.001**, so there is essentially no relationship in this data
- **Fat content:** Low Fat items make up 64.6% of sales and Regular items 35.4%
- **Variation:** sales range from 31.29 to 266.89 (median 143.01, std dev 62.28). No IQR outliers, and 14 records fall beyond 2 SD

## Dashboard Features
- Dropdown filters for Outlet Type, Outlet Location, and Item Fat Content
- KPI cards and auto-updating key takeaways
- Category performance and visibility-vs-sales charts
- Statistical summary panel (quartiles, coefficient of variation, IQR fences, correlation)
- Outlet comparison and category contribution by outlet type
- Top and bottom sales records

## Data Cleaning and Assumptions
- **Fat content:** the raw column had 5 spellings (Low Fat, LF, low fat, Regular, reg). I standardised them into a new clean column to get Low Fat / Regular.
- **Zero visibility:** 526 records have zero visibility. I kept them as recorded and show them as their own band in the visibility analysis.
- **Missing weights:** 1,463 blank Item Weight values were left as is, since weight isn't needed for any objective.
- **Outliers:** IQR rule (primary) and z-score threshold (secondary), both with editable parameters.
- The dataset has no currency or date field, so sales are shown as plain numbers and no time trend is possible.

## Workbook Structure
| Sheet | Purpose |
|---|---|
| Dashboard | Management view with filters, KPIs, charts, takeaways |
| Analysis | All calculations, organised by Objectives 1 to 4 |
| Notes | How to use, assumptions, and data quality notes |
| BlinkIT Grocery Data | Source data plus one cleaned column |

## Tools
Microsoft Excel: formulas (SUMIFS, SUMPRODUCT, QUARTILE, CORREL), data validation dropdowns, and charts.

## Files
- `Supermarket_Sales_Analysis_Dashboard(V.2).xlsx`: the dashboard workbook
- `Sapphire IQ Supermarket Sales Analysis(V.2) (1).pdf`: the project brief

## Author
**Anmol Kumar**, Data Analyst
[LinkedIn](https://www.linkedin.com/in/anmol-kumar-245493425) | [Portfolio](https://anmolswebiste.lovable.app)
