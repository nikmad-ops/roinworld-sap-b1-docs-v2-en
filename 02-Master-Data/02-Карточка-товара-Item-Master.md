## Item Code and numbering

The Item Code is the unique identifier of an item in SAP Business One. Two approaches are used to generate the code:

* manual numbering, used for items coming from iiko. The iiko item code is used as the SAP Item Code; these items use the Manual numbering series
* automatic numbering, used for items that exist only in SAP. At the time this instruction was written, these are service items (Admin, Selling, and Utilities expenses)

| Numbering Series | Prefix | Description | Example Code |
|------------------|--------|-------------|--------------|
| AdmExp | S22x | Administrative (general) expenses | S220 Audit fees |
| SellExp | S11x | Selling expenses | S110 - Freight |
| UtilExp | S21x | Utilities expenses | S210 - Electricity |

 <img src="../.assets/d0965f30-f46f-4083-b3ad-368111085ba6.png" alt="" width="100%" />

## Item Group

The Item Group is an attribute that groups items according to posting logic and usage rules. At Item Group level, SAP defines G/L account determination rules and controls for the completeness and quality of the Item Master Data. The main principles are shown below.

| Group Name | Group Description | Inventory\Sales\Purchase | Special Conditions | Accounts |
|------------|-------------------|----------------------------|--------------------|----------|
| Finished Goods | Finished products | Yes\Yes\No | A Bill of Materials is required before the item can be activated | Inventory Production Item, COGS Production, Revenue Production Exempt\Taxable |
| Semi-Finished Goods | Semi-finished products | Yes\No\No | A Bill of Materials is required before the item can be activated | Inventory Semi-Finished, COGS Production, Revenue Exempt\Taxable |
| Raw Materials | Raw materials, ingredients | Yes\No\Yes | Withholding Tax setting is required before the item can be activated | Inventory Raw Materials, COGS Goods for Resale, Revenue Goods for Resale Exempt\Taxable |
| Package and Tableware | Packaging and tableware | Yes\Yes\Yes | Withholding Tax setting is required before the item can be activated | Inventory Package, COGS Goods for Resale, Revenue Goods for Resale Exempt\Taxable |
| Goods for Resale | Goods for resale | Yes\Yes\Yes | Withholding Tax setting is required before the item can be activated | Inventory Good for Resale, COGS Goods for Resale, Revenue Goods for Resale Exempt\Taxable |
| Non-Trade Inventory | Items for internal consumption | Yes\No\Yes | Withholding Tax setting is required before the item can be activated | Inventory Non-Trade |
| Services | Services, S-items | No\No\Yes | Only items using a service numbering series | Expense accounts are assigned individually |

## Item Properties

Item properties determine whether the item can be used in specific document types and how it is reflected in inventory/accounting.  
Inventory Item - the item is managed in stock and appears in inventory reports and documents such as Goods Receipt, Goods Issue, and Inventory Counting.  
Sales Item - the item can be used in sales documents such as Sales Order, Delivery, and A/R Invoice.  
Purchase Item - the item can be used in purchasing documents such as Purchase Request, Purchase Order, Goods Receipt PO, and A/P Invoice.  
<img src="../.assets/cdd81f7d-8071-41b4-8acb-36811eda8f6d.png" alt="" width="100%" />

## Minimum Required Information

For correct use of an Item Master Data record, a minimum required set of information must be maintained. The data in the record must not contradict each other. A correctly completed item record ensures that, when the item is used, the System fills all required document fields, assigns the correct tax, and generates the correct accounting postings. The minimum required information includes:

* Numbering (cannot be changed after the item is first used in a document)
* Item name in 3 languages
* Item Group and Item Type (cannot be changed while stock is available)
* Tax settings
* Units of Measure and conversion rules (cannot be changed while stock is available)

Please note that validation procedures have been implemented to control this minimum data set. The System will not allow the record to be saved with the item status Active if the required minimum information is incomplete. For intermediate saving as a draft, the item can be saved with status Inactive.

 <img src="../.assets/e0031961-d450-464f-be90-adb67ee859b6.png" alt="" width="100%" />

## Creating Item Master Data

If you need to create items in bulk, contact support. In this case, the OITM template must be completed and uploaded using administrative tools. Service items must always be created through support because G/L account usage rules need to be configured. If approximately 10 records need to be created, it is usually faster to create them directly in the interface.

To create an Item Master Data record:

1. From the Main Menu, open Inventory → Item Master Data.

<img src="../.assets/799f3abe-620d-4d9a-8f79-03df1eb85ebf.png" alt="" width="100%" />

2. The System opens Item Master Data in Find Mode (yellow fields). Switch to Add Mode by pressing [Ctrl]+[A].

3. Open the additional panel with user-defined fields by pressing [Ctrl]+[Shift]+[U]. The side panel will be shown (or hidden if it was already open).

<img src="../.assets/c4e91703-b4f3-4e86-98bc-a3136ce53273.png" alt="" width="100%" />

