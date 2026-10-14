An A/R Invoice is an accounting document that creates the Customer receivable and records sales revenue.

The following sales types are used depending on the sales process:

| Sales Type | Numbering Series | Base Document | Specifics |
|------------|------------------|---------------|-----------|
| POS Sale | BK26, FT26, ST26 | Sales Order | Standard document. Inventory is issued from the warehouse. |
| Office Sale | 2026 | Delivery | Invoice with document-level grouping |

## POS Sale

The A/R Invoice is created from a Sales Order previously prepared from the POS sales report.  
To create the A/R Invoice:

1. Open Sales Order from Main Menu → Sales - A/R → Sales Order.

<img src="../.assets/ba445e85-1051-4727-b6fd-ac2e37aacd1a.png" alt="" width="100%" />

2. Switch the form to Find Mode by pressing [Ctrl]+[F].

3. Enter search criteria in the yellow fields (Customer, Numbering Series, or Sales Order number) and click [Find].

<img src="../.assets/5fe3423d-5244-4f2d-a49c-b0ed3c29bdb3.png" alt="" width="100%" />

4. Select the required Sales Order to be used as the base document and open it by double-clicking.

5. Verify that the analytical dimensions in the document are correct.

<img src="../.assets/3dcfbf21-a24a-4798-b06d-92b2c8ecbee3.png" alt="" width="100%" />

6. Click [Copy To] and select A/R Invoice from the drop-down list.

 <img src="../.assets/79086155-4fb2-4074-b5aa-f45c69781b01.png" alt="" width="100%" />

7. The System opens the A/R Invoice form and copies the Sales Order data into the document table.

8. Set:

(1) The Numbering Series corresponding to the sales type (Stella in this example).  
(2) The document date. For Stella, Foodtruck, and Bakery, use the date for which the posting is being made.  
<img src="../.assets/495fb9e4-2ebf-451e-8bdc-e2a533d8e5b3.png" alt="" width="100%" />

9. Perform a preliminary validation by generating a Journal Entry Preview. This runs document-rule validation and checks whether sufficient inventory is available in the selected warehouse.

Click [Journal Entry Preview] on the Tool Panel.  
<img src="../.assets/434c63f9-0589-42ae-b392-433b28c25882.png" alt="" width="100%" />

If the System opens the Journal Entry form, the document has passed validation and sufficient stock is available.

10. Verify that no grouping is applied to the document.

<img src="../.assets/44b8253a-7fb5-4aac-8fdf-c10fbf554b36.png" alt="" width="100%" />

11. Sign the document by selecting your signature in the Owner field (1). To record the cash receipt, click the Payment Means button (2).

<img src="../.assets/00e742a4-937c-4fbd-9614-0ec6b96a7409.png" alt="" width="100%" />

12. In the Payment Means form, specify:

(1) Cash as the payment method.  
(2) The General Ledger account to which the cash will be posted.  
(3) The total amount. To copy the balance, press [Ctrl]+[B] or right-click the field and select Copy Balance Due.  
(4) Select the Cash Flow Item from the list.  

<img src="../.assets/baa9ca16-f99d-4c3c-b9fa-ba020370b150.png" alt="" width="100%" />

13. After completing Payment Means, click [OK]. Back in the A/R Invoice, click [Add] to post the document.

### Result of Posting a POS A/R Invoice

Posting the A/R Invoice in this way creates two Journal Entries in the System.

A/R Invoice:  
 <img src="../.assets/9c3caf93-0f28-4d16-89b9-dfe27dcab5df.png" alt="" width="100%" />

Payment:

 <img src="../.assets/2072d8a4-2842-4459-8427-43162d9e9cbe.png" alt="" width="100%" />

Because no Delivery base document was used, the related inventory movement is also recorded:

 <img src="../.assets/f4ffdc74-b9c7-4c83-b3e0-3f9c9cf6892e.png" alt="" width="100%" />

## Office Sale

An Office A/R Invoice is created from one or more Delivery documents using the Copy From function.  
Specifics of this process:

* invoicing is performed later than the physical delivery
* inventory movement was already recorded by the Delivery base document
* the A/R Invoice uses document-level grouping and does not show the individual sold items in the grouped view; this is required by the associated print layout

To create the A/R Invoice:

1. Open A/R Invoice from Main Menu → Sales - A/R → A/R Invoice.

 <img src="../.assets/9f6d818d-fd4b-4ef0-837b-02d34456c64d.png" alt="" width="100%" />

2. Complete the Header.

(1) Specify the Customer Code or Name.  
(2) Select the Office Numbering Series (2026).  
(3) Specify the document date. Due Date is calculated according to the Customer payment terms (45 days in this example).  
(4) In the [BP Reference No.] field, click the magnifying-glass icon to generate the invoice number in the required format.  
(5) Verify the Customer currency exchange rate. It is taken from the exchange-rate table for the Posting Date. Important: the currency must match the currency used in the base Delivery document.  
<img src="../.assets/a8f17273-8f5c-4ada-bc96-3e3362a11e9c.png" alt="" width="100%" />

3. Click [Copy From] and select Deliveries.

<img src="../.assets/3d5d37ef-9fd8-49dc-a85d-57cdc7c0b478.png" alt="" width="100%" />

4. The System opens the list of available base documents. Double-click the required Delivery. To select multiple documents, hold [Ctrl]+[Shift].

<img src="../.assets/be3a69bd-9034-4907-b0be-f7e4a70e75b0.png" alt="" width="100%" />

5. The System opens the Draw Document Wizard.

Select the required data-transfer method and exchange-rate rules.  
<img src="../.assets/e668491d-ec51-4795-bf99-729006b368e2.png" alt="" width="100%" />

6. Click [Next] / [Finish].

7. Data from the base document(s) is copied to the document table.

<img src="../.assets/b8d8ebd3-4240-4fba-9f76-3d2627b59ba7.png" alt="" width="100%" />

8. Set data grouping to By Documents.

This groups the table by base documents.

 <img src="../.assets/342d8413-4850-481a-b696-0f795843a9f7.png" alt="" width="100%" />

9. Sign the document by selecting your signature in the Owner field.

<img src="../.assets/c053ec97-6286-4934-ba36-37b8cf929fcb.png" alt="" width="100%" />

10. Perform a preliminary validation by generating a Journal Entry Preview. This runs the document-rule validation process.

Click [Journal Entry Preview] on the Tool Panel.

 <img src="../.assets/6f32c5a8-4a15-4c67-83a2-82aba515c81a.png" alt="" width="100%" />

If the System opens the Journal Entry form, the document has passed validation.

11. Verify the preliminary Journal Entry.

<img src="../.assets/8f9cbcc7-dc89-4d69-9dae-fd966b256bdb.png" alt="" width="100%" />

12. Return to the document and click [Add] to post the A/R Invoice.

13. If required, generate the Invoice print layout by clicking Preview on the Tool Panel.

 <img src="../.assets/4eaf4e47-9b87-4080-9782-65d9b8e1bb62.png" alt="" width="100%" />

### Result of Posting an Office A/R Invoice

Posting the A/R Invoice creates the following Journal Entry:

 <img src="../.assets/379b8f62-1a18-4b60-ae3c-03234246238e.png" alt="" width="100%" />

It also creates the Customer Accounts Receivable balance.  
 <img src="../.assets/55727871-3fc4-4c24-8381-17ca6e33ad03.png" alt="" width="100%" />
