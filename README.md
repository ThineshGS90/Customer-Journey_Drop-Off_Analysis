🧭 Customer Journey Funnel & Drop-off Analysis

This project explores user behavior across the conversion funnel—from viewing a product, adding it to the cart, and completing a purchase—using data from the Google Merchandise Store.

🎯 Objective

- Understand how users move through a typical eCommerce funnel.
- Quantify drop-offs at each stage.
- Derive insights for improving conversion rates.

🛠 Tools Used

BigQuery: For querying Google Analytics public dataset (`ga_sessions_*`) and transforming it using advanced SQL (e.g., `UNNEST`, `CASE`, `COUNTIF`, `NULLIF`).
Google Looker Studio: For building a stacked area funnel chart that visualizes user drop-off and stage conversion over time.
SQL: Custom SQL to model funnel behavior and calculate conversion rates.

📊 Funnel Stages Defined

1. Viewed Product – Users who viewed a product page.
2. Added to Cart – Users who triggered an “Add to Cart” event.
3. Completed Transaction – Users who completed a purchase.

## 📉 Sample Funnel Metrics (Jan–July 2017)

| Funnel Stage              | Sessions |
|---------------------------|----------|
| Total Sessions            | 464,197  |
| Viewed Product            |    |
| Added to Cart             |    |
| Completed Transaction     | 6308    |


🧠 Key Insights

- A high drop-off rate before product view suggests a weak landing or irrelevant traffic.
- Only ~15% of product viewers add items to the cart—retargeting or better CTAs may help.
- Over 50% of users who add to cart don't complete a purchase—this could be improved with cart recovery emails or checkout optimization.

📄 SQL Code

The full SQL code used is in Funnel_Analysis_SQL_Code.rtf

📈 Visualization

A stacked area funnel chart was built in Looker Studio** to show changes in stage conversions over time. You can explore the trends interactively here:
(https://lookerstudio.google.com/reporting/9dd92bd4-4d54-4e07-b7eb-a4b767960d5b)

![Funnel Visualization](lookml/funnel_chart_screenshot.png)

---

📚 Dataset

- Source: Google Analytics Sample Data  
- Accessed via: BigQuery Public Dataset  
- `bigquery-public-data.google_analytics_sample.ga_sessions_*`

📌 Skills Demonstrated

- Working with nested data in BigQuery using `UNNEST`
- Custom funnel modeling using SQL
- Handling NULL values and division-by-zero in SQL
- Building dashboards in Looker Studio
