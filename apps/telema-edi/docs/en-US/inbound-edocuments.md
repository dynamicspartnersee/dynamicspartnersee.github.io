---
---
# Inbound e-documents

## How to receive e-documents from Telema
Open list  **Inbound E-Documents** and run action  **Get Documents from Telema**. New documents are downloaded from Telema sever and saved into the  **Inbound E-Documents**  table.

## Save e-document into NAV document
Open the  **Inbound E-Documents** list. You can see the list of the e-documents that are not yet saved to NAV documents.

Run action  **Save Document to NAV**.

Selected entry will be offered as a default filter for the action. To save all the received e-documents, remove the filter.

If the saving of the e-document is successful,  **Handling Status**  will be updated to  **Saved to NAV**  and e-document will be moved to the  **Handled Inbound E-Documents**.

If the saving of the e-document is unsuccessful,  **Handling Status**  will be updated to  **Error**  and  **Handling Error** will contain the error message (first 250 symbols).

If you choose  **Stop on Error**  option, the action will stop on first error and display the detailed error message.

Typical errors could be:
·  E-document contains a unrecognizable partner
·  E-document contains a unrecognizable item

If problems with e-documents appear you can use action  **View Document XML** which enables to open the document (in web browser), save and inspect the content of the document.

If the problem with e-document cannot be solved you can cancel further handling of the e-document with action  **Cancel Document.**

If there is a need to process (save to NAV document) manually corrected XML file use  **Create Document from XML** action. This action creates new e-document based on the given XML file.

## How to automate receiving and saving e-documents with NAS

To automate Telema EDI jobs, NAV Application Server must be set up and running the  **Job Queue**  functionality.

Open the  **Job Queue Entries**:

·  Create new job entry for the  **Report 24007801 Get e-documents to Telema** for automatic downloads from Telema server.
·  Create new job entry for the  **Report 24007803 Save e-documents to NAV**  to automatically save the downloaded e-documents to NAV documents.

Set up the schedule of the jobs on  **Recurrence**  FastTab.

In case errors appear during automatic handling of the documents you can setup notifications to be sent into the  **My Notifications** window of the  **Role Center**. To set up the notifications open  **Telema Setup** and assign the receiver(s) in the  **Notify on errors in NAS**  field.