---
---
# E-Invoices for Estonia - User Guide
E-Invoices for Estonia solution allows to exchange e-invoices with your business partners. As a prerequisite, you must have entered into a corresponding contract with one of the e-invoice operators Omniva or Fitek.

## Table of Contents
  - [Service Setup](#service-setup)
  - [Job Queue Entries](#job-queue-entries)
  - [Data Exchange Activities Log](#data-exchange-activities-log)
  - [Receive E-Invoices](#receive-e-invoices)
  - [Save E-Invoice to Purchase Invoice](#save-e-invoice-to-purchase-invoice)
  - [Issue E-Invoices](#issue-e-invoices)
  - [Issue G/L Accounts and Dimensions](#issue-gl-accounts-and-dimensions)

<br/>

## Service Setup
Open **Omniva Document Exchange Service Setup** or **Fitek Document Exchange Service Setup** and configure the following fields:

|Fast tab / Field|Explanation|
|--|--|
|**General**||
|Enabled|Activates the service and creates **Job Queue Entries** to automate data exchange.|
|Key User|Notifications of errors of automatic data exchange will be sent to his/her role center.|
|Activity Logging|Determines the level of detail for data exchange activity logging. During the test period it is advisable to use "Activity Message and XML Message" to get the maximum information to solve problems. Logged activities and messages can be viewed on the page **Activity Log**.|
|**Connection**|To setup default values for connection, you can use action **Set URLs to Default**.|
|Service URL|For Omniva you can find it in Omniva invoicing management environment under the Settings->Settings->Data Exchange with ERP.|
|Service Namespace URL|Usually no need to change default value.|
|SOAP Namespace URL|Usually no need to change default value.|
|Authentication Phrase<br/>(Omniva only)|You can find it in the Omniva invoicing management environment under the Settings->Settings->Data Exchange with ERP.|
|User Name<br/>(Fitek only)|Ask from Fitek.|
|Password<br/>(Fitek only)|Ask from Fitek.|
|**Documents**<br/>(Omniva only)||
|Get Invoices Changed Since|Document exchange internal bookmark. Not editable.|
|Get Invoice Which Are|Specifies if invoice is taken from Omniva when it is received or after it has been processed in Omniva invoice management.|
|Get Invoice Attachments|Specifies whether the attachents of the e-invoice are taken. „Main Attachment“ is usually invoice as a PDF.|

To test the connection, use action **Test Connection**.

<br/>

## Job Queue Entries
**Job Queue Entries** for automatic data exchange are created when the service is enabled. To view job queue entries, click **Job Queue Entries** in the service setup. 

|Data Exchange Job|Explanation|
|--|--|
|Send GL Accounts|Sends G/L accounts with checkmark **Send to Omniva**.|
|Send Dimensions|Sends dimensions with checkmark **Send to Omniva**.|
|Get Purch. Invoices|Takes invoices from the operator server and saves to **Incoming Documents**.|
|Send Posted Purch. Invoices No.|Sends posted purch. invoice number for Omniva incoming documents.|
|Send Queued Sales Invoices|Sends sales invoices which **Document Exchange Status** is „Waits for Sending“ or „Sending Error“. Customer must have **Document Sending Profile** which has setup **Estonian E-Invoice**.

Set the desired frequency and activate the jobs with action **Set Status to Ready**.

Manually you can run data exchange activities from the **Omniva Document Exchange Setup** or **Fitek Document Exchange Setup** actions ribbon.

<br/>

## Data Exchange Activities Log
All data exchange activities are logged. In case of error, these help you in solving the problem. Data exchange activity log entries are linked to the underlying data as follows:

|Data record / Page|Data Exchange Activity|
|--|--|
|Omniva (/Fitek) Document Exchange Service Setup|-Send G/L accounts and dimensions <br> -Get purch. invoices batch|
|Incoming Document|-Get purch. invoice attachments <br> -Send posted purch. invoice no.|
|Posted Sales Invoice (or credit memo)|-Send sales invoice|

To view log entries, click **Activity Log** on the service setup or on a document.

<br/>

## Receive E-Invoices
Receiving e-invoices is normally an automated activity. To check this, open **Omniva (/Fitek) Document Exchange Setup**, make sure it is **Enabled**, and click **Job Queue Entries**. Open the job „Get Purchase Invoices“ and make sure it is set up and running the way you want.

If you want to run receiving e-invoices manually, you can do so by clicking **Get Purch. Invoices** on the service setup page.

Received e-invoices are stored to the table **Incoming Documents**.

<br/>

## Save E-Invoice to Purchase Invoice
Open **Incoming Documents**. Select the received e-invoice that you want to save to **Purchase Invoice** and click **Create Document**.

If failed, check the **Incoming Document** fast tab **Errors and Warnings**.

The following mapping rules are used when **Purchase Invoice** is created from e-invoice:

1. Vendor is identified by **Registration No.** If vendor is not found it can be created automatically, but using this feature is not recommended.
2. G/L Account and dimensions are taken from the e-invoice if they are available – this means posting has been done in operator invoice management system.
3. If the G/L account is not found on the e-invoice line, then **Map text to Account** functionality is used. Mapping is searched for the e-invoice line description and if not found then for the vendor name. **NB! Using filters is allowed in mapping texts setup.**
4. Finally, the default accounts are used from the **Data Exchange** fast tab of the **Purchases & Payables Setup**.

<br/>

## Issue E-Invoices
If you want issue e-invoices for the customer, open Customer card and assign the corresponding **Document Sending Profile**.

If there is no profile for e-invoice, open **Document Sending Profiles** and create new profile as follows:

|Field|Value / Explanation|
|--|--|
|Code|"E-ARVE"|
|Description|"E-arve"|
|Estonian E-Invoice|Select your operator.|
|Omniva Delivery Method|Select appropriate.|

To send e-invoice, use the action **Post and Send** on **Sales Invoice** or action **Send** on **Posted Sales Invoice**.

Information about the sending status you can see on the posted invoice field **E-Invoice Status**:

|Value|Explanation|
|--|--|
|Not Sent|Document has not been sent by the user and it will also not be sent by Job Queue.|
|Sending Error|There was an error when sending the document.|
|Sent to Omniva|Document has been sent to Omniva.|
|Sent to Fitek|Document has been sent to Fitek.|

Invoices to be sent will be sent by the periodic **Job Queue** job „Send Queued Sales Invoices“.

Job sends invoices that meet the following conditions:
- Invoice **E-Invoice Status** is „Waits for Sending“ or „Sending Error“.
- Customer **Document Sending Profile** has **Estonian E-Invoice** set.

If invoice has a sending error that cannot be resolved, it is advisable to stop re sending attempts. To do so, click on the field **E-Invoice Status** that will open a data exchange activity log. After closing the log, you can choose whether you want to stop re sending attempts.

<br/>

## Issue G/L Accounts and Dimensions
On the **G/L Account** card and on the **Dimensions** page there is field **Send to Omniva**. Mark this field for those accounts and dimensions you want to send to Omniva.

To send data manually, open the **Omniva Document Exchange Service Setup** and run the actions **Send GL Accounts** and **Send Dimensions**.

G/L Accounts and Dimensions will be sent periodically, if you have set up and running according job queue entries.

***

For more information, please contact one of the partners:

http://www.dynamicspartners.ee