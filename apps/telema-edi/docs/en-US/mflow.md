---
---
# Telema MatchFlow

Read more about MatchFlow on the Telema website: [https://eflow.live/et/mflow/](https://eflow.live/et/mflow/)

With MatchFlow you can match a purchase order and receipt against an incoming invoice. To do this, the purchase order and receipt must be sent to MatchFlow, where the incoming invoice is matched and verified, after which it is ready to be received into the ERP.

## Vendor Setup
To enable MatchFlow for a vendor, configure the vendor card as follows:

| Field | Value | Description |
| - | - | - |
| **Telema mFlow** | 3-way matching | Both the order and the receipt are sent to MatchFlow. |
| **Send E-Order** | Yes or No | Yes, if you also want to send the order to the vendor; No, if only to MatchFlow. |
| **Send E-Receipt** | Yes or No | Yes, if you also want to send the receipt to the vendor; No, if only to MatchFlow. |

## Sending Vendors
If needed, you can send vendor data to the MatchFlow environment.

To create a partners file (an e-document of type 'partners'), open **Outbound E-Documents (EDI)** and run the action:  
Actions -> New -> Create Document from BC -> **Create Partners**

## Sending a Purchase Order
To send a purchase order to MatchFlow, open the purchase order and in the **Telema E-Document** factbox run the action **Issue E-Order**.

If the vendor card has both **Telema mFlow** and **Send E-Order** enabled, two orders will be issued — one for MatchFlow and one for the vendor.

## Sending a Purchase Receipt
The purchase receipt is issued automatically during posting.

If the vendor card has both **Telema mFlow** and **Send E-Receipt** enabled, two receipts will be issued — one for MatchFlow and one for the vendor.

## Receiving a Purchase Invoice
A purchase invoice received from MatchFlow is saved as a purchase invoice with links to the purchase order and purchase receipts.

The purchase invoice is therefore ready for posting.

BC automatically updates the linked purchase order during posting.
