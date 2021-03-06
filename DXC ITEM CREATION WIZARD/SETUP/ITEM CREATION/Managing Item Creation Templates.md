---
# required metadata

title: [DXC Item Creation Wizard]
description: [DXC Item Creation Wizard  - Managing Item Creation Template]
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

### Managing Item Creation Templates
#### Create A New Version

The Item Creation Templates form is used to set up the template within your Dynamics 365 environment and your items. 
Within this form, you will set up the details regarding the items attributes, along with a company that can utilized the item. 
You can reach the item creation template form by navigating to

**Item creation > Setup > Item creation > Item creation templates > New version (button)**

Versions allow the same template to be used but with an update, a new version number is generated.  It is possible to see the version used to create the Product for logging and audit purposes. 

1.	Select the **template** which you wish to copy.
2.	Click **New version** icon from the Ribbon bar.
3.	Select the template in the **Copy from** field, this will default from the record selected.
4.	Select the Version that you wish to copy, this will default from the record selected.
5.	Enter a **Description**.
6.	If this new version should be the Current version click the check box **Set as current version.**
7.	Click **OK**.

##### Manage Versions
###### View Versions

**Item creation > Setup > Item creation > Item creation templates > Versions (button)**

Managing versions by clicking the Versions icon on the Ribbon bar allows the possibility to Edit the description, Activate a version, Set as the current version etc… by clicking the respective button. In addition, it is possible to delete a version, add a new version or copy a version from this form.

1.	Select the **template** which you wish to modify.
2.	Click the **Manage > Versions** icon on the Ribbon bar.
3.	Select the **Version.**
4.	Click the **Activate** button.
5.	To set the 'current' version select click the **Set current** button.

###### Activate a Version
**Item creation > Setup > Item creation > Item creation templates > Activate (button)**
To use an Item Creation template, it must be activated. It is not possible to edit an Activated template.

1.	Select the **template** which you wish to activate.
2.	Click the **Activate** icon on the Ribbon bar.

##### Deactivate a Version
**Item creation > Setup > Item creation > Item creation templates > Deactivate (button)**

It is possible to stop using an Item creation template by deactivating it.
1.	Select the **Template** you wish to deactivate.
2.	Click the **Manage > Deactivate** icon from the Ribbon bar.

#### Copy Versions
**Item creation > Setup > Item creation > Item creation templates > Copy (button)**

It is possible to stop using an Item Creation template by Deactivating it.
1.	Click **Copy.**
2.	Enter a **Template** name. 
3.	Select the **Template type** 
4.	Select the **Status** that the Product gets set to when using this template for Product creation.
5.	To copy only the current version, tick the check box **Only current version.**
6.	Click **OK.** 
