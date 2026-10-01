# Office Furniture Sales Analysis

I used Power BI measures to examine completed orders, cancellations, and customer purchasing in an office furniture dataset. The analysis is framed for a simulated sales manager deciding which product and customer groups need further review.

Observed period: **24 September 2023 to 23 September 2024**.

The repository contains the available analytical findings and exported DAX definitions. A saved report file and public dashboard have not been verified for this release.

## 📚 Table of Contents

- [Business need](#business-need)
- [Business questions](#business-questions)
- [Findings](#findings)
- [Recommendations](#recommendations)
- [Data and methods](#data-and-methods)
- [Power BI](#power-bi)
- [Project files](#project-files)
- [Limitations](#limitations)

## Business need

A sales manager wants to distinguish completed business from cancelled orders and understand how products and customer groups contribute. These comparisons help select groups for investigation; the data does not establish the reasons for cancellation or repeat buying.

## Business questions

| Question | Measures | Decision supported |
| --- | --- | --- |
| How much order activity completes or cancels? | Completed/cancelled counts, rates, and separate order values | Select material cancellation patterns for investigation. |
| Which products contribute most to completed value? | Product value, completed volume, and cancellations | Prioritize product-level review. |
| What share of buyers purchase repeatedly? | Buyers with at least two completed orders in the observed period | Assess whether purchasing patterns warrant further analysis. |
| How concentrated is completed value across customers? | Customer contribution and cumulative share | Identify commercially important customer groups. |

## Findings

- **6,704 of 9,999 orders** were completed, while **3,295** were cancelled. Completed and cancelled orders need separate populations when interpreting activity.
- Completed Order Value was **16,543,233.66**, compared with **8,235,962.59** of Cancelled Order Value. Values use quantity multiplied by the current product-table unit price. Currency is unspecified, and these estimates are not confirmed booked revenue.
- **1,512 of 4,771** buyers with a completed order placed at least two completed orders in the observed period. This describes repeat buying within the extract; it does not establish cohort retention or customer lifetime value.

The figures come from the recorded model evidence dated 3 September 2026. Preparing this repository did not refresh the Power BI model. A compact [analytical summary](report/case_study.md) provides the definitions and interpretation.

## Recommendations

Review product and customer groups with material cancellation counts and value. Examine repeat purchasing within the observed period before proposing customer actions. Cancellation reasons, earlier transaction history, and operational context would be needed to explain the patterns or design an intervention.

## Data and methods

The working model uses order, customer, product, payment, and shipping tables. Status variants are normalized into the documented completed and cancelled groups. Repeat buying is derived from completed-order history, rather than relying on an existing customer-status flag.

The [data notes](data/README.md) describe the model inputs. Original dataset provenance and redistribution rights remain unconfirmed; this repository contains no raw customer or order records.

## Power BI

The [Power BI folder](powerbi/README.md) includes exported measure and support-table definitions. Planned report pages are Sales, Product, and Customer. Dashboard link:

## Project files

| Folder | Contents |
| --- | --- |
| [data/](data/) | Source notes and data dictionary. |
| [powerbi/](powerbi/) | Existing DAX definitions and model notes. |
| [report/](report/) | Analytical summary and aggregate snapshot. |

No SQL files were found in the inspected materials for this project.

## Limitations

Currency is unspecified. Order-value estimates use current product-table prices, rather than confirmed historical selling prices. Earlier customer history and cancellation reasons are unavailable. Repeat buying is an observed-period measure. The findings do not establish causation, profitability, or measured business impact.

AI assisted with drafting and review. Numerical claims refer to the saved model evidence.

[Back to portfolio](https://github.com/Mt-H-Anh/data-powerbi-portfolio)
