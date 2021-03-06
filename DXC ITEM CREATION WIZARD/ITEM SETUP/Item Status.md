---
# required metadata

title: [DXC Item Creation Wizard ]
description: [DXC Item Creation Wizard -Setting up for Item Status  ]
author: [helenho]
manager: Kym Parker
ms.date: 02/03/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [DXC Item Creation Wizard ]
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

## Setting up for Item Status

Prior to using the Item Status functionality, some setup must be completed.
### Set up Parameters

Before you start using the item status, setup must be completed for the parameters applicable to **item status.**

**Item creation > Setup > Item creation parameters> Item status (tab)**

It is possible to enable/disable the Item status functionality as well as set a default item status to suit organisation/business needs for new items.  
1.	Select the **Status control enabled** flag.  This will enable the transactions specified in the Item status setup form. 
2.	Select the **Default item status** if required. 

Note: The **Default item status** will be setup at the item level.

### Set up Item Status

The item status form is used to set up the status of your items in Dynamics 365 environment. 
Within this form, you will set up the details regarding the status of the items, 
along with a status indicator that will be utilized for sales order, sales picking, sales delivery, web sales, sales return and sales indicator. 
You can reach the Item status form by navigating to

**Item creation > Setup > Item Setup > Item Status**
The items status controls whether a product can be purchased, sales order (create a sales order), sales picking (create a pick list or output order) or sales return (allow sales returns).  

1.	Click the **New** button. 
2.	Enter a **Status** name which will be recognised by the business users.
3.	Tick the **Purchase order** check box to select whether a product with this status can be purchased. 

*Note: Even if this was not ticked it will still be possible to return a product.*

4.	Tick the **Sales order** check box to select whether a product with this status can be selected on a sales order.
5.	Tick the **Sales picking** check box to select whether a product with this status can be picked.
6.	Tick the **Sales delivery** check box to select whether a product with this status can be delivered or invoiced.
7.	Tick the **Sales return** check box to allow a product to be returned.
8.	Select a **Status indicator** to identify the status of the item on the Released products list page and from the Purchase and Sales lines.

*Note: The status indicator is displayed on the Released products form as a display only field.*

#### Set up Allowed Status transitions

This option is to limiti the amendment of a status transition allows the organisation to control how the user changes the lifecycle of a product. 

**Item creation > Setup > Item Setup > Item status > Allowed status transitions (button)**

1.	Within the Status form select the **status.** 
2.	Click the button **Allowed status transitions.**
3.	Click the **New** button. 
4.	Select the To Status. 
5.	Repeat as necessary. 
6.	Click **Close** once completed. 

