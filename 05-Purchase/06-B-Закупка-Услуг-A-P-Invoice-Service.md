# Service Procurement

This instruction describes service procurement using a contract with automatic monthly invoice generation as an example. Of all steps described below, the technically mandatory document is the A/P Invoice.

## Specifics

An A/P Invoice using a service item does not require a base document. In other words, the A/P Invoice can be created without a preceding Purchase Order or Goods Receipt PO.

## Process

1. Create a recurring transaction template for the A/P Invoice (optional).
2. Create the Purchase Blanket Agreement.
3. Approve the Purchase Blanket Agreement.
4. Process recurring transactions.

## 1. Creating a Recurring Transaction Template for the A/P Invoice

A recurring transaction template allows a prepared document to be reused.

1. From the Main Menu, open Purchasing - A/P → Recurring Transaction Templates.

<img width="379" height="178" alt="image" src="https://github.com/user-attachments/assets/43adbed2-59d3-4f18-b157-212df51280fa" />

2. In the window that opens, leave the criteria blank and click [OK].

<img width="565" height="399" alt="image" src="https://github.com/user-attachments/assets/b9694818-5b5c-4e2f-afaa-43c5669adfca" />

3. The System opens the list of existing templates.

<img width="1530" height="160" alt="image" src="https://github.com/user-attachments/assets/81de6eb5-c021-4c33-b352-150b1f4762d2" />

Complete a new row as follows:

(1) Enter a unique 7-character code.  
(2) Enter the template description. If the field is not visible, use Form Settings to display it.  
(3) Configure the recurrence frequency.  
(4) Click the button in the Document Number field.

4. In the window that opens, click [New] to create a new draft.

<img width="722" height="407" alt="image" src="https://github.com/user-attachments/assets/00059e65-e44e-460e-a1d7-a9deba8f2682" />

5. Complete the A/P Invoice form exactly as the document should appear when it is generated each month.

<img width="1670" height="627" alt="image" src="https://github.com/user-attachments/assets/926d6e8c-23e9-49c8-a6ba-0ab5b83d1077" />

6. Click [Add Draft].

<img width="411" height="72" alt="image" src="https://github.com/user-attachments/assets/d9aa0a18-df98-4305-b75c-0d55e8e361a8" />

7. Close the A/P Invoice form and return to the recurring-transaction-template table.

8. Click the button in the Document Number field and select the draft created in the previous step. Click [Choose].

<img width="826" height="527" alt="image" src="https://github.com/user-attachments/assets/dc17e132-b250-4e73-9bd3-8540caf47e76" />

9. Click [Update] to save the new template.

## Purchase Blanket Agreement

A Purchase Blanket Agreement in SAP can be Item Type or Monetary Type. It can be configured to generate linked documents periodically or to operate without recurring-document generation.

### Agreement Types

**Item Type** — defines delivery of specified items at agreed prices during the agreement validity period.

**Monetary Type** — defines purchases from an unspecified list of items/services within an agreed total amount and validity period.

### Agreement Status

**Draft** — all fields can be edited. The agreement cannot be used in documents.  
**Approved** — editing is restricted. The agreement can be used in documents.  
**On Hold** — some fields remain editable. The agreement cannot be used in documents.  
**Terminated** — the agreement has ended and cannot be used in documents.

## Creating the Purchase Blanket Agreement

1. From the Main Menu, open Purchasing - A/P → Purchase Blanket Agreement.

<img width="291" height="179" alt="image" src="https://github.com/user-attachments/assets/8a48d517-1d37-4adf-bb08-1589fe7115fc" />

2. The agreement form opens in Find Mode (yellow fields). Press [Ctrl]+[A] to switch to Add Mode.

3. Complete the header:

(1) Vendor.  
(2) Contract/agreement number.  
(3) Agreement Method — Monetary.  
(4) Agreement validity dates.  
(5) Signing date.  
(6) Optionally, enter a free-text Description.

<img width="754" height="251" alt="image" src="https://github.com/user-attachments/assets/29e8b4c6-320f-41b4-b388-29ef02a69260" />

4. Continue with the tabs.

5. On the General tab, complete only the fields indicated in the screenshot.

<img width="1166" height="197" alt="image" src="https://github.com/user-attachments/assets/7d8929dd-c438-4aea-b6d4-81c54116e189" />

6. On the Details tab:

6.1. Enter the total planned contract amount in Planned Amount.

6.2. Double-click the row number to open the details and enter the planned amounts. The example shows monthly amounts. Click [Update] when finished.

<img width="1168" height="100" alt="image" src="https://github.com/user-attachments/assets/9e0960f4-df6c-4036-bf8b-6d78cffe9be9" />

<img width="1311" height="448" alt="image" src="https://github.com/user-attachments/assets/35928b10-64ed-4bc6-a41a-b0a7117226e5" />

7. On the Recurring Transactions tab, click the Template field and select the template created in step 1.

<img width="1060" height="519" alt="image" src="https://github.com/user-attachments/assets/683094dc-8449-4de2-a2a8-23522d8ed17b" />

8. Click [Add] to save the agreement.

<img width="292" height="69" alt="image" src="https://github.com/user-attachments/assets/42ba8c2b-c30b-4fcc-a899-6635570a166b" />

## Approving the Agreement

1. When the agreement with the Vendor has been signed, change its status on the General tab from Draft to Approved.

2. After the status is changed, add the agreement number to the A/P Invoice draft/template. This is required for the generated A/P Invoice to be linked to the Purchase Blanket Agreement.

3. Open the approved agreement, go to the Recurring Transactions tab, and open the draft through the linked template.

<img width="923" height="299" alt="image" src="https://github.com/user-attachments/assets/234f03c8-5b9e-4c94-b820-ae2564bf47ca" />

4. In the draft rows, select the created Purchase Blanket Agreement in the corresponding field.

<img width="1668" height="768" alt="image" src="https://github.com/user-attachments/assets/99c828e4-8e10-46f1-83ca-b6e6e59a1951" />

5. Save the changes by clicking [Save as Draft].

## Processing Recurring Transactions

1. When a user with the recurring-transaction notification enabled logs into the System, the Recurring Transactions Confirmation window opens.

<img width="888" height="709" alt="image" src="https://github.com/user-attachments/assets/881b3fd9-ac94-45cb-98ac-2626870d9c5c" />

2. Select the transactions to process and click [Execute].

<img width="889" height="486" alt="image" src="https://github.com/user-attachments/assets/a10b4b5c-7cfa-414a-85da-e186693115b6" />

3. The document is processed automatically without further user input. If an approval procedure is configured for this document type, the generated document is sent for approval.

<img width="703" height="189" alt="image" src="https://github.com/user-attachments/assets/854c01b8-64f2-4c7c-b070-d7748fc08af0" />

# Result

## Purchase Blanket Agreement

The Purchase Blanket Agreement form displays all documents whose rows contain a reference to that agreement.

The Details tab shows the amounts against the agreement:

<img width="1167" height="301" alt="image" src="https://github.com/user-attachments/assets/532ffa27-4b73-48cd-bcfe-eb4ed98a9787" />

The Documents tab shows the list of linked documents:

<img width="1524" height="272" alt="image" src="https://github.com/user-attachments/assets/d17db3ea-4c5b-48d3-a6d8-9b6fc9288222" />
