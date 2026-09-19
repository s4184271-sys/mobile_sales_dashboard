# Mobile Brand Sales Dashboard — Power BI

An interactive Power BI dashboard analyzing mobile phone sales, pricing, payment behavior, customer ratings, and brand/model performance.

## Business Questions

1. What are the total sales and quantities for each mobile brand?
2. How do sales vary across days and months?
3. Which payment methods do customers use most?
4. What is the average price customers are paying?
5. How does the average price of each brand compare with customer affordability?
6. Which brands or models show a potential affordability gap?

## Solution

The dashboard combines KPI cards, geographic analysis, time trends, brand/model comparisons, payment-method analysis, customer-rating distribution, and interactive slicers.

### Dashboard Components

| Visual | Purpose |
|---|---|
| KPI Cards | Total Sales, Total Quantity, Transactions, Average Price |
| City Map | Geographic distribution of sales |
| Line Chart | Quantity trends by month/day |
| Area Chart | Day-wise sales pattern |
| Bar Chart | Sales by mobile model |
| Pie Chart | Transactions by payment method |
| Funnel | Customer rating distribution |
| Brand Table | Brand-wise quantity, transactions, and sales |
| Slicers | Brand, Model, Payment Method, Day |

## Key Analysis

A central analysis compares **customer affordability** with the **average price of phones by brand**. This helps identify potential pricing gaps that may affect the sales volume of higher-priced models.

The dashboard can therefore be used to investigate:
- More accessible price tiers
- EMI/payment options
- Value-for-money improvements
- Payment-method availability

These are analytical considerations based on the dashboard results, not claims about actual pricing strategy decisions by the brands.

## How to Use

1. Open `mobile_ sales_dashboard.pbix` in Power BI Desktop.
2. Use the slicers to filter the report.
3. Review the KPI cards for an overview.
4. Compare brands and models using the charts and table.
5. Explore payment behavior and day-wise trends.

## Data Model

The report uses a `Sales_data` table containing fields such as Date, City, Brand, Mobile Model, Payment Method, Customer Ratings, Total Sales, Total Quantity, Transactions, and Average Price.

## DAX

Measures were created using functions including `SUM`, `SUMX`, `AVERAGE`, and `DATEDIFF`.

## Tools

**Power BI Desktop · DAX**

## Suggested Future Analysis

- Add a dedicated affordability-vs-price visual
- Track EMI adoption if additional payment data becomes available
- Analyze customer rating against phone price
