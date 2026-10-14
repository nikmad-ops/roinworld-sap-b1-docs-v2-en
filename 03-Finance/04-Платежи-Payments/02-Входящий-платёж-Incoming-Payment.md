An Incoming Payment in SAP Business One can be created:

* with reference to a document generating Accounts Receivable (A/R Down Payment Invoice, A/R Invoice, Journal Entry)
* with reference to a document generating negative Accounts Payable (A/P Credit Memo, Journal Entry)
* without reference to a document, as a payment on account to a Business Partner

## Creating a Payment with Reference to a Document

To create a payment:

1. Open Incoming Payment from Main Menu → Banking → Incoming Payments → Incoming Payments.

 <img src="../../.assets/5c486c52-cc91-442f-aa32-6c86ea96a7f3.png" alt="" width="100%" />

2. Complete the Header fields:

(1) Business Partner Code or Name  

(2) Business Partner Type (Customer for Accounts Receivable; Vendor for Accounts Payable)  
(3) Payment Date  
(4) Payment Reference (bank payment order number or cash report number)  

(5) If applicable, select the Contract number from the list  

 <img src="../../.assets/a0766f92-5c1a-409d-b139-da84b3f84060.png" alt="" width="100%" />

3. The document table displays open (unpaid) documents and postings. Selection of documents and payment amounts is performed in this table.

(1) Select the checkbox for each document to be included in the payment. Any number of documents can be included.  
(2) Number, type, and date of the base document  
(3) Number of overdue days (difference between the document Due Date and the Payment Posting Date)  
(4) Original document amount  
(5) Unpaid amount of the document  
(6) Payment amount field (needs to be changed only for partial payment)  
(7) Key/Milestone and Department dimensions  
(8) The Payment on Account checkbox must remain empty when the payment is linked to a document. The exception is when the remaining payment amount is posted to the Business Partner account.  

 <img src="../../.assets/cb25a3fd-c78d-437b-9e20-90c837dbf956.png" alt="" width="100%" />

4. After selecting the documents, verify the payment amount for each one. The total will be shown in the [Total Payment] field.

 <img src="../../.assets/4bf9400b-aca3-403c-b4e7-628cd20dc919.png" alt="" width="100%" />

5. Click button (1) [Payment Means], located to the right of the total amount.

6. The Payment Means form opens.

7. In the Payment Means form:

(1) Select the required payment method.  
(2) Click the magnifying-glass icon in the G/L Account field and select the account to which the payment will be posted.  
(3) Place the cursor in the amount field and press [Ctrl]+[B], or right-click to open the context menu and select [Copy Balance].  

(4) Select the Cash Flow item from the list.  

 <img src="../../.assets/b4f6239f-354d-4a3c-a6c5-06f111d0c623.png" alt="" width="100%" />

8. Click [OK] to return to the payment form.

9. Click [Add] to post the payment.

 <img src="../../.assets/09d84970-ee74-41d8-a3c1-1633b2a1f754.png" alt="" width="100%" />

## Creating a Payment Without Reference to a Document

To create a payment:

1. Open Incoming Payment from Main Menu → Banking → Incoming Payments → Incoming Payments.

 <img src="../../.assets/b642bbe3-6662-4a7e-b2ba-50a9fdf706c3.png" alt="" width="100%" />

2. Complete the Header fields:

(1) Business Partner Code or Name  

(2) Business Partner Type (Customer for Accounts Receivable; Vendor for Accounts Payable)  
(3) Payment Date  
(4) Payment Reference (bank payment order number or cash report number)  

(5) If applicable, select the Contract number from the list  

 <img src="../../.assets/9982b6ef-c73e-4e44-88f3-1c8ab6092c5f.png" alt="" width="100%" />

3. In the [Payment on Account] section below the table, select checkbox (1) and enter the amount in field (2). To open Payment Means, click button (3).

<img src="../../.assets/5f7904bb-e2d7-4f81-b1d4-9130bd9ea8e3.png" alt="" width="100%" />

4. In the Payment Means form:

(1) Select the required payment method.  
(2) Click the magnifying-glass icon in the G/L Account field and select the account to which the payment will be posted.  
(3) Place the cursor in the amount field and press [Ctrl]+[B], or right-click to open the context menu and select [Copy Balance].  

(4) Select the Cash Flow item from the list.  

 <img src="../../.assets/cfa6dac3-c3b0-44a3-ac27-090025f118af.png" alt="" width="100%" />

5. Click [OK] to return to the payment form.

6. Click [Add] to post the payment.
