---
---
# Estonian Intrastat Reporting - User Guide
This app adds Estonian requirements and XML file format to the Intrastat reporting functionality in Dynamics 365 Business Central.

Please read more about Business Central Intrastat reporting on:  
<a href="https://docs.microsoft.com/en-US/dynamics365/business-central/finance-how-setup-report-intrastat" target="_blank">Set up Intrastat reporting</a>  

## Setup Intrastat
The required level of detail in Estonian Intrastat reporting can be different from company to company.

To setup the appropriate requirements for your company,  open **Intrastat Setup** and fill in the **Purchase Mandatory Fields** and **Sales Mandatory Fields** on **Estonian Intrastat** fast tab:

Value | Description
-- | --
Not in Use | Intrastat specific fields are not required on sales and purchases.
Basic Requirements | "Tariff No.", "Country/Region of Origin Code", "Net Weight" are required on Item card and "Transaction Type" on document.
Additional Requirements | Basic Requirements + "Entry/Exit Point" are required on document.<br>_(Documents with posting date until 31st december 2021 have as required fields also "Transport Method" and "Shipment Method Code")._  

Check if field **Format Configured** is 'Yes' on **Estonian Intrastat** fast tab.  
You can also click on 'Yes', to see the Intrastat report format configuration entry in VAT Reports Configuration page.  
_(Content Codeunit ID should be 24007763 and Validate Codeunit ID should be 24007762)._  
_This makes possible the creation of Intrastat Report file in XML format, that meets the Estonian requirements._ 

## Setup Tariff Numbers
In Estonia, some of the tariff numbers require reporting of quantity in supplementary units in addition to the weight.

To setup this, open **Tariff Numbers** and mark a **Supplementary Units** checkbox for tariffs if required.  
_(Previously (until BC24) it was required to fill also Supplem. UoM Code there, but that has now (from BC25) moved to Item card)._

Items belonging to such tariffs, need to have the same unit of measure setup in **Items Unit of Measure** window.

When doing Intrastat reporting, as a result, **Supplem. UoM Code** and a **Supplem. UoM Quantity** will be filled in on lines for these items.  
Please note that to XML file the **Supplem. UoM Quantity** value is taken from **Units of Measure** table field **International Standard Code** _(case there is no value, then the value on line is used)_.

## Reporting Intrastat
If on **Intrastat report** (_previously on Intrastat Jnl. Batch_) field **Statistics Period** is filled (for example december 2024 is 2412) and status is **Open** (_previously on batch Reported must be false_), then action **Suggest Lines** retrieves all the item entries in the statistics period and inserts them as report lines.  

Action **Create File** shall create an XML file of Intrastat report.  
Saved XML file can be submitted in <a href="https://estat.stat.ee/" target="_blank">estat</a> environment.

***

For more information, please contact:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
