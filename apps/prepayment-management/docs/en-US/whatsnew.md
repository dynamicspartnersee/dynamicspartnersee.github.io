---
---
##### Version 26.0.26234.0 _(available from 2026-10-04)_
- Latvian language added.

##### Version 26.0.26116.0 _(available from 2026-04-27)_
- Solution made compatible with BC28.
- Improved user experience of the "Get Customer-Based/Vendor-Based Prepayment" action on sales and purchase credit memos.
  - _The action can add a line only if the document has no lines of any other type (this is validated on posting)._
- Improved the prepayment invoice posting check so that a prepayment invoice can no longer be posted if the corresponding line has a deferral code.
- Improved the prepayment invoice posting check so that no error occurs when an invoice contains a line of an empty No. type.
- Internal technical improvements that do not affect functionality.  

##### Version 26.0.25255.0 _(available from 2025-09-12)_
- Solution made compatible with BC27.
  - _The new version of the solution is therefore suitable only for BC26 and later._
- Added the "Get Customer-Based Prepayment" action to the sales credit memo to make it easier to create a credit memo for a customer-based prepayment invoice.
- Added the "Get Vendor-Based Prepayment" action to the purchase credit memo to make it easier to create a credit memo for a vendor-based prepayment invoice.  

##### Version 20.0.23335.0 _(available from 2023-12-01)_
- Added support for the new extensible invoice entry engine.
- Fixed retrieving a prepayment to a sales line with reverse charge VAT.  

##### Version 17.0.23268.0 _(available from 2023-09-26)_
- Added events _(OnBeforeInsertPrepaymentEntry, OnBeforeSetPrepaymentEntryFilter, OnBeforePrepaymentEntryFindFirst, OnBeforeSetPrice, OnBeforeSalesLineInsert, OnApplyPrepaymentEntries)_ so that custom development can extend the prepayment handling and management logic.  

##### Version 17.0.23262.0 _(available from 2023-09-19)_
- Updated the app logo.  

##### Version 17.0.23158.0 _(available from 2023-06-09)_
- Fixed the "Please check VAT base amounts" error that occurred when using a customer-based prepayment entry on a sales document with "Prices Including VAT" set and lines with different VAT %.  

##### Version 17.0.23146.0 _(available from 2023-05-27)_
- Improved retrieving a customer-based prepayment to a sales order/sales invoice so that, when "Prices Including VAT" is set, the system also retrieves a prepayment amount that does not exceed the document total.
- Added a check on posting that the VAT product posting group used on the prepayment line matches the group on the corresponding entry in the prepayment journal.
- Added a field "Related Prepayment Entry No." (hidden by default) to the sales order and sales invoice lines pages so that the user can show it if needed and thereby find the line referred to by an error message.
- Fixed the error "Call to function LOCKTABLE ... TryFunction".
- Technical improvements.  

##### Version 15.3.22095.1 _(available from 2022-04-05)_
- Added vendor-based prepayment functionality (activated in Purchases & Payables Setup).
- Added currency revaluation of prepayments.
- Fixed the error "The value of field Remaining Amount must not be -0.01" that occurred on posting when "Prices Including VAT" was activated.
- Technical improvements for compatibility with recent BC versions.  
