---
---
# Prepayment Management - User Guide 
Prepayment management functionality enables the following:
- Issuing of a prepayment request, i.e. prepayment invoice.
- According to the VAT Act, treating prepayment of customers as turnover and subject it to the calculation of VAT.
- Keep the accounting of customer’s prepayments and use them on (deduct from) the main invoices issued to the customer.
- Support for standard Prepayment Unrealized VAT functionality.
- Link prepayments with jobs module.

## Settings
To use the functionality, standard prepayment settings are required. 
In the **General Posting Setup**, the **_Sales Prepayment Account_** must be determined.

### _Prepayment Unrealized VAT setup_

If it is preferable to declare VAT amounts from prepayment invoices after they are paid by customer, then following setup must be made.

As a first step you have to open **General Ledger Setup** and mark _**Prepayment Unrealized VAT**_ as Yes.

As a second step you have to open **VAT Posting Setup** and modify necessary _**VAT Bus. Posting Group**_ and _**VAT Product Posting Group**_ combinations. On selected combinations you have to define _**Unrealized VAT Type**_ (for an example _Percentage_) and also setup _**Sales VAT Unreal. Account**_.

## Use
### Registration of customer-specific prepayment and issuing of a prepayment invoice

In BC, customer-specific prepayment is registered through a sales invoice. For that, a sales invoice is created for the customer, including the account from the **_Sales Prepayment Account_** column of the general posting setting in its line.

**Job related** prepayment invoice begins, as ordinary job sales invoice, from Job planning line and all mentioned above is applying. With Job related prepayment invoice columns  **Job no.** and **Job Task No.** will be filled in **Prepayment Ledger**.

#### **_Important!_**
---
_On a prepayment invoice field **Customer Specific Prepayment Invoice** is marked automatically in the background on posting (the value of the field is transferred to the posted invoice or posted credit memo)._

_Therefore following will apply:_
- _Upon posting of invoices the number series of the posted prepayment invoices / credit memos are used._
- _With such an invoice it is only possible to sell from prepayment accounts determined in the general posting setup. Checking takes place at the moment of posting._

---

If sales prepayment account is selected for an invoice line, BC automatically creates prepayment entries into the prepayment ledger and a prepayment invoice is printed upon printing of the posted invoice (either from the Post and Print button or from the list of posted sales invoices). 

### Checking of customer-specific prepayment entries
There are two options for checking of prepayment entries.
- In the FactBox Pane **Sell-to Customer Sales History** in the list of customers or customer card, where the number of open prepayment entries is displayed in field **Number of Open Prepayments**
- In the FactBox Pane **Sell-to Customer Sales History** in the page of the sales invoice, sales order or credit memo, where the number of open prepayment entries is displayed in field **Number of Open Prepayments**

Clicking a number opens a page with entries of the customer prepayments ledger displayed 

Explanations of the main fields. Explanations of the main fields.

|Field|Explanation|
|---|---|
|Amount |Original Prepayment Amount.
|Remaining Amount |Unused Prepayment Amount.
|Open |A check mark in the field refers to an open prepayment entry, which can be used (in such an event the **Remaining Amount** cannot be zero). 
|Cust. Ledger Entry No. |A reference to the Customer’s Ledger Entry number associated with the entry in the Prepayment Ledger. Prepayment Ledger.
|Invoice Paid Fully |Shows whether a cash receipt from the customer is registered for a prepayment entry or not. If the value is **No**, the Customer Ledger Entry is open, i.e. prepayment cash receipt from the customer has not yet been registered in BC. **Yes** marks a closed Customer Ledger Entry, referring to a registered cash receipt. 
|Job No. / Job Task No.| Is filled on entries that are linked to Jobs.|

#### **_Important!_** 

---
_It must be noted that the lines displayed in the **Prepayment Ledger** are not cash receipts of customer prepayment. The value in field **Invoice Paid Fully** shows whether prepayment has been received from the customer. If the value is **Yes**, the **Customer Ledger Entry** is closed, i.e. prepayment cash receipt from the customer has been registered in BC. **No** means an open **Customer Ledger Entry**, referring to an unpaid invoice._

---

