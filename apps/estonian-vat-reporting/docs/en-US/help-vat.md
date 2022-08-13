---
---
# Estonian VAT Report - User Guide
This functionality enables you to gather the data necessary for the main VAT declaration (Form KMD) and declaration’s appendix (Form KMD INF) and submit the data in XML file format.

## How to collect data for VAT report
Using VAT Statements functionality, you can pre-fill the VAT main report based on your VAT Statement. You have to define relations between VAT Statement and VAT Report fields.

Open **VAT Statements** and edit the statement you would like to use for reporting. You can choose for every line of the VAT Statement whether to export the line’s result to the VAT Report. In order to do so, enter the according VAT main declaration line number to the field **Box No**. If you leave the field or line you will see declaration line description in **Box Description**. A tip: clicking on the **Box Description** field will show all the declaration Form KMD lines you could use.

### No. of Cars
In addition to monetary amounts, VAT declaration main report has two quantity type of fields:
* Number of cars used for business purposes (100%)
* Number of cars used partially for business purposes
To pre-fill these fields on new declarations, open **VAT Report Setup** and setup these figures on the **Estonian VAT Report** tab.

## How to collect data for appendix of VAT Report
Open **VAT Report Setup** and on the **Estonian VAT Report** tab setup the following fields:
* **Transaction Partner to report** - choose, which of the parties will be used on declaration:
    * *Pay-to Vendor/Bill-to Customer*
    * *Buy-from Vendor/Sell-to Customer*
    * *Buy-from Vendor/Sell-to Customer (Only If VAT Reg. No. Exists)* – with this option Buy-from/Sell-to is used if **VAT Reg. No.** exist for them, otherwise Pay-to/Bill-to will be used.
* **Use Ext. Doc. No. on INF-A** - Specifies if External Document No. from Sales invoice is used on INF-A as Invoice No. (_only if Ext. Doc. No is not empty_).
* **Limit Amount** - enter transactions limit amount specified by the law (usually 1000).

The data of VAT Report appendix is collected from **VAT Entries**. To set up the necessary conditions to collect the correct data, open **VAT Posting Setup**.

For each combination of VAT posting groups you can define whether the transaction posted with that combination has to be reported or not, and set up the necessary specialities.

In order to automatically separate the transactions which have to be declared and which not, the transactions have to be posted with different VAT posting groups. The transactions to be described as exceptions, have to be posted with separate VAT posting groups as well.

Examples:
1. Transactions with companies have to be declared and transactions with private persons do not have to be declared.  Therefore, the customers and vendors who are private persons, should be posted with separate **VAT Business Posting Group** (e.g. *PRIVATE*)
2. When invoice(s) is/are issued for professional services which are treated as confidential by the laws, those transactions do not have to be declared and the sale of those services should be posted with separate **VAT Product Posting Group**.

Place a check mark to the **KMD No Declarating on INF** to those **VAT Posting Setup** lines, of which transactions do not have to be declared. You do not have to place a check mark to the **VAT Posting Setup** lines where **VAT %** is zero – those transactions will be excluded automatically.

Edit the **VAT Posting Setup** lines where you want to set up specialities. Select the speciality code to the field **KMD Speciality on Sale** or **KMD Speciality on Purchase**. Specialty '03' does not have to be and cannot be set up – this specialty will be added automatically if sales invoice has lines with VAT and also lines without VAT.

## How to create VAT Report
Open **VAT Reports** (or **VAT Returns**), create a new report, assign **No.** and choose 'EST' for **Version**.

### Getting the data
To get the data to the report, run the action **Suggest Lines** and choose the VAT statement to use and a period.

The function fills the VAT declaration data on the report lines (if you have set up the relations described in previous sections) and VAT declaration appendixes under the fields **INF-A Lines** and **INF-B Lines**.

To review the **INF-A Lines** and **INF-B Lines**, drilldown on these fields.

If needed, you can manually add data. When you want to see the details of some sales or purchase transaction on the appendixes, you can use **Navigate** function.

### Checking and completing of Registration numbers
Transaction partner name is used on the declaration if transaction partner registration number is missing. However, to prevent possible identification problems (name in BC is slightly different from the name in Tax Office database) it is recommended to fill in registration numbers in BC (on customer/vendor card). To review the list of the transaction partners with missing registration numbers, click on the appendixes **Customers without Reg. No.** or **Vendors without Reg. No.**

In order to automatically complete the missing registration numbers, you can use the function **Update Data from Business Register** in both lists. After running the update, the lists will contain those transaction partners who were not found in Business Register. Edit those customers/vendors one by one, by running function **Query from Business Register** and specifying the company name to search.

## Creating the XML file for submitting the declaration

Place the check mark **Report All Transactions** if you wish to include the invoices of those transaction partners, whose transactions total amount is below the limit (usually 1000€).

Click **Generate** to save the report into XML file. Upload and submit the file in E-Tax Board.

---
## Requirements for postings in Business Central:
1. Posted VAT Entries are required, because VAT report appendix data is based on VAT Entries. The requirement 1 is supported by following the requirements 2 and 3.
2. Transactions must be posted, using customer and vendor cards. The data of customer and vendor cards has to match the actual company information of those transaction partners.
3. Transactions must be posted as invoice or credit memo, or from the General Journal, when document type is defined as Invoice or Credit Memo.
4. The transaction partners to be declared / not to be declared must be set up with different VAT Business Posting Groups. That allows you to define the combinations of VAT posting groups in VAT Posting Setup, which have to be excluded from the declared data.
5. The items/services to be declared / not to be declared must be set up with different VAT Product Posting Groups. That allows you to define the combinations of VAT posting groups in VAT Posting Setup, which have to be excluded from the declared data.
6. The expense documents submitted by authorized employees should be posted as purchase invoices.
7. In order to declare prepayments, you must post and issue prepayment invoice(s), because the appendix of VAT Declaration is based on invoicing information and not payments information.
8. In order to include prepayment invoice in declaration only when it has been paid, you have to use BC functionality Prepayment Unrealized VAT.
