# Data Model

This document describes the tables, columns and measures used by the report.

> **Note:** Items marked **(verify)** could not be confirmed from the report layout alone. Please check them in Power BI Desktop (Model view / Table view) and fill in the details.

## Tables

The model contains four tables:

| Table | Role | Description |
|---|---|---|
| `Sales` | Fact | One row per sale/transaction; links customers, products and stores |
| `Customers` | Dimension | Customer demographics and location |
| `Products` | Dimension | Product catalogue |
| `Stores` | Dimension | Store details |

## Columns used in the report

### Sales
| Column | Type | Used for |
|---|---|---|
| `CustomerID` | Key (verify type) | Customer count; relationship to `Customers` |
| `SaleDate` | Date | Auto date hierarchy (Year, Month) for trend charts |
| Product key (verify name) | Key | Relationship to `Products` |
| Store key (verify name) | Key | Relationship to `Stores` |

### Customers
| Column | Used for |
|---|---|
| `Age` | Age range slicer |
| `Gender` | Gender slicer, sales-by-gender pie chart |
| `Region` | Region slicer, sales by region and category |
| `City` | Sales by city |

### Products
| Column | Used for |
|---|---|
| `Category` | Region/category clustered bar, yearly stacked area |
| `ProductName` | Average sales per customer by product |

### Stores
| Column | Used for |
|---|---|
| `StoreName` | Store name slicer |
| `Location` | Store location slicer |
| `Manager` | Sales by store manager |

## Measures

| Measure | Table | Purpose | DAX |
|---|---|---|---|
| `Total sales` | Sales | Sum of sales value | _(verify, paste DAX here)_ |
| `Average sales per customer` | Sales | Total sales divided by customers | _(verify, paste DAX here)_ |
| `Top category sold` | Customers | Category with the highest sales in the current filter context | _(verify, paste DAX here)_ |

The **Customer count** card uses an implicit aggregation: *Count (non-blank)* of `Sales[CustomerID]`.

## Relationships

Four tables appear in the model diagram. Expected star schema (verify keys, cardinality and filter direction in Model view):

| From | To | Cardinality | Filter direction |
|---|---|---|---|
| `Customers` | `Sales` | One-to-many (verify) | Single (verify) |
| `Products` | `Sales` | One-to-many (verify) | Single (verify) |
| `Stores` | `Sales` | One-to-many (verify) | Single (verify) |

## Data source

- **Source:** _(add: CSV / Excel / SQL / Kaggle dataset link)_
- **Refresh:** data is embedded in the `.pbix`
- **Period covered:** _(add)_
- **Rows in `Sales`:** _(add)_

## Tip: documenting measures quickly

Use Tabular Editor or DAX Studio (*Define All Measures*) to export every measure's DAX, then paste it above.
