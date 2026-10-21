# Executive-Sales-Dashboard-
Interactive Power BI executive sales dashboard for tracking revenue, profit, orders, quantity, sales channels, product categories, and country performance.

# Power BI Executive Sales Dashboard

An interactive Power BI dashboard for exploring sales performance across time, products, countries, and sales channels.

## Dashboard Preview

The dashboard presents key sales KPIs and breakdowns in one executive view. Add a screenshot of your dashboard to this repository and update the path below:

![Executive Sales Dashboard](<Dashboard Image.png>)

## Key Metrics

- **Total Revenue:** 645.22K
- **Total Gross Profit:** 296.38K
- **Gross Margin:** 45.94%
- **Total Orders:** 2,707
- **Total Quantity Sold:** 6,698

*Figures shown are from the dashboard preview provided with this project.*

## Dashboard Features

- KPI cards for revenue, gross profit, gross margin, orders, and quantity
- Month-wise revenue and profit comparison
- Revenue by product category
- Revenue comparison by sales channel
- Top and bottom countries by revenue
- Slicers for quarter, month, product category, and country

## DAX Measures

```dax
Total Revenue =
SUM(Sales_Data[Revenue])

Total Gross Profit =
SUM(Sales_Data[Gross Profit])

Gross Margin =
DIVIDE([Total Gross Profit], [Total Revenue])

Total Quantity =
SUM(Sales_Data[Units Sold])

Total Orders =
DISTINCTCOUNT(Sales_Data[ID])
```

## Calculated Columns

### Date Table Columns

```dax
Year = YEAR(Date_Table[Date])
```

```dax
Quarter = "Q" & QUARTER(Date_Table[Date])
```

```dax
Month_Number = MONTH(Date_Table[Date])
```

```dax
Month_Name = FORMAT(Date_Table[Date], "MMMM")
```

```dax
Day_Name = FORMAT(Date_Table[Date], "DDDD")
```
## Tools Used

- Microsoft Power BI Desktop
- DAX (Data Analysis Expressions)
- GitHub

## Project Files

- `Power BI Executive Sales Dashboard Project.pdf` — dashboard preview
- `Calculated Column.xlsx` — calculated column formulas
- `Measure Dax.xlsx` — DAX measure formulas




