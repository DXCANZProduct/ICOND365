---
# required metadata

title: [Finance Utilities ]
description: [Finance Utilities - Budget Import ]
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

# Budget Import
## Budget Import Setup

The budget import form is used to import your budget data into your Dynamics 365 environment. 
Within this form, you will set up the details regarding the transaction details in csv import file format that will be utilized for sending data through the budget import form into the  Dynamics 365 environment.

You can reach the DIMENSIONS form by navigating to

**BUDGETING > SETUP > BASIC BUDGETING > DIMENSIONS**

Select the financial dimensions to use for budgeting. Only these ‘Budget dimensions’ will be available in the Budget Utilities parameters *

You can reach the BUDGET UTILITIES PARAMETERS form by navigating to

**BUDGETING > SETUP > BASIC BUDGETING > BUDGET UTILITIES PARAMETERS**
The Parameters’ form is used to set the file format for the import:
|   Field    |   Description   |
|-|-|
|  Field Separator  |  Specify the field separator for the CSV file  |
|  Number of Months  |  Specify the number of months that will be imported in the file  |
|  Skip Rows  |  If the file has a header row, you can specify 1 in this field.  With this setup, the 2nd row will be the 1st row to be imported  |
|  Dimension Code  |  Select the dimensions required in the import fields for the budget register entries *  |
|  Chart of Accounts Delimiter  |  Select the delimiter used as the delimiter between the dimension elements in the import fields  |
|  Dimension Format  |  When the dimensions are selected in the dimension code field, these will automatically be populated the Dimension Format field in financial dimension sort order.  To change the order of these fields, simply cut & paste dimensions into required order to match the import file.      <br>      *Note: For all accounts a valid value must be populated in the import file for each financial dimension specified even where the account structure does not require this dimension.* |  
