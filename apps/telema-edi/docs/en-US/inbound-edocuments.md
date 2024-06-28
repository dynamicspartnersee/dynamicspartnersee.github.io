---
---
# Inbound e-documents

## How to receive e-documents
Open list  **Inbound E-Documents** and run action  **New/Get Documents**. New documents are downloaded and saved into the  **Inbound E-Documents**  table.

## Save e-document into BC document
Open the  **Inbound E-Documents** list. You can see the list of the e-documents that are not yet saved to BC documents.

Run action  **Save Document to BC**.

Selected entry will be offered as a default filter for the action. To save all the received e-documents, remove the filter.

If the saving of the e-document is successful,  **Handling Status**  will be updated to  **Saved to BC**  and e-document will be moved to the  **Handled Inbound E-Documents**.

If the saving of the e-document is unsuccessful,  **Handling Status**  will be updated to  **Error**  and  **Handling Error** will contain the error message (first 250 symbols).

If you choose  **Stop on Error**  option, the action will stop on first error and display the detailed error message.

Typical errors could be:
- E-document contains a unrecognizable partner
- E-document contains a unrecognizable item

If problems with e-documents appear you can use action  **View Document XML** which enables to open the document (in web browser), save and inspect the content of the document.

If the problem with e-document cannot be solved you can cancel further handling of the e-document with action  **Cancel Document.**

If there is a need to process (save to NAV document) manually corrected XML file use  **Create Document from XML** action. This action creates new e-document based on the given XML file.

## How to automate receiving and saving e-documents using Job Queue
To automate EDI jobs, **Job Queue** must be set up and running

Open the  **Job Queue Entries**:

- Create new job entry for the  **Report 24007801 Get e-documents from Channel** for automatic downloads from operator server (selected on job report query window). 
- Create new job entry for the  **Report 24007803 Save e-documents to BC**  to automatically save the downloaded e-documents to BC documents.

Set up the schedule of the jobs on  **Recurrence**  FastTab.

In case of errors during automatic handling of the documents you can setup e-mail notifications in **EDI Setup** field **Handling Errors E-mail**.
