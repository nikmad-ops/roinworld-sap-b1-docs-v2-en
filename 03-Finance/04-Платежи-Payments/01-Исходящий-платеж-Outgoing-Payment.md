An Outgoing Payment in SAP Business One can be created:

* with reference to a document generating Accounts Payable (A/P Down Payment Invoice, A/P Invoice, Journal Entry)
* with reference to a document generating negative Accounts Receivable (A/R Credit Memo, Journal Entry)
* without reference to a document, as a payment on account to a Business Partner

## Creating a Payment with Reference to a Document

To create a payment:

1. Open Outgoing Payment from Main Menu → Banking → Outgoing Payments → Outgoing Payments.

 <img src="../../.assets/60785fdb-5cb0-47ae-84b9-b05da0a8c247.png" alt="" width="100%" />

2. Complete the Header fields:

(1) Business Partner Code or Name  

(2) Business Partner Type (Vendor for Accounts Payable; Customer for Accounts Receivable)  
(3) Payment Date  
(4) Payment Reference (bank payment order number)  

(5) If applicable, select the Contract number from the list  

 <img src="../../.assets/838310aa-0cc1-409c-ab0b-488adc03bf13.png" alt="" width="100%" />

3. The document table displays open (unpaid) documents and postings. Selection of documents and payment amounts is performed in this table.

(1) Select the checkbox for each document to be included in the payment. Any number of documents can be included.  
(2) Number, type, and date of the base document  
(3) Number of overdue days (difference between the document Due Date and the Payment Posting Date)  
(4) Original document amount  
(5) Withholding Tax amount (based on the tax settings, it will be calculated when the payment is posted)  
(6) Unpaid amount of the document  
(7) Payment amount field (needs to be changed only for partial payment)  
(8) Key/Milestone and Department dimensions  
(9) The Payment on Account checkbox must remain empty when the payment is linked to a document. The exception is when the remaining payment amount is posted to the Business Partner account.  

 <img src="../../.assets/b6b5f69d-af83-4553-a35d-2b190ee52398.png" alt="" width="100%" />

4. After selecting the documents, verify the payment amount for each one. The total will be shown in the [Total Payment] field.

<img src="../../.assets/bfd10728-7cdb-454b-9f9b-66ebeab032b2.png" alt="" width="100%" />

5. Click button (1) [Payment Means], located to the right of the total amount.

6. The Payment Means form opens.

7. In the Payment Means form:

(1) Select the required payment method.  
(2) Click the magnifying-glass icon in the G/L Account field and select the account from which the payment will be made.  
(3) Enter the payment date.  
(4) Place the cursor in the amount field and press [Ctrl]+[B], or right-click to open the context menu and select [Copy Balance].  

(5) Select the Cash Flow item from the list.  
<img src="../../.assets/302190fb-b5fc-42a8-b33f-b119e51fd566.png" alt="" width="100%" />

8. Click [OK] to return to the payment form.

9. Click [Add] to post the payment.

<img src="../../.assets/8a8b8fa6-e86d-4539-92f7-cc1bd52aeb5d.png" alt="" width="100%" />

10. The payment will be sent for approval.

11. After approval is received, post the payment.

## Creating a Payment Without Reference to a Document

To create a payment:

1. Open Outgoing Payment from Main Menu → Banking → Outgoing Payments → Outgoing Payments.

 <img src="../../.assets/3b1b393a-b0f6-423e-8de8-cb0991444f22.png" alt="" width="100%" />

2. Complete the Header fields:

(1) Business Partner Code or Name  

(2) Business Partner Type (Vendor for Accounts Payable; Customer for Accounts Receivable)  
(3) Payment Date  
(4) Payment Reference (bank payment order number)  

(5) If applicable, select the Contract number from the list  

 <img src="../../.assets/74b0fa91-6c81-4d48-a649-87f5e02ac996.png" alt="" width="100%" />

3. In the [Payment on Account] section below the table, select checkbox (1) and enter the amount in field (2). To open Payment Means, click button (3).

 <img src="../../.assets/ab0c9a01-95a3-445b-90e9-63b834afc68b.png" alt="" width="100%" />

4. In the Payment Means form:

(1) Select the required payment method.  
(2) Click the magnifying-glass icon in the G/L Account field and select the account from which the payment will be made.  
(3) Enter the payment date.  
(4) Place the cursor in the amount field and press [Ctrl]+[B], or right-click to open the context menu and select [Copy Balance].  

(5) Select the Cash Flow item from the list.  

 <img src="../../.assets/4a0989e7-4f39-47a1-b3fc-757150adf25e.png" alt="" width="100%" />

5. Click [OK] to return to the payment form.

6. Click [Add] to post the payment.
