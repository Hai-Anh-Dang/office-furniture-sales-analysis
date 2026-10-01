# Power BI

The inspected implementation records 32 explicit measures and four support tables. This folder contains their exported DAX definitions, without raw model records or local connections.

- [Measures](measures.dax)
- [Measure descriptions](measure_catalogue.md)
- [Support tables](support_tables.dax)

The analytical design covers Sales, Product, and Customer pages. A saved PBIX and public report have not been verified for this release; no downloadable PBIX is included.

Completed and cancelled order values use separate populations. Observed repeat buying comes from completed-order history. Date and product/customer selections must preserve the measure definitions described in the project.

[Project overview](../README.md)
