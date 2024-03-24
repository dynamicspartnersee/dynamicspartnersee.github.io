---
---
# E-Invoices for Estonia - User Guide
E-Invoices for Estonia solution allows to exchange e-invoices with your business partners.  
As a prerequisite, you must have a contract with e-invoice operator Finbite (formerly Omniva) or Unifiedpost (formerly Fitek).  

## Table of Contents
  - [Service Setup](#service-setup)
  - [Job Queue Entries](#job-queue-entries)
  - [Data Exchange Activities Log](#data-exchange-activities-log)
  - [Receive E-Invoices](#receive-e-invoices)
  - [Create Purchase Invoice from E-Invoice](#create-purchase-invoice-from-e-invoice)
  - [Send E-Invoices](#send-e-invoices)
  - [Send Master Data](#send-master-data)

<br>

## Service Setup
Open **Finbite (Omniva) Document Exchange Service Setup** or **Unifiedpost (FitekIn) Document Exchange Service Setup** and configure the following fields:

|Fast tab / Field|Explanation|
|--|--|
|**General**||
|Enabled|Activates the service and creates **Job Queue Entries** to automate data exchange.|
|Key User|Notifications of errors of automatic data exchange will be sent to his/her role center.|
|Activity Logging|Determines the level of detail for data exchange activity logging. During the test period it is advisable to use "Activity Message and XML Message" to get the maximum information to solve problems. Logged activities and messages can be viewed on the page **Activity Log**.|
|Activate Peppol (Finbite)<br><br>Activate Roaming(Unifiedpost)|Activates international e-invoice sending through Finbite using Peppol. PeppolId can be specified on Customer Card.<br>Activates international e-invoice sending through Unifiedpost using roaming. ChannelId and Channel Address can be specified on Customer card.|
|**Connection**|To setup default values for connection, you can use action **Set URLs to Default**.|
|Service URL|For Finbite you can find it in Finbite invoicing management environment under the Settings->Settings->Data Exchange with ERP.|
|Service Namespace URL|Usually no need to change default value.|
|SOAP Namespace URL|Usually no need to change default value.|
|Authentication Phrase<br>(Finbite only)|You can find it in the Finbite invoicing management environment under the Settings->Settings->Data Exchange with ERP.|
|User Name<br>(Unifiedpost only)|Ask from Unifiedpost.|
|Password<br>(Unifiedpost only)|Ask from Unifiedpost.|
|**Master Data**<br>(Unifiedpost only)||
|Send Code Mandatory Dimensions with G/L accounts|Specifies if G/L account's Code Mandatory dimensions are sent to FitekIn as Mandatory Cost Objectives for that account.|
|Delete Unused Masterdata|Specifies if unused Accounts/Dimensions/Vendors cleanup is performed in FitekIn before data import.|
|PropagateToChild|Specifies FitekIn API to propagate the request to child entities. For example, performing a request to some Organization with PropagateToChild set to True will perform the same request on each Company belonging to the target Organization.|
|**Documents**<br>(Finbite only)||
|Get Invoices Changed Since|Document exchange internal bookmark. Not editable.|
|Get Invoice Which Are|Receive invoice if status is: <br> a) Processed - invoice is marked as Ready for sending to ERP. <br> b) Received - invoice is received as soon as they arrive to Finbite. <br> c) Confirmed - invoce has been approved in Finbite invoice management.
|Get Invoice Attachments|Specifies whether the attachents of the e-invoice are taken. „Main Attachment“ is usually invoice as a PDF.|

To test the connection, use action **Test Connection**.

<br>

## Job Queue Entries
**Job Queue Entries** for automatic data exchange are created when the service is enabled. To view job queue entries, click **Job Queue Entries** in the service setup. 

|Data Exchange Job|Parameter String|Explanation|
|--|--|--|
|Send GL Accounts|SEND-ACC|Sends G/L accounts with checkmark **Send to Finbite/FitekIn**.|
|Send Dimensions|SEND-DIM|Sends dimension values with checkmark **Send to Finbite/FitekIn**. <br>Note! In FitekIn a dimension must be created prior to sending dim.values.|
|Send Vendors|SEND-VEND|Sends vendors with checkmark **Send to Finbite/FitekIn**.  <br>Finbite only! Marked customers can also be sent to Finbite.|
|Get Purch. Invoices|GET-PINV|Takes invoices from the operator server and saves to **Incoming Documents**.|
|Send Posted Purch. Invoices No.|SEND-PINV-NO|Sends posted purchase invoice numbers to Finbite or FitekIn. |
|Send Queued Sales Invoices|SEND-SINV|Sends posted sales invoices (and posted sales credit memos) that have **Document Exchange Status** as „Waits for Sending“ or „Sending Error“. Customer must have **Document Sending Profile** which has setup **Estonian E-Invoice**.
|Send Queued Service Invoices|SEND-SMINV|Sends posted service invoices (and posted service credit memos) that have **Document Exchange Status** as „Waits for Sending“ or „Sending Error“. Customer must have **Document Sending Profile** which has setup **Estonian E-Invoice**.

Set the desired frequency and activate the jobs with action **Set Status to Ready**.

Manually you can run data exchange activities from the **Finbite Document Exchange Setup** or **Unifiedpost Document Exchange Setup** actions ribbon.

<br>

## Data Exchange Activities Log
All data exchange activities are logged. In case of error, these help you in solving the problem. Data exchange activity log entries are linked to the underlying data as follows:

|Data record / Page|Data Exchange Activity|
|--|--|
|Finbite (/Unifiedpost) Document Exchange Service Setup|-Send G/L accounts and dimensions <br> -Send vendors (and customers) <br> -Get purchase invoices|
|Incoming Document|-Get purch. invoice attachments <br> -Send posted purch. invoice no.|
|Posted Sales Invoice (or credit memo)|-Send sales invoice|
|Posted Service Invoice (or credit memo)|-Send service invoice|

To view log entries, click **Activity Log** on the service setup or on a document.

<br>

## Receive E-Invoices
Receiving e-invoices is normally an automated activity. To check this, open **Finbite (/Unifiedpost) Document Exchange Setup**, make sure it is **Enabled**, and click **Job Queue Entries**. Open the job „Get Purchase Invoices“ and make sure it is set up and running the way you want.

If you want to run receiving e-invoices manually, you can do so by clicking **Get Purch. Invoices** on the service setup page.

Received e-invoices are stored to the table **Incoming Documents**.

<br>

## Create Purchase Invoice from E-Invoice

Functionality of the solution (inc. invoice creation logic and retaining line information) can be specified on **Purchases & Payables Setup**:

![Purchases & Payables Setup](1-Purchases_and_Payables_Setup.png "Fields rounded with red line specify the functionality of the solution")

- In fast tab **Default Accounts** you can specify a G/L account that is automatically inserted on purchase lines that are created from e-invoices when the line does not contain an identifiable G/L account or item (look below point 5).
- In fast tab **E-Invoicing for Estonia Settings** you can:
  - **General**:
    - Activate check duplicate document functionality when purchase document is created (_to find duplicate immediately_)
    - Activate find items from e-invoice functionality (look below point 2)
    - Activate find discounts from e-invoice functionality (look below point 7)
    - Specify conditions to find Pay-to Vendor using PayToName from e-invoice XML
    - Activate allow amount difference on posting (_to override purchase invoice amount and incoming document amount matching validation_)
    - Specify logic to retain information on purchase line (look below Retain Line information specification)
  - <span style="color:blue">**Automatic Rounding**:</span>
    - Specify the maximum invoice difference amount allowed for automatic rounding. If invoice difference up to this amount is found (during creation of purchase invoices from incoming documents), then an extra rounding line is created on purchase invoice using G/L account specified in field "Account for Invoice Rounding"
      - It's also recommended to setup "Max. VAT Difference Allowed" on "General Ledger Setup", since that is used to automatically round VAT differences (usually the difference in invoice total amount is caused by VAT difference)
    - Specify G/L account that is used to automatically round invoice differences
      - Selected account should have "Gen. Prod. Posting Group" and "VAT Prod. Posting Group" specified on "Chart of Accounts"
      - In "VAT Posting Setup" the lines with this "VAT Prod. Posting Group" should have 0 (zero) as VAT % (to avoid creation of additional VAT differences on invoice when rounding line is automatically added)


**Process:**


Open **Incoming Documents**. Select the received e-invoice that you want to save to **Purchase Invoice** and click **Create Document**.

If failed, check the **Incoming Document** fast tab **Errors and Warnings**.

<br>

To automatically create a purchase document from an incoming document You can create a workflow using template **Incoming Document Exchange Workflow**.

<br>

**The following logic is used when Purchase Invoice is created from e-invoice:**

1. **Vendor is identified** using the following order:   
a) BC Vendor code (in XML “UniqueCode” tag) <br>
b) Registration No. <br>
c) VAT Registration No. <br>
d) Vendor Name (system searches for exact match in XML) <br>
If vendor is not found it can be created automatically (*if New Vendor Template is specified in Countries/Regions table*), but using this feature is not recommended.  
_Puchase invoices mediated by Finbite can have fllowing country codes: "EE", "LT", "LV" or "ZZ", where the last one means all other countries. Therefore one should create a so called virtual country with code "ZZ" to Countries/Regions table._
4. **Items are identified** only if  **Activate Find Items from e-invoice** is activated on **Purchases & Payables Setup**. <br>
Items are identified using the following order: <br> 
a) BC Item No. (in item code in BuyerProductId tag) <br>
b) EAN (firstly GTIN on item, then barcode from item reference) <br>
c) Seller Item No. (firstly from item reference, then solution checks if a BC Item No. with this code exists) <br>
3. G/L Account and dimensions are taken from the e-invoice if they are available – this means preposting has been done in operator invoice management system.
4. If the G/L account is not found on the e-invoice line, then **Map text to Account** functionality is used. Mapping is searched for the e-invoice line description and if not found then for the vendor name. **NB! Using filters is allowed in Text-to-Account Mapping page.**
5. Finally, the default accounts are used from the **Default Accounts** fast tab of the **Purchases & Payables Setup**.
6. **VAT Prod. Posting Group** is taken from e-invoice (if it exists). If it's not on e-invoice then a VAT Prod. Posting Group that's specified on Item or G/L Account is used. <br> Note! If VAT % on e-invoice line is smaller then on purchase invoice line, then system finds and uses a first suitable VAT Prod. Posting Group with a matching VAT % (*in combination with VAT Bus. Posting Group from Vendor*).
7. **Discount** is added to invoice line only if **Activate Find Discounts from e-invoice** is activated on  **Purchases & Payables Setup** and if discount information exists on e-invoice and if it passes mathematic checks (like Line amount less Line discount amount must equal SumBeforeVAT on e-invoice XML).

