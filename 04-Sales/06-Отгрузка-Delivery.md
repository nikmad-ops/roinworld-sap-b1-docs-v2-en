A Delivery is the document that records the movement of goods when they are shipped to a Customer. Posting a Delivery also creates a Journal Entry for the relevant inventory accounts. From a process perspective, the Delivery records the outgoing movement of finished goods without invoicing. At the end of the financial period, an A/R Invoice is created based on the Delivery.

Delivery is used only for the Meals sales process. It is not created for sales processed through the POS.

## Delivery Based on One or More Sales Orders

A Delivery is created using the Copy From function.  
To create the document:

1. Open Delivery from Main Menu → Sales - A/R → Delivery.

 <img src="../.assets/c325de63-93ac-4936-b3cc-b7130b9c5cc6.png" alt="" width="100%" />

2. Complete the Header.

(1) Specify the Customer Code or Name.  
(2) Specify the document date and delivery date. By default, they should be the same.  
<img src="../.assets/2107b18e-cc95-439e-b571-ec5e02ffbec1.png" alt="" width="100%" />  

3. Click [Copy From] and select Sales Order from the drop-down list.

 <img src="../.assets/7a4785db-deb3-43eb-9049-c2b07492765b.png" alt="" width="100%" />

4. In the window that opens, select the Sales Order to be used as the base document. To select several Sales Orders, hold [Ctrl]+[Shift].

 <img src="../.assets/e47499a7-2855-4630-ae20-c28d7a009654.png" alt="" width="100%" />

5. The System opens the Draw Document Wizard.

Specify how the information should be copied into the Delivery.  
<img src="../.assets/da12dddc-75e4-4cc2-a8ed-009159778945.png" alt="" width="100%" />

6. Click [Next] through all steps, verifying the information.

<img src="../.assets/063c924e-100a-4efa-a7a1-1c38999e2fba.png" alt="" width="100%" />

7. Data from the selected Sales Orders is copied to the Delivery table.

<img src="../.assets/6b546905-d4a0-4ead-bf85-90d29f980f1f.png" alt="" width="100%" />

8. Verify the information and sign the document by selecting your signature in the Owner field.

<img src="../.assets/89ed53d1-3f62-40a7-8730-3941b5efd15c.png" alt="" width="100%" />

9. Click [Add] to post the document.

## Result of Posting the Document

### Journal Entry

Posting the Delivery creates the following Journal Entry:

 <img src="../.assets/a2a31c74-90ea-43e5-91d2-3ea5c01b185d.png" alt="" width="100%" />

Because the Business Partner currency in this example is USD, the posting is recorded in three currencies:  
(1) FC - Foreign Currency (USD)  
(2) Local Currency (EGP)  
(3) SC - System Currency (SYS)  

### Inventory Movement

Posting the Delivery reduces the item quantities in the warehouse. It also reduces the quantities shown in the Sales (Ordered) informational fields.

 <img src="../.assets/ed650cc7-a05f-46c1-801e-332e1228728f.png" alt="" width="100%" />

 <img src="../.assets/63b42586-5828-4391-a7e6-bafd739eae65.png" alt="" width="100%" />

### Gross Profit

Posting the Delivery also creates the Gross Profit calculation record.

 <img src="../.assets/9f6d92af-1940-41d4-ae5a-82ca9484d3be.png" alt="" width="100%" />
