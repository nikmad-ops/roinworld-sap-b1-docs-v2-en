Recording production operations is a mandatory part of entering actual data into SAP. Production posting provides:

* calculation of direct production cost for Products and Semi-Finished Products
* recording of inventory movements (receipt of products and semi-finished products, issue of ingredients and semi-finished products, and generation of requirements)
* recording of accounting movements (changes in inventory and expense account balances)

For one-off production operations, a Production Order can be created without a Bill of Materials. In most cases, however, a Production Order is created using a Bill of Materials. A correctly maintained BOM is the basis for a correctly generated Production Order.  
During the initial period of SAP use, BOM composition will need to be reviewed and corrected carefully.

### The Production Process Consists of the Following Stages

1. Demand generation (Sales Order)

2. Generation of supply documents for Finished Goods (Production Order)

3. Generation of supply documents for Semi-Finished Goods (Production Order)

4. Recording receipt of Semi-Finished Goods and issue of ingredients (Receipt from Production and Issue for Production)

5. Recording receipt of Finished Goods (Receipt from Production and Issue for Production)

### Production Order Statuses

* Planned. The order has been created and can be edited. Component issue and production posting are not available.
* Released. The order has been released for execution. Component issue and production posting are available.
* Closed. The order is complete, the product has been received into stock, components have been issued, and production cost has been calculated.

### Production Orders by Creation Method

* Manual. Can be created from a Bill of Materials or without a Bill of Materials. Manually created Production Orders are not linked to other SAP documents, but their posting result is the same as for automatically created Production Orders.
* Automatic. Includes orders created from a Sales Order, from another Production Order, or by using the document-generation wizard based on demand.

## Creating a Production Order
### Manually Creating a Production Order for an Item Without a BOM (Rare Case)

1. Open Production Order from Main Menu → Production → Production Order.

2. Complete the Production Order Header as follows:

(1) Type - Special. This type allows one-off Production Orders to be created for items without a BOM.  
(2) Specify the Code/Name of the finished product.  
(3) Specify the Planned Quantity. This is the quantity that will be received into stock as a result of posting this Order. Verify the Unit of Measure, sourced from Item Master Data. Verify the Warehouse; this is the warehouse where the production output will be received.  
(4) Specify the dates. Order Date is the order creation date. Start Date is the planned production start date (shown in red in the example because the planned start is overdue). Due Date is calculated automatically and represents when the product can be received into stock.  
(5) If the Production Order is being executed for a specific Sales Order or another Production Order, specify references to those documents.  
(6) Key/Milestone and Department dimensions are mandatory. They determine the financial dimensions used in accounting postings.  

 <img src="../.assets/6a13ecf1-88e2-451e-a5fd-57cbed3015ce.png" alt="" width="100%" />

3. Go to the Components tab and specify:

(1) Select row type Item and specify the ingredient used in production.  
(2) Base Quantity - quantity of the ingredient directly consumed in production.  
(3) Additional Quantity - quantity of the component consumed once for the whole order and not increased when output quantity increases. For example, an unavoidable residue in a juicer is generated once regardless of how many apples are processed and how much juice is produced.  
(4) Planned Quantity - total ingredient quantity required for the output quantity specified in the Header (Base Quantity + Additional Quantity).  
(5) Warehouse from which the ingredients will be issued.  
(6) Key/Milestone and Department dimensions used in the postings. They must correspond to the Warehouse.  

 <img src="../.assets/cbe0eb81-a3b6-4ca2-8323-a39c6e060cc7.png" alt="" width="100%" />

4. Repeat the steps as required to add additional ingredients.

The Production Order above can be read as follows:  
One-off production of one portion of fresh apple juice from 1.2 kilograms of apples for the Foodtruck point of sale.

### Manually Creating a Production Order for an Item with a BOM (Rare Case)

1. Open Production Order from Main Menu → Production → Production Order.