<br><br>

**Retain Line information specification**

Field | Selections with descriptions
|--|--|
**Retain Description & Unit Cost** | Specifies whether to retain line's Description, Unit of Measure, Unit Cost and Line discount amount after a change on field No. or Location code. <br><br> a) No (BC Standard) - use Business Centrali standard logic meaning a G/L Account change shall result in data loss on fields mentioned above. <br> b) for E-invoice Lines - if purchase line is created from e-invoice XML, then change on fields No. or Location code does not result in data loss on fields mentioned above. <br> c) for All lines - no matter if line is created manually or from e-invoice, a change on fields No. or Location code does not result in data loss on fields mentioned above. <br><br> **NB!** If you selected b) or c) then solution stops user form changing line Type *(for example G/L Account is changed to Item)*. To change line type you should create a new line with suitable data and then delete the line created from e-invoice.
**Line Dimension Change Logic** | Specifies logic for changing or retaining dimension values after a change in fields No., Job No., Job Task No. <br><br> a) Default Dimensions (BC Standard) - standard BC behaviour meaning dimensions on line depend on default dimensions from values of fields mentioned above. <br> b) Ask User - every change on fields mentioned abouve activate checking if dimension set ID has changed and if so, then user is asked Do You want to change line dimensions with default dimensions. If user confirms then selection a) applies and if not then dimension values are retained. <br> c) Retain for E-invoice Lines - dimension values are retained only on lines created from e-invoice XML.

