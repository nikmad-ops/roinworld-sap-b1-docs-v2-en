# Returning Received Goods

There are two ways to return purchased goods:

<img width="794" height="121" alt="image" src="https://github.com/user-attachments/assets/7cbfa732-4437-4143-817c-df395ccdfb69" />

The following restrictions apply:

* The item must be available in the SAME warehouse and in the SAME quantity as in the document being reversed.
* If subsequent documents were created from the Goods Receipt PO, such as an A/P Invoice or Payment, reversal must always start from the last document in the chain.
* If goods from the Goods Receipt PO were used in production and then sold, reversal must start with cancelling the related sales and production documents.
* A Goods Receipt PO can only be cancelled within the cancellation period configured in the System (365 days).
* The cancellation document must use the same dates as the document being cancelled.

## Cancelling a Goods Receipt PO

To cancel a Goods Receipt PO:

1. Open the document to be cancelled and verify that it has Open status and no linked downstream documents.

<img width="1250" height="863" alt="image" src="https://github.com/user-attachments/assets/ab844a1b-2652-44b6-9fd1-a91f4f4de924" />

Verify that sufficient stock is available in the warehouse so that cancellation will not result in negative inventory. Use the relevant warehouse report for this check.

2. Right-click the grey area of the document header to open the context menu.

3. Select [Cancel].

<img width="935" height="342" alt="image" src="https://github.com/user-attachments/assets/70e70782-6211-4705-b345-ded88610aa36" />

4. The System opens a new cancellation document for the Goods Receipt PO.

<img width="935" height="342" alt="image" src="https://github.com/user-attachments/assets/6b5fc6c6-142c-49ea-9c7b-261b05a7ee06" />

5. Verify the dates of the cancellation document.

6. Click [Add] to post the document.

7. Review subsequent System messages and, depending on the business situation, confirm or reject reopening of the Purchase Order.

## Goods Return to Vendor

1. Open Goods Return from Main Menu → Purchasing - A/P → Goods Return.

<img width="416" height="186" alt="image" src="https://github.com/user-attachments/assets/b3b0e594-9e21-4aea-b7ff-9aa3b7ae8714" />

2. Complete the document header.

<img width="1023" height="227" alt="image" src="https://github.com/user-attachments/assets/f737a46d-3f2a-4286-baeb-6fc405ccf0be" />

3. Click [Copy From] and select Goods Receipt PO from the context menu.

<img width="321" height="102" alt="image" src="https://github.com/user-attachments/assets/ca994645-06a2-4516-9c4c-3f4ef965d388" />

4. The System displays the list of available source documents. Select the required Goods Receipt PO.

<img width="1153" height="148" alt="image" src="https://github.com/user-attachments/assets/57695f12-06ec-4626-942e-d5cb621df55a" />

5. The Draw Document Wizard opens. Select the required options and click [Next].

<img width="1477" height="768" alt="image" src="https://github.com/user-attachments/assets/c9d34e0d-ad81-48a2-abc1-239dc32d8303" />

6. Select the item rows to be returned. For a partial return, adjust the quantity in the Quantity column and click [Finish].

<img width="1473" height="461" alt="image" src="https://github.com/user-attachments/assets/9727f2bc-02b5-4810-9e28-2db35029d7b0" />

7. The data is copied to the Goods Return document.

8. Verify the document rows.

9. Specify the Return Reason and Return Type.

<img width="457" height="137" alt="image" src="https://github.com/user-attachments/assets/989fc4fe-1c31-480b-b286-0bc257b1424c" />

10. Click [Add].

11. The System displays a confirmation message. Depending on the context of the return, choose whether the corresponding rows in the base Purchase Order should be reopened or remain closed.

<img width="679" height="233" alt="image" src="https://github.com/user-attachments/assets/ecfdf733-1487-4c41-9548-aff94179e938" />

12. Posting the Goods Return creates a transaction reversing the Goods Receipt PO transaction.

<img width="867" height="86" alt="image" src="https://github.com/user-attachments/assets/4d9f33c0-a58c-461a-aadf-e8e92961f57b" />
