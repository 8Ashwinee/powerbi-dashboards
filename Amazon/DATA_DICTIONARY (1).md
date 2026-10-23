# Data Dictionary

Only fields confirmed in the report are listed. Add further columns from your source file as needed.

## Table: `Amazon`

| Field | Type | Description | Used in |
|---|---|---|---|
| `Date` | Date | Order date, with Year/Quarter/Month/Day hierarchy | Trend chart |
| `Status` | Text | Order status: *Cancelled*, *Shipped*, *Shipped – Delivered to Buyer* | Status slicer, page filter |
| `ship-city` | Text | Destination city | Sales by city |
| `ship-state` | Text | Destination state | Sales by State |

### Measures
| Measure | Description |
|---|---|
| `All overall_sale` | Total sales across the dataset, ignoring slicer selections |
| `Sale_Amount` | Sales amount KPI |
| `Filter_Sale` | Sales respecting active filters; main value in all charts |

## Table: `amazon-fashion - YT`

| Field | Type | Description |
|---|---|---|
| `Category` | Text | Product category (BoysBoxerShorts, BoysClothingSets, BoysDhotisMundus, BoysEthnicWear, BoysHatsCaps, BoysKurtaSets, BoysPyjamaSets, BoysSportsShirts, …) |
| `large.1` | Text (URL) | Product image URL shown in the image slicer |

## Table: `Sale_Option`

| Field | Type | Description |
|---|---|---|
| `Name` | Text | Toggle options: *Sales*, *Units* |
