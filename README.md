# mobile_sales_dashboard
sales analysis on mobile brands
# 📱 Mobile Brand Sales Dashboard (Power BI)

## Overview
This project is a **Power BI dashboard** (`mobile__sales_dashboard.pbix`) built to analyze the sales performance of mobile phone brands. It brings together sales volume, revenue, pricing, payment behavior, and customer ratings into a single interactive report, helping stakeholders understand not just *how much* is being sold, but *why* certain brands and models are underperforming — particularly around affordability.

## Dashboard Contents
The report is built on a single `Sales_data` table and includes the following visuals:

| Visual | Purpose |
|---|---|
| KPI Cards | Total Sales, Total Quantity, Transactions, Average Price |
| Map (by City) | Geographic distribution of total sales |
| Line Chart | Total quantity sold by Month / Day (trend over time) |
| Area Chart | Total sales by Day Name (day-wise sales pattern) |
| Clustered Bar Chart | Total sales by Mobile Model (top-performing models) |
| Pie Chart | Transactions split by Payment Method |
| Funnel Chart | Customer Ratings distribution |
| Table | Brand-wise summary — Total Quantity, Transactions, Total Sales |
| Slicers | Mobile Model, Payment Method, Brand, Day Name |

## Problem Statements
This dashboard was built to answer the following business questions:

1. **What are the total sales of each mobile brand?** — comparing revenue and quantity sold across brands.
2. **How do sales vary day-wise?** — identifying which days generate the highest/lowest sales.
3. **What payment methods do customers prefer?** — understanding the split between Cash, Card, UPI, EMI, etc.
4. **What is the average price customers can actually afford?** — benchmarking real customer spending capacity.
5. **What is the average price of each brand's phones?** — comparing brand pricing against customer affordability.

Together, these questions surface a core insight: **there is a gap between what brands price their phones at and what the average customer is willing/able to pay**, which directly impacts sales volume for premium models.

## Key Insight
By comparing the **Average Price customers can afford** against the **Average Price per brand**, the dashboard reveals that many mobile models are priced above the affordability threshold of the majority of customers — leading to lower transaction volumes for higher-end models despite strong demand for the brand overall.

## Proposed Solutions
Based on the affordability gap identified above, the following actions are recommended:

- **Reprice / tier the portfolio** — brands are pricing phones out of reach for a large customer segment; introducing more accessible price points can capture lost demand.
- **Offer EMI options on expensive phones** — enabling installment-based payment for high-value models to make them accessible without changing the sticker price.
- **Improve features at existing price points** — enhancing value-for-money on mid-range phones to justify pricing and improve customer ratings.
- **Support all payment methods** — ensuring every mobile phone/model can be purchased via all available payment modes (Cash, Card, UPI, Net Banking, EMI, Wallets) to remove friction at checkout and avoid losing sales due to limited payment options.

## How to Use
1. Open `mobile__sales_dashboard.pbix` in **Power BI Desktop**.
2. Use the slicers (Mobile Model, Payment Method, Brand, Day Name) at the top of the report to filter the view.
3. Review the KPI cards for a quick summary, then drill into the Brand table, Model bar chart, and Payment Method pie chart for deeper analysis.
4. Use the Day-wise area/line charts to spot demand patterns and plan promotions/EMI offers around low-sales days.

## Tech Stack
- **Power BI Desktop** (.pbix)
- Data model: `Sales_data` table with fields including Date, City, Brand, Mobile Model, Payment Method, Customer Ratings, Total_Sales, Total_Quantity, Transactions, Avg_price
- **DAX** for all calculated measures

## DAX Functions Used
The measures powering the KPI cards, charts, and table (Total_Sales, Total_Quantity, Transactions, Avg_price, etc.) were built using:

| Function | Used For |
|---|---|
| `SUM` | Aggregating base numeric columns (e.g., total sales value, total quantity sold) |
| `SUMX` | Row-by-row calculations aggregated across the table (e.g., quantity × price to get total sales/revenue) |
| `AVERAGE` | Calculating average price/rating measures (e.g., Avg_price, average customer rating) |
| `DATEDIFF` | Date-based calculations such as day gaps/time-based comparisons for day-wise and trend analysis |

These measures feed directly into the KPI cards, the line/area charts (day- and month-wise trends), the brand/model comparisons, and the affordability vs. brand-price analysis described above.

## Suggested Next Steps
- Add a dedicated **Affordability vs Brand Price** comparison visual (e.g., a scatter or combo chart) to make the core insight explicit on the dashboard itself.
- Add an **EMI adoption tracker** once EMI options are rolled out, to measure impact on sales of expensive models.
- Add **Customer Rating vs Price** analysis to validate whether "improve features" is closing the value gap over time.
