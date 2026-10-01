# Measure catalogue

Descriptions accompany the exported existing measure definitions. These are reference exports, not a complete report file.

| Measure | Description | Format |
| --- | --- | --- |
| Total Orders | Distinct order IDs in current selection. Source has one row per order. | `#,0` |
| Ordering Customers | Distinct customers with any order status in the current selection; not all customer-master records. | `#,0` |
| Completed Orders | Distinct completed order IDs in current selection. | `#,0` |
| Cancelled Orders | Distinct cancelled order IDs in current selection. | `#,0` |
| Total Submitted Order Value | All-status quantity multiplied by product-dimension unit price. Currency and historical price stability unconfirmed; not accounting revenue. | `#,0.00` |
| Completed Order Value | Completed orders only, valued at product-dimension unit price. Not confirmed accounting revenue. | `#,0.00` |
| Cancelled Order Value | Submitted order value attached to cancellations; not lost revenue or recoverable profit. | `#,0.00` |
| Order Completion Rate | Completed distinct orders / all distinct orders in current selection. | `0.00%` |
| Average Completed Order Value | Completed order value / distinct completed orders. | `#,0.00` |
| Completed Quantity | Units on completed orders; not number of products/SKUs. | `#,0` |
| Completed Buyers | Distinct customers with at least one completed order in current selection. | `#,0` |
| First-Observed Customers | Customers in current selection whose global first order of any status is in selected Date values. Product/payment/shipping restrict customer population, not first-date lookup. No pre-window history: not proven acquisition. | `#,0` |
| Repeat Completed Buyers | Buyers with at least two distinct completed orders in current selection; date/product/payment/shipping make this slice-specific. | `#,0` |
| Observed-Period Repeat Buyer Rate | Repeat completed buyers / completed buyers in current selection. Not cohort retention or churn. | `0.00%` |
| Average Completed Value per Buyer | Completed order value / completed buyers, excluding cancellation-only and never-order master records. | `#,0.00` |
| Average Completed Orders per Buyer | Distinct completed orders / completed buyers in current selection. | `0.00` |
| Cancel-Only Customers | Ordering customers with cancellations and no completed order in current selection. | `#,0` |
| Cancellation Cohort Customers | Population: customers active in current selection. Classification uses their entire observed order history across products/payment/shipping through selected Date end. Any strictly later calendar-date order counts as return. Same-day order sequence unknown; recent cancellations are right-censored. | `#,0` |
| Came Back Customers | Population: customers active in current selection. Classification uses their entire observed order history across products/payment/shipping through selected Date end. Any strictly later calendar-date order counts as return. Same-day order sequence unknown; recent cancellations are right-censored. | `#,0` |
| No Observed Return Customers | Population: customers active in current selection. Classification uses their entire observed order history across products/payment/shipping through selected Date end. Any strictly later calendar-date order counts as return. Same-day order sequence unknown; recent cancellations are right-censored. | `#,0` |
| Cancellation Recovery Rate | Population: customers active in current selection. Classification uses their entire observed order history across products/payment/shipping through selected Date end. Any strictly later calendar-date order counts as return. Same-day order sequence unknown; recent cancellations are right-censored. Numerator returned customers / cancellation-cohort customers. | `0.00%` |
| Customers by Lifecycle | Population: customers active in current selection. Classification uses their entire observed order history across products/payment/shipping through selected Date end. Any strictly later calendar-date order counts as return. Same-day order sequence unknown; recent cancellations are right-censored. Cancellation categories take precedence over one-time/repeat segments. Use Customer Lifecycle[Status] axis. | `#,0` |
| Completed Buyers by Frequency | Dynamic completed-buyer counts in 1, 2, 3, 4+ bands. Use Purchase Frequency[Band] axis. Excludes zero completed orders. | `#,0` |
| Top 10% Buyer Count | Ceiling of 10% of completed-value-positive buyers. Exact size with customer ID tie-break. | `#,0` |
| Top 10% Completed Value | Exact top 10% ranked completed value DESC, unique customer ID ASC. Dynamic in current selection. | `#,0.00` |
| Top 10% Value Share | Exact top 10% completed value / total completed order value in current selection. | `0.00%` |
| Top 20% Buyer Count | Ceiling of 20% of completed-value-positive buyers. Exact size with customer ID tie-break. | `#,0` |
| Top 20% Completed Value | Exact top 20% ranked completed value DESC, unique customer ID ASC. Dynamic in current selection. | `#,0.00` |
| Top 20% Value Share | Exact top 20% completed value / total completed order value in current selection. | `0.00%` |
| Customer Value Band Buyers | Exact rank-band customer counts. Use Customer Value Band[Band] axis. | `#,0` |
| Customer Value Band Value | Completed value within exact rank band. No dense-rank percentile approximation. | `#,0.00` |
| Customer Value Cumulative Share | Cumulative completed-value share through the band's upper rank boundary. Must reach 100%. | `0.00%` |
