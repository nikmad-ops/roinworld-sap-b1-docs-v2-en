## Types of Inventory Issue Postings
SAP uses three main types of inventory issue movements:

* **Issue for Production**. The document is created by the System and linked to a specific Production Order. The cost of the issued materials is automatically included in the cost of the production output. In Roin World processes, these documents are configured to be created automatically when Receipt from Production is posted. Creation is described in the Production Posting section.
* **Inventory Difference Posting**. The document is created as a result of posting an Inventory Counting / Inventory Posting process. The cost of the issued inventory is posted to the expense account predefined for this document type. Creation is described in the Inventory Counting section. The document is linked to the inventory-counting document, identifying the issue as the result of a physical stock count.
* **Goods Issue**. The document is created manually and is not system-linked to another base document. Because of this, **Issue Reason** is mandatory so that the required analytics are available. The inventory cost is credited from the inventory account and debited to the expense account specified in the document rows.

## Issue Reasons
| Reason | Description |
|--------|-------------|
| **Consumption** | Items not used in Production and consumed internally by employees. |
| **Defective** | Items damaged during storage. |
| **Expired** | Items written off because their shelf life has expired. |
| **Leftover** | Semi-finished products produced for a parent Production Order but not consumed because the actual required quantity was lower. This can indicate inaccuracies in BOMs or Order Multiple settings. |
| **Shrinkage** | Loss caused by processing characteristics such as evaporation, trimming, or shrinkage. |
| **Theft** | Loss/theft identified outside the regular periodic inventory-counting process. |

## Preparing and Posting a Goods Issue

### Identifying Unissued Semi-Finished Product Balances
Important: checking balances for write-off of semi-finished products should be performed only after the relevant Production Orders have been fully closed.

1. Run the Query Manager report '202.2.1. Status of Semi-Finished Product Issues'.

 <img src="../.assets/9aef3f43-d67c-459b-9ac9-a09fb2c7890b.png" alt="" width="100%" />

2. In the report, filter the Status column using the rule Does Not Contain with the value 'Fully Issued'. This filters the report to show statuses that are not fully issued.

 <img src="../.assets/ef6a2930-7236-4b65-8c58-c4bff42e98de.png" alt="" width="100%" />

3. The table will then show semi-finished products that have not been fully issued to Production.

 <img src="../.assets/638c84e8-71ec-49b3-8243-468d66cebe7e.png" alt="" width="100%" />

4. Export the result to Excel for convenient data copying.

### Posting a Goods Issue

1. To post an inventory write-off, open Goods Issue from Main Menu → Inventory → Inventory Transactions → Goods Issue.

 <img src="../.assets/7acc1eff-17ef-4a76-9cc7-da83a93742d2.png" alt="" width="100%" />

2. Complete the Header:

(1) Posting Date  
(2) Issue Reason. It must correspond to the G/L Account used on the Contents tab.  
(3) Optionally specify a reference document, such as the Sales Order to which the write-off relates. If such a link exists, the cost can be attributed to the specific order.  

   <img src="../.assets/c44c1a71-a544-41bb-965c-3fc63ab67ea3.png" alt="" width="100%" />

   \
