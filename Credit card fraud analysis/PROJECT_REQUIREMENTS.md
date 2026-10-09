# Credit Card Fraud Analysis Dashboard --- Project Requirements

## 1. Project Title

**Credit Card Fraud Analysis Dashboard**

## 2. Project Purpose

Develop an interactive Power BI dashboard that summarizes credit-card
fraud activity and helps users explore fraud patterns by fraud type,
transaction category, state, merchant, month, transaction amount, and
risk level.

## 3. Business Objectives

-   Provide a single-screen overview of key fraud indicators.
-   Track the count and value of fraudulent transactions.
-   Compare fraud-related transaction amounts across fraud types and
    transaction categories.
-   Identify states with comparatively high fraudulent-transaction
    counts.
-   Analyze monthly changes in fraudulent transactions.
-   Examine transaction value across risk levels.
-   Allow users to filter the analysis by fraud type, state, and
    merchant.

## 4. Intended Users

-   Fraud and risk analysts
-   Business intelligence analysts
-   Operations and compliance teams
-   Managers who monitor fraud trends

## 5. Data Requirements

The dataset should include, where available:

  -----------------------------------------------------------------------
  Data field                          Requirement
  ----------------------------------- -----------------------------------
  Transaction ID                      Unique identifier for each
                                      transaction

  Transaction Date                    Date of the transaction

  Transaction Amount (INR)            Numeric transaction value

  Fraud Status / Fraud Flag           Identifies whether a transaction is
                                      fraudulent

  Fraud Type                          Fraud category

  Transaction Category                Category associated with the
                                      transaction

  State                               State associated with the
                                      transaction

  Merchant Name                       Merchant identifier or name

  Fraud Risk                          Risk level such as Low, Medium,
                                      High, or Critical
  -----------------------------------------------------------------------

Data should be checked for missing values, duplicate transaction IDs,
inconsistent category labels, invalid dates, and non-numeric transaction
amounts before analysis.

## 6. Functional Requirements

### FR-01: KPI summary

The dashboard shall display headline indicators for: - Fraud rate (%) -
Number of fraudulent transactions - Critical-risk transactions or the
configured critical-risk measure - Total amount associated with
fraudulent transactions - Top fraud type

### FR-02: Fraud-type and category comparison

The dashboard shall include a stacked bar chart showing transaction
amount by fraud type and transaction category.

### FR-03: State-level analysis

The dashboard shall show fraudulent-transaction counts by state and make
state comparisons easy to read.

### FR-04: Risk-level analysis

The dashboard shall show transaction amount split by fraud-risk
category, including Low, Medium, High, and Critical where those
categories exist in the dataset.

### FR-05: Monthly trend

The dashboard shall show fraudulent-transaction counts by month in
chronological order.

### FR-06: Interactive slicers

The dashboard shall provide slicers for: - Fraud Type - State - Merchant
Name

All relevant visuals and KPI cards should respond consistently to slicer
selections.

### FR-07: Metric consistency

All KPIs and visuals shall use clearly defined measures. Fraud rate,
transaction count, transaction amount, and risk metrics must be
calculated consistently throughout the report.

### FR-08: Reset and usability

Users should be able to clear slicer selections and return to the
overall dashboard view. If a reset button is not implemented, the report
should make the slicers' clear-selection controls easy to find.

## 7. Visual and UI Requirements

-   Use a dark dashboard background with high-contrast visual elements.
-   Place the dashboard title prominently at the top.
-   Display KPI cards in a single row beneath the title.
-   Place filters in a dedicated panel on the left.
-   Arrange analytical charts in a readable grid.
-   Use consistent typography, spacing, labels, and chart formatting.
-   Ensure chart titles and axis labels are readable.
-   Avoid truncated KPI labels where possible.
-   Use a consistent color mapping for fraud-risk levels and transaction
    categories.
-   Format transaction amounts in INR and display units clearly.

## 8. Non-Functional Requirements

-   **Usability:** Users should be able to understand the main
    indicators quickly.
-   **Performance:** Slicers and visuals should respond smoothly on the
    intended dataset.
-   **Accuracy:** Measures must match documented business definitions.
-   **Maintainability:** Data fields, measures, and transformations
    should use clear names.
-   **Readability:** Visuals should remain legible at the intended
    report resolution.
-   **Data privacy:** Sensitive cardholder or personally identifiable
    information should not be exposed unnecessarily.

## 9. KPI Definitions to Confirm

The following definitions must be documented and validated against the
report's DAX measures:

-   **Fraud Rate (%)** = fraudulent transaction count ÷ total
    transaction count × 100.
-   **Fraudulent Transactions** = count of transactions marked as
    fraudulent.
-   **Fraudulent Transaction Amount** = sum of amounts for transactions
    marked as fraudulent.
-   **Critical Risk Transactions** = count of transactions classified as
    Critical, unless the chosen KPI is explicitly a rate or amount.
-   **Top Fraud Type** = fraud type with the highest value for the
    selected measure (count or amount). The chosen measure must be
    stated.

## 10. Acceptance Criteria

The dashboard is considered complete when:

-   [ ] All required KPI cards are present and use validated measures.
-   [ ] Fraud-type/category, state, risk, and monthly visuals are
    present.
-   [ ] Fraud Type, State, and Merchant Name slicers work correctly.
-   [ ] Slicer selections update all intended visuals.
-   [ ] Monthly data is sorted chronologically.
-   [ ] Transaction amounts are clearly identified as INR.
-   [ ] Risk levels and category colors are consistent.
-   [ ] Labels, legends, and axes are readable.
-   [ ] KPI definitions and data limitations are documented.
-   [ ] The `.pbix` file opens and refreshes successfully in Power BI
    Desktop.

## 11. Deliverables

-   Power BI report file (`.pbix`)
-   Project README
-   Dashboard preview image
-   Short description of data sources and KPI definitions

## 12. Scope Note

These requirements are based on the visible dashboard layout and chart
titles. Confirm the underlying dataset, exact KPI formulas, filters'
interaction settings, and displayed units in Power BI before treating
the figures or definitions as final.
