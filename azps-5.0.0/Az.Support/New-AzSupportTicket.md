---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271686"
---
# <span data-ttu-id="9a70a-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9a70a-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="9a70a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a70a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a70a-103">Skapar ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="9a70a-103">Creates a support ticket.</span></span>

## <span data-ttu-id="9a70a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a70a-104">SYNTAX</span></span>

### <span data-ttu-id="9a70a-105">CreateSupportTicketWithContactDetailParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9a70a-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a70a-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a70a-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a70a-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a70a-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a70a-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a70a-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a70a-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a70a-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a70a-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a70a-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a70a-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a70a-111">DESCRIPTION</span></span>
<span data-ttu-id="9a70a-112">Denna cmdlet kan användas för att skapa ett support ärende för fakturering, prenumerations hantering, kvot eller tekniska problem.</span><span class="sxs-lookup"><span data-stu-id="9a70a-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="9a70a-113">Använd Get-AzSupportService-och Get-AzSupportProblemClassification cmdlets för att identifiera Azure-tjänsten och dess motsvarande problem klassificeringar för vilka du vill begära support.</span><span class="sxs-lookup"><span data-stu-id="9a70a-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="9a70a-114">Du måste ange följande parametrar:</span><span class="sxs-lookup"><span data-stu-id="9a70a-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="9a70a-115">Du kan använda New-AzSupportContactProfileObject Helper-cmdlet för att skapa CustomerContactDetail-objekt.</span><span class="sxs-lookup"><span data-stu-id="9a70a-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="9a70a-116">Med moln lösnings leverantörer kan du skapa ett support ärende för deras kund abonnemang genom att logga in på deras klient organisation och ange deras hem klient-ID genom att använda parametern *CSPHomeTenantId* .</span><span class="sxs-lookup"><span data-stu-id="9a70a-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="9a70a-117">__För tekniska biljetter:__</span><span class="sxs-lookup"><span data-stu-id="9a70a-117">__For technical tickets:__</span></span>

<span data-ttu-id="9a70a-118">Ange resursens namn genom att ange resurs-ID för ARM genom att använda parametern *TechnicalTicketResourceId* .</span><span class="sxs-lookup"><span data-stu-id="9a70a-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="9a70a-119">Visa ett exempel nedan.</span><span class="sxs-lookup"><span data-stu-id="9a70a-119">See an example below.</span></span> 

<span data-ttu-id="9a70a-120">__För kvot biljetter:__</span><span class="sxs-lookup"><span data-stu-id="9a70a-120">__For quota tickets:__</span></span>