2. Complete the Production Order Header as follows:

(1) Type - Standard. This type is used for Production Orders for items with a BOM.  
(2) Specify the Code/Name of the finished product.  
(3) Specify the Planned Quantity. This is the quantity that will be received into stock as a result of posting this Order. Verify the Unit of Measure, sourced from Item Master Data. Verify the Warehouse; this is the warehouse where the production output will be received.  
(4) Specify the dates. Order Date is the order creation date. Start Date is the planned production start date (shown in red in the example because the planned start is overdue). Due Date is calculated automatically and represents when the product can be received into stock.  
(5) If the Production Order is being executed for a specific Sales Order or another Production Order, specify references to those documents.  
(6) Key/Milestone and Department dimensions are mandatory. They determine the financial dimensions used in accounting postings.  

 <img src="../.assets/b10494f7-b943-4c11-adbb-70a30e9f52b8.png" alt="" width="100%" />

3. When a Production Order is created for an item with a BOM, selecting the product in the Header automatically loads the BOM components into the table. The ingredient composition can be adjusted for a specific Production Order if required.

Verify and, if necessary, adjust the table data:  
(1) Verify the ingredient used in production.  
(2) Base Quantity - quantity of the ingredient directly consumed in production.  
(3) Additional Quantity - quantity of the component consumed once for the whole order and not increased when output quantity increases.  
(4) Planned Quantity - total ingredient quantity required for the output quantity specified in the Header (Base Quantity + Additional Quantity).  
(5) Warehouse from which the ingredients will be issued.  
(6) Key/Milestone and Department dimensions used in postings. They must correspond to the Warehouse.  

 <img src="../.assets/010fc994-54ff-441b-aebc-4775f3e74402.png" alt="" width="100%" />

### Generating a Production Order from a Sales Order (Common Scenario)

1. Open the Sales Order. The example uses a Foodtruck POS Sales Order, but the same approach applies to the Kitchen warehouse.

2. Go to the Logistics tab and select 'Purchase Non-Drop-Ship Items'.

 <img src="../.assets/8a3bc6b9-1c58-4846-8274-886ea906d854.png" alt="" width="100%" />

3. The System asks whether the rows should be updated. Click [Yes].

 <img src="../.assets/887c5856-ef21-4077-b140-60dea2006abf.png" alt="" width="100%" />

4. Save the Sales Order changes by clicking [Update].

 <img src="../.assets/7a2870ca-d0c3-4a30-a1af-dc8e5fdcc5bc.png" alt="" width="100%" />

5. The System opens the wizard where generation criteria must be defined step by step. Because the wizard was launched from a Sales Order, most pages are prepopulated. The first step identifies the Customer. Click [Next].

 <img src="../.assets/b8133d26-83a7-4265-a167-e6ea4279dd0c.png" alt="" width="100%" />

6. The second step identifies the base documents used for calculation. Click [Next].

 <img src="../.assets/e400a146-16ad-4cea-be05-cd7c5cd1570f.png" alt="" width="100%" />

7. The third step defines the item positions and target document type.

(!) Important: verify the target document type. It must be Production Order.

 <img src="../.assets/d4c8473e-0c60-40af-a494-c9c66ac58667.png" alt="" width="100%" />

8. Change the Target Document type to Production Order. The item list below will be refreshed to show manufactured items.

Specify the Delivery Date and click [Next].

9. On the next step, the wizard offers consolidation options. Select No Consolidation and click [Next].

 <img src="../.assets/396c209a-03c0-4b9c-8f95-0aa7c5106fc7.png" alt="" width="100%" />

10. The final step shows the preliminary result of the wizard. Verify the table data and click [Next].

11. The System creates the requested orders. If an error occurs, the reason is shown in this table.

 <img src="../.assets/b1897c05-9b31-4d91-8234-0225a40e667d.png" alt="" width="100%" />

12. Use the golden arrow to open the created orders.

