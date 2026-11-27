---
layout: default
title: External Fund Transfer Fees
parent: Tools
grand_parent: Financial Officer
nav_order: 5
permalink: /docs/05-financial-officer/tools/external-fund-transfer-fees/
---

# External Fund Transfer Fee Calculator

Use this calculator to prepare an internal fee calculation record for **one
batch of payments** administered for a participating organization. It calculates
the annual fee when due, the batch fee, the percentage processing fee, and the
multi-transfer fee for batches of more than 10 payments.

[Open the External Fund Transfer Fee Calculator]({{ site.baseurl }}/assets/external-fund-transfer-fee-calculator/){: .btn .btn-primary }

{: .note }
> The calculator runs entirely in your browser. It does not transmit the
> organization or payment information. Use **Download calculation record (PDF)**
> to save the itemized result locally.

## Fee Basis

The calculator uses the **February 2026** baseline rates in the
[House-Finance Policy, Appendix III, section 3](https://gss.ubc.ca/by-laws-code-policies/):

| Fee | February 2026 baseline rate |
|-----|-----------------------------|
| Annual flat fee | $40 once per GSS fiscal year, when due |
| Batch transfer fee | $20 for each payment batch |
| Transfer processing fee | 0.33% of the batch's total transfer value |
| Multi-transfer fee | $2 for every individual payment when a batch has more than 10 payments |

Each fee component is rounded to cents before the total administration fee and
**net transfer value** (`Transfer value` minus `Total administration fee`) are
calculated.

Under **House-Finance Policy, Appendix III and Appendix IV**, the fixed dollar
fees ($40, $20, and $2) adjust annually on **June 1** using the 12-month
percentage change (April of the previous year to March of the current year) in
the [Statistics Canada Consumer Price Index (CPI) for Vancouver, All-items (Table 18-10-0004-01)](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1810000401),
subject to a **0% deflationary floor**. The 0.33% transfer processing rate is
unadjusted by CPI because it already scales with nominal transfer value. The
calculator's **CPI adjustment (%)** field defaults to `0.00` (February 2026
baseline); enter the applicable cumulative CPI percentage once an annual
adjustment takes effect. The current policy is marked for review in April 2027.

## Using the Calculation Record

1. Enter the participating organization, calculation date, total transfer value,
   number of individual payments, the CPI adjustment percentage (`0.00` for the
   February 2026 baseline), and whether the annual fee is due.
2. Select **Calculate fees** and review the itemized **Administration fee** and
   **Net transfer value** results.
3. Select **Download calculation record (PDF)** and save it with the batch's
   supporting documentation.

{: .warning }
> This is an internal calculation record, not an invoice, approval, tax
> calculation, or substitute for a written agreement that may be required for
> externally sourced funds. Follow the approval and documentation requirements
> in the [House-Finance Policy](https://gss.ubc.ca/by-laws-code-policies/) and
> accounting procedures.
