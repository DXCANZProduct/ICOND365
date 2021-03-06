---
# required metadata

title: [Finance Utilities ]
description: [Finance Utilities - Save Electronic reporting file to secure location ]
author: [helenho]
manager: Kym Parker
ms.date: 02/03/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [Finance Utilities ]
audience: [Application User]
# ms.devlang: 
ms.reviewer: [helenho]
ms.search.scope: [Which Operations client to show this topic as help for, to be set by content strategist, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
# ms.tgt_pltfrm: 
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: [Global]
# ms.search.industry: [leave blank for most, retail, public sector]
ms.author: [helenho]
ms.search.validFrom: [September 2017]
ms.dyn365.ops.version: [name of release that feature was introduced in, see list here: https://microsoft.sharepoint.com/teams/DynDoc/_layouts/15/WopiFrame.aspx?sourcedoc={23419e1c-eb64-42e9-aa9b-79875b428718}&action=edit&wd=target%28Core%20Dynamics%20AX%20CP%20requirements%2Eone%7C4CC185C0%2DEFAA%2D42CD%2D94B9%2D8F2A45E7F61A%2FVersions%20list%20for%20docs%20topics%7CC14BE630%2D5151%2D49D6%2D8305%2D554B5084593C%2F%29]
---

## Save Electronic reporting file to secure location
The file exported cn be used for any Electronic reporting file, but the example provided is for a Vendor GER EFT payment. The feature uses the Archive functionality with the following setup steps
-	Step 1: Setup Electronic reporting export connection
-	Step 2: Setup Document types, using Step 1’s Connection
-	Step 3: Setup Electronic reporting destination, using Step 2’s Document type
-	Step 4: Setup AP Method of payment and select the Export format configuration from Step 3

Processing: When generating a payment for a method of payment with above GER, the Archive destination is defaulted, and EFT payment file is saved to assigned connection path.

### Setup location
####	Electronic reporting export connections
**ORGANISATION ADMINISTRATION > ELECTRONIC REPORTING > ELECTRONIC REPORTING EXPORT CONNECTIONS**

Create the location where GER file is to be saved. Connection options include FTP/FTPS, SFTP or Azure blob

|   Field    |   Description   |   Example or Options   |
|-|-|-|
| Name |	Enter a name for your connection | ANZ_FTP |
| Connection type	| Select the applicable connection type	| -	FTP <br>	- Azure blob <br> - SFTP |
| Error action |	The action to take when there is an error with the connection | - Error <br> - Warning |

Click Save the applicable Setup will be displayed as per Connection type selected

**FTP:**

|   Field    |   Description   |   Example or Options   |
|-|-|-|
| Host | Specify the Host for the FTP site <br> Note: FTP:// is not required ||
|Path |	Enter the path where the files are to be saved on the FTP site. |	/GER_ANZ|
|Port |	Specify the Port for the FTP site |	22|
|Enable TLS |	Select to enable FTPS using TLS |	-	Yes: FTPS <br>	- No: FTP |
|User	Specify the Username used for authentication to the FTP site	||
|Credential type |	Select applicable Credential type for FTP site |	- Key vault <br> -	Database |
|Password	| Enabled when Credential type = Database. <br> Specify the Password used for authentication to the FTP site. <br> Note: this is encrypted and displayed as •••••••••• within the form.	||
|Key vault certificate |	Enabled when Credential type = Key vault. Select applicable Key vault certificate.	||

**Azure blob:**		
|   Field    |   Description   |   Example or Options   |
|-|-|-|
| Container name |	Specify the blob storage container	||
| Credential type |Select applicable Credential type for Azure blob |	-	Key vault <br>	- Database |
|Storage account name |	Enabled when Credential type = Database	||
|Storage account key |	Enabled when Credential type = Database	||
|Connection string |	Enabled when Credential type = Key vault	||

**SFTP:**
|   Field    |   Description   |   Example or Options   |
|-|-|-|
| Host |	Specify the Host for the SFTP site <br> Note: SFTP:// is not required	||
| Path	| Enter the path where the files are to be saved on the SFTP site. |	/GER_ANZ|
| Port	| Specify the Port for the SFTP site |	22 |
| Enable TLS |	Select to enable SFTP over TLS | -	Yes: SFTP over TLS <br> -	No: SFTP|
| User	| Specify the **Username** used for authentication to the SFTP site	||
| Credential type	| Select applicable Credential type for SFTP site |	-	Key vault <br> - Database |
|Password	| Enabled when Credential type = Database. Specify the Password used for authentication to the SFTP site. *Note: this is encrypted and displayed as •••••••••• within the form.* ||
|Key vault certificate |	Enabled when Credential type = Key vault. Select applicable Key vault certificate.	||


####	Document types

**ORGANISATION ADMINISTRATION > DOCUMENT MANAGEMENT > DOCUMENT TYPES**
Setup the Document type and assign the connection created in step 1

|   Field    |   Description   |   Example or Options   |
|-|-|-|
|  Type  |  Enter the type  |  Example GER  |
|  Name  |  Enter a name for the document type  |  |
|  Class  |  Select Attach file  |  -	Attach file <br> -	Attach URL <br> -	Simple note      |
|  Group  |  Select  File   |  -	Note <br> -	File <br> -	Image <br> - Document <br> - Worksheet <br> - URL         |
|  Category  |  Select a Category  |  -	None         |
|  Location SharePoint Address |  Not used, select any Not used  |  - Azure storage <br> - Database <br> - SharePoint         |
|  Remove  |  Document and physical file  |           |
|  Ask for confirmation  |  Should confirmation be requested priori to removing the file  |  - Yes <br> - No         |
|  Electronic report export connection  |  Select the Electronic reporting export connection setup in step 1 |  Example ANZ_FTP         |

####	Electronic reporting destination
**ORGANISATION ADMINISTRATION > ELECTRONIC REPORTING > ELECTRONIC REPORTING DESTINATION**

Setup Electronic reporting destination for selected GER and allocate Document type created in step 2.

|   Field    |   Description   |    Example or Options   |
|-|-|-|
|  Reference  |  Select the  Electronic reporting Reference  |  Example ‘ANZ Direct Credit Service (AU)’  |
|  Click  + New  in File  |  |  |
|  Name |  Enter name for the destination  |   |
|  File component name |  Select  PaymentFile   |   PaymentFile   |
|  Settings |  |  |
|  Stop processing on failure  |  If enabled and there are errors when saving the file to location, vendor payment processing  Generate payment  will create a file and attach to the job. The Payment status will remain  None   |  -	Yes <br> -	No          |
|  Click Settings button and select Archive destination |  |  |
|  Enabled  |  Enable the Archive destination  |  - Yes <br> - No          |
|  Save in job archive  |  Enable saving  |  - Yes <br> - No          |
|  Type  |  Select the Document type created in step 2  |  Example GER          |

####	Method of payment
Enable Generic electronic Export format and select the Electronic reporting reference from Setup Step 3 in the Accounts payable Method of payment’s Export format configuration

###	Generate payment
When a Vendor payment journal with the above Method of payment is used, the archive destination is defaulted when generating the payment.

If there is an error saving the file to secure location and Stop processing on failure was enabled the processing will error and Payment status remains None. Example error ‘The process stopped because the delivery of file ‘%’ to the destination failed. The payments cannot be generated.’

