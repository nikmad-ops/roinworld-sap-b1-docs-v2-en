The System is configured to notify responsible employees when documents require processing.  
At regular intervals of X minutes, the Purchasing Manager receives an internal SAP mail notification about open (unprocessed) Purchase Requests.

 <img src="../.assets/c1c8828b-a350-4d14-8f33-2a40b8058828.png" alt="" width="100%" />

1. To review the Purchase Request, select the message in the upper part of the form. The message content is displayed in the lower part.

2. To open the Purchase Request, click the golden arrow in the Doc # column.

3. The Purchase Request document opens.

 <img src="../.assets/0d844d03-f0b2-4f4e-bcc3-7a2282b1f7d0.png" alt="" width="100%" />

The Purchase Request is a task to identify a Vendor and agree delivery dates and prices. Once a Vendor is selected and the supply conditions are agreed, this is reflected in the Purchase Request by completing the [Vendor] field.

## Creating a Purchase Order from a Purchase Request

Once the order has been placed with the Vendor and no further changes are expected, a Purchase Order is created from the Purchase Request.

1. Open Purchase Order from Main Menu → Purchasing - A/P → Purchase Order.

 <img src="../.assets/73afa457-5865-471f-914a-7f4e4d06464d.png" alt="" width="100%" />

2. Complete the Business Partner details, agreed delivery date, and, if applicable, the Vendor's order number.

 <img src="../.assets/0382f786-e700-4d74-9cd6-fed0753c45d9.png" alt="" width="100%" />

3. Click [Copy From] at the bottom of the form and select Purchase Request.

 <img src="../.assets/7b49911d-34db-42ad-9e6d-86a07dc0f2fa.png" alt="" width="100%" />

4. The System opens the list of active Purchase Requests.

 <img src="../.assets/4c11707d-74b9-48bc-9702-0aabbca39e12.png" alt="" width="100%" />

5. Select the required Purchase Request and click [Choose].

Note: multiple selection is available in this window. Hold [Ctrl]+[Shift] and select the documents with the mouse.

6. The Draw Document Wizard opens.

 <img src="../.assets/d3209698-65b7-438b-bf9b-0cc1ee192cfc.png" alt="" width="100%" />

7. Select [Choose] and click [Next].

8. The window for selecting rows to copy from the Purchase Request into the Purchase Order opens.

9. Hold [Ctrl] while selecting the required rows. A blue highlight means the row will be copied to the Purchase Order.

The Purchase Request is the source of the Quantity for each item. If a different quantity was agreed with the Vendor, enter the actual ordered quantity in the relevant column. If the ordered quantity is lower than the original requested quantity, the corresponding row in the Purchase Request remains open.

 <img src="../.assets/6f1a77c3-b77f-46c7-88df-e951be2fabd1.png" alt="" width="100%" />

10. After verifying Item, Quantity, Unit of Measure, delivery Warehouse, and Key/Department dimensions, click [Finish].

11. The System copies the selected rows to the Purchase Order table.

12. Verify the agreed Delivery Date and select your signature in the Owner field.

 <img src="../.assets/ad2e0817-4054-44ea-9647-6c1708721b21.png" alt="" width="100%" />

13. Verify the prices in the table.

14. Click [Add] to save the document.

## Result of Creating a Purchase Order

After the document is added to the System, the following updates occur:

### Purchase Request
Rows for which a Purchase Order has been created for the full requested quantity are closed. Closed rows are shown in gray.

 <img src="../.assets/9734b5c6-80a0-4c7f-a1e7-96e05092cc8f.png" alt="" width="100%" />

### Inventory Reports
The ordered quantity is shown in inventory reports as Purchases (Ordered).

 <img src="../.assets/cd4b06aa-2baa-471a-8288-078fe1be26e1.png" alt="" width="100%" />

### Notifications
The creator of the Purchase Request receives an internal SAP mail notification that the Purchase Request has been copied to a Purchase Order.

 <img src="../.assets/2f835115-d3e6-4d7f-be34-ed0de9329714.png" alt="" width="100%" />
