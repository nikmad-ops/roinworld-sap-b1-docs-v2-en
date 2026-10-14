## Chart of Accounts
The current Roin World Chart of Accounts has been loaded into SAP Business One, including the accounts required for SAP operation:

* Technical accounts
* Control accounts

The Chart of Accounts is loaded as a hierarchical structure, with active (postable) accounts placed at hierarchy level 5.

## Layout
The Chart of Accounts object consists of three sections:  
(1) Tabs used to select a Chart of Accounts section (account level 1)  
(2) Section for displaying/selecting an account from the hierarchy (account levels 2-5)  
(3) Section showing information about the selected account  

 <img src="../.assets/317de151-69d7-4b59-8c19-f56973b6eaa4.png" alt="" width="100%" />

## Account Types
SAP Business One has the following predefined account types:

* Revenue: Revenue accounts
* Expenses: Expense and Cost of Goods Sold (COGS) accounts
* Other: all remaining accounts

## Account Settings
The set of configurable account properties depends on the Account Type. In addition, the Chart of Accounts contains settings used to automate completion of document fields associated with the account.  
The following account settings are relevant for Roin World:

### Account Currency
This setting determines the currencies in which postings can be made to the account. By default, all accounts are maintained in two currencies: Local Currency (EGP) and System Currency (SYS-USD). If an account is assigned a currency other than the local currency (a Foreign Currency), postings to that account can be made only in that currency. An account can also be defined as All Currencies, allowing postings in any currency available in the System. In practice, however, using one account with multiple currencies can create additional complexity.  
The account currency can be configured until the first posting is made to the account. After the first posting, the currency setting can only be broadened - for example, an account can be changed to All Currencies, but not restricted again afterward.

### Confidential
Controls visibility of the account and its balance to users. Access authorization for accounts with this property can be configured for user groups and individual users.

### Business Partner Account / Control Account
A G/L account property that links Business Partner subledger accounting (customer and vendor balances) with the general financial statements.

### Cash Account
Property used to identify bank and cash accounts.

### Block Manual Posting
Prevents the account from being used in manual Journal Entries. This ensures that postings to the account are supported by an originating document.

### Relevant to Cash Flow
Applicable to cash accounts. Activates validation of the Cash Flow Assignment field used in Journal Entries, Incoming Payments, and Outgoing Payments.

### Key/Milestone and Department
Applicable to Revenue and Expense accounts. Activates validation of the relevant cost-center fields in documents associated with the account. If a cost center is also specified in the account settings, it will be proposed automatically in documents using that account.
