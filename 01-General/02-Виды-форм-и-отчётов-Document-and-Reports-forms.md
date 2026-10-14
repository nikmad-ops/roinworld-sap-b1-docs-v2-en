# Types of SAP Business One Objects
## Master Data
This category includes master-data records such as Item Master Data, Business Partner Master Data, warehouses, etc. Data in each master-data object is stored as individual records (for example, an item record, business partner record, or warehouse record). Each record has an assigned Code (Item Code, Business Partner Code, Warehouse Code, etc.). The Code is a unique identifier. Two records with the same Code cannot be created within the same master-data object. In addition to the Code, each record contains attributes specific to that object (for items - units of measure and names; for business partners - names and company details).  
Data in a master-data record can be changed as follows:  
Changing the Code - possible until the record is first used in documents or configuration.  
Changing Data - unrestricted before first use; after transactions have been posted using the record, restrictions apply. For example, the Unit of Measure cannot be changed for an item that has stock on hand.  
Deleting a record is possible until it is first used in documents or configuration.

## Dropdown Lists / Secondary Data
This category includes datasets stored as tables and lists. Similar to Master Data, these records have a unique Code and a set of values associated with that Code. Lists can be system-defined (predefined datasets such as countries and taxes) or user-defined (datasets configured during implementation and subsequent use of the System). Lists simplify the completion of forms and documents: the user selects an available value from a drop-down list instead of typing free text. Lists also standardize field completion by ensuring consistent values. User-defined lists can be assigned to most fields available in the System. The selected list value can also be controlled by automation logic (for example: if Field A equals X, select value Y from the list in Field B).  
Deleting records from system lists is subject to restrictions.  
Deleting records from user-defined lists is possible if the record has not been used in a document or configuration.

## Marketing Documents
In SAP Business One, the term Marketing Documents covers the main transactional document types. These can be Sales, Purchasing, or Inventory documents. Each document has a unique technical identifier (DocEntry), incremented by +1 within each document type, and a user-facing document number (DocNum), incremented by +1 within each document type and numbering period (year). Several DocNum numbering series can exist in the System at the same time. For example, one numbering series can be used for Foodtruck orders (1 to xxx), and another for Bakery orders (1 to xxx). A numbering series can also include a prefix, for example FT2026\1 and BK2026\1.  
Marketing Documents are divided into documents that create accounting postings (actual documents) and documents that do not create postings (planning documents).  
Planning documents include: Sales Quotation, Purchase Request, Order, Draft, Inventory Counting, Production Order.  
Actual documents include: Delivery/Goods Receipt PO, A/R Invoice/A/P Invoice, Payment, Goods Issue, Goods Receipt.  
Documents cannot be deleted after they are saved, with the exception of Drafts.  
Planning documents can be changed while they have Open status. After they are closed, only comment fields remain editable.  
Actual documents cannot be changed. After they are saved, only comment fields remain editable.  
To correct the substance of a document, SAP Business One uses corrective/reversing documents. The document used depends on the business context. For example, if an A/R Invoice contains an error, an A/R Invoice Cancellation document can be created. If a discount or return has been agreed with the customer, an A/R Credit Memo is created instead.  
Inventory documents are reversed by creating a document with the opposite inventory movement (for example, Goods Receipt to reverse Goods Issue).

## Standard Reports
SAP standard reports are reports delivered by SAP. When a report is launched, the user can define filtering criteria. These are typically attributes from the primary data source used by the report (for example, Item Group and document dates for a sales report). Standard reports are generally displayed as plain tables. Some standard reports use a hierarchical structure, such as Customer/Vendor Ageing and Balance Sheet. The set of report fields is predefined and cannot be extended.

## Choose from List
A type of standard report generated on the fly. These reports create lists of Master Data or Documents based on criteria entered in the related document/master-data form. For example, an item list can be generated from Item Master Data while the form is in Find Mode. As the name suggests, a Choose from List report allows the user to open the relevant document/master-data record by clicking it. The set of fields in this type of report can be configured, but only fields available in the related document/master-data object can be added.

## Drag and Relate
A type of SAP standard report. This type of report is generated by dragging a field from an open document/master-data record onto the corresponding Main Menu section (see the separate instruction for this report type). The report field set is predefined and cannot be extended.

## User-Defined Reports
User-defined reports are reports created to meet user requirements. Their fields, calculation logic, and data sources are limited only by the data available in the database.

## Alerts
A type of user-defined report distributed through SAP internal mail. An alert can be configured to run when a specific event occurs in the System (for example, when a new document is created) or on a recurring schedule (for example, period sales sent once per day/week). Because the report is user-defined, its fields and logic can be configured to meet user requirements.

## Dashboards
A type of user-defined report whose distinctive feature is the online display of information directly on the user's desktop. The desktop refresh delay depends on configuration and is typically 1 to 3 minutes. The visual format of the widgets is predefined by the System, while the data displayed can be configured to meet user requirements.
