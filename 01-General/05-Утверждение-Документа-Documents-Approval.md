A document approval procedure is activated in the System. At the time this document was written, approval is active for the following document types:

* A/P Invoice
* Outgoing Payment

The approval-request processing service runs in 5-minute cycles. This means that, depending on when a document is sent for approval, it may take from 1 to 5 minutes for the related notification to be received.

## Actions of the document originator

1. When [Add] is clicked, the System opens the Document Generation Request form, which accompanies the document when it is sent for approval.

 <img src="../.assets/cda99e39-f887-41ee-a519-ec8477ca8f23.png" alt="" width="100%" />

2. Optionally, explanatory free text can be entered in the Remarks field. This text will be delivered to the approver.

3. Click [OK] to send the document for approval.

The System will confirm the submission in the status bar.

 <img src="../.assets/b546f047-45fc-4e3c-a85a-7f0c9fc7c708.png" alt="" width="100%" />

4. If the document is not approved, an internal-mail message will be received indicating that it was rejected (1).

The message body will contain a comment from the approver if one was added (2). To open the document, click the golden arrow (3).

 <img src="../.assets/1054cd10-4c46-465a-880a-6bf53a26b9f7.png" alt="" width="100%" />

5. After correcting the document, repeat step 3 to resubmit it for approval.

6. When a positive approval message is received, open the document by clicking the golden arrow in the message body and click [Add].

   > If the document is changed after approval but before the document is created, it will be sent for approval again.

## Actions of the approver

1. Notification that a document requires approval is delivered through SAP internal mail. A sound notification will be played and the mailbox will open.

 <img src="../.assets/1a2fb702-a9b1-4752-aa2d-93eec811b9b7.png" alt="" width="100%" />

1.B. To check the mailbox manually, open Messages/Alerts Overview from the Tool Panel.
<img width="535" height="127" alt="image" src="https://github.com/user-attachments/assets/44bdeba9-d981-4c99-96e3-5f5b32664be5" />

2. To review the document, click the golden arrow in the message body.

3. The System opens the approval-request processing form.

(1) To open the document itself, click the golden arrow in the Document Draft Details section.  
(2) Summary information showing which approval templates were applied and the current approval status.  
(3) The Remarks field shows the message from the document originator.  

 <img src="../.assets/467110fc-e726-4d06-b211-cbe21f9cbbfd.png" alt="" width="100%" />

4. The following example shows how to return a document for revision. After reviewing the document (**important:** any changes made by the approver will not be saved in the draft), the approver selects a decision in the Answer field. Optionally, a free-text message can be added and will be delivered to the document originator.

 <img src="../.assets/5bc1b81b-7759-4e5b-a169-86f2662060ab.png" alt="" width="100%" />In this case, the originator will receive a rejection notification with the specified reason.

5. If the Approved answer is selected, the originator receives a message allowing the document-creation process to continue. Once a document has been approved, entering new data into it is not available.

## Approval process reports
All available approval reports are located under Main Menu → Administration → Approval Procedures.

 <img src="../.assets/4e79a288-824a-40a2-860b-f11a6babbf92.png" alt="" width="100%" />

### Approval Status Report
The report starts with a criteria-selection step. This determines which documents will be included in the report. At present, A/P Invoice and Outgoing Payment are the critical document types and should be selected as criteria.

 <img src="../.assets/b0a9cf48-e52b-494d-aec6-873123d63d03.png" alt="" width="100%" />

After selecting the criteria, click [OK].  
A report showing the current approval status will open.

 <img src="../.assets/96c79d0c-63a6-460a-8dda-2bfa3768e40c.png" alt="" width="100%" />