<br>

## Send E-Invoices
If you want send e-invoices to the customer, open Customer card and assign the corresponding **Document Sending Profile**.  

<br>

To send international e-invoices activate Peppol for Finbite or roaming for Unifiedpost. Then on Customer Card fill field(s):

|Field|Explanation|
|--|--|
|ChannelId|Specifies for UnifiedPost the Customer's E-Invoice roaming channel ID (like PEPPOL, fEAb, INEX, ERIGA). Value is added to XML Invoice tag as channelId attribute.|
|PeppolId or Channel's address|Specifies for Finbite Customer's Peppol ID used in PartyEN extension. (example 0192:979920261).<br>Specifies for Unifiedpost Customer's E-Invoice roaming channel Address (get this from Customer or for finland look https://verkkolaskuosoite.fi/client/index.html). Value is added to XML Invoice tag as channelAddress attribute.|  

<br>

If there is no profile for e-invoice, open **Document Sending Profiles** and create new profile for example as follows:  

|Field|Value / Explanation|
|--|--|
|Code|"E-ARVE"|
|Description|"E-arve"|
|Estonian E-Invoice|Select your partner.|
|Send Estonia E-Invoice Automatically | Posted invoice E-Invoice Status will be set to "Waits for Sending" and will be sent by the Job Queue job "Send Queued Sales Invoices".
|Finbite Delivery Method|Select appropriate. <br>Note!If selection is Bank, then in XML serviceId shall be reference no. and channelId shall be customer's IBAN from preferred bank account specified on customer card.|
|Finbite Invoice Management| Specifies if invoice is immediately sent to the customer or to Finbite Invoice Management (meaning from there the invoice has to be manually sent to customer).|