Regardless of the creation method, the result is a Production Order in the System. The order is created with Planned status and requires further processing.

# Processing a Production Order
The Production Order processing flow consists of:

* determining the current production-posting status
* exploding/generating lower-level Production Orders
* posting component issue and Receipt from Production
* closing Production Order chains
* writing off remaining balances

## Determining Current Status
### Open Production Orders (Standard SAP Report)

1. Open Main Menu → Production → Production Reports → Open Items List.

 <img src="../.assets/6486db07-7e6e-4b71-bc25-948433c8658d.png" alt="" width="100%" />

2. Verify the document type displayed in the window.

 <img src="../.assets/8621db67-5f6e-4c0f-a7e0-972a7c86d21f.png" alt="" width="100%" />

3. Filter the report to show Released orders.

 <img src="../.assets/7c54abe8-eec3-4618-a17f-bf158f39e12c.png" alt="" width="100%" />

4. Process the listed orders.

### Released Production Orders (User-Defined Report)

1. Open Query Manager from the Tool Panel.

 <img src="../.assets/176b4076-d573-4dff-a4d4-3d07a875406e.png" alt="" width="100%" />

2. Select the category and run report '202.1.3. Production Orders Requiring Closure (Released)'.

   <img src="../.assets/5f07c29f-55bd-4467-be2d-bc643d3979da.png" alt="" width="100%" />

3. Review the report and process the relevant orders.

 <img src="../.assets/483334df-9a2a-4419-bf51-9925c1f81c26.png" alt="" width="100%" />

### Component Issue Status (User-Defined Report)

1. Open Query Manager from the Tool Panel.

 <img src="../.assets/198f23d8-cb03-4789-8953-8e37ba28800a.png" alt="" width="100%" />

2. Select the category and run report '202.2.1. Semi-Finished Product Issue Status'.

 <img src="../.assets/46e244e7-bada-4c50-a9e9-fcf98eafde00.png" alt="" width="100%" />

3. Review the report and process the documents.

 <img src="../.assets/a49e8190-8735-4364-9159-ae438119b467.png" alt="" width="100%" />

### Child Production Order Creation Status (User-Defined Report)

1. Open Query Manager from the Tool Panel.

 <img src="../.assets/a535fff6-7fcd-4925-9d5b-d34de2a14df8.png" alt="" width="100%" />

2. Depending on the situation, run one of the available reports.

 <img src="../.assets/ee10b8e4-b19e-4c97-9bc2-e028cc226418.png" alt="" width="100%" />

3. Review the report and process the documents.

Summary report:

 <img src="../.assets/9f82d94c-f657-4860-a50b-46e5d404826d.png" alt="" width="100%" />

Detailed report:

 <img src="../.assets/d3bfb0a9-597a-452c-bb3e-e14a9d173aa9.png" alt="" width="100%" />

## Exploding Production Orders

1. Run the relevant report from Query Manager. In this example, report '202.3.4. Explosion Status (Details, All Orders)' is used.

2. In the report, filter the rows to show only positions for which child orders have not yet been created.  
<img src="../.assets/bbdf3b52-ef4d-46d6-ab56-b20920108ed0.png" alt="" width="100%" />

The report is now filtered.

 <img src="../.assets/6a122b1d-d429-46ea-b97f-c37d7962c5a2.png" alt="" width="100%" />

3. Open the parent Production Order by clicking the golden arrow.

4. Verify and, if necessary, adjust the order data.

5. Select the option to generate supply documents and click [Update] to save the changes.

 <img src="../.assets/a0825745-e093-4218-a597-fdd4d7bf3628.png" alt="" width="100%" />

6. The System starts the Procurement Document Generation Wizard. Click [Next].

 <img src="../.assets/8d500f21-7654-491e-8a85-92c0d3fc1a75.png" alt="" width="100%" />

