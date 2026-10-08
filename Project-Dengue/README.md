# Project 1: Dengue Cases & Medicine Sales Dashboard (Power BI)

Two-page Power BI report that combines dengue case tracking from two sources with dengue medicine sales across countries, using a fiscal year (April–March). Built from a written business requirement: every slicer, interaction, bookmark and navigation button follows the spec.

![Dengue Cases in the World](images/dengue-report.png)
![Medicine Sales for Dengue Disease](images/medicine-sales.png)

## Business Questions
- How many dengue cases, active (hospitalised) cases, critical cases and deaths are there, month-to-date, year-to-date and since inception?
- How do cases split by gender and country?
- How do cases build up month by month over the fiscal year?
- Which medicines and countries generate the most sales, and how do sales change by fiscal month?

## Dataset
`Dengue_cases_in_the_WORLD_-_Project_Dataset.xlsx`

| Sheet | Content |
|---|---|
| Source 1 | Monthly aggregated dengue cases by area, country and gender |
| Source 2 | 318 patient-level case records (Jan 2022 – Jun 2023) |
| Medicine Sales | Daily medicine sales records for 5 products across 20 countries |

## Report Pages
**Page 1: Dengue Cases in the World**
- Dropdown slicers: Area, Country, Year (calendar), Fiscal Year, Source
- KPI cards: Total, Active, Critical and Death cases, driven by an MTD / YTD / Inception tile slicer
- Donut chart: gender share of total cases
- Treemap: top 6 countries by total cases
- Clustered column chart: Monthly and Cumulative cases by fiscal month, switched with two bookmark buttons
- "Go to Medicine Report" navigation button

**Page 2: Medicine Sales for Dengue Disease**
- Dropdown slicers: Area, Country, Year, Fiscal Year, Brand
- Clustered bar chart: sales by product
- Line chart: sales by fiscal month
- Clustered column chart: sales by country, with USA, India, China, Russia, Mexico and Philippines shown separately and the rest grouped as "Other"
- "Back to Report" navigation button

## Key Features
- **Source switch:** selecting Source 1 or Source 2 changes every case measure to show only that source.
- **Single select** on Year and Fiscal Year; Area, Country, Year and Fiscal Year are **synced** across both pages.
- **Controlled interactions:** cards ignore the Year and Fiscal Year slicers, the treemap ignores Area and Country, the column charts and Page 2 line chart ignore the Year slicer, and the time tile slicer affects only the cards.
- **Time intelligence:** MTD, YTD and Inception use a fiscal year ending 31 March, anchored on the latest date that has data.
- **Bookmarks:** two rounded buttons toggle Monthly and Cumulative views.
- **Country groups:** created with Power BI's grouping feature.

## Key Insights
Insights below come from the exported report with Source 1, Year 2023 and FY 22-23 selected.
- **Cumulative cases (Source 1)** grow from 1.1K in April to 10.3K by March.
- **Gender split:** Female 563 (34.1%), Male 563 (34.1%) and Others 523 (31.7%), so cases are spread almost evenly.
- **Top countries by cases:** Australia, Kenya, USA, Brazil, Chile and Mexico.
- **Medicine sales by product:** Product A leads with 48M (about 43% of the 112M shown), followed by EA (27M), B (17M), C (15M) and D (5M).
- **Sales by fiscal month (FY 22-23):** sales range from 31.4M in July to a peak of 49.3M in June.
- **Sales by country:** Mexico (14M) and India (12M) lead the named countries, while the grouped "Other" countries total 61M.
- **Source 2 (patient records):** 318 cases in total, with the largest monthly counts in Apr–Jun 2023 (38, 36 and 46).

## Tools
Power BI Desktop · DAX · Power Query · Excel

## Files
- `Dengue_Data_Report.pbix`: Power BI report
- `Dengue_Data_Report.pdf`: exported dashboard
- `Dengue_cases_in_the_WORLD_-_Project_Dataset.xlsx`: source data
- `Business_Requirement.txt`: requirement specification

## Note
Sample/practice dataset built to demonstrate data modelling, DAX and dashboard design. Not real clinical or epidemiological data.
