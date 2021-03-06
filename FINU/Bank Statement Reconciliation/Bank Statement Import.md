---
# required metadata

title: [Finance Utilities ]
description: [Finance Utilities - Bank Statement Import ]
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

## Bank Statement Import 

The Bank Statement Import form is used to import the bank statement into your Dynamics 365 environment. 
Within this form, you will set up the bank statement import details regarding your vendor of the payment transaction. 

You can reach the  BANK STATEMENTS – IMPORT STATEMENT form by navigating to
***CASH AND BANK MANAGEMENT > BANK STATEMENT RECONCILIATION > BANK STATEMENTS – IMPORT STATEMENT***

Where the selected statement format is marked as **customised format** the following features are available; 

|    Field   |    Description   |
|-|-|
|   From date   |  Select transactions equal to, or more recent than, this date  |
|   To date   |  Select transactions equal to, or earlier than, this date  |
 
 The Bank statement import also provides user the option to specify which date to use as accounting / transaction date when posting the mark as new transaction/s. Available options are:
- Today’s date
- Statement Transaction Date (To date of Statement header)
Where the bank statement file contains transactions related to multiple dates and multiple bank accounts (i.e. the file is imported using the option **Import statement for multiple bank accounts in all legal entities**, separate bank statement records get created in Dynamics 365 for each bank account. 
 
The **Statement ID** number sequence in Cash and bank management parameters is used to generate the Statement identifier. 

When a bank statement (BAI2/NAI/BRS/Flat file) is imported, statement lines will only be imported where the following matching rules are validated:  
1.	Transaction date in the bank statement line has to be between the **From date** and **To date** specified in the ‘import bank statement’ screen.  

2.	If **Import statement for multiple bank accounts in all legal entities** is NOT enabled in the import bank statement screen, the bank account number in the bank statement line has to match the bank account number of the bank account selected in the import bank statement screen. 

3.	If **Import statement for multiple bank accounts in all legal entities** is enabled in the import bank statement screen, the **bank account number** in the bank statement line has to match the bank account number of one of the bank accounts in bank master. 

In addition, where Import statement for multiple bank accounts in all legal entities is enabled, and if Dynamics 365 finds multiple bank accounts in same/different legal entities with the same bank account number while importing the statement, following order of priority is applied: 

1.	Bank accounts with the same **bank account number** in the same D365 entity in which user is importing the bank statement, system imports the bank statement to the first identified bank account record. 

2.	If the bank account exists within multiple D365 entities, the bank statement is imported into the bank account in the D365 entity from which user is importing the bank statement. If this bank account is not in the entity in which user is importing the bank statement, system imports the bank statement to the first identified bank account record 

