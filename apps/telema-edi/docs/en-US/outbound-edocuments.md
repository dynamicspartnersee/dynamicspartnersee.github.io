---
---
# Outbound e-documents

## How to create e-document from BC document
Generally, there is no need to manually create e-documents. We recommend to setup creating e-documents on posting in  **Setup**.

To manually create e-documents open  **Outbound E-Documents** and on the  **Actions** tab actions group  **Create Document from BC** select the desired action.

Filter out the documents that you want to convert into e-documents and press  **OK.** E-documents are created only for these customers whose setup allows sending out e-documents.

If there is existing not cancelled e-document available for any selected BC document, confirmation to create new e-document will be asked.

## How to send e-documents
Open  **Outbound E-Documents**. There is a list of e-documents, this shows documents that are created from NAV documents but are not sent to Telema yet.

Run action  **Send Document**. By default the current row is in filter. To send out all e-documents remove the filter.

If sending of e-document is successful, the value of  **Handling Status** field will be changed to  **Sent**  and e-document moves to page  **Handled Outbound E-Documents.**

If sending of e-documents is not successful, the value of  **Handling Status** field will be changed to  **Error** and field  **Handling Error** displays the error message (first 250 symbols).

If you check the box  **Stop on Error**  then handling will be stopped whenever first error occurs and detailed error message is displayed.

Typical causes of errors can be:
- E-document does not comply with format requirements
- E-document does not comply with requirements set by counterparty

If problems with e-documents appear you can use action  **View Document XML** which enables to open the document (in web browser), save and inspect the content of the document.

If the problem with e-document cannot be solved you can cancel further handling of the e-document with action  **Cancel Document.**

If there is need to process (send to Telema) manually corrected XML file use  **Create Document from XML** action. This action creates new e-document based on the given XML file.

**Outbound e-Document** could be rejected by the Telema server if it is duplicate. There could be two reasons for this error:

- It is real duplicate (a document from the same sender with the same document type and number within the same year). This can happen if user creates document manually.
- Document has been sent to the Telema server, but receiving confirmation did not reach back to NAV and document’s  **Handling Status**  is not marked as  **Sent**.

In both cases user should cancel the further handling attempts of the document by using the action  **Cancel Document**.

## How to automate creating and sending e-documents using Job Queue
To automate EDI jobs, **Job Queue** must be set up and running.

Open the  **Job Queue Entries**. 
- Create new job entry for the  **Report 24007809 Create Outbound E-Documents**. This can be used in case e-document creating on posting is disabled. Please open job report request page for more options.
- Create new job entry for the  **Report 24007802 Send E-Documents**.  
  
Set up the schedule of the job on  **Recurrence**  FastTab.

In case of errors during automatic handling of the documents you can setup e-mail notifications in **EDI Setup** field **Handling Errors E-mail**.
