# Project 2: Sales Data Analysis Dashboard (Power BI)

Interactive Power BI report analysing 4 years of retail sales (Jan 2020 – Dec 2023) across Indian cities, 30 products, 50 customers and 5 promotion campaigns.

![Sales Trend Dashboard](images/sales-trend.png)

## Business Questions
- How have sales trended over time, and when did they peak?
- Which products drive sales, profit and volume, and which lag?
- Which promotions give the deepest discounts?
- How does one date range compare against another?

## Dataset
`Store_Data.xlsx` – star-schema style model:
| Table | Content |
|---|---|
| Sheet3 (fact) | 3,510 transactions: date, customer, promotion, product, units sold |
| Dim Customers | 50 customers with city and state |
| Dim Product | 30 products across 8 product lines, with unit price (INR) |
| Dim Promotion | 5 campaigns with ad type, coupon code, price-reduction type |

Total Sales, Discount and Net Sales are calculated in Power BI (price × units, discount %, net of discount).

## Dashboard Pages
1. **Sales Trend** – daily sales line (2020–2024), sales by city map, number of orders, average discount by promotion, profit vs net sales.
2. **Product Performance** – top and bottom 5 products by sales, quantity and profit.
3. **Period Comparison** – Total Sales, Profit and Units Sold for two independent date filters.
4. **Transaction Detail** – drill-through table with slicers for date, customer, product and promotion.

## Key Insights
- **Overall:** 122M total sales, 12.2M profit and 7.1K units sold across 3.51K orders.
- **Product concentration:** the top 5 products (all high-ticket electronics) generate about 90M, roughly 74% of total sales.
- **Apple iPhone 14** leads on sales (21.4M), profit (2.14M) and units sold (281).
- **Low performers:** the bottom 5 products (personal care and kitchenware) each sell under 0.3M; Colgate Toothpaste is lowest at 0.02M.
- **Promotions:** Weekend Flash Sale (23K) and Clearance Sale (18K) carry the highest average discounts; Festive Diwali is close to zero.
- **Peak sales:** the highest single-day sales reach about 0.65M (late 2022), with recurring spikes of 0.4–0.55M each year.
- **Profit** scales linearly with net sales (about a 10% margin), so profit varies only with sales volume in this dataset.

## Tools
Power BI Desktop · DAX · Power Query · Excel

## Files
- `Sales_Data_Report.pbix` – Power BI report
- `Sales_Data_Report.pdf` – exported dashboard
- `Store_Data.xlsx` – source data

## Note
Sample/practice dataset, built to demonstrate data modelling, DAX and dashboard design.
