---
---
# Estonian Business Register - User Guide
Estonian Business Register app adds **Registration No.** field to the customer and vendor data in Business Central and a functionality **Business Register Query**.

## Business Register Query
Query from Business Register enables to make queries from Business Register free information service “Requisites XML Service” and “E-Invoice Register Service”. 

In order to make queries, one has to have a contract for using e-Business Register. Contract information:
[http://www.rik.ee/en/e-business-registry/contract-info](http://www.rik.ee/en/e-business-registry/contract-info)

The following data is queried from the Business Register:
* Business name
* Address (Street, City, County, Postal Code)
* Registration number
* VAT registration number
* Three last year numbers of submitted annual reports
* Link to the company in e-Business Register database
* E-Invoice Service Provider
 
## How to set up Business Register Query
Open **Business Register Setup** and setup:
* Business Register Service URL - enter the address of Business Register web service. Like: [https://ariregxmlv6.rik.ee/](https://ariregxmlv6.rik.ee/)  
* Requisites Service Username - enter your user name according to contract.  
* Requisites Service Password - enter your password according to contract.
* Default Country/Region Code - choose maching value for Estonia (usually "EE").
* City info with district - Specifies if city info should be with district info or without district info.
* E-Invoice Sending Profile - if you issue e-invoices, choose Document Sending Profile you want to assign for the customers with the e-invoice receiving capability.


Selecting **Apply Default Settings** in the setup will will add the Estonian Business Register web address (https://ariregxmlv6.rik.ee/) to the **Business Register Service URL** field and set **Default Country/Region Code** to Estonia matching value (usually "EE"). Also in table **Countries/Regions** Address format is set to "City+County+Post Code" in order to make field County visible on Customer/Vendor/Contact ect card.


## How to use Business Register Query
E-Business Register query can be used for following purposes:
1. As a batch query which compares customer and vendor data with the business register and shows or updates the differences. Report can be also setup as a Job Queue recurring job. Report compares and updates the fields: 
   * Registration No.
   * VAT Registration No.
   * Document Sending Profile - allows to assign e-invoice profile for the customers who are in e-invoice register.
2. As a detailed query for creating a new customer/vendor/contact or to check and update an existing customer/vendor/contact.
 
**To use batch query**, open Customers or Vendors list. Apply filters if necessary and run a function **Update Data from Business Register**. In a report query page, choose if you want to show the differences and/or also update.
If the Registration No. is missing for the customer or vendor, query is made using a company name without ’OÜ’ and ’AS’.
In cases when a company was not found in Business Register (e.g. company name was written differently) or multiple matches was found, then you can use detailed query to correct the company name or select the correct match from the results.

**To use the detailed query**, open Customers or Vendors or Contacts, edit an existing card or create a new card and assign a **No.** to the new customer/vendor/contact card.   Then run a function **Query from Business Register**, which will open the Business Register Query window.  
NB! You can only run the **Query from Business Register** on contacts that have **Type** "Company". The query is not active when contact type is "Person". 

## Business Register Query window
_In Windows client, you can hide the ribbon with icons to get more working space to the window. Right-click on the ribbon and select Collapse Ribbon._

Enter **Name to Search** and/or **Reg. No. to Search**. Then the query will be run and will return the found result. If necessary, adjust the name to search. 

When expected result is returned, click on the company record.

The company data which are in Business Central, is displayed in the bottom right of the window. The company data which are in e-Business Register, is displayed in the bottom left of the window.

To use the data found from e-Business register to fill in or update data in Business Central, click the button after the desired fields or the field **Select All**.

You can edit the data if necessary. To save the data into the customer/vendor/contact card, click **OK**.

***

For more information, please contact one of the partners:

[http://www.dynamicspartners.ee](http://www.dynamicspartners.ee)
