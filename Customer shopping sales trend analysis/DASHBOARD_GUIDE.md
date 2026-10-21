# Dashboard Guide

How to use and interpret the **Customer Shopping Sales Trend Analysis** report.

## Navigation

The report has two pages. Switch between them using the page tabs at the bottom of Power BI.

| Page | Focus |
|---|---|
| Customer shopping sales trend analysis | KPIs, filters, regional/product performance, monthly trend |
| Customer shopping sales trend analysis 2 | City, gender, store manager and yearly category mix |

## Filter panel (Page 1, left side)

| Slicer | Style | What it does |
|---|---|---|
| Age | Range ("Between") | Restrict to a customer age range |
| Region | Dropdown | Filter by customer region |
| Store location | Dropdown | Filter by store location |
| Store name | Dropdown | Filter by a specific store |
| Gender | Dropdown | Filter by customer gender |

Slicers affect the visuals on the same page. Hold **Ctrl** to multi-select in dropdowns. To clear a filter, click the eraser icon in the slicer header.

## Reading the visuals

### KPI cards
- **Total sales:** overall sales value for the current selection.
- **Count of CustomerID:** number of sales records with a customer ID. This is a non-blank count, **not** a distinct count, so repeat customers are counted each time.
- **Average sales per customer:** total sales relative to customers.
- **Top category sold:** best-selling product category for the current selection.

### Charts
- **Sales by region and category (clustered bar):** compares category performance within each region.
- **Average sales per customer by product (column):** shows which products yield the highest spend per customer.
- **Monthly sales trend (line):** reveals seasonality and growth or decline.
- **Sales by city (bar):** ranks cities by total sales.
- **Sales by gender (pie):** share of sales per gender.
- **Sales by store manager (column):** compares manager performance.
- **Yearly sales by category (stacked area):** shows how the category mix changes over time.

## Interactions

- Click any chart element to **cross-filter** other visuals on the page.
- Click it again, or click blank space, to reset.
- Use **Focus mode** (icon on the visual's top-right) to enlarge a chart.
- Use **Export data** (visual menu `...`) to download the underlying data.

## Known limitations

- Page 2 has no slicers; it responds only to cross-filtering within the page.
- The customer count card uses a non-distinct count (see above).
