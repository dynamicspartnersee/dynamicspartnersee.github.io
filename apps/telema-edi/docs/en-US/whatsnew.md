---
---
##### Versioon 15.0.21235.0
- Better application of purchase invoice to receipt(s).
  
##### Versioon 15.0.21216.0
- According to instruction received from Telema. E-Invoice element ReceiverID value has been changed from "Bill-to Customer No." to "Sell-to Customer No.".
  
##### Versioon 15.0.21189.0
- Edisoft opertator support

##### Versioon 15.0.21122.1
- New option on customer card **Despatch Advice Without Prices**

##### Version 15.0.21122.0
- eFlow document receipt was sometimes not issued on Purchase Invoice post. Fixed.
- New event **OnBeforeSaveSalesOrderLine** on inbound sales order handling.
- New event **OnBeforeEDocCreateEntry** after creating outbound sales document (invoice, shipment, credit memo).

##### Version 15.0.20315.0
- New field "Allow using Item No." on customer and vendor card. In case item is not identified via cross-reference, item number from the e-document is used.

##### Version 15.0.20314.0
- Direct document exchange between Business Central companies using web services
- New document type: Purchase Order Confirmation

##### Versioon 1.0.19161.0
- Purchase Invoice: If item is not idetified, additional functionality will try to idetify cost account ("Based on "Map Text to Account" setup).
