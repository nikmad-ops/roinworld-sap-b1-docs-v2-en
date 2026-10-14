## Numbering
Unlike most other document types, whose numbering is limited to a financial period (year), Journal Entries use their own continuous numbering sequence from 1 to 2,147,483,647. This setting allows uninterrupted posting regardless of the financial period.

## Types of Journal Entries
By creation method, Journal Entries are divided into two types:

* **Automatic** - a posting created by the System when a document affecting the Company's General Ledger assets or liabilities is created.
* **Manual** - a posting created by a user by completing the Journal Entry fields.

Visually, Automatic Journal Entries differ because they contain a reference to the originating document.  
Automatic:  
 <img src="../.assets/4bd40771-1626-493a-b9ca-1fc3bd9ac590.png" alt="" width="100%" />

Manual:  
 <img src="../.assets/c5026a98-adb7-4c6a-ba42-35c758658a4f.png" alt="" width="100%" />

## Layout
Like other SAP documents, a Journal Entry consists of a Header and a document matrix containing rows/tables. The layout is described below using the example of recording payroll accrual and payment.

## Entry Specifics
In SAP Business One, all Journal Entries are recorded in at least two currencies: Local Currency and System Currency. Optionally, an entry can also be recorded in a Foreign Currency. In that case, the Foreign Currency entry must also be balanced. Availability of Foreign Currency posting depends on the currency settings of the account used.

## Example of Creating a Manual Journal Entry
To create a manual Journal Entry:

1. Open Journal Entry from Main Menu → Financials → Journal Entry.

   <img src="../.assets/80dc4541-1099-41cf-929d-70f9201abf3a.png" alt="" width="100%" />

2. Complete the Header fields.

(1) Posting Date - if due-date control is required, also complete the Due Date field.  
(2) Remarks - free-text field.  
(3) Reference data that can later be used in reporting.  
<img src="../.assets/62eb20c7-7e7d-42e4-91d0-c42d1f848b9b.png" alt="" width="100%" />

3. Complete the table on the [Contents] tab.

Data can be entered in Collapsed View directly into the row columns, or in Expanded View using the detailed fields:  
<img src="../.assets/e79ee0f8-6738-46d1-8b3c-388fdf653156.png" alt="" width="100%" />

In Expanded View, the displayed fields relate to the row currently selected in the table.

 <img src="../.assets/00a20c5c-87ea-423c-9450-226c9ece2c4b.png" alt="" width="100%" />

4. To enter/select an account, place the cursor in the G/L Account/BP Code field and press:

a) [Tab] to select a General Ledger account  
b) [Ctrl]+[Tab] to select a Business Partner  

Depending on the key combination, the System opens either (a) the List of Accounts or (b) the List of Business Partners.

5. For the selected account, enter:

(1) Debit or Credit amount.  
(2) The System calculates the amount in System Currency using the System Currency exchange rate on the Posting Date.  
(3) To display Foreign Currency amount fields, select [Display FC].  
(4) For Expense accounts, specify Key/Milestone and Department dimensions.

   <img src="../.assets/208ba4f5-82f4-4e48-867b-6781d7f643ac.png" alt="" width="100%" />

5.1. When using Foreign Currency fields, enter the amount together with the currency code in format [xxx.xx RUB]. The Debit/Credit fields in Local Currency should be cleared. In exceptional cases, enter the Debit/Credit amount in Local Currency first, and then the Debit/Credit amount in Foreign Currency.

6. After completing the first row, click the number of the next empty row. Select the account in the same way as for the first row, then click the Credit or Debit field in the second row. This triggers the balancing mechanism and the System fills the field by copying the corresponding value from the opposite entry line. For Expense accounts, specify Key/Milestone and Department dimensions.

 <img src="../.assets/6f1210be-b4e4-4d0f-810a-ce770c60def1.png" alt="" width="100%" />

7. The following fields are optional depending on the situation:

**Cash Flow Assignment** - mandatory for accounts with the Relevant to Cash Flow setting enabled. Data from this field is used in the Cash Flow report.  
**Tax Type** - to add a posting row to a tax account, specify the applicable tax type. This option is available only when Automatic Tax is selected in the Header.

8. To attach office documents or scanned copies to the Journal Entry, add the relevant files on the [Attachments] tab.

9. To post the Journal Entry, click [Add].
