An A/P Invoice is an accounting document that creates Accounts Payable postings in the System.

### By Document Type, an A/P Invoice can be
* Item-based: purchased positions are Items from Item Master Data. For an item-based A/P Invoice, a Purchase Order is required as the base document of the process.
* Service-based: the purchased position is a General Ledger account from the expense section. A service A/P Invoice can be created without a preceding Purchase Order.

### By Creation Method, an A/P Invoice can be created
* For inventory items, based on a Goods Receipt PO. In this case, the following Journal Entry is created:  
DR Goods Received Not Invoiced  
CR Supplier Control Account  
* For non-inventory items, without a Goods Receipt PO base document. In this case, the following Journal Entry is created:  
DR Expense Account  
CR Supplier Control Account

## Creating an A/P Invoice for Non-Inventory Items (S-item)

1. Open A/P Invoice from Main Menu → Purchasing - A/P → A/P Invoice.

 <img src="../.assets/0be3b2a7-20b1-4706-bbf4-b05e03397fe9.png" alt="" width="100%" />

2. Complete the Header.

(1) Vendor Code and Name  
(2) Invoice number in the Vendor's system. This field is mandatory.  
(3) Select the document currency if it differs from Local Currency (EGP).  
(4) Enter the invoice date in Posting Date and the payment due date in Due Date.  

 <img src="../.assets/11a54e2f-e204-4d92-a79e-0611e0d8e761.png" alt="" width="100%" />

3. Complete the document table on the Contents tab.

(1) Select the appropriate S-item.  
(2) Enter the amount excluding VAT.  
(3) Verify and, if necessary, change the applicable VAT code.  

 <img src="../.assets/8c4d8376-1f30-4e51-94e5-7b148815ace6.png" alt="" width="100%" />

(4) Verify and, if necessary, change the warehouse.  
(5) Verify the assigned G/L Account.  
(6) Specify the Key/Milestone dimension.  
(7) Specify the Department dimension.  

 <img src="../.assets/a0e4bdec-5533-4304-8ed5-6425fde1e5b4.png" alt="" width="100%" />

4. Go to the Accounting tab.

(1) Verify and, if necessary, change the Control Account used for the Credit posting.  
(2) Verify and, if necessary, change the Payment Terms. The default value comes from Business Partner Master Data.  
(3) Verify the configured consolidation setting.  

 <img src="../.assets/eeaf5586-04e9-45a9-b294-4afd59cdb8a2.png" alt="" width="100%" />

5. Select your signature in the Owner field, verify the document totals, and click [Add].

 <img src="../.assets/366bea4a-f9a1-4187-a79d-956873497155.png" alt="" width="100%" />

6. When the document is added to the System, the following Journal Entry is created:

 <img src="../.assets/8f50067b-990f-479c-b09d-288ae4230ef7.png" alt="" width="100%" />

## Creating an A/P Invoice for Inventory Items

1. Open A/P Invoice from Main Menu → Purchasing - A/P → A/P Invoice.

 <img src="../.assets/81a8735e-919b-4367-96b2-68d0cb71149f.png" alt="" width="100%" />

2. Complete the Header.

(1) Vendor Code and Name  
(2) Invoice number in the Vendor's system. This field is mandatory.  
(3) Select the document currency if it differs from Local Currency (EGP). Important: the Goods Receipt PO list shown in the next step depends on the currency. The currencies must match. For example, if the Goods Receipt PO was created in EGP, the A/P Invoice must also be in EGP.  
(4) Enter the invoice date in Posting Date and the payment due date in Due Date.  

 <img src="../.assets/f004469f-3837-492e-bc5e-f649657f5d4a.png" alt="" width="100%" />

3. To populate the document table, click [Copy From] at the bottom of the form and select Goods Receipt PO.

 <img src="../.assets/e44d775c-448f-4e48-b60e-5e4efff3eaa0.png" alt="" width="100%" />

