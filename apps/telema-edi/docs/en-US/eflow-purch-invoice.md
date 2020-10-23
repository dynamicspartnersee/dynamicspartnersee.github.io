---
---
# Receciving Processed Purchase Invoice (eFlow accounting entry document)

Allows you to save Telema ’entrec’ type of e-document as a  **Purchase Invoice**  and issues e-document receipt as a reply for it.

Below is the mapping and usage description of the main data entities.

E-document number is saved on the **E-Invoice Entry Doc. No.**  field on the  **General**  fasttab of the  **Purchase Invoice.** Clikking on  **E-Invoice Entry Doc. No.**  opens an  **Inbound E-Document**  where you can view the accompanied PDF with the  **View Document PDF**  action.

**Buy-from Vendor No.** is identified from the following e-document elements and in this priority order:
1.  SellerParty/PartyCode
2.  SellerParty/RegNum

**Pay-to Vendor No.** is identified from the following e-document elements and in this priority order:
1.  FactorParty/PartyCode
2.  FactorParty/RegNum
3.  PayToParty/PartyCode
4.  PayToParty/RegNum

This means if a factoring partner is found from the e-document it is assigned as a  **Pay-to Vendor**.

If  **Pay-to Vendor**  cannot be identified from the e-document it is assigned according to NAV default setup.

In addition to vendors, vendor bank account is identified from the e-document. If vendor bank account for the IBAN is missing from NAV, new  **Vendor Bank Account**  is created and assigned as a  **Prefered Bank Account**  on the  **Vendor**  card.

See also:  [How to create missing vendors automatically](#how-to-create-new-vendors-automatically)

In addition the following fields are filled in on the  **Purchase Invoice**:

|Purchase Invoice field|E-document element|
|--|--|
|**Posting Date**|TransactionDate|
|**Document Date**|InvoiceDate|
|**Due Date**|DueDate|
|**Vendor Invoice No.**|SourceDocumentNum (type INVOICE)|
|**Your Reference**|SourceDocumentNum (type ORDER)|
|**Reference No.**|PaymentRefNum|
|**Currency Code**|Currency|

As  **Purchase Invoice**  lines e-document lines with the ’AccountType’ value ’E’ (expense lines) are saved.

The fields are filled as follows:

|Purchase Invoice Line field|E-document element or constant|
|--|--|
|**Type**|’PR konto’|
|**No.**|AccountID|
|**Description**|ItemDescription|
|**Quantity**|’1’ or if EntryItemType=CRE then ’-1’|
|**Direct Unit Cost**|Sum|

**Purchase Invoice**  line  **Dimensions**  are updated according to the dimension information presented in the  **E-Document**.

After saving the  **Pucrhase Invoice**, e-document total amounts are compared with NAV document  **Total Amount**  and  **Total Amount incl. VAT**. If required, rounding line is added and/or VAT amount is corrected in NAV.

After posting the  **Purchase Invoice**, reply receipt containing reference to the posted invoice will be issued to inform about successful processing of the  **Inbound E-Document**.

If saving of the  **Inbound E-Document**  as a  **Purchase Invoice**  fails (eg. missing or incorrect data on the document), you can cancel the further processing of the e-document with the action  **Cancel Document**. As a result, reply receipt containing the error information will be issued. After that you can correct the entry document in Telema eFlow and send it again to NAV.

## How to create new vendors automatically

Missing vendors can be created automatically when Purchase Invoice (accounting entry document of expense invoice) is received.

Create  **Configuration Templates**  for the vendor table and choose fields and values you would like to fill in automatically for new vendors. Create several templates (domestic, foreign) if you need. Assign template(s) in the  **Countries/Regions**  list into the field  **New Vendor Template**. NAV identifies vendor country from the e-document and finds according template to create new vendor.

The following vendor card fields will be filled based on the data in e-document:

Vendor field:
**Name**
**Registration No.**
**VAT Registration No.**
**Phone No.**
**E-Mail**
**Address**
**City**
**Post Code**
**Country/Region Code**

To enable this functionality open  **Telema Setup**  and check the  **Create New Vendors**.