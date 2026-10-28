---
layout: default
title: Zoho
parent: Systems
grand_parent: Financial Officer
nav_order: 1
permalink: /docs/05-financial-officer/systems/zoho/
---

# Zoho Expenses and Zoho Books

The GSS uses two Zoho products: **Zoho Expenses** for transaction approval
workflows and **Zoho Books** for the accounting ledger and financial reports.

{: .note }
Claude can read Zoho Books reports and review Zoho Expense reports through the
[Zoho MCP](../../tools/claude/#zoho-mcp) connector.

---

## Zoho Expenses — Approval Chain

All payment requests, bill submissions, reimbursement submissions, and any
transaction over $100 not budgeted (or budgeted but over $100) must go through
Zoho Expenses.

The approval chain is **four levels**:

| Level | Approver | Role |
|-------|----------|------|
| 1 | Department Head | Reviews and approves departmental expenses before the FO's biweekly review |
| 2 | President | Reviews and approves |
| 3 | VP UAA | Reviews and approves |
| 4 | **Financial Officer (you)** | Final review of budget code, amount, purpose, every two weeks |
| Post-approval | Bookkeeper | Enters approved expense into Zoho Books |

After FO approval, the Zoho Expense AP entry flows directly to Plooto (for
payment processing) and is then reflected in Zoho Books.

### Your review checklist (level 4)
- Budget code is correct and aligns with the right department and line
- Amount is reasonable relative to the budget
- Purpose is documented and business-related
- Supporting documentation (receipt, invoice) is attached
- No unusual or suspicious transactions (escalate to HFC if needed)

---

## Credit Card Expense Process

**Cardholder responsibilities:**
1. Within 3 business days of receiving the monthly statement, upload credit
   card expenses with supporting documentation to Zoho Expenses for Department
   Head and FO approval.
2. Retain original receipts for all transactions.
3. Lost or stolen corporate cards must be reported immediately to the
   Accountant, GM, and FO.

**FO supervisory responsibilities:**
- Ensure all credit card transactions are business-related.
- Ensure all supporting documentation is provided in Zoho Expenses.
- Review and approve pending expenses at the
  [biweekly review](../../regular-tasks/biweekly/#credit-card-and-plooto-approvals-zoho-expenses).
- Any unusual transaction must be reconciled with the cardholder immediately.

---

## Expense Submission Details

**Receipt requirements:**
- PDF invoices are preferred when available
- Photos of receipts are acceptable if taken flat and well-lit with a clear background
- Every receipt must show: date of purchase, merchant name, total amount paid, itemized description
- For restaurant expenses: provide photos of both the itemized receipt AND the payment receipt showing tip. Tips should not exceed 18%

**Filling in expense details:**
- **Description:** Be specific — state what was purchased, where, and for what business purpose
- **Budget Line:** The department head specifies; if unsure, consult the FO before submitting
- **T4A Reportable Payment:** Check this box ONLY if payment is made to an individual (not a corporation) for scholarships, awards, honoraria, or service-based compensation. Do NOT check for corporations, expense reimbursements, or payroll

{: .note }
Ensure all submitted expense amounts match the actual final credit card transaction amount. Mismatches are common for merchants such as Save-On, Instacart, and Uber.

---

## Budget Lines (Account Codes)

From June 1, 2026 (FY2026-27), every budget line uses a 4-digit code, and the old 3-digit
codes are inactive in Zoho. The full list, with a search box and real examples, is on the
finance guide's [Budget Categories](https://ubcgss.github.io/finance_accounting_guide/zoho/budget-categories/)
page. It is the only maintained list, so it is not repeated here. If no line fits, confirm
with the FO before using `6990` Other Expenses - Operating.

---

## Zoho Books — Financial Reports

Zoho Books contains all financial statements, the general ledger, revenue
receipts, and monthly trial balances.

**Your access:** The Accountant and GM have primary access to the accounting
data and software. The FO may request access. In practice, the monthly
financial report is prepared by the Bookkeeper and Accountant and forwarded
to the FO and HFC.

### How to read the monthly financial report

The monthly report typically includes:
- **Profit and loss statement** — revenues vs. expenses for the period and
  year-to-date, compared against budget
- **Trial balance** — all general ledger account totals
- **Notes on variances** — any significant differences between budget and actuals

When reviewing, look at each department (10–14) and identify:
1. Are revenues tracking to budget?
2. Are expenses within budget for the period?
3. Are there large variances that need explanation?
4. Are there any transactions inconsistent with the approved budget purpose?

Raise questions with the Accountant by **the end of Monday of the Council
meeting week**.