4. Select the Goods Receipt PO base document from which the data will be copied. Multiple selection is also possible by holding [Ctrl]. When selection is complete, click [Choose].

 <img src="../.assets/a3512789-8d75-41a4-bf80-1ced63701032.png" alt="" width="100%" />

5. The System opens the Draw Document Wizard. The first step determines which exchange rate will be used when posting. Even if the document is in Local Currency, every posting is also recorded in System Currency, which is USD.

 <img src="../.assets/e055c9e0-e2f6-4942-8b34-a0400d9783bc.png" alt="" width="100%" />

6. On the next step, select which data from the Goods Receipt PO will be transferred to the A/P Invoice. A blue row highlight means the row will be transferred. To include/exclude a row, click its row number in column # (1).

(2) Verify the item prices shown on the Vendor invoice.  
(3) Verify the item quantities shown on the Vendor invoice.  

 <img src="../.assets/bb2b1358-8436-4593-ae7d-26fee67316e0.png" alt="" width="100%" />

If there are differences between SAP data and the Vendor invoice, discuss them with the Vendor first. Technically, SAP allows the A/P Invoice data to differ from the Goods Receipt PO, but the following System behavior must be considered:  
**If the quantity in the Goods Receipt PO differs from the quantity in the invoice:**  
*Goods Receipt PO quantity is greater than A/P Invoice quantity* - the quantity received into stock does not change, but the cost of the uninvoiced quantity remains on the Goods Received Not Invoiced account, and the Goods Receipt PO row remains open. The remaining quantity can be processed by another A/P Invoice.  
*Goods Receipt PO quantity is less than A/P Invoice quantity* - the System blocks posting the A/P Invoice. Such a posting is technically not possible.  
**If the item price in the Goods Receipt PO differs from the invoice price:**  
The difference in item cost is posted to the inventory account if the item is still in stock, or to COGS if the item has already been sold.

7. After verifying the table data, click [Finish].

8. The Wizard transfers the Goods Receipt PO data to the A/P Invoice and creates the required links between the documents.

9. Verify all fields in the table.

10. Go to the Accounting tab and verify, and if necessary change, the Control Account and Payment Terms.

 <img src="../.assets/0a12346b-75ad-4126-b731-24b0f61f3681.png" alt="" width="100%" />

11. To enter Withholding Tax information, right-click the gray Header area to open the context menu and select [Withholding Tax Table].

 <img src="../.assets/f096606a-7ce4-43dc-82ac-02408f027af5.png" alt="" width="100%" />

12. In the form that opens, select the applicable WHT tax, verify the data, and click [Update].

 <img src="../.assets/e9d17d93-428f-4236-aa6f-b7123b45cb6e.png" alt="" width="100%" />

13. Return to the A/P Invoice and select your signature in the Owner field.

 <img src="../.assets/3bf0735d-6ac1-4eee-a873-ff4c24eb0224.png" alt="" width="100%" />

14. Generate a Journal Entry Preview by clicking the corresponding Tool Panel icon. The System generates the accounting posting in preview mode and checks the document for errors. If the Journal Entry Preview form opens, the document has passed validation.

15. Verify the posting and click [Close] to return to the A/P Invoice.

16. Click [Add] to post the A/P Invoice.

If the document is saved successfully, the System confirms this in the Status Bar.

 <img src="../.assets/2e5914d4-0cb1-4670-b6a9-5419765dba95.png" alt="" width="100%" />

## Result of Posting the A/P Invoice

Posting the A/P Invoice increases Accounts Payable to the Vendor. This is reflected:

1. In the Vendor Master Data:

 <img src="../.assets/4e1ba7e2-b803-45ea-a29c-8e168e110ac2.png" alt="" width="100%" />

2. In the Accounts Payable ageing report:

 <img src="../.assets/4a767511-1af6-44f4-a9ab-09b51c8765f1.png" alt="" width="100%" />

3. In the balance of the General Ledger Control Account:

 <img src="../.assets/092037e3-292c-400f-84cb-6b1db0f30454.png" alt="" width="100%" />
