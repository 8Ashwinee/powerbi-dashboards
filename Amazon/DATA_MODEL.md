# Data Model

## Tables

| Table | Type | Purpose |
|---|---|---|
| `Amazon` | Fact | Order-level sales data, auto date hierarchy, all measures |
| `amazon-fashion - YT` | Dimension | Product categories and image URLs (`Category`, `large.1`) |
| `Sale_Option` | Disconnected helper | Holds the *Sales* / *Units* options for the toggle |

> ℹ️ Relationships, DAX and Power Query steps are stored inside the compressed data model and could not be read automatically. Open **Model view** in Power BI Desktop and fill in the TODO sections below.

## Relationships

| From | To | Cardinality | Cross-filter | Active |
|---|---|---|---|---|
| _TODO_ | _TODO_ | _TODO_ | _TODO_ | _TODO_ |

## Date Handling
`Amazon[Date]` uses Power BI's **auto date/time hierarchy** (Year, Quarter, Month, Day), used on the trend chart.

## Measures

| Measure | Table | DAX |
|---|---|---|
| `All overall_sale` | Amazon | _paste DAX here_ |
| `Sale_Amount` | Amazon | _paste DAX here_ |
| `Filter_Sale` | Amazon | _paste DAX here_ |

**Tip:** To export all DAX automatically, use [Tabular Editor](https://tabulareditor.com/) or DAX Studio.

## Data Source & Refresh
- **Source:** _e.g. Amazon Sale Report CSV / Excel_ (update)
- **Refresh:** Manual (Home → Refresh)
- **Transformations (Power Query):** _list steps, e.g. type changes, city/state cleaning, null handling_
