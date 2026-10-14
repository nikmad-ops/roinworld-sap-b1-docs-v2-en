## Bill of Materials Types

SAP Business One supports the following Bill of Materials (BOM) types:

| Type | SAP Name | Purpose | Specifics |
|------|----------|---------|-----------|
| Assembly | Assembly | Not used in the Roin World project | |
| Sales | Sales | Used for items sold through the POS (Foodtruck). No production process is started. When the parent item is added to a sales document, the BOM components are added to that document. When the sales document is posted, the components are issued from inventory. | The parent item must be a non-inventory item. |
| Production | Production | Used for all manufactured items: Finished Goods and Semi-Finished Goods. | The parent item is an inventory item. Production posting is required. |
| Template | Template | Not used in the Roin World project | |

## BOM Levels

BOM levels are created when child BOMs (semi-finished products) are included in a parent BOM. The maximum nesting depth is limited only by System performance. SAP recommends keeping nesting to approximately 10-15 levels. In practice, each production level requires BOM explosion and posting of a separate Production Order.  
(1) First-level BOM  

(2) Second-level BOMs  

 <img src="../.assets/e7265384-4e78-410c-86e7-6c977d2469e7.png" alt="" width="100%" />

## Viewing a Bill of Materials

A BOM can be opened in one of the following ways:

* From the Main Menu: Production → Bill of Materials
<img src="../.assets/479fead9-05e0-4124-bc2f-4fb768a9fbe8.png" alt="" width="100%" />

\  
* From Item Master Data. On the Production Data tab, click the golden arrow in the Bill of Materials Type field.

  <img src="../.assets/2772f250-d45c-47a7-b694-77b1f0448bf5.png" alt="" width="100%" />

\

\

\

\  
* From Item Master Data. On any tab, right-click to open the context menu and select Bill of Materials.

  <img src="../.assets/0a4755b2-a83b-4bc9-832f-79d8c81abf31.png" alt="" width="100%" />

\

\

\  
## Additional Quantity and Planned Average Production Quantity

(!) Use of this mechanism is optional. Initially, all BOMs were loaded without these fields being populated.  
These fields are used to add a fixed quantity of a component for a defined production batch size.  
The [Planned Average Production Quantity] field specifies the quantity of the parent item produced in one production run. For example, a pancake pan may produce 4 pancakes per run.  
The [Additional Quantity] field specifies the quantity of a component consumed once per production run.  
In other words, if a Production Order is created for 8 pancakes, the Additional Quantity will be calculated/issued twice. An order for 2 pancakes will include the Additional Quantity once.  
(The base component quantity is still calculated for every additional pancake in the order.)

## Creating a Bill of Materials

To create a new BOM:

1. Open Item Master Data and open the Bill of Materials form from the context menu.

 <img src="../.assets/b25b7e36-1713-43a4-8d53-be0e1cf807dd.png" alt="" width="100%" />

\

\

\  
2. Complete the BOM header and table.  
(1) Enter the code/name of the manufactured item, select the BOM type, and specify the quantity of the parent item for which the component quantities in the table are defined.  
(2) Enter the code/name of the components required for production.  
(3) Specify the warehouse from which the components will be issued. Material requirements will be generated for this warehouse.  
(4) Specify the component quantity required for the parent quantity entered in item (1).  
(5) Specify the Additional Quantity taking into account the Planned Average Production Quantity.  
(6) Verify the price source for the components (at the time this instruction was written: Base of Purchase). The price is populated if a price has been maintained for the item in the relevant price list. This is an estimated cost; the actual cost is calculated in the Production Order based on the actual cost of the components issued to the order.  
(7) Specify Key/Milestone and Department dimensions for each row. These will be used when components are issued.  
(8) Specify Key/Milestone and Department dimensions in the header. These will be used for the parent item receipt.  
(9) Click the Down Arrow button to calculate and save the estimated production cost based on the BOM.

 <img src="../.assets/8d3d5795-c4ba-4dc3-8af8-e98b4a7d1854.png" alt="" width="100%" />

3. Optionally, row-level remarks and text rows describing production/technology specifics can be added to the BOM.

4. Click [Add] to save the changes.
