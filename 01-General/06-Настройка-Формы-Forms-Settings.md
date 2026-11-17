## User Interface Templates

Every SAP Business One object contains many fields. Some System fields are hidden because they are not relevant to RoinWorld processes.

As part of the SAP implementation, a set of User Interface (UI) templates has been configured to define which fields should be displayed to users.

Configuration of the UI template set is an administrator responsibility and cannot be performed by an end user because it affects all System users.

However, end users can customize their own form layout. User-specific changes affect only that user and do not affect other System users.

## Important Notes

1. The list of fields available for customization depends on the object type. For documents and reports, the available list is limited by the SAP core.
2. Fields in User Reports created through Query Manager cannot be configured through Form Settings. If a field must be added to a User Report, contact the administrator.
3. A field being available in the settings list does not guarantee that the field contains values.
4. Any customization is performed at the user's own responsibility and should have a clear business reason.
5. The field-settings tool has known behavioral limitations and, in some versions of the SAP client, can mark additional fields as visible unintentionally.
6. User-specific settings are guaranteed to be saved only if the user exits SAP at the end of the working day through File → Exit. Saving is not guaranteed when the client is closed using the [X] button.

## Customizing a Form

Customization is performed separately for each form.

To configure field visibility and display order:

1. Open the form to be customized.

2. With the form in focus, click [Form Settings] on the toolbar.

<img width="333" height="95" alt="image" src="https://github.com/user-attachments/assets/e8b2a206-b9c0-4b16-a4ef-82d6ce09acc2" />

3. In the window that opens, go to the Table Format tab.

<img width="549" height="333" alt="image" src="https://github.com/user-attachments/assets/6608af71-12d0-421c-8fdb-bae61b9cb215" />

4. The tab shows all fields available for configuration:

(1) Field visibility.  
(2) Field activity/editability.  
(3) Display order. The top position is shown first on the left; subsequent positions are displayed from left to right.

<img width="427" height="682" alt="image" src="https://github.com/user-attachments/assets/841c9830-10ff-4633-a0aa-07680b2da281" />

5. Select or clear the Visibility checkbox for each field as required.

6. If necessary, change the field order:

6.1. Click and hold the left mouse button on the row containing the field.  
6.2. Wait until a black border appears around the field name.

<img width="316" height="76" alt="image" src="https://github.com/user-attachments/assets/1978a294-eeda-4b61-a157-a99ddc79f63e" />

6.3. While holding the mouse button, drag the row to the required position.  
6.4. To scroll the list while dragging, move the selected row to the top or bottom edge of the visible area and wait briefly.  
6.5. Release the mouse button.

7. After completing the changes, click [OK].

The form configuration is complete and the form will be displayed according to the selected field visibility and order.

## Known Form Settings Behavior

During step 6.4, if the selected row is dragged over other fields while the cursor is positioned over the Visibility column, those fields can be marked as visible unintentionally. Similar behavior can occur while scrolling the field list during drag-and-drop.

If this happens, reopen Form Settings and clear the Visibility checkboxes for fields that should not be displayed.
