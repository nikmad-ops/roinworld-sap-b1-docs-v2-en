This instruction will be updated after testing is completed (once the minimum required set of fields for Business Partner Master Data has been defined).

To create a new Business Partner (BP) record:
1. Make sure that the required BP has not already been created.
2. Create the BP record in Business Partner Master Data.

## Checking whether the BP already exists
To check whether the Business Partner already exists in the System:

1. Open Business Partner Master Data from Main Menu → Business Partners → Business Partner Master Data.

<img width="394" height="204" alt="image" src="https://github.com/user-attachments/assets/50c6b993-ed9f-4c3f-8e50-e96828dd0aaf" />

2. SAP opens Business Partner Master Data.

3. Make sure the form is in Find Mode (the fields are yellow).  
   If the fields are white, switch the form to Find Mode by clicking the Find button on the toolbar or pressing [Ctrl]+[F].

<img width="543" height="262" alt="image" src="https://github.com/user-attachments/assets/246ebfee-d6ee-4b6f-9fb6-76245f2d8010" />

4. Enter any known attribute of the BP, for example Tax ID or name.  
   Use the * (asterisk) character as a wildcard for the unknown part of the value.  
   For example, Tax ID 123456 can be entered in the Code field as *123456*.  
   The name Muhammad Mahmoud Muhammad Shahwi can be searched as *Muhammad*.

<img width="423" height="133" alt="image" src="https://github.com/user-attachments/assets/435635c8-82b9-4b70-8714-5ddc2789c1d7" />

5. Click [Find] at the bottom of the form.

6. If several BPs match the criteria, the System displays a list of matching Business Partners.  
   If only one BP matches, its master-data record opens directly.  
   If no matching record exists, the System displays an error.

<img width="703" height="36" alt="image" src="https://github.com/user-attachments/assets/53422e45-b7f4-48c7-b011-19809de1a001" />

## Creating Business Partner Master Data

1. Switch Business Partner Master Data to Add Mode.  
   Click Add on the toolbar or press [Ctrl]+[A].

<img width="449" height="248" alt="image" src="https://github.com/user-attachments/assets/dbc3d6c0-baf6-46f5-9212-47d80f8291e5" />

2. In Add Mode (white fields), complete the following MINIMUM required set of fields.

<img width="435" height="198" alt="image" src="https://github.com/user-attachments/assets/2f5f2d31-3c6a-45ae-8b7f-2506ddc171ac" />

(1) Code — the Business Partner Tax ID prefixed with the two-letter ISO country code. For Egyptian residents, use EG.  
(2) BP Type — Vendor or Customer.  
(3) Name — Business Partner name in Latin characters.  
    Foreign Name — Business Partner name in Arabic, if available.  
(4) BP Group — select the group corresponding to the BP role.  
(5) Currency — the currency in which documents will be created. Important: after the first document is posted, the currency cannot be changed.  
(6) Tax ID — Tax ID without the country prefix.

3. Go to the Payment Terms tab.

<img width="594" height="213" alt="image" src="https://github.com/user-attachments/assets/8c718f83-a6fa-4d1f-9fe2-21dd0dc171ac" />

Select the payment terms and price list that will be applied when documents are created.

4. Go to the Accounting tab.  
   On the Tax tab, specify the applicable tax.

<img width="814" height="163" alt="image" src="https://github.com/user-attachments/assets/fd3865cf-8719-44cb-a9ea-07f643cb8a60" />

5. If Withholding Tax is required, select the Subject to Withholding Tax option on the Tax tab and choose the applicable WHT rates.

<img width="751" height="306" alt="image" src="https://github.com/user-attachments/assets/09c1d376-64c2-4b80-8a99-5fd629adfb22" />

6. When all data has been entered, click [Add] to save the Business Partner Master Data record.