7. On the next step, verify the parent-item information and click [Next].

 <img src="../.assets/2e7f67d1-46d7-401c-ba3d-23473130cb5e.png" alt="" width="100%" />

8. On the next step, change Target Document to Production Order and specify the Delivery Date. Verify quantities and component warehouses in the table. If necessary, select/deselect the rows for which Production Orders should be generated. Click [Next].

 <img src="../.assets/6c6c7967-ea6d-4ef3-a586-dc151fd2e35e.png" alt="" width="100%" />

9. On the following steps, select document generation without consolidation and review the preliminary calculation.

10. The System creates Production Orders for the selected positions.

 <img src="../.assets/7651ba7e-0311-43f7-83ec-4180c3d5096d.png" alt="" width="100%" />

11. Repeat the steps above to explode all semi-finished products down to the lowest level containing only raw materials. The final result should include Production Orders at every required BOM level:

 <img src="../.assets/eb1f7bed-015b-4987-86ec-404bc2ba95b7.png" alt="" width="100%" />

## Closing a Production Order: Component Transfer/Issue and Receipt from Production
Production Orders are closed from the deepest BOM level to the highest level as semi-finished products become available in stock. When components are issued for orders using FT/BK/ST warehouses, an Inventory Transfer between warehouses is required. For the central GN warehouse, this transfer is not required and components can be issued directly from GN.

1. Run report '202.1.3. Production Orders Requiring Closure (Released)' or open the Production Order by any other method.

 <img src="../.assets/164f83a1-146d-491e-a44b-1509f7a26132.png" alt="" width="100%" />

2. To create the transfer, right-click to open the context menu and select Component Transfer.

 <img src="../.assets/13c5b599-4e3f-4306-bbbf-8c1dd5700a73.png" alt="" width="100%" />

3. In the window that opens, choose the quantity calculation method:

* Open Quantity - component quantity taking into account quantities already issued earlier to the Production Order.
* Parent Item Quantity - component quantity calculated from the original requirement of the Production Order, without considering quantities already issued.

 <img src="../.assets/1625147e-556c-4f99-9d04-57576e39863f.png" alt="" width="100%" />

4. Verify and, if necessary, correct the source warehouse and target warehouse. In the SAP version installed when this instruction was written, there is a known issue where these fields may be populated with the System default warehouse. In this situation, reselect/change the warehouse in the Header to refresh the table data.

 <img src="../.assets/f684684f-563f-4270-a69e-955c12318c29.png" alt="" width="100%" />

5. Click [Add] to post the Inventory Transfer.

6. Once the required components are available in the warehouse, open the context menu and select 'Report Completion'.

 <img src="../.assets/abef4030-2298-48cd-a333-2ed3e85ffa1f.png" alt="" width="100%" />

7. The System opens the Receipt from Production document. This posts the semi-finished product receipt into stock. Components used in production are issued when the production receipt is posted.

Verify and, if necessary, adjust the table data (Warehouse, Key/Milestone, Department), then click [Add].

 <img src="../.assets/47dc3855-10a7-4918-a1f7-39f2442c3c08.png" alt="" width="100%" />

8. After components are issued and the product is received, change the Order status to Closed and save the changes.

9. Return to the Production Order and verify/change its Status to Closed.

10. Close the Production Order and return to step 1 to check whether other orders also require closure.

## Result of Posting the Production Order

The component row in the Production Order becomes closed for editing:

 <img src="../.assets/f5ff4900-24e6-44fb-bfd6-fe5fcf52f9d1.png" alt="" width="100%" />

The component issue is reflected in inventory movement and in the Journal Entry:

 <img src="../.assets/e55e9c72-2a25-48e9-9272-9b667d822ef2.png" alt="" width="100%" />

The product (in this example, a semi-finished product) is received into stock using Receipt from Production and reflected in the related Journal Entry:

 <img src="../.assets/a3061751-9c3a-4a80-a34d-29d7681170e1.png" alt="" width="100%" />
