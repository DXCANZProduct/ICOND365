---
# required metadata

title: [Finance Utilities ]
description: [Finance Utilities - Data Entities ]
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

#	Data entities

DXC Finance utilities include its own data entities in Dynamics 365 environment :

|   Entity    |   Target entity   |
|-|-|
|  Financial utilities parameters  |  SAB_FinUtilParametersEntity  |
|  Budget utilities parameters |  SAB_FinBudgetParametersEntity |

And extended the following standard data entities:

|   Entity    |   Target entity   |
|-|-|
|  Bank statement format  |  BankStatementFormatEntity  |
|  Bank accounts |  BankAccountEntity           <br> - BPAY batch ID        <br> -	Extra balance line on EFT           <br> -	Include balance line in record count           <br> -	Total line order           <br> -	Use vendor bank name      <br> -	User identification          |
|  Vendor bank accounts  |  VendVendorBankAccountEntity  |
|  Reconciliation matching rules  |  BankReconciliationMatchingRuleEntity   <br>  -	Include in.              <br> -	Group by document number             <br> -	Offset company   <br> -	Offset account type   <br>  -	Offset account    <br>  -	GST group          <br>  -	Item GST group |