By selection action **Navigate** you can navigate to invoice and entries from the marked prepayment entry.

### Using of prepayment

A customer prepayment can be used on a sales order and invoice or on job planning line by using **Get Cust. Spec. Prepayment** button on the order/invoice/Job Planning Lines page. The page that opens shows open prepayment entries with remaining amounts, from which mark the entry you wish to use and press **OK**

By pressing **OK**, the following checks are carried out:
- It is checked that the currency of the entry corresponds to the currency in the document currency in the document
- It is checked that the prepayment type of the entry is not Order-specific, i.e. the entry should be Customer-specific
 
The following information is copied from the entry to a new document line or job planning line:
- Account No.
- Description 
- All posting groups
- In sales line/job planning line, the **Applied Prepayment Entry No.** field is filled with the number of the associated prepayment entry. The field is hidden and the information can only be viewed using zoom. 
- The quantity for the line is minus one (-1). ty for the line is minus one (-1). 
- If the invoice amount with VAT is smaller than the open prepayment, the invoice amount shall be decreased accordingly.  
  

#### **_Important!_**

***
- _Prepayment lines for the sales document/job planning line are selected one by one, i.e. several lines cannot be selected at once._
- _If the remaining amount of the prepayment entry should not be used at once, decrease the amount of the prepayment line in the **Unit Price Excl. VAT** / **Unit Price** column. In such an event the prepayment entry will stay open with the remaining amount after the posting of the document._
- _**NB!** In case of job related prepayment the next step is to create sales invoice from planning line._
- _Upon posting of a sales document with a prepayment line, BC checks if the sales line with prepayment exceeds the remaining amount of the prepayment entry. In the event of an error, an error message is displayed to the user._
- _If the whole prepaid amount was used, the prepayment entry shall be marked as closed after posting the sales document and it can no longer be selected for the document. for the document._
- _If only a part of the prepaid amount was used, the prepayment entry shall remain open and the remaining amount of the entry can be used with another sales document._

---

### Cancel a prepayment invoice
An already posted customer-specific prepayment invoice can be canceled through a sales credit memo. An invoice can be created from scratch or by using the **Copy Document** functionality or by using the **Create Corrective Credit Memo** functionality from the **Posted Sales Invoices** list.
 
On a prepayment credit memo field **Customer Specific Prepayment Invoice** is marked automatically in the background on posting. This determines that the number of the posted credit memo is retrieved from the number series determined in the settings of prepayment credit memo.

For the line of the credit memo, the sales prepayment account from the general posting setup, quantity 1, the amount and the prepayment entry to be cancelled in the **Applied Prepayment Entry No.** field shall be selected.


#### **_Important!_**

--- 
- _When posting a credit memo, it shall be checked if a prepayment entry number is selected for the **Applied Prepayment Entry No.** field. If it has not been done, an error message is displayed to the user during posting_
- _If the total prepayment entry should not be used, decrease the prepayment line amount on the credit memo in the **Unit Price Excl. VAT** column. In such an event the prepayment entry will stay open with the remaining amount after the posting of the document (the remaining amount is decreased by the credit amount)._
- _Upon posting of a credit memo with a prepayment line, BC checks if the line with prepayment exceeds the remaining amount of the prepayment entry. In the event of error, a message is displayed to the user._
- _If the whole prepaid amount was cancelled, the prepayment entry shall be marked as closed after the posting of the credit document and it cannot be selected for the document any longer._
- _If only a part of the prepaid amount was cancelled, the prepayment entry shall remain open and the remaining amount of the entry can be used with another sales document._ 

---


### Cancel a sales invoice on which prepayment has been used
Cancellation takes place through a sales credit invoice or sales return order. The document can be created from scratch by using the **Copy Document** functionality or, in the event of a return order, the **Get Posted Document Lines to Reverse…** activity.

For the document line, the sales prepayment account no. determined in the general posting setup, quantity -1, and the amount are selected (copied). The **Applied Prepayment Entry No.** field shall be left empty.

#### **_Note!_**

--- 
_After posting, a new prepayment ledger entry is created for the customer to be used for the new sales document._


***

For more information, please contact:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
