Reconciliation is the process of matching and closing open Debit and Credit transactions. SAP Business One distinguishes two types of internal reconciliation:

* Internal G/L Reconciliation
* Internal Business Partner Reconciliation

By creation method, reconciliation can be:

* Automatic Reconciliation - for example, a payment that closes an invoice is reconciled automatically by the System.
* Manual Reconciliation - reconciliation created by a user.

## G/L Reconciliation
This type of reconciliation is used to match and close open Debit and Credit transactions for a selected General Ledger account.

G/L reconciliation is located under Main Menu → Financials → Internal Reconciliations → Reconciliation.

 <img src="../.assets/97a953ed-7fa1-41e2-ab14-cf0e2414d92b.png" alt="" width="100%" />

## Business Partner Reconciliation
Reconciliation within one or several Business Partners. This type can be used to close open balances between a Business Partner maintained as a Customer and the same or another Business Partner maintained as a Vendor, for example in three-party transactions.  
It is located under Main Menu → Business Partners → Internal Reconciliations → Reconciliation.

 <img src="../.assets/5c1e9951-6ab5-4aa2-bbc2-d78be382539d.png" alt="" width="100%" />

## Reconciliation Example

The example below shows reconciliation between two Business Partners. Other reconciliation types are performed in a similar way.

1. Open Internal Reconciliation for Business Partners.

2. Complete the Selection Criteria window.

   Set Reconciliation Type to Manual.  
Select the Multiple Business Partners option.  
Select the Business Partners to be reconciled in the table.  
Click [Reconcile].  
<img src="../.assets/c138c6aa-6ddd-43e5-a3ba-1d6f020ac994.png" alt="" width="100%" />

   \

3. After clicking [Reconcile], a window opens where the reconciliation amount must be entered for each side. The table shows Accounts Receivable and Accounts Payable transactions:

   <img src="../.assets/fc0dbdb6-7c7d-4ef7-9db3-32f718f7aa08.png" alt="" width="100%" />
(1) The reconciliation total must equal zero.  
After selecting the documents/transactions to reconcile, click [Reconcile].

## Managing Previous Reconciliations

The Manage Previous Reconciliations window shows both automatic and manual reconciliations. However, only reconciliations created manually by a user can be cancelled directly. To reverse an automatic reconciliation, the originating documents must be cancelled/reversed instead, such as the related payment or invoice.

1. Open Main Menu → Financials → Internal Reconciliations → Manage Previous Reconciliations.

 <img src="../.assets/35a5c0fb-1dc5-49d1-8930-08a27b4292eb.png" alt="" width="100%" />

2. Before the form opens, the System displays the selection-criteria window where the reconciliation type to be processed must be selected.

<img src="../.assets/d1d1c6ff-075d-4fc9-949b-dfe06d76cd10.png" alt="" width="100%" />

3. After the criteria are defined, the reconciliation-management window opens.

<img src="../.assets/5f5b970d-b8f7-4785-8d32-e870dd51756a.png" alt="" width="100%" />

The window consists of two dependent tables: the Reconciliation Journal and Reconciliation Details.

4. To cancel a reconciliation, select the relevant row in the Journal and verify that the correct reconciliation transaction has been selected.

5. Click [Cancel Reconciliation].

   The reconciliation will be cancelled.
