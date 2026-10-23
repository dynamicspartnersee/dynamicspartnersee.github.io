---
---
##### Version 25.0.26282.0 _(available from 2026-10-23)_
- Latvian language has been added.
- The balance statement number and the parties' registration numbers have been added to the printouts.

##### Version 25.0.26107.0 _(available from 2026-04-18)_
- Solution made compatible with BC28.
  - _New multiple attachments display in the balance statements list._  

##### Version 24.0.25345.0 _(available from 2025-12-12)_
- Added the option to issue balance statements by payment reference numbers.
  - Required e.g. when customers/vendors have different payment reference numbers on invoices for different services.
  - In the balance statement creation options, under "Show more", the "**By Payment Reference**" option can be turned on.
    - _In this case balance statements are created per payment reference number and the reference numbers are shown on the balance statement printout._
  - Through personalization, the "Payment Reference No." column can be added to the balance statements list (and Factbox) to get an overview of created balance statements by payment reference number in the list as well.
- Added the option to issue balance statements together with information on the turnover of a specific period.
  - Required e.g. when an auditor requests confirmation from a customer/vendor of the turnover of a specific period (e.g. the first 9 months of the year).
  - In the balance statement creation options, under "Show more", a date range (e.g. 01.01..30.09) can be entered in the "**Include Turnover in Period**" field.
    - _In this case a separate "Turnover" block is added to the balance statements, showing turnover by currency for the specified date range._
      - _If "Print in LCY" is selected (which may be useful for transactions in foreign currency), the columns "Amount (LCY)" and "Amount Incl. VAT (LCY)" are also added to show the period turnover in local currency._
    - _If a layout with a feedback section is used, a row is added where the recipient of the balance statement can write the turnover amount for the period._
  - If the "By Payment Reference" option is used, turnover is also shown per payment reference number.
- Minor technical improvements (some code optimization and modernization).  

##### Version 24.0.25254.0 _(available from 2025-09-12)_
- Technical improvements to make the solution **compatible with BC27** _(2025 wave 2)_.  

##### Version 20.0.24318.0
- Added Acquisition Date (AcquisitionDate) with its label (AcquisitionDateLbl) to the "**FA Balance**" report dataset. Also added the label for Disposal Date (DisposalDateLbl).
- Some variables of the "FA Balance" report made accessible to customer-specific extensions.
- Fixed an issue introduced in version 20.0.24268.0 where no balance statement was created for a customer/vendor although the balance on the balance date was not zero _(because there were no open entries on the creation date)_.  

##### Version 20.0.24268.0
- Added the option "**Create Statement Also When Balance Is Zero**" to both customer and vendor balance statement creation, which creates a balance statement even when there are no open ledger entries on the balance date.
  - _Previously a balance statement for a zero balance was created only if there were open ledger entries._
- Added the AL permission set SBS - OBJECTS (Balance Statements - Code Objects).
- Minor UX improvements.  

##### Version 20.0.24071.1
- Extended the "**FA Balance**" report so that it can be grouped by both Responsible Employee and Responsible Employee (Payroll).
- Minor technical improvements to the "FA Balance" report to allow customer-specific variations.  

##### Version 20.0.23348.0
- Technical improvements to **allow multiple alternative layouts** for the same report (starting from BC20).
- Added alternative balance statement layouts that show the balance statement number and include a manually completed feedback section at the bottom, selectable on the "Report Layout Selection" page:
  - "**Customer Balance Statement with Feedback**"
  - "**Vendor Balance Statement with Feedback**"  

##### Version 19.3.23251.0
- Technical improvements to make the solution **compatible with BC23**.
- Fixed an issue where a red cross appeared on the balance statement printout when the company had no picture (logo).
- Updated the app logo to comply with the changed Microsoft AppSource requirements.  

##### Version 18.0.23152.0
- Added a new grouping option "Main Asset" to the **FA Balance** report.  

##### Version 18.0.22365.1
- Bug fixes:
  - Adding attachments in the Factbox failed in BC20 or later.
  - Customized balance statement texts did not change when navigating between cards.  

##### Version 18.0.22365.0
- Customer and vendor **balance statement texts can now be easily customized** on the Balance Statements Setup page.
  - Both Estonian and English texts can be customized.  

##### Version 18.0.22355.0
- When creating customer and vendor statements, it is now possible to choose whether to include the list of entries that make up the balance.
- When creating customer statements, it is now possible to choose whether to **use the external document number instead of the invoice number**.  

##### Version 18.0.22124.1
- In the **FA Balance** report, it is now possible to choose whether disposed fixed assets are included.

##### Version 18.0.22005.0
- Non-functional technical improvements.

##### Version 18.0.212331.0
- **Sent balance statements** can now also be **found in the customer/vendor card**, on the Sent Emails page.
- Fixed a bug that caused the sending email account to change to the default email account in the email editing window.
- Usability improvements to the FA Balance report.

##### Version 17.1.21327.0
- **Balance statements can** now be **sent** with the enhanced email functionality (**email scenario Balance Statement**).
- Added the option to edit the email message before sending.
- Added the Balance Date column to the balance statements list.
- **Added the FA Balance report to the fixed assets list.**

##### Version 15.3.21243.0
- Balance statements are now created even if the customer/vendor card has no email address.
- A missing email address can be added (or changed) in the balance statements list and saved to the customer/vendor card for next time.
- Statement creation parameters are now saved.
- Improved the balance statement layout, including additional information and a visual fix.
- Many usability improvements (e.g. clearer field names, tooltips, better attachment file name).

##### Version 15.3.21148.0
- Extended the dataset of the customer and vendor balance statement printouts for both customer/vendor and company data:
  - about 10-15 fields were added for each underlying table, which can now additionally be used in custom layouts.