4. Complete the record header.  
(1) Select the [Manual] numbering series from the drop-down list.  
(2) Enter the iiko code. The code must be unique and must not be used by another item.  
(3) Enter the English item name in CAPITAL LETTERS and the Arabic item name. If the Arabic name is not yet available, the [#] character may be used temporarily. This will include the item in the follow-up notification report.  
(4) Set Item Type to [Items] and select the appropriate Item Group.  
(5) Select the Unit of Measure Group.  
(6) Set the Item Properties.  
(7) Create the item barcode (EGS code) by clicking the [...] button.

<img src="../.assets/1dca7501-816e-41b0-ae60-4827abdfc9c2.png" alt="" width="100%" />

4.1. In the window that opens, enter the EGS code in format EG-xxxx-yyyy, where EG is the fixed prefix, xxxx is the Roin World tax ID, and yyyy is the item code (iiko code). Click [Update].

<img src="../.assets/723f5485-42d9-4d56-b98c-5f17b2863bf5.png" alt="" width="100%" />

5. Go to the General tab.  
(1) Select Subject to Withholding Tax. This activates the Withholding Tax assignment mechanism during purchasing.  
(2) If applicable, enter the additional item code.  
(3) Verify that batch or serial-number management is not enabled.  
(4) Set the item status. If the minimum required data is not yet available, the System will allow the record to be saved only with status Inactive.  
(5) A comment about the item status can be entered in Remarks, for example: "Name translation required".

<img src="../.assets/3df77e24-aac2-465f-b907-078952450472.png" alt="" width="100%" />

6. Go to the Purchasing Data tab.  
(1) Verify that the correct Purchasing UoM is selected. It will be used by default in purchasing documents. This UoM can differ from those on other tabs. In a specific document, it can be changed to another UoM defined in the Unit of Measure Group.  
(2) Optionally, enter the item's size and weight characteristics. These values can later be used in reports.

<img src="../.assets/f5fdfcab-57b7-496b-9e22-c74bc4c74761.png" alt="" width="100%" />

7. Specify the tax code applicable to purchasing.

<img src="../.assets/cbfc54bc-5081-4600-ba9e-003c0e92007a.png" alt="" width="100%" />

8. Go to the Sales Data tab.  
(1) Specify the tax code applicable to sales.  
(2) Verify that the correct Sales UoM is selected. It will be used by default in sales documents. This UoM can differ from those on other tabs. In a specific document, it can be changed to another UoM defined in the Unit of Measure Group.  
(3) Optionally, enter size and weight characteristics. These values can later be used in reports.

<img src="../.assets/097a1615-a11e-4ab7-bdd9-490b769eb17a.png" alt="" width="100%" />

9. Go to the Inventory Data tab.  
(1) From the drop-down menu, select Set Inventory UoM and specify the warehouse inventory unit of measure. This UoM will be used by default for opening balances and production. If weight is entered, the System will offer to recalculate the weight on the Purchasing Data and Sales Data tabs using the Unit of Measure Group conversion rules.  
(2) Set the Inventory Counting UoM.  
(3) For advanced stock planning, select or clear the Manage Inventory by Warehouse option. If selected, the Minimum Inventory value (4) is maintained separately for each warehouse. If cleared, the minimum quantity is maintained for the Company as a whole. This value can be used by Purchasing when planning replenishment and maintaining safety stock.  
(5) Set the valuation method as follows: manufactured items (Finished Goods and Semi-Finished Goods) - FIFO; all other Item Groups - Moving Average.

<img src="../.assets/d98e9a70-905f-4590-8f60-96004e247897.png" alt="" width="100%" />

10. Go to the Planning Data tab.  
(1) Set Planning Method to MRP for all items except internal-consumption items. Set Procurement Method to Buy for purchased items and Make for Finished Goods and Semi-Finished Goods.  
(2) Set Order Multiple to the quantity that the System should use when calculating material requirements (for example, a dessert can only be produced in batches of 16 pieces, or soft drinks can only be purchased in packs of 24 cans).

<img src="../.assets/8bc10bbd-2ab4-4928-ac46-d7347ed8f7a6.png" alt="" width="100%" />

11. Go to the Production Data tab and set Issue Method to Backflush. In this case, the item will be issued automatically when Receipt from Production is posted for the parent item in the Production Order. In other words, the Goods Issue will be created without additional user action.

<img src="../.assets/85e94760-9892-4572-9ef2-5bbef969b489.png" alt="" width="100%" />

12. Open the additional panel and complete the Russian Name and nutrition fields (calories/protein/fat/carbohydrates).

<img src="../.assets/42c7b8e7-0e32-4b06-b0f2-73fe6de6d0d3.png" alt="" width="100%" />

13. If the item being created is a manufactured item, set the item status to Inactive.

14. Verify that all required fields in Item Master Data are completed and click [Add].

15. For manufactured items, create the Bill of Materials and then change the item status to Active.

As a result, the Item Master Data record is added to the System and becomes available for use.
