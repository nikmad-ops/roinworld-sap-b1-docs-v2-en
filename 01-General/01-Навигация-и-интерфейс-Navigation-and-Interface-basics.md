# Important disclaimer:
Using keyboard shortcuts for navigation and data entry is the most efficient way to work with the System. However, please note that **the [Enter] key is the most dangerous key**. Pressing it while entering data into a Document may save (post) the document. For some documents (Delivery/A/R Invoice, Goods Receipt PO/A/P Invoice, Payment, Goods Issue, Goods Receipt), this action is irreversible and a reversing document will be required.  
**In SAP, the [Enter] key is not used to move between rows/fields. This function is assigned to the [Tab] key.**  
At the user's request, this behavior of the [Enter] key can be disabled. To change the key behavior, contact SAP support.  
At the same time, **the [Enter] key is also one of the most useful keys in SAP**.  
The difference between risk and benefit depends on constantly understanding the current Form Mode (see the Form Mode section below).

# Workspace
This section uses standardized names for interface elements. Please remember them, as these terms are used throughout the documentation, training, and support.

SAP Business One workspace:

 <img src="../.assets/cdd310b6-291b-4487-9a28-04a9cb2ee90f.png" alt="" width="100%" />

(1) Horizontal menu  
(2) Company Name|User. This is a button.  
(3) Tool Panel  
(4) Hamburger. Shows/hides the Main Menu  
(5) Modules. Opens the module sections of the Main Menu  
(6) Main Menu Search. Searches the sections of the Main Menu  
(7) Main Menu. Main Menu sections  
(8) Drag&Relate. Opens the Drag and Relate reporting sections  
(9) Corporate Search. Searches data stored in the System  
(10) Status bar  
(11) User info bar  
(12) Fiori Desktop  

## (1) Horizontal menu
A standard Windows-style application menu. It includes the usual File, View, Edit, and Help sections, as well as SAP-specific sections such as Data, Modules, Tools, and Window.  
The items shown in the drop-down menus depend on which object is currently open in the Workspace. The Modules section duplicates the Main Menu sections and can therefore be used to open forms without using the Main Menu.  
Important items:  
*View - User-Defined Fields*. Controls the additional form panel containing user-defined fields.  
*View - Fit Column Width*. Optimizes the display of table columns by resizing them to fit their contents.  
*Tools - Change Log*. Opens the change log for the current document/master-data record.  
*Tools - User Shortcuts*. Allows actions to be assigned to the F2-F12 keys.  
*Window - Close All*. Closes all windows currently open in the workspace.  
*Window - Close All But This*. Closes all open windows except the currently active window.

## (2) Company Name|User
An indicator button. Clicking it opens the list of available SAP company databases.

## (3) Tool Panel
A horizontal bar containing icon buttons. Button availability depends on the form/document that is currently open and active. It also depends on the form status (Find Mode/Add Mode/View Mode).  
Icons are grouped by their purpose.

### File
 <img src="../.assets/0aca2ea0-e651-47da-ad3e-297479c063ef.png" alt="" width="100%" />

**Preview** - previews the print layout. The default layout configured for the document is used.  
**Print** - prints the document layout. As with Preview, the default layout configured for the document is used.  
**SAP Business One Mailer** - sends the document via SAP internal mail.  
**SMS** - the document-by-SMS module is not activated for Roin World.  
Fax - the document-by-fax module is not activated for Roin World.  
**MS Excel** - exports data from the open window to Microsoft Excel. Important: before saving, change the file extension to .xls or .xlsx.  
**MS Word** - exports the print layout to Microsoft Word.  
**PDF** - exports the print layout to a PDF file. The default layout configured for the document is used.  
**Launch Application** - launches an application predefined in the System configuration. Not activated for Roin World.  
Lock Screen - locks the screen if the user needs to leave the computer.

### Data
 <img src="../.assets/f6f2cfa4-5621-4299-8132-c06080394548.png" alt="" width="100%" />

**Find** - switches the open document to Find Mode.  
**Add** - switches the open document to Add Mode.  
To understand the following buttons, imagine that all documents are arranged from left to right, from number 1 to number N. The following icons allow navigation between documents **within the same document type**.  
**First Data Record** - opens the document with the lowest number.  
**Previous Record** - opens the document with a lower document number than the current one.  
**Next Record** - opens the document with a higher document number than the current one.  
**Last Data Record** - opens the document with the highest number (the most recently created document).  
**Filter Table** - applies a filter to table-type documents and reports.  
**Sort Table** - sorts data in table-type documents and reports.

