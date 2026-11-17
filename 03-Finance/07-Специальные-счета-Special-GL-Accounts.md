## General Ledger Accounts

Accounts in the SAP Business One Chart of Accounts can be divided into the following practical categories:

1. **Standard G/L Accounts.**  
   These accounts can be used for direct postings, including manual postings. They can also be selected by a user when a document is created. Examples include a cash/bank account in a Payment or an income/expense account in inventory receipt or issue postings.

2. **Technical G/L Accounts.**  
   Use of these accounts is controlled by SAP. Their use in postings depends on rules defined:
   - by the System localization. For example, postings in a VAT localization differ from postings in localizations where VAT is not used;
   - by the document type and posting logic. For example, an A/R Invoice created from a Delivery may post Business Partner Control Account versus Revenue Account. An A/R Invoice without a preceding Delivery can additionally post Inventory Account versus COGS Account;
   - by Company-specific rules configured during implementation. This includes Advanced G/L Account Determination. At RoinWorld, these rules determine, for example, which expense accounts are used when certain services are purchased, and which inventory accounts are used depending on the Item Group.

The same accounts can also be classified by whether they are optional or required:

1. **Optional accounts.**  
   These are G/L accounts defined by Company accounting policy. They are not technically required for the System itself to function. In other words, this is the familiar accounting Chart of Accounts.

2. **Required accounts.**  
   For correct System operation, certain G/L accounts must exist because SAP uses them in internal processes. Examples include:

   - **Opening Balance Account** — used by the opening-balance utility for G/L Accounts and Business Partners.
   - **WIP Inventory Account / WIP Inventory Variance Account** — hold component cost until a Production Order is closed and record planned-versus-actual variance on closing.
   - **Period-End Closing Account** — temporary technical account used when P&L accounts are closed to equity.
   - **Realized Exchange Rate Difference Account** — records exchange-rate differences when foreign-currency balances are reconciled or paid.
   - **Exchange Rate Difference Account** — records exchange-rate differences between Goods Receipt PO and A/P Invoice.
   - **Control Account Receivables / Payables** — accumulation accounts for Accounts Receivable and Accounts Payable balances. See below.
   - **Payment Advances Accounts** — used for A/R Down Payment Invoice and A/P Down Payment Invoice transactions.
   - **Allocation Account** — technical account for goods received but not yet invoiced; used by Goods Receipt PO and cleared by A/P Invoice.
   - **Price Difference Account** — absorbs cost differences in edge cases where inventory quantity is zero. For example, if a Goods Receipt PO is posted at $1 and a later A/P Invoice is received at $1.50, the item would normally be revalued if stock remains. If the stock has already been sold, the $0.50 difference is posted to the Price Difference Account.
   - **Rounding Account** — used automatically when a document produces a rounding difference.
   - **Sales Returns Account** — used for product returns posted through Credit Memo or Return documents.
   - **Revenue Account** — used in A/R Invoice postings.
   - **COGS Account** — depending on the document flow, used in Delivery or A/R Invoice postings.

## Control Accounts and Down Payment Accounts

Control Accounts are a special type of mandatory technical account. SAP automatically uses a Control Account whenever a document is posted for a Customer or Vendor, including A/R or A/P Invoices, Payments, and Credit Memos.

In the logical hierarchy of the Control Account, each Customer or Vendor behaves as a subaccount. Each Business Partner is therefore represented within the applicable Control Accounts configured in the System.

<img width="444" height="263" alt="image" src="https://github.com/user-attachments/assets/4897a74c-ff7e-44d6-a2d4-d78e972a3d0e" />

When a Business Partner Master Data record is created, it receives a default Control Account. The System uses this account automatically when documents are posted. Before posting, the Control Account can be changed for a specific document where permitted.

This mechanism allows the System to maintain Accounts Receivable and Accounts Payable balances and perform Business Partner reconciliation.

**Down Payment Accounts** solve a different accounting problem: the timing of asset or liability recognition.

For example, when a Customer pays an advance, the goods have not yet been delivered and the incoming payment is not yet revenue; it is a liability to deliver the goods or refund the advance. The payment is therefore not posted to the standard Accounts Receivable Control Account but to an advance-received liability account.

Likewise, an advance paid to a Vendor is not an expense. It is an asset representing the right to receive goods/services or to receive a refund.

Revenue or expense is recognized when the related A/R Invoice or A/P Invoice is posted. SAP automatically moves the relevant amount from the Down Payment Account when the down payment is applied to the invoice.

See step 8 in the [A/P Down Payment Invoice](../05-Purchase/04-Счёт-на-предоплату-Downpayment-Invoice.md) instruction.
