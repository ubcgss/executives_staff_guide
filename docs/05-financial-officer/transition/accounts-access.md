---
layout: default
title: System Access
parent: Transition
grand_parent: Financial Officer
nav_order: 1
permalink: /docs/05-financial-officer/transition/accounts-access/
---

# System Access

For each system the FO uses, the table below documents what access is needed,
how to request or transfer it, and who the relevant contact is.

---

## Access Summary

| System | FO access needed | How to transfer | Contact |
|--------|-----------------|----------------|---------|
| **Zoho Expenses** | Level-4 approver role | GM adds/removes users in Zoho admin | GM |
| **Zoho Books** | Read access (request via GM) | GM grants/revokes access | GM |
| **Vancity banking** | Signer with online banking login and access card | Change of signer at the branch (see [Changing Signing Authority](#changing-signing-authority)) | GM / Krystina Narayan (Vancity account manager) |
| **Vancity credit cards** | Credit card site administrator (separate login from banking) | Update the Visa administrator (see [Credit Cards](#credit-cards)) | Vancity business card line / Krystina Narayan |
| **Plooto** | Approval rights for payment runs | GM adds/removes in Plooto admin | GM |
| **Payworks** | Timesheet / payroll approval | GM adds/removes | GM |
| **Dropbox** | Access to Work/UBC GSS/ folder tree | GM or President invites | GM |
| **Notion** | Access to GSS workspace | GM or President invites | GM |
| **Spark** | `finance@gss.ubc.ca` mailbox | GM transfers mailbox access; incoming FO adds it to Spark | GM |
| **Claude** | GSS Claude account; Zoho MCP and Notion connectors | Outgoing FO disables their Zoho MCP access; incoming FO sets up their own ([How to set it up](../../tools/claude/#how-to-set-it-up)) | GM |
| **RBC PH&N** (investment manager) | Online access to the fund accounts; authorized signatory status | Outgoing FO contacts Fiona Bao to confirm whether a new login is needed; signatory change needs RBC PH&N paperwork | FO / Fiona Bao (RBC PH&N) |
| **CRA** | Access to the CRA account through the FO's personal provincial partner login | Outgoing FO arranges the account transfer with the incoming FO | Outgoing FO / Accountant |
| **Vancity access card** | FO access card for online banking | Outgoing FO returns or destroys card; incoming FO issued new card at the branch | GM / Vancity branch |

---

## Notes on Specific Systems

### Zoho Expenses and Zoho Books
The Accountant and GM have primary access to Zoho Books accounting data. The
FO may request access. On transition, the GM should update the approver list
in Zoho Expenses so the new FO receives the level-4 approval queue.

### Claude and the Zoho MCP
Each FO connects Claude to Zoho through their own connection on the
AutomatedGSSReports server, so access does not pass on automatically.

**Outgoing FO** (on or before August 31):
1. In Claude, go to [Customize → Connectors](https://claude.ai/new#customize/connectors)
   and remove the Zoho Expense connector.
2. In [Zoho MCP](https://mcp.zoho.com/mcp-client/933047808#/server), open the
   AutomatedGSSReports server and revoke or delete the integration URL /
   connection you used.

**Incoming FO:**
1. Confirm the previous FO's connection is gone from the AutomatedGSSReports
   server.
2. Follow [How to set it up](../../tools/claude/#how-to-set-it-up) to create
   your own connection, keep the delete tools off, and install the receipt skill.

### Vancity
The GSS account manager at Vancity is **Krystina Narayan**
(Krystina_Narayan@vancity.com, Pinetree branch). Contact her for signer
changes, adding or removing credit card holders, card limits, and general
account questions. The step-by-step process for signers and cards is under
[Changing Signing Authority](#changing-signing-authority); see
[Banking](../../systems/banking/#vancity-credit-union) for an overview of the
GSS accounts.

Banking and credit cards have separate support lines:
- **Business banking:** 604-648-5180 (Monday to Friday, 9 am to 5 pm)
- **Business credit cards:** 604-676-8431

### Access Card
Each signer holds a Vancity access card for online banking. The GSS no longer
issues debit cards. The outgoing FO returns or destroys their card; the
incoming FO is issued a new one at the branch.

### Changing Signing Authority

Signing authority is the legal power delegated to specific individuals to sign
contracts, approve expenditures, and bind the organization to legally
enforceable agreements. Under GSS Policy 11, the FO, President, and VP UAA
hold signing authority; in the absence of either the FO or President, the
VP UAA may sign, but no single person may sign for both. In practice, all
three are registered signers on every bank account and must be updated
whenever one of these positions turns over.

Signing authority must be changed separately for the banking accounts and the
credit cards.

#### Timeline

Aim to have incoming executives registered as signers shortly after their term
begins on May 1. Work backwards from that date:

| Date | Action |
|------|--------|
| April 15 | Complete pre-appointment phone call with Vancity |
| ~April 17 | Confirm branch visit date with incoming signers |
| May 1 or shortly after | Go to branch; all signers activate online accounts |

#### Banking Accounts

1. **Schedule a pre-appointment phone call.**
   Go to [appointments.vancity.com](https://appointments.vancity.com/) and book
   a *Change of Signer for Business Account* phone appointment under Business
   Banking. Schedule at least two weeks before your planned branch visit to
   ensure availability.

2. **Go to the branch and sign the relevant forms.**
   The [Kitsilano Vancity](https://maps.app.goo.gl/zuafcR7Jpt6BQGLb92B1) branch
   has offered reliable service for this process.

3. **Activate accounts after signing.**
   Vancity will provide each new signer a password and secret word to log in to
   their website. Make sure all signers complete the online setup immediately
   after the signing is updated, and record credentials in Zoho Vault. Signers
   will need online access to approve transfers and payments.

   If the incoming executives are inheriting existing online credentials from the
   prior term, ensure they obtain the current password, change it, and transfer
   2FA to their own device.

4. **Retrieve cards from outgoing executives.**
   Ask each incoming executive to retrieve and destroy the cards that previous
   executives held.

#### Credit Cards

Credit cards are managed on the
[Vancity credit card site](https://creditcards.vancity.com/), which is
separate from online banking. Update the Visa administrator. If you need
additional cards, you can also request to add additional card holders. For
this, call the business credit card line (604-676-8431) or contact the GSS
account manager (see [Vancity](#vancity)); this can be done online. Cancel or
reassign the card of any outgoing cardholder.

### RBC PH&N
GSS investments are managed by **RBC PH&N**, with one account per fund (see
[Investment Accounts](../../systems/investment/)). The GSS contact at RBC PH&N
is **Fiona Bao** (fiona.bao@rbc.com). Log in at the
[RBC PH&N sign-in page](https://www1.royalbank.com/cgi-bin/rbaccess/rbunxcgi?F6=1&F7=IB&F21=IB&F22=IB&REQUEST=ClientSignin&IDP=IVC&LANGUAGE=ENGLISH&SYSTEM=PHN).

**Online access.** On transition, the outgoing FO contacts Fiona Bao to
confirm whether the incoming FO needs a new login. No 2FA is active on the
account.

**Signatories.** Changing the authorized signatories requires paperwork with
RBC PH&N. The outgoing FO coordinates it, starting at least two weeks before
leaving office.

The step-by-step handoff is in the [Checklists](../checklist/).

### CRA
CRA notices are downloaded and sent to the Accountant monthly (see
[Download and Send CRA Notices to Accountant](../../regular-tasks/monthly/#download-and-send-cra-notices-to-accountant)).
Access is linked to the FO's **personal** CRA login, which is reached through
the provincial partner app, so it does not pass to the next FO automatically.

**On transition.** The outgoing FO should arrange with the incoming FO the
transfer of the CRA account, so the incoming FO inherits the authorization and
can sign in with their own provincial partner app. The step-by-step handoff is
in the [Checklists](../checklist/).

### GSS Email and Internal Platforms
Confirm with the GM what GSS email address and Microsoft Teams access the FO
holds, and ensure these are transferred on the same timeline.
