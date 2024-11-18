---
---
# Estonian Business Register - User Guide
Estonian Business Register app makes possible to use **Business Register Query** functionality on customer, vendor and contact card.

## Business Register Query
Query from Business Register enables to make queries from Business Register free information service “Requisites XML Service” and “E-Invoice Register Service”. 

In order to make queries, one has to have a contract for using e-Business Register.  
Contract information:  
<a href="https://www.rik.ee/en/e-business-register/contract-information" target="_blank">https://www.rik.ee/en/e-business-register/contract-information</a>  

The following data is queried from the Business Register:
* Business name
* Address (Street, City, County, Postal Code)
* Registration number
* VAT registration number
* Three last year numbers of submitted annual reports
* Link to the company in e-Business Register database
* E-Invoice Service Provider
 
<br>
<br>
 
## How to set up Business Register Query
Open **Business Register Setup** and setup:
* Business Register Service URL - enter the address of Business Register web service. Like: [https://ariregxmlv6.rik.ee/](https://ariregxmlv6.rik.ee/)  
* Requisites Service Username - enter your user name according to contract.  
* Requisites Service Password - enter your password according to contract.
* Default Country/Region Code - choose maching value for Estonia (usually "EE").
* City info with district - Specifies if city info should be with district info or without district info.
* E-Invoice Sending Profile - if you issue e-invoices, choose Document Sending Profile you want to assign for the **customers** with the e-invoice receiving capability.


Selecting **Apply Default Settings** in the setup will will add the Estonian Business Register web address (https://ariregxmlv6.rik.ee/) to the **Business Register Service URL** field and set **Default Country/Region Code** to Estonia matching value (usually "EE").  
Also in table **Countries/Regions** Address format is set to "City+County+Post Code" in order to make field County visible on Customer/Vendor/Contact ect card.  

<br>
<br>

## How to use Business Register Query
E-Business Register query can be used for following purposes:
1. As a batch query which compares customer and vendor data with the business register and shows or updates the differences. Report can be also setup as a Job Queue recurring job. Report compares and updates the fields: 
   * Registration No.
   * VAT Registration No.
   * Document Sending Profile - allows to assign e-invoice profile for the customers who are in e-invoice register.
2. As a detailed query for creating a new customer/vendor/contact or to check and update an existing customer/vendor/contact.
 
**To use batch query**, open Customers or Vendors list. Apply filters if necessary and run a function **Update Data from Business Register**. In a report query page, choose if you want to show the differences and/or also update.
If the Registration No. is missing for the customer or vendor, query is made using a company name without most common form of business pre- and suffixes _(OÜ, AS, UÜ, TÜ, MTÜ, FIE, OSAÜHING, TÄISÜHING, AKTSIASELTS, USALDUSÜHING, KORTERIÜHISTU, TULUNDUSÜHISTU, MITTETULUNDUSÜHING ja FÜÜSILISEST ISIKUST ETTEVÕTJA)_.  
In cases when a company was not found in Business Register (e.g. company name was written differently) or multiple matches was found, then you can use detailed query to correct the company name or select the correct match from the results.  

**To use the detailed query**, open Customers or Vendors or Contacts, edit an existing card or create a new card and assign a **No.** to the new customer/vendor/contact card.   Then run a function **Query from Business Register**, which will open the Business Register Query window.  
_When running query on existing Customer/Vendor/Contact and if Registration No. exists and meets requirements, then query shall be done using Registration No._  
NB! You can only run the **Query from Business Register** on contacts that have **Type** "Company". The query is not active when contact type is "Person".  

## Business Register Query window

Enter **Name to Search** and/or **Reg. No. to Search**. Then the query will be run and will return the found result. If necessary, adjust the name or Reg. No. to search. 

When expected result is returned, click on the company record.

The company data which are in Business Central, is displayed in the bottom right of the window. The company data which are in e-Business Register, is displayed in the bottom left of the window.

To use the data found from e-Business register to fill in or update data in Business Central, click the button after the desired fields or the field **Select All**.

You can edit the data if necessary. To save the data into the customer/vendor/contact card, click **OK**.

***

<br>


For more information, please contact:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
