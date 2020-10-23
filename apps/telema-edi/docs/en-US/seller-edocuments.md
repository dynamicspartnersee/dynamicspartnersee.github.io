---
---
# E-Documents for Seller

## Table of Contents
 - [Receive Sales Order or Sales Return Order](#receive-sales-order-or-sales-return-order)
 - [Issue Sales Shipment](#issue-sales-shipment)
 - [Receive Receiving Advice](#receive-receiving-advice)
 - [Issue Sales Invoice or Credit Memo](#issue-sales-invoice-incl-credit-memo)


## Receive Sales Order or Sales Return Order

Allows to save Telema „order“ type of e-documents as  **Sales Orders**  and subtype „return“ type of e-documents as  **Sales Return Orders**.

For those partners who use 4 document system, checkbox  **Require E-Receiving Advice** should be selected on the sell-to customer card. In this case sales order field  **E-Receiving Advice Status** will be used. It will show the handling status of the order. While creating sales order the field value will change to ‘**Required**’, which gives indication to warehouse that sales order cannot be invoiced before Receiving Advice  has arrived from the customer.

Below is the mapping description of the main entities.

Customers order number will be saved to  **E-Order No.**  field. The field is also visible in order list which gives an overview which orders have arrived through electronic channels.

All entries form e-document element ‘AdditionalInfo’ will be saved to  **Comments.**

**Sell-to Customer No.** will be identified in the following priority order:
1.  OrderParty/PartyCode
2.  OrderParty/GLN
3.  DeliveryParty/PartyCode
4.  DeliveryParty/GLN
5.  BuyerParty/PartyCode
6.  BuyerParty/GLN

**Bill-to Customer No.** is not taken from the file, NAV default remains in use.

**Applies-to Doc. Type** and **Applies-to Doc. No.** will be filled for sales return orders if it includes reference to the original invoice.

**Item No.** will be identified in the following priority order and  **Item variant** is not handled:

1.  Lookup of 'GTIN' from the  **Item Cross Reference** table
2.  Lookup of 'SellerItemCode' from the  **Item Cross Reference**  table
3.  Lookup of ‘BuyerItemCode’ from the  **Item Cross reference**  table

**Quantity** will be identified by the following:

1.  If 'BaseUnit' matches the NAV default unit of measure on the sales order then 'AmountOrdered' will be used.
2.  If 'BaseUnit' does not match the default unit of measure on the sales order then 'AmountOrdered' will be divided by the  **Qty. per Unit of Measure**. The assumption is that the quantity in file is base unit.

Unit price will be taken from ‘ItemPrice’ element if on the customer card checkbox  **Take Price from E-Order**  is selected. This is the final price and discounts will not be applied. If the customer card checkbox  **Take Price from E-Order**  is not selected then the price and discount will be applied according to NAV pricing structure.

In Sales Return order the prices and discounts will be taken from the original invoice when e-sales return order includes a reference to the original invoice. Applications for the exact cost storno will not be made.

**Lot no.** information is not handled.

## Issue Sales Shipment

Allows to create delivery note out of posted e-shipment.

To send e-shipment to customers firstly you need to set up  **Customer card.** The setup is needed for  **Sell-to Customer** (not  **Bill-to Customers)** cards.

Open customer card and make the following setup on  **Telema EDI** FastTab:

|Field|Usage|
|--|--|
|**Issue E-shipment**|Check the box if you wish to send out sales shipments.|
|**Customers GLN**|If the customer has Global Location Number you can enter it to this field.|

In addition completion of  **Telema Setup** page is needed.
Open  **Telema Setup** page and fill in the FastTab  **E-Documents**  as follows:

|Field|Usage|
|--|--|
|**Create E-Shipments on Posting**|Check the box if you wish to send out shipments during the posting process. **This is recommended setup!**|
|**Only Item Lines on E-shipments**|Check the box if you wish to bring only item lines to e-shipments.|
|**Company GLN**|If the company has Global Location Number you can enter it to this field. You can apply for GLN for your company through GS1 Estonia (www.gs1.ee)|

Below is the mapping description of the main data entities.

|NAV entity|Telema eDoc entity|Explanation|
|--|--|--|
|**Header**|
|Bill-to Customer|BuyerParty|
|Sell-to Customer|DeliveryParty|
|Company information|SellerParty|
|E-order no.|SourceDoument|Reference to order.|
|**Lines**||If  **Only Item Lines on E-Shipment** box in  **Telema Setup** is checked then only item lines will appear.|
|No.|SellerItemCode|
|Variant code||Variant information is not sent.|
|Barcode type of cross reference|GTIN|
|Customer type of cross reference|BuyerItemCode|
|Quantity (base)|AmountDespatched|Quantity in base measuring unit.|
|Amount / Quantity (base)|ItemPrice|Will be taken from order line. Necessary for Bauhof. Final price which includes discounts. Information is sent based on the accuracy set in customer card  **Price Round. Prec. on E-Invoice** field.|
||SourceDocument|Reference to e-order and line number of the e-order.|
|**Item tracking**|ItemReserve|Lot no., serial no., and best before info is sent.|

You can look at the e-document created from posted document if you use action  **Navigate** on the posted document. Together with other entries this function also finds  **Outbound E-Document** entry.

## Receive Receiving Advice

Receiving advice allows buyer to confirm the delivery of the goods. In case there are differences you can make required corrections (on  **Posted Sales Shipment** lines action  **Functions->Undo Shipment**) and post new line(s).

**NB!** When posting a correction document mark  **Do not Send as E-Document.**

To save data from the e-receiving advice, related  **Sales Order**  will be searched and  the following information will be updated:
·  On the sales lines  **E-Receiving Advice Quantity**  will be updated
·  (On the sales lines  **E-Receiving Advice Price incl. Disc.**  will be updated)
·  On the sales header  **Status of**  **E-Receiving Advice** will be updated

**Status of** **E-Receiving Advice** will be change to ‘Confirmed’ if there is no differences and to ‘Differences’ if some line contains one of these differences:
·  **E-Receiving Advice Quantity** value  differs from the  **Shipped Quantity** value.
·  **E-Receiving Advice Price incl. Disc.** is filled (in Bauhof case) and it differs from the value calculated as following:  **Line Amount**  divided by  **Quantity.** Prices incl. discounts are compared and with accuracy of two decimal places.

If differences occurred and you have made the corrections, update the  **Status of**  **E-Receiving Advice** to ‘Confirmed’. Otherwise invoice cannot be issued.

Below is the mapping and usage description of the main data entities.

All entries in ‘AdditionalInfo’ will be saved under  **Comments.**

**Item no.** will be identified with the same principle as for  **Sales Order** and  **Item Variants** will not be handled.

Sales Order line associated with E-Receiving Advice line will be found based on Item No. Therefore orders with the same Item no. on multiple lines are not supported.

If E-Receiving Advice contains reference to the order line then this reference information is used to match the lines. Otherwise Sales Order line will be matched with E-Receiving Advice line based on Item No. In latter case documents with the same Item no. on multiple lines are not supported.

To save  **E-Receiving Advice Quantity** e-document element ‘AmountAccepted’ is used. If this element is not found then ‘AmountActual’ is used. If  **E-Receiving Advice Quantity** is already filled, previous value is not deleted and new value will be added.

To save  **E-Receiving Advice Price incl. Disc.** e-document element ‘ItemPrice’ is used.

If necessary the values will be converted to the right unit of measure with the same principle as on  **Sales Order.**

**Lot no.** information is not handled.

## Issue Sales Invoice (incl. Credit Memo)

Allows to create e-invoice out of posted sales invoice and credit memo.

To send e-invoice to customers firstly you need to set up  **Customer card.** The setup is needed for  **Sell-to Customer** (not  **Bill-to Customers)** cards.

Open customer card and make the following setup on  **Telema EDI** FastTab:

|Field|Usage|
|--|--|
|**Issue E-Invoice**|Check the box if you wish to send out sales invoices (also credit memos).|
|**Customers GLN**|If the customer has Global Location Number you can enter it to this field.|
|**Price Round. Prec. on E-Invoice**|For example if you wish to have 5 decimal places after comma, insert 0,00001. Rounding might be needed because final price is calculated by dividing line amount (€) with quantity. Discounts are not inserted to e-invoices.|

In addition completion of  **Telema Setup** page is needed.

Open  **Telema Setup** page and fill in the FastTab  **E-Documents**  as follows:

|Field|Usage|
|--|--|
|**Create E-invoices on Posting**|Check the box if you wish to create the e-invoices (also credit memos) during the posting process. **This is recommended setup!**|
|**Only Item Lines on E-invoices**|Check the box if you wish to bring only item lines to e-invoices.|
|**Company GLN**|If the company has Global Location Number you can enter it to this field. You can apply for GLN for your company through GS1 Estonia (www.gs1.ee)|


Below is the mapping description of the main data entities.

|NAV entity|Telema eDoc entity|Explanation|
|--|--|--|
|**Header**|
|Bill-to Customer|BuyerParty|
|Sell-to Customer|DeliveryParty|
|Company information|SellerParty|
||SourceDoument|In case of Invoice there is a reference to order, shipment and receiving advice. In case of credit memo there is a reference to return order and original invoice if field  **Applies-to Doc. No.** if filled
|Line Amount|DocumentSum|
|Line Amount incl. VAT|TotalSum|
|**Lines**||If  **Only Item Lines on E-Invoices** box in  **Telema Setup** is checked then only item lines will appear.|
|No.|SellerItemCode|
|Variant code||Variant information is not sent.|
|Barcode type of cross reference|GTIN|
|Customer type of cross reference|BuyerItemCode|
|Quantity (base)|AmountInvoiced|Quantity in base measuring unit|
|Amount / Quantity (base)|ItemPrice|Final price which includes discounts. Information is sent based on the accuracy set in customer card  **Price Round. Prec. on E-Invoice** field.|
|Amount|ItemSum|ItemSum includes all discounts.|
||SourceDocument|Reference to e-order and line number of the e-order.|
|**Item tracking**|ItemReserve|Lot no., serial no., and best before info is sent.|

You can look at the e-document created from posted document if you use action  **Navigate** on the posted document. Together with other entries this function also finds  **Outbound E-Document** entry.