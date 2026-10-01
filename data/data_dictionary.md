# Data dictionary

| Input or concept | Role in the inspected analysis |
| --- | --- |
| Order ID | Distinct transaction key. The recorded snapshot has one row per order. |
| Order date | Reporting-date basis and observed customer history. |
| Order status | Normalized completed/cancelled status for the recorded two-status population. |
| Customer ID | Link for distinct ordering buyers and completed-order history. |
| Product ID | Product link for value and volume comparisons. |
| Quantity | Multiplied by current product-table unit price for estimated order value. |
| Product unit price | Current product-table amount; historical selling price is not confirmed. |
| Payment and shipping attributes | Descriptive selections in the working model. |
| Repeat buyer | Buyer with at least two completed orders in the observed period. |

The existing customer-status flag is not used to define observed repeat buying. Customer details and record-level identifiers are not published here.
