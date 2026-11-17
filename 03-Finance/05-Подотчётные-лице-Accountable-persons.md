# Accounting for Funds Issued to Accountable Persons

Issuing funds to an accountable person is recorded in SAP using a Journal Entry.

## Issuing Funds

To record the issue of funds:

1. From the Main Menu, open Financials → Journal Entry.

<img width="310" height="185" alt="image" src="https://github.com/user-attachments/assets/78da471c-de08-4ee8-ba24-7c67620f1237" />

2. Complete the Journal Entry header.

<img width="1355" height="331" alt="image" src="https://github.com/user-attachments/assets/dfa6d30d-0610-4811-9d28-259564ba29cf" />

(1) Posting Date.  
(2) Due Date — the deadline for submitting the expense report for the amount issued.  
(3) Remarks — a description of the transaction that will be visible in reports.  
(4) In the Accountable Person field, click the magnifying-glass icon and select the recipient of the funds.

3. Complete the Journal Entry rows. Note that the marked fields shown below are equivalent ways of entering the relevant data.

<img width="1195" height="331" alt="image" src="https://github.com/user-attachments/assets/65365a68-ba6b-4c4d-b937-750042e2b27e" />

4. Complete the table as follows:

<img width="1682" height="303" alt="image" src="https://github.com/user-attachments/assets/d298dc22-ce32-41ca-92ce-41014430626f" />

(1) Verify that the Accountable Person is specified in the rows.  
(2) For the Credit row, select the Cash Flow Line Item "Cash issued to accountable person".  
(3) Use the Custody account for the corresponding entry.

5. **Applicable to the production database:** go to the Attachments tab and attach the source document.

<img width="1815" height="129" alt="image" src="https://github.com/user-attachments/assets/5451f450-2860-4a0d-b58f-2f62700b256c" />

## Clearing Previously Issued Funds

1. Open Journal Entry and complete the header.

<img width="1038" height="144" alt="image" src="https://github.com/user-attachments/assets/f1981eb4-2bbd-40de-afcc-af94108bf048" />

2. Complete the line-item section:

For the Credit account, specify the Cash Flow Line Item "Clearing funds previously issued to accountable person".

To enter the Business Partner whose document will be settled by the clearing entry, place the cursor in the G/L Acct/BP Code field and press [Ctrl]+[Tab]. This opens the list of Business Partners.

<img width="725" height="77" alt="image" src="https://github.com/user-attachments/assets/64ee39ce-c805-40f2-b008-5c2d108e64ee" />

3. Verify that all fields are completed correctly.

<img width="1680" height="302" alt="image" src="https://github.com/user-attachments/assets/27e4b2ae-73ad-4ca6-8972-8f29379e7120" />

4. Click [Add] to post the Journal Entry.

5. **Applicable to the production database:** go to the Attachments tab and attach the source document.

6. Reconcile the created Journal Entry with the corresponding purchasing document (A/P Invoice).

See the Reconciliation instruction: [Reconciliation](03-Выверка-Reconciliation.md)
