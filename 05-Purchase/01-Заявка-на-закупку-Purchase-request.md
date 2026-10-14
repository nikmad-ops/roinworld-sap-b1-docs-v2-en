A Purchase Request is the entry point into the planned procurement process. The items and quantities specified in a Purchase Request are not reflected in inventory-status reports. This document is a request from business users/departments to the Purchasing Department - a formal request to procure goods or materials.

When a Purchase Request is created, a Vendor does not need to be specified. The Purchasing Department adds the Vendor information later.

The example below describes a Purchase Request for raw materials required for Production. If the Purchase Request is being created to replenish warehouse stock or to purchase items from a group intended for internal consumption, start from step 2 and skip the steps related to exporting the Demand report.

1. Generate the Demand report and export it to Excel.

2. Review and, if necessary, adjust the proposed order quantity.

3. In SAP, open Purchase Request from Main Menu → Purchasing - A/P → Purchase Request.

4. Complete the Header and specify the required delivery date.

 <img src="../.assets/341f58ac-888a-489c-b396-69cd25430147.png" alt="" width="100%" />

5. In the Demand report, filter the table to show purchased components only.

 <img src="../.assets/6e49d51c-65d1-43c5-b91c-1422147d1ae4.png" alt="" width="100%" />

6. Copy the Item Code column to the clipboard without the header.

For a large number of rows, use [Ctrl]+[Shift]+[Down Arrow], then [Ctrl]+[C].

7. Return to SAP. Place the cursor in the first row of the Item Code column.

<img src="../.assets/e2f2a81e-2a10-4382-b91d-a8e0b2ddb011.png" alt="" width="100%" />

8. Press [Ctrl]+[V].

 <img src="../.assets/4616e881-c85c-4839-84e0-7d68e138b033.png" alt="" width="100%" />

Repeat the same operation for the required quantities:

9. Return to Excel and copy the Order Quantity column to the clipboard.

10. Return to SAP, place the cursor in the **[Required Qty]** column in the first row of the Purchase Request, and press [Ctrl]+[V].

11. Verify the columns:

(1) Information about the items to be purchased  

(2) Complete Key/Milestone - the key to which the purchase relates.  
(3) Complete Department - the Company department to which the purchase relates.  
To copy the same value down the document, enter the value in the first row, place the cursor in the second row, and press [Ctrl]+[Up Arrow]. Repeat for all rows.

12. Complete the Owner field to sign the Purchase Request. Click the list button and select your signature.

<img src="../.assets/c9927ba7-d8a8-4002-b1cd-2561cd4a1122.png" alt="" width="100%" />

13. Click [Add] to save the Purchase Request.

The saved Purchase Request becomes available for processing by the Purchasing Department.
