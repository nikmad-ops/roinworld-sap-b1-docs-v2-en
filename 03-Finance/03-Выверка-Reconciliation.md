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

3. After clicking [Reconcile], a window opens where the reconciliation amount must be entered for each side. The table shows Accounts Receivable and Accounts Payable transactions:

<img src="../.assets/fc0dbdb6-7c7d-4ef7-9db3-32f718f7aa08.png" alt="" width="100%" />

(1) The reconciliation total must equal zero.  
After selecting the documents/transactions to reconcile, click [Reconcile].

## Reconciling a Payment with a Document

Reconciliation can also be performed within a single Business Partner. The purpose is to close a Business Partner balance using a payment that was posted earlier or later as a payment on account.

The entry point to reconciliation depends on the situation. You can use the method described above or the following route:

1. Open the Business Partner Master Data record and click the Golden Arrow in the Account Balance field.

<img width="1194" height="186" alt="image" src="https://github.com/user-attachments/assets/bca53296-5bf8-44d7-9399-32c03f7f6b09" />

2. The System opens the Business Partner Account Balance report. Click [Internal Reconciliation].

<img width="1746" height="524" alt="image" src="https://github.com/user-attachments/assets/74dbd448-3eec-4cd7-8eeb-8e40e4ee09f7" />

3. The Internal Reconciliation window opens.

<img width="1361" height="564" alt="image" src="https://github.com/user-attachments/assets/e5669e4f-ede2-4f0d-9c0d-4ba180ecf709" />

4. Select the transactions to reconcile, for example an A/R Invoice and a Payment.  
   The total of the selected transactions must equal zero.

<img width="1340" height="325" alt="image" src="https://github.com/user-attachments/assets/35c84dd7-c741-4c1a-9ae5-804714558bc8" />

5. Click [Reconcile].

## Reconciliation with Posting to an Expense Account

1. Open the Internal Reconciliation form using one of the methods described above.

2. Select the transaction to be balanced through an expense account and click [Adjustment].

<img width="1339" height="436" alt="image" src="https://github.com/user-attachments/assets/c4363244-72c3-4ea9-84a4-c15f94cb435a" />

3. In the window that opens, select Create Journal Entry and click [OK].

<img width="800" height="328" alt="image" src="https://github.com/user-attachments/assets/079750e0-34b7-4673-9086-df5ccee48056" />

4. The System opens the Journal Entry form and pre-fills the first row with the transaction selected for adjustment.

<img width="1137" height="91" alt="image" src="https://github.com/user-attachments/assets/9ae35f5a-d65d-407d-847b-3071a19009a9" />

5. In the second row of the Journal Entry, specify the expense G/L Account. In the example shown, the posting is made to the Debit of that account. After selecting the account, click the Debit field in the second row; this triggers the System to balance the amount from the first row.

<img width="1087" height="81" alt="image" src="https://github.com/user-attachments/assets/a56e18e8-da38-4e2a-8011-a087580745fd" />

<img width="352" height="83" alt="image" src="https://github.com/user-attachments/assets/67cc6f47-942a-4508-ad7f-7aae6a6d9f5e" />

6. Complete the Remarks field.

<img width="398" height="55" alt="image" src="https://github.com/user-attachments/assets/f6d0b186-63e3-4246-8344-f6a104644106" />

7. In the row containing the expense account, complete the Key and Department analytical fields.

<img width="1100" height="85" alt="image" src="https://github.com/user-attachments/assets/88bbafc6-552d-49dc-91c9-5e01061865c4" />

8. Click [Add] to save the Journal Entry.

9. Return to Internal Reconciliation. The System automatically selects the Journal Entry that was just created. Click [Reconcile].

<img width="1362" height="436" alt="image" src="https://github.com/user-attachments/assets/6c2a9703-3565-49b3-acab-2b2a2f6a3c50" />

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
