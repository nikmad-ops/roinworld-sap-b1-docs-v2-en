An A/P Down Payment Invoice is an accounting document that creates postings to Accounts Payable. Creating this document in SAP records receipt of a supplier's down payment invoice. The document is then paid and can later be applied when an A/P Invoice is created.

To create an A/P Down Payment Invoice:

1. Open the document from Main Menu → Purchasing - A/P → A/P Down Payment Invoice.

(*In the Russian interface this item is translated differently; the original English name is Down Payment Invoice.)

 <img src="../.assets/fc0de8e2-b4fa-477f-8ffd-d5e433ef28f8.png" alt="" width="100%" />

2. Complete the Header:

(1) Vendor Code or Name  
(2) Invoice Date (Posting Date) and Due Date (the date by which the invoice must be paid)  

(3) BP Reference No. - the supplier invoice number. It will be used later for reconciliation with the Vendor.  
<img src="../.assets/e6035178-bda8-4138-b304-ef683cf76584.png" alt="" width="100%" />

3. Click [Copy From] and select Purchase Orders.

<img src="../.assets/3f5e1981-78a2-4cb6-8586-1af187bda298.png" alt="" width="100%" />

4. The System opens the list of available base documents. Double-click the required document. To select several documents, hold [Ctrl]+[Shift].

 <img src="../.assets/5ff8edd8-f6ed-4cd6-8cb1-fe8e8cd3a36b.png" alt="" width="100%" />

5. The System starts the Draw Document Wizard.

6. Because the invoice normally applies to the entire Purchase Order rather than to individual rows, select Extract All Data and click [Finish].

   \  
   <img src="../.assets/006cec94-606c-4a7d-961c-53e569ec6c6f.png" alt="" width="100%" />

7. Data from the Purchase Order is copied to the A/P Down Payment Invoice.

<img src="../.assets/8fc50a47-4be0-48f1-914a-dc24131b7f29.png" alt="" width="100%" />

8. In the lower part of the document, specify the required down-payment percentage by entering either the percentage (1) or the amount (2).

 <img src="../.assets/37227222-587d-4bc9-9455-3527bd0b30d4.png" alt="" width="100%" />

9. Sign the document by selecting your signature in the Owner field.

<img src="../.assets/bf7cd116-eb5a-4fa7-8d4a-e507c1bc350a.png" alt="" width="100%" />

10. Click [Add] to post the invoice in the System.

## Result of Posting the A/P Down Payment Invoice

### Journal Entry

 <img src="../.assets/08486f14-3ef4-4540-b26c-326f5545148a.png" alt="" width="100%" />

### Accounts Payable

 <img src="../.assets/e4ada510-7b68-4c2b-98f0-73492d765922.png" alt="" width="100%" />
