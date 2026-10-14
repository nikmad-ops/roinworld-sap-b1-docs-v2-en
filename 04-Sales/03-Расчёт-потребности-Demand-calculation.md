## Running Demand Calculation

1. Open a previously saved Sales Quotation. Demand calculation is available only for a document that has already been added to the database: [Sales Quotation](02-Коммерческое-Предложение-Sales-Quotation.md)

2. Press the key assigned to the Dynamic Report, between [F2] and [F12].

[Assigning a Dynamic Report](../01-General/04-Назначение-Динамического-отчёта.md)  
This is a user-specific setting and depends on how each user has configured their work in the System.

3. The System calculates Demand and displays the result in a table. Filtering and sorting tools available on the Tool Panel can be used with the table.

 <img src="../.assets/63fe168c-1c21-487c-8b65-6c37b1e36534.png" alt="" width="100%" />

4. The Demand table is calculated as follows:

(The description below applies to version 1.0 of the Demand calculation procedure, current at the time this instruction was written.)  
The report displays **only items with a demand requirement**.  
For example: if 10 eggs are required to produce scrambled eggs and all 10 eggs are available in stock, eggs will not appear in the report as demand. However, if another order already exists in the System for another dish that also requires eggs, eggs may appear in Demand.  

Reconciliation rule:  
Quantity in Stock - Quantity in Sales + Quantity in Purchasing - Demand Quantity  

The calculation is performed from the top-level BOM down through lower-level BOMs to the ingredients.

 <img src="../.assets/7ba7d67f-a864-45ad-b488-628ffe82ae48.png" alt="" width="100%" />(1) Demand Type. Purchase - items must be purchased (they are not BOMs); a Purchase Request must be created for these items. Production - items with BOMs; a Production Order must be created for these items.  
(2) Processing sequence for the rows. SAP technical behavior: an empty field means 0 (the value 0 is not displayed).  
(3) Depth - informational column showing the BOM nesting level.  
(4) Item Code and Item Name.  
(5) Warehouse Code. Stock availability and open orders are considered only for the specified warehouse.  
(6) Required Quantity. Total demand quantity collected by the report from all BOM levels.  
(7) Order Quantity. Quantity calculated from demand taking the Order Multiple into account. The source of the multiple is the BOM for manufactured items and Item Master Data for purchased items.  
For example, a dessert can only be produced in batches of 16 pieces. If 35 pieces are required, the System will calculate the required order quantity as 48.  
(8) Order Multiple - informational column showing the multiple used in the calculation.  
(9) In Stock - item quantity in the warehouse specified in column (5).  
(10) Ordered (Sales). Quantity for which Sales Orders, Production Orders, and outgoing Inventory Transfer Requests already exist for the warehouse specified in column (5).  
(11) Ordered (Purchase). Quantity for which Purchase Orders, Production Orders, and incoming Inventory Transfer Requests already exist for the warehouse specified in column (5).  
(12) Used in Items. Informational column showing the BOMs **within this calculation** in which the item from the row is used.  

## Exporting Demand Calculation
To simplify transfer of data into Purchase Requests and Production Orders, export the Demand calculation to Excel.

1. Click the Excel button on the Tool Panel.

<img src="../.assets/c59671ac-ef6d-4c59-a039-5ab9c7c64f6c.png" alt="" width="100%" />

2. In the window that opens, specify the file path, select format *.xlsx, and click [Save].

 <img src="../.assets/a64af1d4-4fbe-4cbb-9287-065afe78d21b.png" alt="" width="100%" />

3. The System opens a dialog asking how numeric fields should be formatted.

Select No. This ensures compatibility of numeric field formats in Excel.

 <img src="../.assets/c9617c01-8c63-45e6-98b6-a1e091c2b4ac.png" alt="" width="100%" />

4. The Demand calculation file is saved and can be used to create supply documents such as Purchase Requests.

The Production Posting section describes an alternative way to collect demand. The alternative is used after a Sales Order has already been created.

[Production Order](../06-Production/01-Производственный-заказ-Production-Order.md)