### Go To
 <img src="../.assets/5e779e90-1046-4fa1-96c8-4f5c873c90f6.png" alt="" width="100%" />

**Base Document** - opens the base document. The button is active when a base document exists. For example, the base document for a Delivery is a Sales Order.  
**Target Document** - opens the target document, if one exists.  
For example, the target document for a Delivery can be an A/R Invoice.  
**Gross Profit** - opens the window for viewing and configuring the gross-profit calculation for the document.  
**Payment Means** - opens the window for entering payment details. The button is active for documents that can create a payment posting (A/P and A/R invoices and Payments).  
**Volume and Weight Calculation** - opens the calculation of the total volume and weight of the items in the document. Weight data must be maintained in the Item Master Data.  
**Journal Entry** - opens the related accounting postings.  
**Journal Entry Preview** - previews the journal entry that will be created if the document has not yet been saved. This is a very useful tool. When the preview is generated, the System checks the document for errors. No posting is created, giving the user an opportunity to correct the document before posting.

### Tools
 <img src="../.assets/445e1a68-324c-4f34-ad8b-222cd25aed9a.png" alt="" width="100%" />

**Print Layout Designer** - a technical tool used to configure printing and select layouts. Configuration is not available to regular users.  
**Form Settings** - opens field-display settings. In table-type documents, it allows columns to be hidden, displayed, or moved.  
**Query Manager** - opens the repository of user-defined queries (reports). This is the primary user tool for running custom reports.  
**Live Collaboration** and **Send to Chat** - internal collaboration chat buttons. Not activated for Roin World.

### Window
 <img src="../.assets/665d84a9-fce5-412f-9552-97fc4086acb9.png" alt="" width="100%" />

**Workflow Messages Overview** - not activated for Roin World.  
**Messages/Alerts Overview** - opens the user's mailbox (SAP Business One Mailer).  
**Calendar** - opens the user's calendar.  
**Select Default Branch** - not activated for Roin World.  
**My Personal Settings** - opens the user settings. Font, interface language, and activation of SAP services can be changed here.

### Extreme Apps
 <img src="../.assets/0c6d252c-30e8-48cc-8064-3c7c6c864971.png" alt="" width="100%" />

**Available-to-Promise Check** - opens the ATP tool. Not activated for Roin World.  
**Delivery Schedule Management** - opens the ATP tool. Not activated for Roin World.  
**Cash Flow Forecast** - opens the SAP HANA cash-flow and liquidity forecast tool.  
**Pervasive Analytics** - opens the SAP HANA analytics tool. It can be used to create dashboards for the Fiori Desktop.  
**Web Client** - launches the SAP Business One Web Client.

### Help
 <img src="../.assets/3046ec53-7be7-4b01-ae78-bb24593a7049.png" alt="" width="100%" />

**Help** - opens SAP Business One Help.

## (8) Drag&Relate
A functional section of the Main Menu used to generate reports on the fly. To use it, expand the required Drag&Relate section and open the data source to be used for the report. The example below uses Business Partner Master Data. In the Business Partner Master Data window, click and hold the required field until a black frame appears around it, then drag the frame to the required Drag&Relate item and drop it. In the example, the Business Partner Name is dropped onto the sales report at Sales Order row level.

 <img src="../.assets/f18ef081-69c6-43da-bed2-2474f70e17b8.png" alt="" width="100%" />

\

\

\

\  
Because Sales Order rows contain items, a report will be generated showing the items used in Sales Orders for the selected Business Partner:  
 <img src="../.assets/83821ea2-9902-495f-a52e-731babda3e74.png" alt="" width="100%" />

## (9) Corporate Search
Google-like search across documents and master data stored in the database.

## (10) Status bar
The interface area where SAP messages are displayed.

## (11) User info bar
An interface area divided into four fields. The user can drag a field from a document or master-data record (for example, from the Logistics tab) into any of these fields. The selected value will then be displayed for the active document without the user having to open the relevant tab.

## (12) Fiori Desktop
The SAP Business One workspace area used to display current information as dashboards and KPI indicators. The Fiori Desktop has two modes:

* User desktop
* Preconfigured dashboard template

