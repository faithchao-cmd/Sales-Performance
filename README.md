# Simple Sales Dashboard Design

## Description
An interactive sales performance dashboard built in Power BI, showing sales
performance by product, region, and month.

## Objective
Turn cleaned data and KPIs into an interactive view a stakeholder could
actually use — not a static report.

## Tools
- Power BI Desktop
- DAX (Data Analysis Expressions)

## Project Structure
```
Sales-Dashboard/
├── data/
│   └── Sample_Sales_Dataset.xlsx     # source data (480 records)
├── dashboard/
│   └── Sales_Dashboard.pbix           # interactive Power BI dashboard
├── docs/
│   └── Dashboard_Reading_Guide.docx   # one-page guide for stakeholders
└── README.md
```

## Data Overview
480 transaction-level records covering:
- 12 months (Jan–Dec 2024)
- 5 regions: North, South, East, West, Central
- 8 products across 3 categories: Electronics, Furniture, Stationery

A seasonal pattern is present in the data, with a marked sales increase
toward November–December.

## Key Performance Indicators
Built as DAX measures so they recalculate live as slicers are applied:

| Measure | Value |
|---|---|
| Total Revenue | $3.19M |
| Total Profit | $1.27M |
| Total Units Sold | 50K |
| Profit Margin % | `DIVIDE([Total Profit], [Total Revenue], 0)` |

Four KPIs were deliberately chosen (not more), following the principle of
keeping a first dashboard focused rather than overwhelming a viewer with
every available metric.

## Visuals
1. **Profit by Region** (bar chart) — East leads at $280K; South and West
   trail slightly. Spread across regions is narrow (~18% between highest
   and lowest), showing fairly balanced regional performance.
2. **Revenue Trend Over Time** (line chart) — dips in February, flat
   through mid-year, sharp rise October–December, consistent with a
   holiday-season pattern.
3. **Revenue by Product** (ribbon chart) — products ranked highest to
   lowest revenue. Laptop Pro 15 alone contributes ~46% of total product
   revenue, showing heavy concentration in a single item.

## Interactivity
Two slicers — **Region** and **Month** — filter every visual and KPI card
simultaneously, letting a viewer explore the data themselves without
needing a new report built for each question.

## Top Insights
1. **Revenue is heavily concentrated in one product.** Laptop Pro 15
   drives nearly half of total product revenue — a risk worth monitoring
   for any real business.
2. **Sales are strongly seasonal.** Revenue climbs sharply from October
   into December, useful for planning inventory and staffing.
3. **Regional performance is fairly balanced.** Only an 18% spread between
   the strongest and weakest region suggests growth strategies may work
   better applied company-wide rather than targeted at one region.

## How to Open
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. Open `dashboard/Sales_Dashboard.pbix`.
3. Use the Region and Month slicers on the left to filter the view.

