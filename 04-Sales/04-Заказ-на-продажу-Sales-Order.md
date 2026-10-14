A Sales Order is a planning document. Adding it to the System does not create inventory or accounting postings, so it can be changed until a Delivery is created from the Order. Creating a Sales Order closes the related Sales Quotation lines and makes those lines non-editable.  
The Sales Order is a base document in SAP Business One. A sales process may exist without a Sales Quotation, but the Sales Order is mandatory. This document marks the transition from Menu planning to actual fulfillment and the start of production.

## Numbering Series
Because the Sales Order is a base document in the sales process, the System creates and validates a set of details when the Order is created. These details are later used for invoicing. One of them is the Numbering Series.  
Several parallel numbering series exist for each document type. Each series defines how the document number is generated.  
For example, the following series are configured for Sales Orders, where x is the sequential number of the order:

| **Numbering Series** | **First No.** | **Last No.** | **Prefix** | **Example Number** | **Usage** |
|----------------------|---------------|--------------|------------|--------------------|-----------|
| OF26 | 100001 | 199999 | SO2026/ | SO2026/100001 | Meals\Menu |
| ST26 | 200001 | 299999 | SO2026/ST/ | SO2026/ST/200001 | Stella |
| FT26 | 300001 | 399999 | SO2026/FT/ | SO2026/FT/300001 | Foodtruck |
| BK26 | 400001 | 499999 | SO2026/BK/ | SO2026/BK/400001 | Bakery |
| LO26 | 900001 | 999999 | SO2026/IC/ | SO2026/IC/900001 | Intercompany |

The table above shows the full document-number formats. In the user interface, however, the System displays only the numeric part of the number, for example 200103 for a Stella order or 499423 for a Bakery order.

Each numbering series is associated with a specific sales channel, and the sales channel is determined by the warehouse specified in the Order. Therefore, the System validates that the numbering series selected by the user corresponds to the warehouse in the document rows. If they do not match, the System blocks saving the Sales Order.

## Sales Order

The Sales Order is used differently in different processes:

* In the Meals\Menu sales process, the Sales Order follows a Sales Quotation.
* In POS sales processes, the Sales Order is the entry-point document, meaning the first document in the chain.

The process type is determined by the Numbering Series. When a Sales Order is saved, the System checks for a preceding Sales Quotation and blocks saving if a Meals\Menu Sales Order was not created from a Quotation. For Stella\Foodtruck\Bakery numbering series, the preceding document is not checked.  
The Sales Order creation procedure therefore differs between the two processes. If a preceding document exists, the Sales Order is created by copying data from the Sales Quotation. For POS sales, the Sales Order is created from scratch. The validation performed before saving is otherwise the same.

### Meals\Menu
To create a Sales Order from a Sales Quotation:

1. Open Sales Order from Main Menu → Sales - A/R → Sales Order.

2. Complete the Header.

(1) Specify the Customer details.  
(2) Verify and, if necessary, change the Numbering Series.  
(3) Specify the planned delivery date.  

 <img src="../.assets/20d57cb6-a580-4452-9ee8-24a3a0a653cc.png" alt="" width="100%" />

3. Click [Copy From] and select Sales Quotation from the menu.

 <img src="../.assets/3d6c516d-5108-4228-93e8-43c495f155f8.png" alt="" width="100%" />

4. In the window that opens, select the source Sales Quotation and click [Choose].

 <img src="../.assets/5bd5c21f-aeff-4550-bace-9c51da4fb709.png" alt="" width="100%" />

5. The System opens the Draw Document Wizard.

On the first page, select the required options shown below and click [Next].

 <img src="../.assets/37a6a02b-2870-4399-93e7-48bb69a5356c.png" alt="" width="100%" />

6. On the second page, review and, if necessary, modify the rows. Select the rows to be copied. To select multiple rows, hold [Ctrl] while selecting them. When finished, click [Finish].

 <img src="../.assets/26e957a6-61ec-40a0-b9a3-ba0241a5e8ec.png" alt="" width="100%" />

7. The System copies the selected rows into the Sales Order.

8. Sign the document by selecting your signature in the Owner field.

 <img src="../.assets/2f9799ec-21ef-48fb-8055-1a570b51faf8.png" alt="" width="100%" />

9. Click [Add] to save the document.

### Foodtruck \ Bakery \ Stella
(!) Only the OTC customer (One Time Customer) may be used for POS sales.

1. Open Sales Order from Main Menu → Sales - A/R → Sales Order.

2. Complete the Header.

(1) Specify Customer - OTC.  
(2) Select the Numbering Series corresponding to the point of sale (Foodtruck in the example).  
(3) Enter the reference number (shift, date, or Z-report).  
(4) Enter the document dates. The actual sales date must be entered in the System.  

 <img src="../.assets/4d9d32c6-80f2-4ded-8b0b-9fd7c9d5e9e4.png" alt="" width="100%" />

3. Go to the Contents tab.

4. Enter the items sold. Copy and paste one of the following values into the relevant columns:

(1) Item Code, or (2) Item EGS Code, or (3) Item Name  
(4) Copy and paste the quantity sold into the Quantity column.  

 <img src="../.assets/a17b0eef-2472-4135-b1fd-475d08487154.png" alt="" width="100%" />

5. Verify and, if necessary, correct the following fields:

Document Total - must match the total amount on the receipt.  
Unit Price - by default, the price is taken from the price list linked to OTC.  
Tax Code - by default, the tax code configured for OTC and the item is proposed.  
Warehouse - must correspond to the point of sale.  
Key/Milestone and Department - cost centers must correspond to the Warehouse and Numbering Series.  
Blanket Agreement - must remain empty for POS sales.

6. Sign the document by specifying:

Sales Employee - cashier  
Owner - employee who created the Sales Order in SAP

 <img src="../.assets/3d6bcdb8-9219-4193-8675-ce559aef9438.png" alt="" width="100%" />

7. Click [Add] to save the document.
