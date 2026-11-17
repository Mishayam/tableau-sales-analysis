# Tableau Sales Analysis

A learning portfolio project by Sam, based on the supplied Superstore-style order, returns and manager files. Explores regional sales, discounts, profitability and customer performance.

## Open the project

Download `Sales_Analysis.twbx` and open it in Tableau Desktop or Tableau Public 2026.3 or later. The packaged workbook contains its data. Alternatively, keep `Sales_Analysis.twb` alongside the `Data` folder.

## Scope and controls

The original workbook unions Orders 2015 and Orders 2016. The separate 2017 file is intentionally outside this project's scope. One order line is the fact-table grain; order count must use COUNTD([Order ID]).

| Measure | Value |
| --- | ---: |
| Order lines | 4,689 |
| Distinct orders | 2,353 |
| Sales, source units | 1,079,738.11 |
| Profit, source units | 143,413.78 |
| Profit margin | 13.3% |

## Improvements

- Replaced generic worksheet and dashboard names with descriptive labels.
- Removed returns records accidentally appended to the order union. Returns remain available through the existing model.
- Replaced summed discount percentages with average line discount in the standard regional and segment views.
- Packaged all four required source tables in a typed Excel source with relative connections.
- Removed cached thumbnails and machine fingerprint metadata.

## Interpretation

Average discount is an unweighted mean across order lines. Profit margin is SUM([Profit])/SUM([Sales]), rather than an average of row margins. Customer Records by Profit Bin counts records, not distinct people. Customer sets, manual groups and bins are retained as learning exercises and should be reviewed when refreshing data.

The Regional Extension Exploration sheet retains the original third-party visual extension and may require network access or extension approval. The standard charts do not require that visual. No private business data or business results are claimed. Dataset provenance and redistribution licence were not supplied; confirm them before public redistribution.

## Validation

XML parsing, ZIP integrity and packaged connection paths checked. Data controls were independently calculated from the supplied sources. Tableau could not expose an application window in this session, so native rendering, refresh, dashboard actions and the revised Excel connection remain unverified. Open in Tableau 2026.3 or later and refresh before publishing screenshots.

See `data_checks.json` for reproducible source control totals. This is a revised learning project, not a production reporting deployment.
