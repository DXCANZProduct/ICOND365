---
# required metadata

title: [Finance Utilities-Bank Reconciliation Matching Rules ]
description: [Introduction to Finance Utilities-Bank Reconciliation Matching Rules]
author: [helenho]
manager: Kym Parker
ms.date: 02/03/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [Finance Utilities-Bank Reconciliation Matching Rules ]
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

### Bank Reconciliation Matching Rules
#### Group by Document Capability

D365 standard does not have the capability to match one transaction in the bank statement to multiple transactions in the D365 Bank Transactions that have the same journal id or cheque number. This functionality extends the automatic reconciliation matching rules by adding **‘Group by document’.**

The feature can be activated from ***Cash and bank management > Setup > Advanced bank reconciliation setup > Reconciliation matching rules***

| Field | Description |
|-|-|
| **BASIC CRITERIA > Group by document number** | This feature combines the D365 bank transactions amount that have the same Document number (populated with the Journal id or check number) during the Bank reconciliation process, from **Run matching rules.** |

#### Matching Parameter - Included In
If the Parameter Extended matching rule operator is set to Yes, the option ‘Included in’ is available for selection, as shown in Step 1: Define the matching rule. 

When the Operator **Included in** is selected, Dynamics 365 checks whether the Value of the **Field** is included in the Value of the **Statement Fields**.

-	Contains (which is STD) means that the field Payment Reference in D365 contains the value of the Payment reference in the Bank File.
-	The Included in heading means that the field Payment Reference in D365 is included as a part of the value of the Payment reference in the Bank File.

**‘Included in’ example:**

|    Basic Criteria   |    Yes or No   |
|-|-|
|   Match Amount  |  Yes  |
|   Match Date  |  Yes  |
|   Match Document Number  |  No  |
|   Match Transaction Type  |  No  |
|   Match Payment Reference |  No  |

|    Field   |    Operator   |    Included in   |    Value   |    Statement Fields   |
|-|-|-|-|-|
|   Payment reference  |  Contains  |  Tick  |    |  Document number  |

|    Source   |   Matched   |   Booking Date   |   Debit   |   Credit   |   Bank Trx Type   |   Document number    |
|-|-|-|-|-|-|-|
|   D365 Bank Trx  |  |  |  |  |  |  |
|    |  X  |  14/01/2018  |   |  1000  |  01  |  AAU1367611  |
|    |    |  14/01/2018  |   |  1000  |  01  |  AAU1367612  |
|   Bank Statement Trx  |  |  |  |  |  |  |
|    |  X  |  14/01/2018  |   |  1000  |  699  |  CBA pmt AAU1367611   |
|    |  X  |  14/01/2018  |   |  1000  |  699  |  CBA pmt AAU1367613   |

In this example, when the Reconciliation Matching rule **Document No** is run, Dynamics 365 Bank Transactions Line 1 will be matched with Bank Statement Transactions Line 1 because the **Document number** value “AAU1367611” is included in the value of the field Reference No “CBA pmt AAU1367611”.

#### Mark as New Additional Defaults

If the **Extended financial details for new transaction** parameter is set to Yes, the option to capture the following details automatically, if the bank statement line **Mark as new** is selected.
-	Financial dimensions 
-	GST
-	Sub-Ledger offset account

|    Field / Button   |    Description   |
|-|-|
|  **Financial Dimensions > Offset accoun**  |      Financial dimensions that have to be used to post the new transactions                  If the dimensions are filled in, it will override the financial dimensions set by default on the selected main account                  Else, financial dimensions set by default on the selected main account will apply with the new transaction.           |
|  **Offset Company Account**  |    Defaults to the current legal entity.                  Populates the new field Offset Company Account in the Bank Statement Line Details form when a Line – marked as New – is created.           |
|  **Offset Account type**   |      Populates the new field Offset Account Type in the Bank Statement Line Details form when a Line – marked as New - is created.                  Note: This field defaults to Ledger; Extended financial details only support offset account type Ledger, Customer and Vendor          |
|  **Offset Account**   |  Populates the new field Offset Account in the Bank Statement Line Details form when a Line – marked as New - is created.   |
|  **GST Group**   |  Populates the field GST group in the Bank Statement Line Details form when a Line – marked as New - is created.   |
|   **Item GST Group**    |  Populates the field Item GST group in the Bank Statement Line Details form when a Line – marked as New - is created   |

