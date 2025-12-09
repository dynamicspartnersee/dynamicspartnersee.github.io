---
---

##### Versioon 22.5.25343.0
- Telema mFlow functionality has been added, making it easier to verify purchase invoices and reconcile them with orders and receipts.

##### Versioon 22.5.25251.0
- Previously, failed e-documents could only be cancelled one by one. Now it is possible to cancel selected e-documents in bulk.
- Shipped sales order quantities that did not receive delivery confirmation (receiving advice) and remained uninvoiced in the 4doc scheme can now be easily corrected with the "Correct Shipped & Not Invoiced Items" action, which posts the remaining quantities as a fictitious invoice and immediately credits it.

##### Versioon 21.5.25127.0
- Sending invoices to the LV e-address network has been added. To do this, fill in the "LV E-Address" on the Customer card and on the EDI setup (for your own company). 

##### Versioon 21.5.25048.0
- Sending invoices to the PEPPOL network has been added. To do this, fill in the "Peppol ID" on the Customer card and on the EDI setup (for your own company). On the Unit of measures page, fill in the "International Standard Code".

##### Versioon 21.5.24180.0
- Docura operator channel has been added.
- Option to select whether e-order creates order or blanket order was added on the customer card.

##### Versioon 21.5.24074.9
- Issued e-document ReceiverID change according to Telema recommendation: ReceiverID and Delivery Party Code should be the same.

##### Versioon 21.5.24071.0
- Option to select whether e-documents will be created on posting (option in EDI setup) or later with job queue (R24007809).

##### Versioon 21.5.23335.0
- MS added registration number for customers and vendors into standard functionality. EDI solution uses now this field. Thanks to that dependency for Estonian localization Business Register app is not requied any more.

##### Version 17.0.23083.0
- E-Documents need quite a lot of storage space and are often one of the biggest tables in the database. Old e-documents can now be deleted through "Retention Policy" functionality.

##### Version 17.0.23076.0
- According to instruction from Telema, e-document will be canceled in case of error code 0 which means the following typical errors:
  - unknown sender 
  - unknown receiver 
  - missing link between sender and receiver 
  - validation error 
  - duplicate
  
  Cancelling means no new sending attempts occur for the document.

##### Version 17.0.23072.0
- Web Folders functionality has been added which allows file exchange with on-prem servers. Server with file folder needs to publish the folder as IIS Virtual Directory with WebDAW Publishing, Directory Browsing and Basic Authentication activated.

##### Version 17.0.22311.0
- OrderParty has been added to the sales documents in addition to current BuyerParty and DeliveryParty. It means all three parties are supported: Sell-to, Bill-to and Ship-to.

##### Version 17.0.22259.0
- You can setup "Unidentified Item No." in Telema setup. In this case incoming document will not fail when some item is not found, instead this item is used.
- E-Documents need quite a lot of storage space and are often one of the biggest tables in the database. To save the space nearly by half, PDF is not extracted from the XML and saved separately. User experience is not affected by the change - when viewing PDF, it is extracted at the same moment from the XML and is displayd.

##### Version 17.0.22185.0
- Notification system has been added. In the setup you can set e-mail address(es) who will be notified in case of e-document handling error (inbound or outbound).  

##### Version 16.0.22103.0
- New document type: **Sales Order Confirmation**
- New event **OnBeforeModifySalesHeader** on inbound sales order handling.
- New event **OnBeforeSalesLineInsert** on inbound sales order handling.
- New event **OnAfterSaveSalesOrderLine** on inbound sales order handling.
- New event **OnAfterSaveRecAdv** on inbound recadv handling.
- New event **OnAfterModifySalesLineRecAdv** on inbound recadv handling.

##### Version 16.0.21361.0
- License check updated to oauth authentication

##### Version 16.0.21356.0
- App name changed to "Telema & Edisoft EDI"

##### Version 16.0.21285.0
- BC19 support
- GTIN field support
- Item References support (in addition to Cross-References)

##### Version 15.0.21235.0
- Better application of purchase invoice to receipt(s).
  
##### Version 15.0.21216.0
- According to instruction received from Telema. E-Invoice element ReceiverID value has been changed from "Bill-to Customer No." to "Sell-to Customer No.".
  
##### Version 15.0.21189.0
- Edisoft opertator support

##### Version 15.0.21122.1
- New option on customer card **Despatch Advice Without Prices**

##### Version 15.0.21122.0
- eFlow document receipt was sometimes not issued on Purchase Invoice post. Fixed.
- New event **OnBeforeSaveSalesOrderLine** on inbound sales order handling.
- New event **OnBeforeEDocCreateEntry** after creating outbound sales document (invoice, shipment, credit memo).

##### Version 15.0.20315.0
- New field "Allow using Item No." on customer and vendor card. In case item is not identified via cross-reference, item number from the e-document is used.

##### Version 15.0.20314.0
- Direct document exchange between Business Central companies using web services
- New document type: **Purchase Order Confirmation**

##### Version 1.0.19161.0
- Purchase Invoice: If item is not idetified, additional functionality will try to idetify cost account ("Based on "Map Text to Account" setup).
