# 🎬 Netflix Insights --- Power BI Dashboard

> An interactive, two-page Power BI report exploring title counts,
> content ratings, release-year trends, and user scores with a
> Netflix-inspired dark theme.

![Power
BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![Project](https://img.shields.io/badge/Project-Portfolio%20Project-E50914)
![Pages](https://img.shields.io/badge/Report-2%20Pages-222222)

## 📊 Project Overview

**Netflix Insights** is a Power BI dashboard designed to explore a
Netflix-style titles dataset. It combines key metrics and visual
analysis in a two-page report with a black background, red accents, KPI
cards, charts, and interactive slicers.

The report helps viewers explore how titles are distributed across
content ratings and release years, and how recorded user scores vary
across the available data.

## ✨ Dashboard Features

### Page 1 --- Overview

-   KPI cards for total records, scored records, unique titles, and
    average user score.
-   Title counts by release year.
-   Average user score trend by release year.
-   Content-rating comparison or distribution.
-   Interactive slicers for relevant fields.
-   A title table for browsing records.

### Page 2 --- Deep Dive

-   Content Rating Breakdown donut chart.
-   Average User Score gauge.
-   Average User Score by Content Rating bar chart.
-   Average score trend by release year.
-   Title Explorer table.
-   Release-year and rating slicers.

## 🖼️ Dashboard Preview

### Overview

![Netflix Insights --- Overview](images/overview.png)

### Deep Dive

![Netflix Insights --- Deep Dive](images/deep-dive.png)

## 🧰 Tools Used

-   **Microsoft Power BI Desktop** --- report design and interactive
    visualizations
-   **Power Query** --- data cleaning and transformation
-   **DAX** --- measures and KPI calculations
-   **CSV dataset** --- source data (add your permitted dataset file
    separately if redistribution is allowed)

## 🗂️ Suggested Repository Structure

``` text
netflix-powerbi-dashboard/
├── README.md
├── REQUIREMENTS.md
├── DATA_DICTIONARY.md
├── .gitignore
├── images/
│   ├── overview.png
│   └── deep-dive.png
└── Netflix_Insights_Dashboard.pbix   # Add your finished PBIX file
```

## 🚀 How to Open the Dashboard

1.  Install **Microsoft Power BI Desktop**.
2.  Clone or download this repository.
3.  Open `Netflix_Insights_Dashboard.pbix` in Power BI Desktop.
4.  If prompted, select the local CSV file and update the source path in
    Power Query.
5.  Select **Refresh** if required.
6.  Use the page tabs and slicers to explore the report.

> **Note:** The `.pbix` file and source dataset are not included in this
> documentation pack. Add them only when you are ready to share them and
> have permission to redistribute the data.

## 📐 Key Metrics

  -----------------------------------------------------------------------
  Metric                              Meaning
  ----------------------------------- -----------------------------------
  Total Records                       Number of records included in the
                                      current report context

  Scored Records                      Number of records with a nonblank
                                      user score

  Unique Titles                       Number of distinct title names

  Average User Score                  Average of the available user-score
                                      values
  -----------------------------------------------------------------------

Values depend on the dataset version, cleaning steps, and active
filters.

## 🧮 Example DAX Measures

Adjust table and column names to match your Power BI model.

``` dax
Total Records =
COUNTROWS('Netflix')

Unique Titles =
DISTINCTCOUNT('Netflix'[title])

Average User Score =
AVERAGE('Netflix'[user_rating_score])

Scored Records =
COUNT('Netflix'[user_rating_score])
```

These measures count records in the current filter context. They do not
restore rows removed during data cleaning.

## 🎨 Design

-   Netflix-inspired black and charcoal background
-   Red accent color (`#E50914`)
-   White labels and high-contrast KPI values
-   Interactive slicers and cross-filtering
-   Two report pages for overview and deeper analysis

This is a fan-made data-visualization project and is not affiliated with
or endorsed by Netflix. Netflix is a trademark of its respective owner.

## 📌 Data Notes

-   Blank user scores should remain blank rather than being changed to
    zero.
-   If rows with missing values were removed, metrics describe the
    cleaned dataset, not necessarily the original dataset.
-   For average score by rating, use `rating` as the category and
    `Average User Score` as the value.
-   Verify the score scale before setting gauge minimum and maximum
    values.

## 📄 Project Documentation

-   [Requirements and design specification](REQUIREMENTS.md)
-   [Data dictionary](DATA_DICTIONARY.md)

## 👀 Suggested Future Improvements

-   Add a tooltip page with more title-level details.
-   Add drill-through from the title table to a detail view.
-   Add a clear-filters button.
-   Document refresh steps for the final source file.
-   Improve accessibility with descriptive chart titles and readable
    contrast.

------------------------------------------------------------------------

Made as a Power BI portfolio project.