<span data-ttu-id="9a70a-121">Om du vill begära kvot ökning för att **Beräkna virtuella dator kärnor** , **batch** , **SQL-databas** och **SQL Data Warehouse** kan du ange ytterligare uppgifter under *QuotaTicketDetail* -objektet.</span><span class="sxs-lookup"><span data-stu-id="9a70a-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="9a70a-122">QuotaTicketDetail-objekt består av 3 egenskaper enligt beskrivningen nedan.</span><span class="sxs-lookup"><span data-stu-id="9a70a-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="9a70a-123">[Klicka här](https://aka.ms/supportrpquotarequestpayload) om du vill ha mer detaljerad dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9a70a-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="9a70a-124">Om du vill ha mer information om hur du konstruerar nytto last för olika typer av kvoter, [Klicka här](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="9a70a-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="9a70a-125">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a70a-125">EXAMPLES</span></span>

### <span data-ttu-id="9a70a-126">Exempel 1: skapa en support biljett för fakturerings-eller prenumerations hantering.</span><span class="sxs-lookup"><span data-stu-id="9a70a-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="9a70a-127">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för fakturerings-eller hanterings klassificeringar som du vill begära support för</span><span class="sxs-lookup"><span data-stu-id="9a70a-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-128">Exempel 2: skapa en teknisk support-biljett för en virtuell dator för Windows Resource.</span><span class="sxs-lookup"><span data-stu-id="9a70a-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="9a70a-129">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för en virtuell dator för Windows för problem klassificering som du vill begära support för</span><span class="sxs-lookup"><span data-stu-id="9a70a-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-130">Exempel 3: skapa en kvot support för att öka kvoten för virtuella dator kärnor för en viss virtuell dator familj.</span><span class="sxs-lookup"><span data-stu-id="9a70a-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="9a70a-131">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot beräkning av grundläggande problem klassificering av virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="9a70a-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-132">Exempel 4: skapa en kvot support för att öka kvoten för lågprioriterade kärnor för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="9a70a-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="9a70a-133">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="9a70a-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-134">Exempel 5: skapa en kvot support för att öka kvoten för virtuella dator kärnor för en viss virtuell dator familj för ett kommando konto.</span><span class="sxs-lookup"><span data-stu-id="9a70a-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="9a70a-135">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="9a70a-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-136">Exempel 6: skapa ett kvot stöd biljetter för att öka kvoten för pooler för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="9a70a-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="9a70a-137">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="9a70a-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-138">Exempel 7: skapa en kvot support för att öka aktiva jobb och schemaläggning av ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="9a70a-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="9a70a-139">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="9a70a-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-140">Exempel 8: skapa en kvot support för att öka antalet konton för en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9a70a-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="9a70a-141">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="9a70a-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-142">Exempel 9: skapa en kvot support för att öka kvoten för DTUs för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="9a70a-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="9a70a-143">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot klassificering av SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9a70a-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-144">Exempel 10: skapa en kvot support för att öka kvoten för servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="9a70a-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="9a70a-145">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot klassificering av SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9a70a-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-146">Exempel 11: skapa en kvot support för att öka kvoten för DTUs för SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="9a70a-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="9a70a-147">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvoten för SQL-startdatumet.</span><span class="sxs-lookup"><span data-stu-id="9a70a-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-148">Exempel 12: skapa en kvot support för att öka kvoten för servrar för SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="9a70a-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="9a70a-149">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot klassificering av SQL Data Warehouse-problem.</span><span class="sxs-lookup"><span data-stu-id="9a70a-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-150">Exempel 13: skapa en kvot support för att öka kvoten för lågprioriterade kärnor för dator Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9a70a-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="9a70a-151">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta korrekta GUID för problem klassificering för Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9a70a-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-152">Exempel 14: skapa en kvot support för att öka kvoten för virtuella dator kärnor för en viss virtuell dator familj för dator Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9a70a-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="9a70a-153">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta korrekta GUID för problem klassificering för Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9a70a-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-154">Exempel 15: skapa en kvot support för att öka kvoten för en hanterad Azure SQL-instans.</span><span class="sxs-lookup"><span data-stu-id="9a70a-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="9a70a-155">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för SQL-hanterade instans tjänst problem klassificering.</span><span class="sxs-lookup"><span data-stu-id="9a70a-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-156">Exempel 16: skapa ett support ärende genom att ange enskilda parametrar för kund kontakt i stället för CustomerContactDetail-objekt.</span><span class="sxs-lookup"><span data-stu-id="9a70a-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-157">Exempel 17: skapa ett support ärende med begäran om 24 x 7 svar från Azure.</span><span class="sxs-lookup"><span data-stu-id="9a70a-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9a70a-158">Exempel 18: skapa ett support ärende åt din kunds räkning om du är en KRYPTOGRAFIPROVIDER.</span><span class="sxs-lookup"><span data-stu-id="9a70a-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="9a70a-159">KRYPTOGRAFIPROVIDERn ska först logga in i sin klient organisation och sedan logga in i kundens klient organisation enligt exemplet nedan.</span><span class="sxs-lookup"><span data-stu-id="9a70a-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="9a70a-160">De måste sedan använda-CSPHomeTenantId parameter för att ange deras hem klient-ID när du skapar ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="9a70a-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="9a70a-161">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a70a-161">PARAMETERS</span></span>

### <span data-ttu-id="9a70a-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9a70a-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="9a70a-163">Ytterligare e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="9a70a-163">Additional email addresses.</span></span>
<span data-ttu-id="9a70a-164">E-postadresser som listas här kommer att kopieras efter eventuell korrespondens om support ärendet.</span><span class="sxs-lookup"><span data-stu-id="9a70a-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a70a-165">-AsJob</span></span>
<span data-ttu-id="9a70a-166">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="9a70a-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="9a70a-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="9a70a-168">Det här är hem klient organisations-ID: t för moln lösnings leverantören som försöker skapa ett support ärende för sin kund.</span><span class="sxs-lookup"><span data-stu-id="9a70a-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="9a70a-169">-CustomerContactDetail</span></span>
<span data-ttu-id="9a70a-170">Kund kontakt uppgifter är associerade med SupportTicket-resursen.</span><span class="sxs-lookup"><span data-stu-id="9a70a-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="9a70a-171">-CustomerCountry</span></span>
<span data-ttu-id="9a70a-172">Kund land.</span><span class="sxs-lookup"><span data-stu-id="9a70a-172">Customer country.</span></span>
<span data-ttu-id="9a70a-173">Detta måste vara en giltig ISO alpha-3 landkod (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="9a70a-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="9a70a-174">-CustomerFirstName</span></span>
<span data-ttu-id="9a70a-175">Kund förnamn.</span><span class="sxs-lookup"><span data-stu-id="9a70a-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="9a70a-176">-CustomerLastName</span></span>
<span data-ttu-id="9a70a-177">Kund efter namn.</span><span class="sxs-lookup"><span data-stu-id="9a70a-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9a70a-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="9a70a-179">Kund telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="9a70a-179">Customer phone number.</span></span>
<span data-ttu-id="9a70a-180">Det här är obligatoriskt om den rekommenderade kontakt metoden är telefon.</span><span class="sxs-lookup"><span data-stu-id="9a70a-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="9a70a-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="9a70a-182">Peferred språk för anpassade.</span><span class="sxs-lookup"><span data-stu-id="9a70a-182">Peferred language of the custom.</span></span>
<span data-ttu-id="9a70a-183">Detta måste vara ett giltigt språk för fortion för något av de språk som stöds här https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="9a70a-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="9a70a-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="9a70a-185">Anpassad tidszon för kunder.</span><span class="sxs-lookup"><span data-stu-id="9a70a-185">Customer preferred time zone.</span></span>
<span data-ttu-id="9a70a-186">Det måste vara ett giltigt System.TimeZoneInfo.Id-värde.</span><span class="sxs-lookup"><span data-stu-id="9a70a-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9a70a-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="9a70a-188">Kundens primära e-postadress.</span><span class="sxs-lookup"><span data-stu-id="9a70a-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a70a-189">-DefaultProfile</span></span>
<span data-ttu-id="9a70a-190">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a70a-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-191">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9a70a-191">-Description</span></span>
<span data-ttu-id="9a70a-192">Detaljerad beskrivning av frågan eller problemet.</span><span class="sxs-lookup"><span data-stu-id="9a70a-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-193">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a70a-193">-Name</span></span>
<span data-ttu-id="9a70a-194">Namnet på det support ärende som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="9a70a-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="9a70a-195">-PreferredContactMethod</span></span>
<span data-ttu-id="9a70a-196">Önskad kontakt metod.</span><span class="sxs-lookup"><span data-stu-id="9a70a-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="9a70a-197">-ProblemClassificationId</span></span>
<span data-ttu-id="9a70a-198">Varje Azure-tjänst har sin egen uppsättning med problem kategorier som kallas problem klassificering som motsvarar den typ av problem du har uppstått.</span><span class="sxs-lookup"><span data-stu-id="9a70a-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="9a70a-199">Den här parametern är ProblemClassification resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9a70a-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="9a70a-200">-ProblemStartTime</span></span>
<span data-ttu-id="9a70a-201">Datum och tid när problemet startade.</span><span class="sxs-lookup"><span data-stu-id="9a70a-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="9a70a-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="9a70a-203">Ytterligare information för en kvot support.</span><span class="sxs-lookup"><span data-stu-id="9a70a-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="9a70a-204">-Require24X7Response</span></span>
<span data-ttu-id="9a70a-205">Anger om den här Supportens biljett kräver ett svar dygnet runt från Azure.</span><span class="sxs-lookup"><span data-stu-id="9a70a-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-206">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="9a70a-206">-Severity</span></span>
<span data-ttu-id="9a70a-207">Allvarlighets grad för support ärendet.</span><span class="sxs-lookup"><span data-stu-id="9a70a-207">Severity of the support ticket.</span></span>
<span data-ttu-id="9a70a-208">Detta indikerar hur brådskande ärendet är, som i sin tur bestämmer svars tiden enligt service nivå avtalet för det tekniska support abonnemang du har med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a70a-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="9a70a-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="9a70a-210">Det här är resurs-ID för Azure Service-resursen (till exempel: en virtuell dator resurs eller en HDInsight-resurs) som support ärendet skapas för.</span><span class="sxs-lookup"><span data-stu-id="9a70a-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-211">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="9a70a-211">-Title</span></span>
<span data-ttu-id="9a70a-212">Titel på support ärende.</span><span class="sxs-lookup"><span data-stu-id="9a70a-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-213">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a70a-213">-Confirm</span></span>
<span data-ttu-id="9a70a-214">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a70a-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a70a-215">-WhatIf</span></span>
<span data-ttu-id="9a70a-216">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a70a-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a70a-217">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a70a-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a70a-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a70a-218">CommonParameters</span></span>
<span data-ttu-id="9a70a-219">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a70a-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a70a-220">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a70a-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a70a-221">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a70a-221">INPUTS</span></span>

### <span data-ttu-id="9a70a-222">Ingen</span><span class="sxs-lookup"><span data-stu-id="9a70a-222">None</span></span>

## <span data-ttu-id="9a70a-223">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a70a-223">OUTPUTS</span></span>

### <span data-ttu-id="9a70a-224">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9a70a-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9a70a-225">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a70a-225">NOTES</span></span>

## <span data-ttu-id="9a70a-226">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a70a-226">RELATED LINKS</span></span>
