# 🛒 Amazon Sales Dashboard (Power BI)

An interactive Power BI report that analyses Amazon fashion sales across **cities**, **states** and **time**, with order-status filtering, a Sales/Units toggle, and an image-based product category selector.

![Dashboard overview](assets/dashboard-overview.png)

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Report Pages](#-report-pages)
- [Key Metrics](#-key-metrics)
- [Data Model](#-data-model)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Repository Structure](#-repository-structure)
- [Usage Guide](#-usage-guide)
- [Known Limitations](#-known-limitations)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🔍 Overview

This project turns raw Amazon order data into a decision-ready dashboard. It helps answer questions such as:

- How much revenue is generated overall vs. for the current filter selection?
- Which **cities** and **states** contribute the most sales?
- How do sales trend over time (day / month / quarter / year)?
- How do **Shipped**, **Cancelled** and **Shipped – Delivered to Buyer** orders compare?
- Which product categories drive sales?

## ✨ Key Features

| Feature | Description |
|---|---|
| **KPI cards** | Overall sales, sales amount and filter-aware sales at a glance |
| **Order Status slicer** | Filter by Cancelled / Shipped / Shipped – Delivered to Buyer |
| **Sales / Units toggle** | Switch the metric shown in the visuals |
| **Sales by City** | Column chart of top ship-to cities |
| **Sales by State** | Column chart of top ship-to states |
| **Sales trend** | Smoothed area chart with a date hierarchy (Year → Quarter → Month → Day) |
| **Product category selector** | Image-based slicer with product thumbnails (e.g. BoysBoxerShorts, BoysKurtaSets, BoysSportsShirts) |
| **Custom navigation** | Page navigator buttons: Overview · Product · Product View |
| **Branded theme** | Amazon logo with an orange (`#E66C37`) palette on the `CY24SU10` base theme |

## 📄 Report Pages

| Page | Status | Purpose |
|---|---|---|
| **OVERVIEW** | ✅ Built | KPIs, status filter, sales by city/state, sales trend, category selector |
| **PRODUCT** | 🚧 Placeholder | Header and navigation only – product-level analysis planned |
| **PRODUCT VIEW** | 🚧 Placeholder | Header and navigation only – product drill-down planned |

See [`docs/DASHBOARD_GUIDE.md`](docs/DASHBOARD_GUIDE.md) for a visual-by-visual breakdown.

## 📊 Key Metrics

| Measure | Table | Description |
|---|---|---|
| `All overall_sale` | `Amazon` | Total sales, unaffected by the Status filter (**59.60M** in the current snapshot) |
| `Sale_Amount` | `Amazon` | Sales amount KPI (**32.58K** in the current snapshot) |
| `Filter_Sale` | `Amazon` | Sales respecting the active slicers (**32.58K** with *Shipped* selected); drives all charts |

Full definitions: [`docs/DATA_DICTIONARY.md`](docs/DATA_DICTIONARY.md).

## 🧩 Data Model

Three tables are loaded in the model:

| Table | Role |
|---|---|
| `Amazon` | Main fact table (orders, status, ship-city, ship-state, date, measures) |
| `amazon-fashion - YT` | Product category lookup with image URLs for the image slicer |
| `Sale_Option` | Disconnected table powering the **Sales / Units** toggle |

Details: [`docs/DATA_MODEL.md`](docs/DATA_MODEL.md).

## 🛠 Tech Stack

- **Power BI Desktop** – report authoring (file format version 1.28, report layout 5.65)
- **Power Query (M)** – data loading and transformation
- **DAX** – measures
- **Theme** – `CY24SU10` base theme with custom orange accents

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (latest version, Windows)

### Run locally
```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```
1. Open `report/Amazon.pbix` in Power BI Desktop.
2. If prompted, update the data source path: **Home → Transform data → Data source settings**.
3. Click **Refresh** to reload data.
4. Navigate between pages using the buttons in the header.

> 💡 The `.pbix` is a binary file (~17 MB). See [CONTRIBUTING.md](CONTRIBUTING.md) for tips on version-control-friendly workflows.

## 📁 Repository Structure

```
.
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── .gitignore
├── .gitattributes
├── assets/
│   └── dashboard-overview.png
├── docs/
│   ├── DASHBOARD_GUIDE.md
│   ├── DATA_MODEL.md
│   └── DATA_DICTIONARY.md
└── report/
    └── Amazon.pbix
```

## 🧭 Usage Guide

1. **Pick a status** in the *Status* slicer (default: *Shipped*).
2. **Choose a metric** with the *Sales / Units* toggle.
3. **Select a product category** from the image list on the left.
4. **Read the KPIs** at the top: they update with your selection (except `All overall_sale`).
5. **Drill into time** on the area chart using the date hierarchy (Year → Quarter → Month → Day).
6. Click a bar in *Sales by city* or *Sales by State* to **cross-filter** the other visuals.

## ⚠️ Known Limitations

- The **PRODUCT** and **PRODUCT VIEW** pages are empty shells.
- The bottom area chart is titled *"Sales by city"* but plots sales over **time** – the title should be renamed (e.g. *Sales Trend*).
- `Sale_Amount` and `Filter_Sale` currently show the same value under the default filters, so one may be redundant.
- City/state axis labels are truncated at the current visual size.
- The default *Shipped* filter hides Cancelled orders unless the slicer is changed.

## 🗺 Roadmap

- [ ] Build out **PRODUCT** and **PRODUCT VIEW** pages
- [ ] Rename the sales trend chart title
- [ ] Add year-over-year and month-over-month comparison measures
- [ ] Add cancellation-rate KPI
- [ ] Add a mobile layout
- [ ] Migrate to the PBIP project format for Git-friendly diffs
- [ ] Publish to Power BI Service and add a live link

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) first.

## 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE).

> **Disclaimer:** This is an independent portfolio/learning project. It is not affiliated with, endorsed by, or sponsored by Amazon. Amazon trademarks and logos belong to their respective owners.

## 👤 Author

**[Your Name]**
- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [your-profile](https://linkedin.com/in/your-profile)

⭐ If you found this useful, please star the repository!
