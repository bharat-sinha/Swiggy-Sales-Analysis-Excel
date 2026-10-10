# Swiggy Food Delivery Sales Dashboard (Excel)

![Swiggy sales dashboard](Swiggy%20Dashboard.png)

An interactive Excel dashboard that shows where a food delivery business earns its revenue, when demand rises and falls, and how sales spread across cities, food categories and restaurants. It covers about ₹53M in revenue across roughly 197K orders.

**Tools:** Excel (Power Query, PivotTables, PivotCharts, slicers)
**Domain:** Food delivery, e-commerce analytics

---

## Business problem

A food delivery platform depends on a few cities and categories for most of its revenue, and its demand moves with the day of the week and the season. Management needs to see where revenue is concentrated, when demand drops, and which regions and categories to prioritize.

## Questions the dashboard answers

1. How much revenue and how many orders do we have, and what is the average order value?
2. How does demand change across days, weeks, months and quarters?
3. Which cities and states contribute the most revenue?
4. Which food categories lead, and how much does revenue depend on one of them?
5. How satisfied are customers (average rating)?
6. How do restaurants compare within a filtered view?

## Dataset

- **Source:** Swiggy raw data (a public practice dataset, included as `Swiggy Raw Data Excel.xlsx`)
- **Size:** about 197K orders
- **Main fields:** order date, state, city, restaurant, food category, dish, price, rating
- **Note:** this is a sample dataset, not data from the real company.

## Approach

1. **Clean** the raw data in Power Query: fix data types, handle blanks, standardize labels, create date fields (day, week, month, quarter).
2. **Define the metrics** (see below) so each number has one clear meaning.
3. **Analyze** with PivotTables for time trends, geography, category and ratings.
4. **Visualize** with PivotCharts and KPI cards on one dashboard sheet, with slicers for month, category and restaurant.

## Metric definitions

| Metric | Definition |
|---|---|
| Revenue | Sum of order values (about ₹53M) |
| Orders | Number of order records (about 197K) |
| Average order value (AOV) | Revenue ÷ orders (about ₹268) |
| Average rating | Mean of the rating field (4.34) |

## Key findings

| Area | Finding |
|---|---|
| Scale | About ₹53M revenue from about 197K orders, average order value about ₹268 |
| Weekly pattern | Weekend demand spikes above a steady weekday baseline |
| Category | Veg food accounts for about 63% of revenue |
| Geography | Revenue is concentrated in the top metro cities |
| Seasonality | Orders fall by about 33% in Q3, while average ratings stay stable |
| Satisfaction | Average rating 4.34 |

Read these as patterns in the sample data, not as proven causes.

## Recommendations

These are hypotheses for a business team to test, based on what the dashboard shows.

1. **Investigate the Q3 drop before acting on it.** First confirm the data covers all of Q3 and is complete. Then break the drop down by city, category and week to see where it comes from.
2. **Test weekday promotions.** Weekends carry the peaks, so a small weekday offer in selected cities is a low-risk experiment.
3. **Treat metro concentration as a risk, not yet an opportunity.** Revenue sitting in a few cities shows dependence. To judge Tier-2 potential, look at order growth rates and not just revenue share.
4. **Check the veg share by city and restaurant.** A 63% share may be higher or lower in places, and the pattern would guide menu and restaurant partnerships.
5. **Resolve the rating data issue.** Ratings and orders are recorded at different levels, so rating comparisons across segments need care.

## Limitations

- The dataset has no cost, margin or delivery data, so I can describe revenue but not profitability.
- There are no customer IDs, so repeat-purchase behavior can't be measured.
- Ratings and orders differ in granularity, which limits how far rating trends can be trusted.
- The cause of the Q3 drop is unknown from this data.
- The data is a sample covering a limited period.

## Next steps

- Break down the Q3 decline by city, category and week.
- Add growth rates by city to compare metro and Tier-2 potential.
- Add margin and repeat-customer metrics if the data allows.
- Rebuild the dashboard in Power BI and compare it with this Excel version.

## Repository contents

```
├── Swiggy Raw Data Excel.xlsx       # raw dataset
├── pivot + dashboard swiggy.xlsx    # PivotTables and dashboard
├── Swiggy Dashboard.png             # dashboard screenshot
├── swiggy analysis.pdf              # exported report
└── README.md
```

**To explore:** download `pivot + dashboard swiggy.xlsx`, open it in Excel, and use the slicers on the dashboard sheet to filter by month, category and restaurant.

## Skills demonstrated

Data cleaning (Power Query) · PivotTables and PivotCharts · KPI and metric definition · Time-series analysis · Dashboard design with slicers · Turning findings into recommendations

## Author

**Bharat Sinha**, aspiring data analyst
[LinkedIn](https://www.linkedin.com/in/bharat-sinha-122791130/) | [GitHub](https://github.com/bharat-sinha) | sinha.bharat8@gmail.com
