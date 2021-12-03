---
---
# EDI Setup

## Table of Contents
 - [How to setup connection with Telema server](#how-to-setup-connection-with-telema-server)
 - [How to setup connection with Edisoft server](#how-to-setup-connection-with-edisoft-server)
 - [How to setup connection between Business Centrals without operator](#how-to-setup-connection-between-business-centrals-without-operator)
 - [How to send and receive e-documents](#how-to-send-and-receive-e-documents)

## How to setup connection with Telema server
Open  **Telema EDI Setup** and the FastTab  **Connection.**  
Please ask the following information from Telema to fill in here:

| Field: |
| - |
| **API URL** |
| **API Channel Id** |
| **API Key** |

After filling  **Connection** FastTab use function  **Test Connection** to ensure that connection with Telema has been established.

## How to setup connection with Edisoft server
Open  **Telema EDI Setup** and the FastTab  **Connection.**  
Please ask the following information from Edisoft to fill in here:

| Field: |
| - |
| **Edisoft URL** |
| **Edisoft User** |
| **Edisoft Key** |

After filling  **Connection** FastTab use function  **Test Edisoft Connection** to ensure that connection with Edisoft has been established.
## How to setup connection between Business Centrals without operator
Business Central SOAP web services are used to exchange documents. SOAP service must be activated on the receiver side.
### Sending Documents
To send documents, open **Telema EDI Setup** and activate the check box **Publish E-Document Web Service** - this allows document exchange between Business Central companies.
Then open customer card from **Customers** list and on the **Telema EDI** fast tab select **Sending to Channel** *BC E-Document Web Service*.
Please ask the company to whom you want to send documents through BC for the following information:

| Field |
| - |
| **E-Document Web Service URL** |
| **E-Document Web Service User** |
| **E-Document Web Service Key** |

### Receiving Documents

To receive documents, you must provide the sender with the following information: web service URL, user name and password.
To do this, open **Web Services** and select **SOAP URL** from the **TED E-Document Web Service** line. This is the **E-Document Web Service URL**.
Then open **Users** and create a user for the sending company. Specify **User Name** and **Web Service Access Key**.
  
Give the data to the document sender.

## How to send and receive e-documents

See the manual for:  
[Inbound E-Documents](inbound-edocuments)  
[Outbound E-Documents](outbound-edocuments)
