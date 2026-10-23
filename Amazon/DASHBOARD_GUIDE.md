# Dashboard Guide

Canvas size for all pages: **1280 × 720 px**.

## Page 1 – OVERVIEW

![Overview](../assets/dashboard-overview.png)

### Header
| Element | Type | Notes |
|---|---|---|
| Amazon logo | Image | Registered resource in the report |
| OVERVIEW / PRODUCT / PRODUCT VIEW | Page navigator | Outlined pill buttons with check icons and shadow |

### KPI Cards
| Card | Field | Value in snapshot | Behaviour |
|---|---|---|---|
| All overall_sale | `Amazon[All overall_sale]` | 59.60M | Overall total |
| Sale_Amount | `Amazon[Sale_Amount]` | 32.58K | Sales amount |
| Filter_Sale | `Amazon[Filter_Sale]` | 32.58K | Responds to slicers |

Cards use Segoe UI Semibold with orange (`#E66C37`) category labels.

### Slicers
| Slicer | Field | Type | Default |
|---|---|---|---|
| Category selector | `amazon-fashion - YT[Category]` | Advanced slicer (image list) | One category pre-selected |
| Status | `Amazon[Status]` | Basic list | **Shipped** |
| Sales / Units | `Sale_Option[Name]` | Button-style slicer | **Sales** |

Options in the Status slicer: *Cancelled*, *Shipped*, *Shipped – Delivered to Buyer*.

### Charts
| Visual | Type | Axis | Value |
|---|---|---|---|
| Sales by city | Clustered column | `Amazon[ship-city]` | `Filter_Sale` |
| Sales by State | Clustered column | `Amazon[ship-state]` | `Filter_Sale` |
| Sales trend (titled "Sales by city") | Area (smoothed) | `Amazon[Date]` hierarchy: Year → Quarter → Month → Day | `Filter_Sale` |

**Snapshot observations** (default filters): Maharashtra is the highest-selling state, Mumbai the highest-selling city, and the trend spans roughly May–June 2022 with visible peaks in late May and mid-June.

### Interactions
- Clicking a bar cross-filters the other visuals.
- Hover tooltips are enabled (enhanced tooltips).
- The Overview page has a page-level filter on `Status`.

## Page 2 – PRODUCT
Header, logo and navigator only. *Content to be added.*

## Page 3 – PRODUCT VIEW
Header, logo and navigator only. *Content to be added.*

## Design Notes
| Item | Value |
|---|---|
| Base theme | `CY24SU10` |
| Accent colour | `#E66C37` (orange) |
| Font | Segoe UI Semibold |
| Style | Light background, bordered cards with soft orange shadow |
