# Small-Cost Asset Management

## Notes

1. In this instruction, a Small-Cost Asset means any asset that does not meet the definition of a fixed asset managed in the corresponding SAP Business One module.
2. A Financially Responsible Person is an employee who has full material responsibility for Company property assigned to them.

## Master Data

**Small-Cost Asset** — an inventory item purchased into stock through the Purchasing module. A Small-Cost Asset must first be purchased into the Company's central warehouse and only then issued to an employee.

**Small-Cost Asset Warehouse** — a dedicated warehouse with configured G/L account determination rules and virtual bin locations.

**Financially Responsible Person** — represented by a virtual bin location in the Small-Cost Asset warehouse. The bin code is the employee code and the bin description is the employee's first and last name.

## Bin Location Example

<img width="618" height="117" alt="image" src="https://github.com/user-attachments/assets/0dc5afc1-9f8d-43f1-b365-a08edeb1d0cc" />

## Posting the Issue

Issuing a Small-Cost Asset to an employee is recorded in the System by transferring the item to the bin location associated with the Financially Responsible Person.

1. From the Main Menu, open Inventory → Inventory Transactions → Inventory Transfer.

<img width="351" height="229" alt="image" src="https://github.com/user-attachments/assets/1136ebed-85fc-4d79-ba95-f2bf00643028" />

2. Enter the item code in the form.

<img width="1331" height="105" alt="image" src="https://github.com/user-attachments/assets/d8049264-596d-4b0e-a099-2d3b91f832d9" />

3. In the To Warehouse field, select warehouse FRP.

4. In the Quantity field, enter the quantity being issued.

5. After completing the row, click the Golden Arrow in the To Bin Locations field. In the window that opens, select the target bin location corresponding to the employee.

<img width="1507" height="660" alt="image" src="https://github.com/user-attachments/assets/35c32b0a-5dcf-4cff-8089-18313c6689c5" />

6. Click [Update], return to the document, and verify the entered data.

<img width="1252" height="87" alt="image" src="https://github.com/user-attachments/assets/c88f6f42-52d3-4db0-b636-abab25097734" />

7. Click [Add] to post the inventory movement.

## Checking Issued Small-Cost Assets by Warehouse

1. Open the Bin Location Content List report.

2. Review the report-selection criteria and adjust them if necessary.

<img width="780" height="558" alt="image" src="https://github.com/user-attachments/assets/f75a1892-8279-4ce1-b39d-3f62ed027c9c" />

3. The System opens the report. The example below shows the hierarchical view.

<img width="1671" height="420" alt="image" src="https://github.com/user-attachments/assets/65584d83-a7ec-49b4-ac74-298a7ffb430f" />

## Accounting Impact

When the Small-Cost Asset is transferred, the System creates a Journal Entry using the dedicated G/L account.

<img width="1082" height="71" alt="image" src="https://github.com/user-attachments/assets/1522fa89-088f-470f-92ab-e23ec606965d" />

<img width="1389" height="676" alt="image" src="https://github.com/user-attachments/assets/2164d313-4212-4400-a943-40019520210d" />
