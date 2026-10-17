# Netflix Insights Power BI Dashboard --- Requirements

## 1. Project Purpose

Create a two-page interactive Power BI dashboard that summarizes a
Netflix-style titles dataset. The report helps users explore title
counts, release-year patterns, content-rating distribution, and user
scores.

## 2. Scope

### In scope

-   Import and clean the dataset using Power Query.
-   Build a two-page Power BI report.
-   Create KPI cards and chart-based analysis.
-   Add slicers and configure visual interactions.
-   Apply a consistent Netflix-inspired dark theme.
-   Provide a readable title-level table.
-   Document the report and its fields.

### Out of scope

-   Building a streaming service or reproducing Netflix functionality.
-   Claiming official affiliation with Netflix.
-   Guaranteeing live updates unless a refreshable source is configured.
-   Including source data that cannot legally be redistributed.

## 3. Functional Requirements

### FR-01: Data import

The report shall load the source dataset from a supported file, such as
CSV.

### FR-02: Data cleaning

The data preparation process shall: - Use consistent column names and
data types. - Remove or handle duplicate records where appropriate. -
Convert `release_year` to a numeric year. - Convert `user_rating_score`
to a numeric type. - Keep missing score values blank or document any
removal rule. - Avoid replacing missing scores with zero unless zero is
a genuine value.

### FR-03: Overview page

The Overview page shall contain: - Total Records KPI. - Scored Records
KPI. - Unique Titles KPI. - Average User Score KPI. - Title counts by
release year. - Average user score by release year. - Content-rating
comparison or distribution. - A title-level table. - Slicers for
relevant fields.

### FR-04: Deep Dive page

The Deep Dive page shall contain: - Content Rating Breakdown donut
chart. - Average User Score gauge. - Average User Score by Content
Rating chart. - Average score by release year line chart. - Title
Explorer table. - Release-year and rating slicers.

### FR-05: KPI calculations

The report shall calculate: - Total records in the current filter
context. - Distinct title count. - Count of nonblank user-score
values. - Average of nonblank user-score values.

### FR-06: Interactivity

-   Slicers shall filter relevant charts and tables.
-   Visual interactions shall be configured intentionally.
-   Page navigation shall allow users to move between Overview and Deep
    Dive.
-   Users should be able to clear selections and return to the
    unfiltered view.

### FR-07: Visual design

The report shall use: - A dark background. - Red accent color
(`#E50914`). - High-contrast text. - Consistent headings and chart
titles. - Aligned visuals and readable labels. - A layout that avoids
overlapping labels and excessive unused space.

### FR-08: Data integrity

The report shall: - Use the correct aggregation for each visual. -
Display score averages as averages, not counts or percentages. - Use a
gauge scale that matches the actual score range. - Clearly represent the
cleaned dataset and any exclusions.

## 4. Non-Functional Requirements

-   **Usability:** Controls should be easy to locate and understand.
-   **Readability:** Titles, axes, legends, and table values should be
    readable.
-   **Consistency:** Colors, fonts, spacing, and formatting should match
    across pages.
-   **Maintainability:** Measures and transformations should have clear
    names.
-   **Portability:** The report should open in Power BI Desktop with its
    source path configured.
-   **Transparency:** Dataset limitations and cleaning decisions should
    be documented.

## 5. Data Fields

  -----------------------------------------------------------------------
  Field                   Expected type           Use
  ----------------------- ----------------------- -----------------------
  `title`                 Text                    Title labels,
                                                  distinct-title KPI, and
                                                  table

  `release_year`          Whole number            Release-year axis and
                                                  slicer

  `rating`                Text                    Content-rating grouping
                                                  and slicer

  `user_rating_score`     Decimal number          Score average, gauge,
                                                  and score trend
  -----------------------------------------------------------------------

Confirm these names against the actual source file and Power BI model.

## 6. Acceptance Criteria

The dashboard is considered complete when: - Both report pages exist and
have clear names. - KPI measures return values consistent with the
cleaned data. - Rating charts use the intended count or average
aggregation. - Slicers filter relevant visuals. - The gauge range
matches the score scale. - The title table displays expected fields
without unreadable clipping. - Page navigation works. - The report has
been saved as a `.pbix` file. - README, requirements, and data
dictionary documentation are included.

## 7. Deliverables

-   `Netflix_Insights_Dashboard.pbix` --- finished Power BI report.
-   `README.md` --- project overview and usage.
-   `REQUIREMENTS.md` --- functional and non-functional requirements.
-   `DATA_DICTIONARY.md` --- field descriptions and metric definitions.
-   `images/overview.png` --- Overview page screenshot.
-   `images/deep-dive.png` --- Deep Dive page screenshot.

## 8. Limitations

Metric values depend on the source dataset and cleaning steps. If rows
with missing values were removed, the dashboard describes the remaining
cleaned records. Screenshots may not reflect future report edits.
