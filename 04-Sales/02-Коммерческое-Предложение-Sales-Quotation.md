A Sales Quotation is a planning document. It does not create accounting or inventory postings and therefore can be adjusted after it is added to the System. The Quotation can be edited until a Sales Order is created from it. Because a Sales Order is created line by line, the System allows changes to lines that have not yet been copied to a Sales Order.

## Creating the Document
To create a Sales Quotation:

1. Open the Sales Quotation form from Main Menu → Sales - A/R → Sales Quotation.

 <img src="../.assets/3f1e4aac-6b7c-4aae-b552-56ea889d6da6.png" alt="" width="100%" />

2. Complete the Header.

(1) Specify the Customer.  
(2) Optionally enter a customer/internal reference number. This can be the number in the Customer's system or an internal SAP reference that will be available in subsequent documents. For example: "Customer A menu for August 2026".  
(3) Specify the Posting Date (Quotation creation date) and Valid Until date (the latest date until which Sales Orders can be generated from this Quotation).  

   <img src="../.assets/1e0f069a-31bf-438a-b3dc-9962144a32f5.png" alt="" width="100%" />

3. Go to the Contents tab and complete the document matrix.

4. In the first row, select [Text] from the drop-down menu in the [Type] column.

This step is optional. The text row acts as a separator and allows dishes/items to be grouped under a text heading.

   \  
   <img src="../.assets/8c810d74-556d-4066-980b-5b09905100be.png" alt="" width="100%" />

4.1. The System opens a free-text input field.  
4.2. Enter the required text and click [OK] to save it.

 <img src="../.assets/4984bded-38f4-498a-b71a-1aa275f72391.png" alt="" width="100%" />

5. Complete the document matrix as follows:

(1) Specify the Item. The item can be entered using either Item Code or Item Name. The Russian Name and Local Language Name fields are filled automatically from Item Master Data.  
(2) Enter the planned sales quantity.  
(3) Verify the Unit of Measure (source: Item Master Data).  
(4) Enter the sales price. The price is entered before tax. By default, it is entered in the Customer currency.  
(5) Verify and, if necessary, correct the VAT code (source: Customer Master Data).  
(6) Specify the delivery warehouse. This warehouse will be used for Demand calculation.  
(7) Specify the agreed delivery date for the line. If the Quotation contains the same item with different delivery dates, create separate lines and specify the relevant delivery date for each line.  
(8) Specify Key/Milestone and Department dimensions.  
(9) Verify and specify the correct Blanket Agreement related to this delivery. If only one valid Agreement exists in the System, the field is populated automatically.  

 <img src="../.assets/78cd2a37-2895-4fe5-99b3-3e0576fc6f06.png" alt="" width="100%" />

6. Complete the remaining rows in the same way.

 <img src="../.assets/46022549-49ba-4384-8cbd-3fbefc8ba703.png" alt="" width="100%" />

7. Go to the Logistics tab and verify/specify the delivery address for this delivery. **This information applies to the document as a whole, but the Document also supports different addresses by line if required.**

 <img src="../.assets/305d6ee0-a7fa-4784-a7ea-e3ab28286f0d.png" alt="" width="100%" />

8. Select your signature in the Owner field.

 <img src="../.assets/e2bd68cc-5879-4692-804d-242c460d0e01.png" alt="" width="100%" />
