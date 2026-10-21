# Customer Shopping Sales Trend Analysis

An interactive **Power BI** dashboard that analyses retail sales performance across customers, products, stores and regions, with a built-in filter panel for drilling into specific segments.

> **Tagline in the report:** *"Elevate your style"*

![Dashboard preview](docs/images/dashboard-page-1.png)
<!-- TODO: export each report page from Power BI (File > Export > PDF, or screenshot) and save to docs/images/ -->

---

## Table of Contents

- [Overview](#overview)
- [Key Questions Answered](#key-questions-answered)
- [Report Contents](#report-contents)
- [Data Model](#data-model)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [Tech Stack](#tech-stack)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This report analyses shopping and sales trends for a retail business. It brings together four tables (**Sales, Customers, Products, Stores**) and presents:

- Headline KPIs (total sales, customer count, average sales per customer, top category sold)
- Sales trends over time (monthly and yearly)
- Breakdowns by region, city, product category, gender and store manager
- A filter panel for narrowing the analysis by age, region, store location, store name and gender

## Key Questions Answered

- How much are we selling in total, and how is that trending month to month?
- Which regions and cities generate the most sales?
- Which product categories drive revenue in each region, and how has that mix changed by year?
- Which products have the highest average sales per customer?
- How do sales split by customer gender?
- How do individual store managers compare on total sales?
- What is the top-selling category for a given customer segment?

## Report Contents

### Page 1: Customer shopping sales trend analysis

| Visual | Type | Fields |
|---|---|---|
| Total sales | Card | `Sales[Total sales]` |
| Customer count | Card | Count of `Sales[CustomerID]` |
| Top category sold | Card | `Customers[Top category sold]` |
| Average sales per customer | Card | `Sales[Average sales per customer]` |
| Sales by region and category | Clustered bar | `Customers[Region]`, `Products[Category]`, `Sales[Total sales]` |
| Average sales per customer by product | Column | `Products[ProductName]`, `Sales[Average sales per customer]` |
| Total sales by month | Line | `Sales[SaleDate]` (Month), `Sales[Total sales]` |
| **Filter panel** | Slicers | Age (range), Region, Store location, Store name, Gender |

### Page 2: Customer shopping sales trend analysis 2

| Visual | Type | Fields |
|---|---|---|
| Sales by city | Bar | `Customers[City]`, `Sales[Total sales]` |
| Sales by gender | Pie | `Customers[Gender]`, `Sales[Total sales]` |
| Sales by store manager | Column | `Stores[Manager]`, `Sales[Total sales]` |
| Sales by year and category | Stacked area | `Sales[SaleDate]` (Year), `Products[Category]`, `Sales[Total sales]` |

See [docs/DASHBOARD_GUIDE.md](docs/DASHBOARD_GUIDE.md) for how to use the filters and read each visual.

## Data Model

Four tables are loaded in the model: **Sales**, **Customers**, **Products** and **Stores**. Full column and measure documentation is in [docs/DATA_MODEL.md](docs/DATA_MODEL.md).

```
Products ──┐
Stores   ──┼──► Sales ◄── Customers
```
<!-- TODO: verify relationships/cardinality in Model view and update this diagram -->

## Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows). The file was created from release **2025.07** or later; use a current version.
- Alternatively, upload the `.pbix` to the [Power BI Service](https://app.powerbi.com) to view it in the browser.

### Open the report

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Then open `Customer_shopping_sales_trend_analysis.pbix` in Power BI Desktop.

### Refresh the data

The data is stored inside the `.pbix` file. If you connect it to a live source, update it under **Home > Transform data > Data source settings**, then click **Refresh**.

## Repository Structure

```
.
├── Customer_shopping_sales_trend_analysis.pbix   # The Power BI report
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── .gitignore
├── .gitattributes
└── docs/
    ├── DATA_MODEL.md        # Tables, columns, measures, relationships
    ├── DASHBOARD_GUIDE.md   # How to use and read the report
    └── images/              # Screenshots
```

## Tech Stack

- Microsoft Power BI Desktop
- DAX (measures)
- Power Query (data loading)
- Built-in Power BI theme `CY24SU10`

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Released under the MIT License. See [LICENSE](LICENSE).

## Author

**<Your Name>** · [GitHub](https://github.com/<your-username>) · [LinkedIn](https://linkedin.com/in/<your-profile>)
