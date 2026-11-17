## Meals

A Meal / Set is a way to combine dishes into a single inventory item. In SAP Business One, this is implemented using an additional Bill of Materials level with BOM Type set to Production.

### Notes

1. In this instruction, the terms Set and Meal are used as equivalent.
2. Meals use a dedicated numbering series with prefix M. The series determines the validation rules applied by the System when documents are created.
3. Meals use a dedicated Item Group that determines accounting-posting rules and G/L account determination.
4. The cost of a sold Meal is determined by the cost of the dishes and other components issued to production.
5. A clear and consistent naming convention should be used for Meals to avoid duplicate Item Master Data records and BOMs caused by an inability to find an existing record.

### Structure

<img width="616" height="507" alt="image" src="https://github.com/user-attachments/assets/b0b0ada8-5731-4f53-912f-4d5d1d48ac82" />

### Creating Meal Item Master Data

Before creating a new Meal Item Master Data record, make sure that a similar record does not already exist in the System.

1. From the Main Menu, open Inventory → Item Master Data.

2. The System opens Item Master Data in Find Mode. Switch the form to Add Mode using [Ctrl]+[A] or the corresponding toolbar button.

3. Complete the Item Master Data header as follows:

(1) Select the Meals numbering series from the drop-down list.  
(2) Enter the Meal name in English and Arabic.  
(3) Select the Inventory Item and Sales Item properties. Clear Purchase Item.  
(4) Select the Meals Item Group and verify that the Unit of Measure Group is set to Each.  
(5) Enter the Russian name.  
If the record is being created in the test system, the name field is located in the additional side panel. To display it, press [Ctrl]+[U].

<img width="1166" height="211" alt="image" src="https://github.com/user-attachments/assets/7011c6c8-bf35-43b7-b23b-f362d15dd9f2" />

4. Go to the General tab and complete it as follows:

(1) Select Subject to Withholding Tax. This allows deferred/withholding tax to be used for the Meal without making it mandatory.  
(2) Verify that Manage Item By is set to None.  
(3) Verify that the item status is Active. If the record is being completed over several sessions, keep it Inactive until all required information is entered.

<img width="1166" height="642" alt="image" src="https://github.com/user-attachments/assets/ee36d59e-be32-4052-9e2a-51b3069df916" />

5. Go to the Purchasing Data tab:

(1) Even though the item was excluded from purchasing in step 3, verify and set the purchasing unit of measure. For Meals, the standard value is EA.  
(2) Specify the tax code applicable to the Meal. Whether that tax code is actually applied in a document is determined by the System when the document is created, based on the Business Partner settings and other criteria.

<img width="1166" height="469" alt="image" src="https://github.com/user-attachments/assets/5e17ccbe-62a1-4f09-9391-e81de7922ca2" />

6. Go to the Sales Data tab:

(1) Specify the sales tax code applicable to the Meal. Whether it is applied in a document is determined by the System based on Business Partner settings and other criteria.  
(2) Verify and set the sales unit of measure. For Meals, the standard value is EA.

<img width="1166" height="314" alt="image" src="https://github.com/user-attachments/assets/d73b72ac-58c2-4f94-8b5f-2587bad8a5fd" />

7. Go to the Inventory Data tab:

(1) Set Inventory Valuation By to Warehouse.  
(2) Enable Manage Inventory by Warehouse.  
(3) Verify and set the inventory unit of measure. For Meals, the standard value is EA.  
(4) Verify and set the inventory-counting unit of measure. For Meals, the standard value is EA.  
(5) Set Valuation Method to FIFO. For manufactured items, this provides more accurate cost tracking.  
(6) Select the row for the Company's main warehouse and click [Set Default Whse]. This allows the warehouse field to be populated automatically in future documents.

<img width="1166" height="516" alt="image" src="https://github.com/user-attachments/assets/177d0bac-0c77-4613-9ea1-aba3c9d2b3ff" />

8. Go to the Planning Data tab:

(1) Planning Method — MRP.  
(2) Procurement Method — Make.  
(3) Component Warehouse — use the warehouse from the higher-level document row.  
(4) Order Multiple — 1, because a Meal can only be ordered and produced in whole units.

<img width="1166" height="266" alt="image" src="https://github.com/user-attachments/assets/b1709de8-3344-4e3c-b0e0-5dbb95cf1001" />

9. Go to the Production Data tab:

(1) Clear Phantom Item.  
(2) Set Issue Method to Backflush so that the Meal components are issued automatically without a separate manual Goods Issue.  
(3) Verify that Standard Production Cost is zero.

<img width="1166" height="333" alt="image" src="https://github.com/user-attachments/assets/5b42d214-5095-4fe2-b62f-bd5b840eec1e" />

10. Review all values, note the item code assigned to the new record, and click [Add] to save it.

### Creating the Meal Bill of Materials

After the Item Master Data record has been created, define the components of the Meal.

1. Open the previously created Meal Item Master Data record. Correctly created Meal items receive an item code in format Mxxx, where M is the Meals prefix and xxx is the sequential record number.

2. Right-click an empty grey area and select Bill of Materials from the context menu.

<img width="660" height="335" alt="image" src="https://github.com/user-attachments/assets/471dd38f-2838-498a-a9e1-06407ae3a0dd" />

3. The System opens the Bill of Materials form. Complete the header as follows:

(1) Verify that Product No. and Product Description are correct.  
(2) Verify that Quantity is set to 1. Component quantities in the table will therefore be treated as the composition of one Meal.  
(3) Set BOM Type to Production.  
(4) Select the Company's main warehouse (GN).  
(5) In the Distribution Rule field, open the selection window and set Key/Milestone to RWE and Department to KT (Kitchen). Click [Update] and return to the BOM.

<img width="1166" height="379" alt="image" src="https://github.com/user-attachments/assets/28bad407-0206-4531-bd12-9494812a405d" />

4. Complete the BOM rows by entering each dish included in the Meal. Verify that the Warehouse column is set to GN and enter the correct quantity for each component.

<img width="1166" height="178" alt="image" src="https://github.com/user-attachments/assets/98b62680-2542-4881-b779-9566e6d4b0d3" />

5. Click [Add] to save the BOM.

6. The Meal BOM is ready for use.
