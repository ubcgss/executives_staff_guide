---
layout: default
title: Claude
parent: Tools
grand_parent: Financial Officer
nav_order: 1
permalink: /docs/05-financial-officer/tools/claude/
---

# Claude (AI Assistant)

Claude is an AI assistant from Anthropic. The FO uses it in two ways:

- **Claude app** (web, desktop, or mobile) for reading, summarizing, and
  drafting. Connectors let it read Notion, Dropbox, Zoho, and email or calendar
  directly, so you don't have to copy and paste.
- **Claude Code** (a command-line tool) for work on files and repositories, such
  as editing this guide, running scripts, and reusable GSS workflows ("skills").
  The GSS skills and automations live in the private
  [`ubcgss/kip`](https://github.com/ubcgss/kip) repository. Ask the outgoing FO
  or GM for access.

{: .warning }
> **Before using Claude for GSS work:**
>
> 1. **Turn off model training.** In Claude's settings (Settings → Privacy),
>    turn off the option that lets your chats be used to train or improve models.
> 2. **Never share confidential data** with Claude, such as payroll details or
>    GSFA applicant information.
> 3. **Check figures against the source.** Claude can misread a table or a
>    clause, so confirm any number or quote against the original before you act
>    on it.
> 4. **It prepares the work; it doesn't give advice.** It doesn't replace the
>    lawyer, the Accountant, or the HFC.

---

## Use Cases

### 1. Keeping this guide up to date

This guide is plain Markdown in a GitHub repository, so Claude Code can make
edits, check that the site still builds, and open a pull request for review.
It works well for turning a new process you just went through into a guide
page while it's still fresh.

> *"I just changed the rent payment process: invoices now need two signers
> before payment. Update the FO guide's monthly tasks page, build the site, and
> open a PR."*

**You still check:** that policy wording matches the current Bylaws and
policies, and that nothing sensitive (credentials, account numbers, personal
contacts) ends up on the public site.

### 2. Reviewing long email threads in Spark

Vendor, audit, and UBC threads often run to dozens of messages with
attachments. Claude can read the whole thread and return a summary, a timeline
of who agreed to what, the open questions addressed to the FO, and a draft
reply. See [Spark](../spark/) for the email setup.

> *"Summarize the insurance renewal thread: what's been decided, what's still
> open, and what they need from me. Then draft a reply."*

**You still check:** dates and amounts against the original emails, and the tone
of the draft before sending.

### 3. Reviewing tasks and notes from Notion meeting records

Through the Notion connector, Claude can go through meeting notes and pull out
action items, owners, and deadlines, or tell you what changed on a topic since
the last meeting. In `kip`, a daily routine refreshes an issue tracker and
briefing (overdue, upcoming, and watch items) from these Notion records. It
also helps keep the Notion work log current for the
[monthly FO work update](../../regular-tasks/monthly/#monthly-fo-work-updates).

> *"Go through my Notion meeting notes from the last two weeks and list every
> action item assigned to the FO, with its deadline and source meeting."*

**You still check:** that nothing assigned verbally or by email is missing from
the list.

### 4. Analyzing complex legal documents before consulting the lawyer

Leases, space-use agreements, and repayment agreements are long and
cross-referenced. Before paying for counsel's time, have Claude produce a
clause-by-clause map, flag the clauses that shift cost or risk to the GSS, and
draft a list of questions and proposed wording changes. The lawyer then spends
their time on judgement calls instead of reading the document for the first time.

> *"Here is the draft space-use agreement. Map each section, flag anything that
> puts maintenance, insurance, or termination risk on the GSS, and list the
> questions I should bring to our lawyer."*

**You still check:** everything with the lawyer. Treat Claude's reading as
preparation, never as legal advice.

### 5. Daily inbox triage

A scheduled routine in `kip` reviews unreplied mail each weekday morning, sorts
it into **FYI**, **Easy reply**, and **Escalate**, drafts replies where it can,
and sends a digest to the finance inbox. You work through the digest instead of
the raw inbox.

**You still check:** every draft before sending, and anything marked FYI that
looks like it might need action.

### 6. Policy and bylaw lookups

The
[`review-gss-policies`](https://github.com/ubcgss/kip/tree/main/.claude/skills/review-gss-policies)
skill (private `ubcgss/kip` repository) answers questions about the Bylaws,
Executive Policy, and House-Finance Policy, citing the section it relied on.

> *"Who can approve a budget reallocation between departments, and does it
> need to go to Council?"*

**You still check:** the cited section in the current policy document before
quoting it to Council or the HFC.

### 7. Reconciliations and data checks

Claude can compare two lists that should agree, such as project spending in
Zoho Books against a program's own records, and list what's missing, duplicated,
or coded to the wrong budget line.

**You still check:** each flagged item in Zoho before asking the Bookkeeper to
correct anything.

---

## Zoho MCP

The Zoho MCP is a Claude connector that lets Claude work with the GSS Zoho
account directly. Each FO sets up their own connection (see
[Setting up the connector](#setting-up-the-connector-new-fo)). See
[Zoho](../../systems/zoho/) for the systems themselves.

**What it can do:**
- **Zoho Books:** read reports, including budget vs. actuals, profit and loss,
  and expenses by category, customer, or project.
- **Zoho Expense:** read and update expense reports and expenses, create
  reports, and move expenses between reports.

**FO uses:**
- **File receipts.** Turn an autoscanned receipt into a correctly coded draft
  report. See [Filing receipts](#filing-receipts-with-claude) below.
- **Pre-review the approval queue.** Ask Claude to go through the reports
  awaiting your level-4 approval and flag missing receipts, wrong budget lines,
  or amounts that don't match the receipt.
- **Clean up report titles.** Standardize titles to
  `YYYY-MM | PORTFOLIO-CODE | Budget Category | Purpose`, for example
  `2026-06 | 10-CORP | Operations, Facilities & IT | Office Coffee`. Missing parts
  come from the report's Department tag and budget category field, not guesswork.
- **Budget questions.** For example, *"Which department lines are over 80% of
  budget with a quarter left?"*

### Filing receipts with Claude

The `zoho-receipt-to-report` skill (in [`ubcgss/kip`](https://github.com/ubcgss/kip))
holds the GSS coding rules: categories, taxes, cards, departments, budget
categories and the report title format. Claude uses it to fix what Zoho's
autoscan gets wrong and to build the report.

1. **Upload the receipt to Zoho Expense autoscan.** Drag it into the web app, or
   take a photo in the Zoho Expense mobile app. Wait about a minute for the scan.
2. **Drop the same receipt into a Claude chat** and ask, for example, *"File this
   receipt in Zoho."*
3. **Check Claude's table.** It shows what autoscan read and what Claude will
   change: category, tax, card, Department tag, report title and budget
   category. Reply *yes*, or correct it.
4. **Review and submit.** Claude creates the report as a **draft**, re-reads it
   to confirm the total and each tax match the receipt to the cent, and gives
   you the report number. Submit it yourself.

Autoscan reliably reads the merchant, date, total and invoice number. It usually
gets these wrong, so Claude always checks them:

| Field | Typical autoscan result |
|---|---|
| Paid through | `1010 - Petty Cash` / Cash, not the card on the receipt |
| Tax | None, even when the receipt shows GST and PST |
| Department tag | Empty (it is mandatory) |
| Description | Raw text read off the receipt |

### Setting up the connector (new FO)

1. Sign in to the Zoho MCP console with the **FO Zoho account**. Open the GSS
   Zoho Expense server, **delete the previous FO's token**, create a new one, and
   copy the server URL.
2. In the tool list, keep the list, get, create and update tools and
   *remove expenses from report* on. Keep every **delete** tool off. Deleting
   stays a manual step in the Zoho web app.
3. In Claude, go to **Settings → Connectors**, add a custom connector with that
   URL, and connect.
4. Install the skill. In `ubcgss/kip`, download
   `.claude/skills/zoho-receipt-to-report/`, zip the folder, and upload it in
   Claude under **Settings → Capabilities → Skills** (code execution must be on).
   In Claude Code, the skill is already there when you work in the `kip` repo.
5. Test it: *"List my Zoho Expense reports from this month."*

{: .note }
> **Known limits (as of September 2026):**
>
> - **The connector cannot upload files.** Receipts go into Zoho through
>   autoscan (web upload or mobile app), never through Claude.
> - **It cannot read the category or tax lists** (authorization error). The
>   skill carries its own copy of these. Update it when the chart of accounts,
>   taxes or cards change.
> - **Deleting** through the connector fails with an authorization error, so
>   delete in the Zoho web app.
> - To see reports submitted by other people, Claude needs to use the
>   **approval** view. The default view shows only your own reports.
> - On an expense, `amount` is **pre-tax** and `total` is what was actually
>   charged. Match receipts and card statements against `total`.

{: .warning }
Before any change to Zoho, have Claude list the exact changes first (a dry
run), review them, then confirm. Never approve a bulk update you haven't read
line by line.