To send e-invoice, use the action **Post and Send** on **Sales Invoice** or action **Send** on **Posted Sales Invoice**. <br> *If customer has document sending profile with a checkmark "Send Estonia E-Invoice Automatically", then e-invoice will be sent by the Job Queue even when only **Post** action is used.*

Information about the sending status you can see on the posted invoice field **E-Invoice Status**:  

|Value|Explanation|
|--|--|
|Not Sent|Document has not been sent by the user and it will also not be sent by Job Queue.|
|Sending Error|There was an error when sending the document.|
|Sent to Finbite|Document has been sent to Finbite.|
|Sent to Unifiedpost|Document has been sent to Unifiedpost.|

<br>

Invoices to be sent will be sent by the periodic **Job Queue** job „Send Queued Sales Invoices“.

Job sends invoices that meet the following conditions:
- Invoice **E-Invoice Status** is „Waits for Sending“ or „Sending Error“.
- Customer **Document Sending Profile** has **Estonian E-Invoice** set.
  
If invoice has a sending error like Document already received, but it's needed to resend the e-invoice, then on posted sales invoices (also on posted service invoices and sales/service credit memos) action **Send...** opens Send Documents to window, where you can select **Send Again Already Sent E-Invoice**.  

If invoice has a sending error that cannot be resolved, it is advisable to stop re sending attempts.<br>To do so, click on the field **E-Invoice Status** that will open a data exchange activity log. After closing the log, you can choose whether you want to stop re sending attempts.  

<br>

## Send Master Data
You can send the following master data to Finbite Invoice Management or FitekIn:
- **G/L Accounts**
- **Dimensions**
- **Vendors (and Customers (for Finbite only))**

In the respective tables there is field **Send to Finbite/FitekIn**. Mark this field for records that You want to send to partner (Finbite or FitekIn respectively).

<br>

To send data manually, open the respectable **Document Exchange Service Setup** and from Actions -> Master Data select suitable action:
- **Send G/L Accounts** _(For FitekIn, it is also possible to include mandatory cost objectives)_
- **Send Dimensions** _(For FitekIn, a cost objective must be created there first)_
- **Send Vendors** _(In the case of Finbit, it is also possible to send customers)_


Master Data will be sent periodically, if you have set up and running the appropriate job queue entries.

***

For more information, please contact:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
