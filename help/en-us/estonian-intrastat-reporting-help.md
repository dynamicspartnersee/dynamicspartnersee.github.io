# Estonian Intrastat Reporting User Guide
This app adds Estonian requirements and formats to the Intrastat reporting functionality in Dynamics 365 Business Central.

Please read more about Business Central Intrastat reporting on:  
https://docs.microsoft.com/en-US/dynamics365/business-central/finance-how-setup-report-intrastat

## Setup Intrastat
The required level of detail in Estonian Intrastat reporting can be different from company to company.

To setup the appropriate requirements for your company,  open **Intrastat Setup** and fill in the **Purchase Mandatory Fields** and **Sales Mandatory Fields** on **Estonian Intrastat** fast tab:
* Not in Use - Intrastat specific fields are not required on sales and purchases.
* Basic Requirements - "Transaction Type", "Tariff No.", "Country/Region of Origin Code", "Net Weight" are required.
* Additional Requirements - Basic Requirements + "Transport Method", "Shipment Method Code", "Entry/Exit Point" are required.

## Setup Tariff Numbers
In Estonia, some of the tariff numbers require reporting of quantity in supplementary units in addition to the weight.

To setup this, open **Tariff Numbers** and fill in appropriate **Supplem. UoM Code** and a **Supplementary Units** checkbox for tariffs if required.

Items belonging to such tariffs, need to have the same unit of measure setup in **Items Unit of Measure** window.

When doing Intrastat reporting, as a result, **Supplem. UoM Code** and a **Supplem. UoM Quantity** will be filled in on **Intrastat Journal** lines for these items.

## Reporting in Intrastat Journal
Before creating your first Intrastat report, check if Estonian formats are configured. To do this, open **Intrastat Setup** and check if the field **Format Configured** is 'Yes' on **Estonian Intrastat** fast tab. You can also click 'Yes', to see the format configuration entry.

If formats are in place, localized versions of actions **Suggest Lines** and **Make File** will be used in **Intrastat Journal** for reporting.

***

For more information, please contact one of the partners:  
http://www.dynamicspartners.ee