In User Desktop mode, click the '+' symbol and select the dashboards to be placed on the desktop. Dashboards related to Roin World have names starting with RW.  
In template mode, click the Folder icon and select one of the preconfigured templates.

 <img src="../.assets/e5a24dea-e6fd-4a76-8083-0e494f075222.png" alt="" width="100%" />

\

\

\

\

\

The System will refresh the desktop contents and display the dashboards configured in the selected template.

 <img src="../.assets/61789af5-0c94-453a-9ec4-61a7f8d01aa6.png" alt="" width="100%" />

\

\

\

\  
To return to the User Desktop, click the Back symbol [<].  
To refresh the data in the charts, click Refresh. Without pressing Refresh, dashboard data is updated every 3 minutes.

# Form Mode
Every SAP Business One object has several modes. The System indicates the current mode by highlighting form fields and by the text displayed on the form button.

Yellow fields and the default button text [Find] mean that the form is in [Find Mode]:

 <img src="../.assets/81483761-e039-4159-87e5-329e361bafe1.png" alt="" width="100%" />

White fields and the default button text [Add] mean that the form is in [Add Mode]:

 <img src="../.assets/2a89a2c1-a89b-46bb-aebc-d60c3e08a620.png" alt="" width="100%" />

White fields and the default button text [Update] mean that the form is in [Update Mode]:

 <img src="../.assets/9fbf6cca-a0fc-42e8-a365-dc7a83b9bb95.png" alt="" width="100%" />The orange marker on the Form button means that this is the button that will be triggered when [Enter] is pressed on the keyboard.

## Switching between Form Modes
There are two ways to switch between modes:

* Keyboard

To activate [Find Mode], press [Ctrl] + [F].  
To activate [Add Mode], press [Ctrl] + [A] (English keyboard layout).  

* Mouse

To switch Form Mode, click (1) to switch to [Find Mode] and (2) to switch to [Add Mode].

 <img src="../.assets/e27da94b-2ef9-44f0-8eaa-89ee39deb0ee.png" alt="" width="100%" />

The form automatically switches to [Update Mode] when the user changes a field on the Form.

### [Find Mode]
In Find Mode, the user can define search criteria. Any yellow field can be used for entering criteria. Values from drop-down lists or free text can be used, following the approach below (using Item Name as an example):

* pi\* - finds records beginning with pi (**pi**zza with tomato, **pi**nk pizza)
* \*za - finds records ending with za (big fat piz**za**, pink piz**za**)
* \*pa \* - finds records containing pa in the name (lovely **pa**sta meals)
* \*pi%za \* - finds records where one character is unknown (big lovely **pi**z**za**)

If several fields are populated, they are used as a combined set of search criteria.

For example:

Result - all Item Master Data records where the name contains **za**:

 <img src="../.assets/65cc8f87-a067-4baa-bdfd-98c65b7261b6.png" alt="" width="100%" />

Result - all Item Master Data records where the name contains **za**, the Item Group is Finished Goods, and the UoM Group is Each:

 <img src="../.assets/85b71463-e6c5-4ffc-8309-e9313714ffdc.png" alt="" width="100%" />

To run the search, click the [Find] form button. It can be clicked with the mouse or triggered by pressing [Enter].

**Please note!** The System records user interaction with fields and may interpret it as a search criterion. For example, if the user places the cursor in the Name field, enters a value and then deletes it before running the search, the System may attempt to find a record with an empty Name field.

### [Add Mode]
A new record is always entered in a defined sequence: left to right and top to bottom. Complete the Header first, then the Tabs. Tabs should be completed from left to right. The numbering in the screenshot represents the recommended sequence.

 <img src="../.assets/55889e66-84be-41ac-812d-3d9789efb571.png" alt="" width="100%" />This approach is important because forms (especially Documents) often contain dependent fields.  
For example, Warehouse - Account - Department.  
If the Warehouse is changed, the System may change the Account, and the Department may in turn depend on the Account. Therefore, if Department is filled in before Warehouse is changed, the System may clear the Department field.

### [Update Mode]
Update Mode is activated automatically if the user changes any field while in [View Mode]. To save the changes, click the [Update] form button or press [Enter].  
To return to View Mode without saving the change, use the relevant toolbar action described above in the Tool Panel section.

### [View Mode]
The standard mode for documents with Closed status and for Master Data records. The form button shows [OK]. If [Enter] is pressed, the Form will be closed.
