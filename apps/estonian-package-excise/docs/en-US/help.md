---
---
# Estonian Package Excise - User Guide
This extension adds Estonian localization for package excise functionality in Dynamics 365 Business Central.

Once a quarter, entrepreneurs must submit a packaging excise duty declaration. The present functionality of the Estonian localization makes it possible to assemble a dataset necessary for the submission of the excise duty declaration in Business Central. The functionality does not include a printout of the excise duty declaration report.

References to the Packaging Act: 
- <a href="https://www.riigiteataja.ee/en/eli/513052021001/consolide" target="_blank">Packaging Act</a>
- <a href="https://www.riigiteataja.ee/en/eli/504072017009/consolide" target="_blank">Packaging Excise Duty Act</a>

# Settings
## General settings
Settings of packaging materials can be found by typing **Package Materials**
## Packaging excise duty settings for items
### Item Card
On the **Inventory** FastTab, a value is selected for the **Packaging Excise Calculation** field.
Possible values of the field are:

| Value | Explanation |
|--|--|
|No Calculation | The item is not included in packaging excise duty calculation.|
|Use Entry Unit of Measure| Packages must be setup for the units used in transactions.|
|Use Base Unit of Measure| Packages must be setup only for the base unit. Transactions in other units are converted to base units before package quantity calculation.|

### Application of the unit of measurement of an item to packaging materials

For the calculation of packaging excise duty, the measurement unit(s) of an item must be applied to packaging materials. For that, on the **Item Card** in the **_Actions_** tab under **_Item_** press the **Package Materials** button.
In the page that opens, codes and quantities of packaging materials related to the unit of measurement (or different units of measurement) of the item are set.  
There it's possible via personalization to make visible field **Variant Code**, to enter packaging materials for different item variants (in case different item variants have different packaging).  
_Note! If an item variant has no packaging materials, but the item with an empty variant has a packaging material, then the amount of packaging material for the item of the corresponding variant should be set to zero._  
As additional information (e.g. for the auditor) it's possible to add the method how package weight was found (from options Self weighted, Provided By Vendor, Similar item).
With personalization it's possible to add creator and/or modifier information fields to the page.  


# Use
The page for generation of packaging excise duty report **Package Excise Declaration** is launched by typing **Package Excise Declarations** 
Actions:
**New** - a new packaging excise duty declaration is created
**Edit** - enables editing a marked and not submitted packaging excise duty declaration 
**View** - displays a marked packaging excise duty declaration 
**Delete** - deletes a marked packaging excise duty declaration 
 
Upon the creation of a new packaging excise duty declaration, the following fields are filled in the page:

|Field|Explanation|
|--|--|
|No.| The packaging excise duty declaration number is entered in the field|
|Description  | Description of the packaging excise duty declaration|
|Period Start| Determines the beginning of the period|
|Period End| Determines the end of the period|
|Last Modify Time| Time when the packaging excise duty declaration was last modified|
|Last Modify User| The user name of the person having last modified the packaging excise duty declaration|
|Reported| Shows that the packaging excise duty declaration has been submitted. Makes fields (except for Reported) read-only|

Calculation activity of packaging excise duty declaration is started from the **Packaging Excise Declaration** page by pressing **Calculate Lines**. On the request form that opens, determine the filters (those are pre-filled by default), and press **OK**.

Packaging excise duty quantities are calculated on terms determined by the filters.
 
By default, request form filters of the **Calculate Lines** activity are filled with the following filters:
- Entry type = Sales
- Country/Region code = '' and/or Country/Region code from company information
- Posting Date = filter based on report header

The packaging excise duty declaration is filled, using the following logic:
- All entries from the table **Packaging Material**, i.e. all packaging materials set are retrieved.
- Quantities according to the item **Packaging Excise Calculation** and package materials setup for the item. 
- As many **Package Excise Decl. Entries** are generated for the item entry as many different packaging material are specified for the item.
  - If packaging materials are assigned to the items according to the variants, then packaging quantities are calculated according to the variants.
- If the report already has lines, upon the second running of activity **Calculate Lines** a warning is displayed to the user upon the acceptance of which lines are recalculated.

Report lines that have been generated cannot be manually added and deleted. The user can add values to the following columns:
- **Recycle Actual Qty. (KG)**
- **Recircul. Actual Qty. (KG)**
- **Reusage Actual Qty. (KG)**

By clicking the value in column **Package Material Quantity (KG)**, the **Package Excise Decl. Entries** page is opened with detailed entries of which the calculated quantity consists.
If the report has been submitted, the **Reported** field in the header is marked. If the field is marked:
- The fields of the report header are read-only (except for the **Reported** field, which enables reopening of the report) and the report cannot be deleted.
- The lines of the report are read-only and the **Calculate Lines** activity cannot be restarted. 

***

For more information, please contact:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
