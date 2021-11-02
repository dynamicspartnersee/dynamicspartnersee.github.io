---
---
# Estonian Banking Formats - User Guide
This extension adds Estonian localization for banking functionality in Dynamics 365 Business Central.

Estonian localization includes:
- Payment reference numbers for sales
- Sales document layouts (Order, Invoice, Cr. Memo) with commonly used requisites
- Estonian SEPA payment format
- Estonian SEPA statement format
- Payment application rules
  
## Install activities
After the installation of extension page **Estonian Banking Formats Setup** must be opened, because this triggers the background installation of formats needed (_Data Exchange Definitions, Bank Export/Import Setup, Document Layouts_).  
Page must be opened in every company, where Estonian Banking Formats shall be used.  

## Payment Reference Numbers for Sales
Using payment reference numbers in sales helps you apply cash receipts and invoices when processing bank statements.

To use payment reference numbers in sales, open **Estonian Banking Formats Setup** and set **Sales Reference No.** as:
- *Create from Customer No.* - In this case, the **Payment Refernece No.** will be generated for new customers and then taken from customers to the new invoices.
- *Create from Invoice No.* - In this case, if **Payment Refernece No.** is empty before posting, it will be generated from invoice number in the posting process.

## Sales Document Layouts
Three new custom layouts has been added to provide commonly used company and banking information on sales documents:
- *1305 - Estonian Order Confirmation*
- *1306 - Estonian Sales Invoice*
- *1307 - Estonian Sales Credit Memo*

You can see if layouts are installed in **Estonian Banking Formats Setup**. If not installed, please contact your partner.


## Bank Statement Import Format (SEPA Statement Format)
To be able to import bank statements from bank to Business Central, Estonian SEPA statement format has been added.  
You can see if format is installed in **Estonian Banking Formats Setup**. If not installed, please contact your partner.  
To setup statement format for a bank account, open **Bank Accounts** and edit bank account you would like to setup.  
Choose **SEPACAMT-EE** for **Bank Statement Import Format**.  

![Image](formats-setup-onBankAccount.png)

## Payment Export Format (SEPA Payment Format)
To be able to submit payments from Business Central to bank, Estonian SEPA payment format has been added.  
You can see if format is installed in **Estonian Banking Formats Setup**. If not installed, please contact your partner.  
To setup payments format for a bank account, open **Bank Accounts** and edit bank account you would like to setup.  
Choose **SEPACT-EE** for **Payment Export Format**.  


## Payment Application Rules
Business Central payment application rules have been complemented by two new components:
- *Reference No.* - helps in the process of document match.
- *Registration No.* - helps in the process of customer/vendor match.

New rules does not require setup and thus are not visible in **Payment Application Rules**.

Rules are used on action **Apply Automatically** in **Payment Reconciliation Journal**.


## Payment recipient
In case the payment recipient differs from the vendor (for example recipient is factoring company or Ministry of Finance), fill in data under **Recipient** tab on the **Vendor Bank Account Card**.  
If the **Recipient Name** is filled, it is also used in the payment file.  

***

For more information, please contact one of the partners:  
[http://www.dynamicspartners.ee](http://www.dynamicspartners.ee)
