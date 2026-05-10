# Retail Dashboard — Sales, Profit & Segment Analysis | Power BI

> **$2.14M revenue · $270K profit · Consumer = 50%+ of sales · Technology = best margin**  
> Superstore Dataset · Power Query ETL · DAX · Actionable business recommendations

![Retail Dashboard](DASHBOARD.png)

🇫🇷 [Version française disponible ici](README_FR.md)

---

## Business Problem

A retail company needed to understand its growth levers and improvement areas
from historical sales data.

**4 questions from management:**

| Question | Axis |
|---|---|
| What are the sales & profit trends over time? | Time |
| Which customer segments are most profitable? | Customer |
| Which regions and categories contribute most to revenue? | Geographic |
| How to optimize shipping costs and product performance? | Operational |

---

## Key Insights Extracted

| Insight | Detail |
|---|---|
| Total Revenue | **$2.14M** |
| Total Profit | **$270.63K** — 12.6% overall margin |
| Dominant segment | **Consumer** — over 50% of sales |
| Leading regions | **East & West** — majority of revenue concentrated |
| Best category | **Technology** — highest profit margin |
| Warning signal | Growing gap between sales and profits over years → costs or discounts to monitor |

---

## Recommendations Delivered

- **Product profitability:** Monitor margins by SKU and adjust pricing on loss-making products
- **Monthly tracking:** Implement monthly margin reporting to anticipate drops before they become critical
- **Marketing focus:** Concentrate investment on Consumer and Technology segments — best demonstrated ROI
- **Logistics optimization:** Review shipping modes in low-margin regions — shipping cost not offset by selling price

---

## Dashboard — Components

![Dashboard](DASHBOARD.png)

| Visualization | Content |
|---|---|
| Geographic map | Sales by region |
| Time chart | Sales & profit by year — flags the growing gap |
| Segment breakdown | Consumer · Corporate · Home Office |
| Top 5 products | Ranked by sales volume |
| Revenue analysis | By category (Technology · Furniture · Office Supplies) and segment |

---

## DAX Measures

```dax
Total_Revenue   = SUM(Sales[Sales])
Total_Profit    = SUM(Sales[Profit])
Nb_Orders       = DISTINCTCOUNT(Sales[Order ID])
Nb_Customers    = DISTINCTCOUNT(Sales[Customer ID])
Profit_Margin_% = DIVIDE([Total_Profit], [Total_Revenue], 0)
```

---

## ETL Pipeline — Power Query

- Duplicate and missing value checks
- Date field transformation
- Data type correction (dates · numbers · text)
- Geographic field normalization

---

## Dataset

**Source:** Sample Superstore Dataset — [Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)  
**Format:** CSV · Fictional data for analytical purposes  
**Content:** Sales · Profits · Quantities · Categories · Customer segments · Regions · Shipping modes

---

## Tech Stack

- **Power BI Desktop** — interactive dashboard
- **Power Query / M** — ETL and cleaning
- **DAX** — 5 calculated measures
- **CSV** — data source

---

## Quick Start

```bash
git clone https://github.com/bouba02/Dashboard-Retail-Analyse-Ventes.git
```

Open the `.pbix` file in Power BI Desktop.

---

## Author

**Boubacar Nikiema** — Data Analyst & BI Consultant

Specialized in retail & distribution dashboards, commercial analytics and performance
management using Power BI, SQL, Python and Excel. Based in Morocco, working with
clients across Africa and French-speaking Europe.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-boubacar--nikiema-blue?logo=linkedin)](https://linkedin.com/in/boubacar-nikiema)
[![YouTube](https://img.shields.io/badge/YouTube-BoubacarDataAnalyst-red?logo=youtube)](https://youtube.com/@BoubacarDataAnalyst)
[![Email](https://img.shields.io/badge/Email-nikiemaboubacar%40gmail.com-gray?logo=gmail)](mailto:nikiemaboubacar@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-data.ngroupmediadigital.com-green)](https://data.ngroupmediadigital.com)

---

*Fictional data — Sample Superstore Dataset (Kaggle) · Code: MIT License*
