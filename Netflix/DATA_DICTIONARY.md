# Data Dictionary --- Netflix Insights

This dictionary describes the fields used in the dashboard. Confirm the
exact column names and meanings against the original dataset.

  ---------------------------------------------------------------------------
  Field                 Expected type     Description       Dashboard use
  --------------------- ----------------- ----------------- -----------------
  `title`               Text              Name of the       Title Explorer,
                                          listed movie,     record count,
                                          show, or other    distinct-title
                                          title             metric

  `release_year`        Whole number      Release year      Year slicer,
                                          recorded in the   title-count
                                          dataset           chart, score
                                                            trend

  `rating`              Text              Content-rating    Rating slicer,
                                          category supplied donut chart,
                                          by the dataset    score-by-rating
                                                            chart

  `user_rating_score`   Decimal number    User score        Average score
                                          recorded for a    KPI, gauge, score
                                          title             trend
  ---------------------------------------------------------------------------

## Metric definitions

-   **Total Records:** Number of rows currently included by report
    filters.
-   **Scored Records:** Number of nonblank `user_rating_score` values.
-   **Unique Titles:** Number of distinct `title` values.
-   **Average User Score:** Average of nonblank user scores in the
    current filter context.

## Data-quality guidance

-   Keep unknown or missing user scores blank instead of setting them to
    zero.
-   Document whether missing values were left blank or rows were
    removed.
-   Confirm whether each row represents a unique title or a
    title-region/platform record before interpreting row counts.
-   Use the score scale found in the dataset when configuring the gauge.
