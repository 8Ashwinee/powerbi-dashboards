# 💳 Credit Card Fraud Analysis Dashboard

> **Turn suspicious transactions into clear, actionable insights.**\
> An interactive Power BI dashboard designed to explore credit-card
> fraud patterns by fraud type, state, merchant, month, transaction
> value, and risk level.

![Dashboard Preview](dashboard-preview.png)

## 📌 Project Overview

The **Credit Card Fraud Analysis Dashboard** provides a consolidated
view of fraudulent transactions and their patterns. Its dark interface,
high-contrast KPI cards, and focused visualizations help users quickly
identify where fraud is occurring, how it changes over time, and which
fraud categories contribute most to transaction value.

The report is designed for analysts, risk teams, and business
stakeholders who need a quick overview of fraud activity and the ability
to investigate it through filters.

## 🎯 Objectives

-   Monitor key fraud indicators in one place.
-   Compare transaction amounts across fraud types and transaction
    categories.
-   Identify states with higher counts of fraudulent transactions.
-   Track monthly changes in fraud activity.
-   Understand how transactions are distributed across fraud-risk
    levels.
-   Filter the report by fraud type, state, and merchant to investigate
    specific segments.

## 📊 Dashboard Highlights

### KPI cards

The top row summarizes headline indicators, including:

-   **Fraud Rate (%)** --- the percentage of transactions classified as
    fraudulent, according to the report's underlying calculation.
-   **Fraudulent Transactions** --- the count of transactions flagged as
    fraudulent.
-   **Critical Risk Transactions** --- the critical-risk indicator shown
    in the report.
-   **Fraudulent Transaction Amount** --- the total value associated
    with fraudulent transactions.
-   **Top Fraud Type** --- the fraud category with the highest value or
    count, depending on the measure configured in the report.

### Visual analysis

  -----------------------------------------------------------------------
  Visual                              What it helps answer
  ----------------------------------- -----------------------------------
  Total Transaction Amount by Fraud   Which fraud types and transaction
  Type and Transaction Category       categories contribute most to
                                      transaction value?

  Fraudulent Transactions by State    Which states have the highest
                                      number of flagged transactions?

  Transaction Amount by Fraud Risk    How is transaction value
                                      distributed across Low, Medium,
                                      High, and Critical risk?

  Fraudulent Transactions by Month    How does the number of fraudulent
                                      transactions change throughout the
                                      year?
  -----------------------------------------------------------------------

### Interactive filters

Use the slicers in the left panel to narrow the analysis by:

-   **Fraud Type**
-   **State**
-   **Merchant Name**

Selecting a filter updates the report visuals to show the matching
segment, making it easier to explore patterns without leaving the
dashboard.

## 🧰 Tools & Technologies

-   **Microsoft Power BI** --- report design, data modeling, measures,
    and interactive visuals
-   **Power Query** --- data cleaning and transformation, if used in the
    source workflow
-   **DAX** --- calculated measures and KPI logic, where applicable

> The dashboard screenshot confirms the Power BI-style report layout.
> Update this section if your actual data-preparation workflow uses
> different tools.

## 🗂️ Suggested Data Fields

The source dataset should contain fields equivalent to the following.
Exact column names may differ.

  Field                       Purpose
  --------------------------- ----------------------------------------------------
  Transaction ID              Unique transaction identifier
  Transaction Date / Month    Time-based analysis
  Transaction Amount (INR)    Transaction value
  Fraud Flag / Fraud Status   Identifies fraudulent transactions
  Fraud Type                  Fraud-category analysis
  Transaction Category        Category comparison
  State                       Geographic comparison
  Merchant Name               Merchant-level filtering
  Fraud Risk                  Low, Medium, High, or Critical risk classification

## 🚀 How to Use

1.  Open the `.pbix` file in **Power BI Desktop**.
2.  If prompted, connect to or refresh the source dataset.
3.  Confirm that the fields and measures are mapped correctly.
4.  Use the left-side slicers to select a fraud type, state, or
    merchant.
5.  Review the KPI cards and charts to compare the selected segment.
6.  Clear or reset slicers to return to the full overview.

## 📐 Metric Definitions

Metric definitions should match the DAX measures in the `.pbix` file.
Common definitions are:

-   **Fraudulent Transactions:** count of transactions where the fraud
    flag is true.
-   **Fraud Rate:** fraudulent transaction count divided by total
    transaction count, multiplied by 100.
-   **Fraudulent Transaction Amount:** sum of transaction amounts for
    transactions flagged as fraudulent.
-   **Critical Risk Transactions:** count of transactions assigned the
    Critical risk category, unless the report intentionally displays a
    rate.

**Important:** Validate the formula behind every KPI before publishing.
The screenshot alone does not establish the exact denominator or
aggregation used for each displayed metric.

## ✅ Key Takeaways

This dashboard brings fraud monitoring into a single interactive view.
It supports quick performance checks, category comparisons, state-level
investigation, monthly trend analysis, and risk segmentation. It is
intended as an analytical aid; flagged transactions should be reviewed
using the organization's established fraud-investigation process.

## 📷 Preview

Add the dashboard screenshot to this repository as
`dashboard-preview.png`, or replace the image path above with the actual
screenshot filename.

## 🔮 Possible Enhancements

-   Add date-range and risk-level slicers.
-   Include a state map for geographic exploration.
-   Add a drill-through page for transaction-level investigation.
-   Show comparisons against the previous month or period.
-   Add tooltips with transaction counts, amounts, and fraud rates.
-   Include data-refresh time and a definitions page.
-   Add anomaly alerts for sudden increases in fraud activity.

## 👤 Project

**Project:** Credit Card Fraud Analysis Dashboard\
**Platform:** Microsoft Power BI\
**Focus:** Fraud monitoring, transaction analysis, and risk insights

------------------------------------------------------------------------

*Built to make complex fraud patterns easier to explore, explain, and
act on.*
