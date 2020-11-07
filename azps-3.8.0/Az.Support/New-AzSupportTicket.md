---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: dc3beb041a143ed151c19e0623f5db7f5f6d61e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928058"
---
# <span data-ttu-id="4dd97-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4dd97-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="4dd97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dd97-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd97-103">Skapar ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="4dd97-103">Creates a support ticket.</span></span>

## <span data-ttu-id="4dd97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dd97-104">SYNTAX</span></span>

### <span data-ttu-id="4dd97-105">CreateSupportTicketWithContactDetailParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4dd97-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd97-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd97-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd97-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd97-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd97-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd97-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd97-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd97-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd97-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd97-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd97-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dd97-111">DESCRIPTION</span></span>
<span data-ttu-id="4dd97-112">Denna cmdlet kan användas för att skapa ett support ärende för fakturering, prenumerations hantering, kvot eller tekniska problem.</span><span class="sxs-lookup"><span data-stu-id="4dd97-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="4dd97-113">Använd Get-AzSupportService-och Get-AzSupportProblemClassification cmdlets för att identifiera Azure-tjänsten och dess motsvarande problem klassificeringar för vilka du vill begära support.</span><span class="sxs-lookup"><span data-stu-id="4dd97-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="4dd97-114">Du måste ange följande parametrar:</span><span class="sxs-lookup"><span data-stu-id="4dd97-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="4dd97-115">Du kan använda New-AzSupportContactProfileObject Helper-cmdlet för att skapa CustomerContactDetail-objekt.</span><span class="sxs-lookup"><span data-stu-id="4dd97-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="4dd97-116">Med moln lösnings leverantörer kan du skapa ett support ärende för deras kund abonnemang genom att logga in på deras klient organisation och ange deras hem klient-ID genom att använda parametern *CSPHomeTenantId* .</span><span class="sxs-lookup"><span data-stu-id="4dd97-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="4dd97-117">__För tekniska biljetter:__</span><span class="sxs-lookup"><span data-stu-id="4dd97-117">__For technical tickets:__</span></span>

<span data-ttu-id="4dd97-118">Ange resursens namn genom att ange resurs-ID för ARM genom att använda parametern *TechnicalTicketResourceId* .</span><span class="sxs-lookup"><span data-stu-id="4dd97-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="4dd97-119">Visa ett exempel nedan.</span><span class="sxs-lookup"><span data-stu-id="4dd97-119">See an example below.</span></span> 

<span data-ttu-id="4dd97-120">__För kvot biljetter:__</span><span class="sxs-lookup"><span data-stu-id="4dd97-120">__For quota tickets:__</span></span>

<span data-ttu-id="4dd97-121">Om du vill begära kvot ökning för att **Beräkna virtuella dator kärnor** , **batch** , **SQL-databas** och **SQL Data Warehouse** kan du ange ytterligare uppgifter under *QuotaTicketDetail* -objektet.</span><span class="sxs-lookup"><span data-stu-id="4dd97-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="4dd97-122">QuotaTicketDetail-objekt består av 3 egenskaper enligt beskrivningen nedan.</span><span class="sxs-lookup"><span data-stu-id="4dd97-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="4dd97-123">[Klicka här](https://aka.ms/supportrpquotarequestpayload) om du vill ha mer detaljerad dokumentation.</span><span class="sxs-lookup"><span data-stu-id="4dd97-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="4dd97-124">Om du vill ha mer information om hur du konstruerar nytto last för olika typer av kvoter, [Klicka här](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="4dd97-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="4dd97-125">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dd97-125">EXAMPLES</span></span>

### <span data-ttu-id="4dd97-126">Exempel 1: skapa en support biljett för fakturerings-eller prenumerations hantering.</span><span class="sxs-lookup"><span data-stu-id="4dd97-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="4dd97-127">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för fakturerings-eller hanterings klassificeringar som du vill begära support för</span><span class="sxs-lookup"><span data-stu-id="4dd97-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-128">Exempel 2: skapa en teknisk support-biljett för en virtuell dator för Windows Resource.</span><span class="sxs-lookup"><span data-stu-id="4dd97-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="4dd97-129">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för en virtuell dator för Windows för problem klassificering som du vill begära support för</span><span class="sxs-lookup"><span data-stu-id="4dd97-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-130">Exempel 3: skapa en kvot support för att öka kvoten för virtuella dator kärnor för en viss virtuell dator familj.</span><span class="sxs-lookup"><span data-stu-id="4dd97-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="4dd97-131">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot beräkning av grundläggande problem klassificering av virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="4dd97-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-132">Exempel 4: skapa en kvot support för att öka kvoten för lågprioriterade kärnor för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4dd97-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="4dd97-133">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="4dd97-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-134">Exempel 5: skapa en kvot support för att öka kvoten för virtuella dator kärnor för en viss virtuell dator familj för ett kommando konto.</span><span class="sxs-lookup"><span data-stu-id="4dd97-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="4dd97-135">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="4dd97-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-136">Exempel 6: skapa ett kvot stöd biljetter för att öka kvoten för pooler för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4dd97-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="4dd97-137">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="4dd97-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-138">Exempel 7: skapa en kvot support för att öka aktiva jobb och schemaläggning av ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4dd97-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="4dd97-139">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="4dd97-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-140">Exempel 8: skapa en kvot support för att öka antalet konton för en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4dd97-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="4dd97-141">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för klassificering av problem med kvot satsen.</span><span class="sxs-lookup"><span data-stu-id="4dd97-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-142">Exempel 9: skapa en kvot support för att öka kvoten för DTUs för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="4dd97-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="4dd97-143">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot klassificering av SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4dd97-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-144">Exempel 10: skapa en kvot support för att öka kvoten för servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="4dd97-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="4dd97-145">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot klassificering av SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4dd97-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-146">Exempel 11: skapa en kvot support för att öka kvoten för DTUs för SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="4dd97-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="4dd97-147">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvoten för SQL-startdatumet.</span><span class="sxs-lookup"><span data-stu-id="4dd97-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-148">Exempel 12: skapa en kvot support för att öka kvoten för servrar för SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="4dd97-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="4dd97-149">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta rätt GUID för kvot klassificering av SQL Data Warehouse-problem.</span><span class="sxs-lookup"><span data-stu-id="4dd97-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-150">Exempel 13: skapa en kvot support för att öka kvoten för lågprioriterade kärnor för dator Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4dd97-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="4dd97-151">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta korrekta GUID för problem klassificering för Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4dd97-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-152">Exempel 14: skapa en kvot support för att öka kvoten för virtuella dator kärnor för en viss virtuell dator familj för dator Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4dd97-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="4dd97-153">Använd Get-AzSupportService och Get-AzSupportProblemClassification för att hämta korrekta GUID för problem klassificering för Learning-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4dd97-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-154">Exempel 15: skapa ett support ärende genom att ange enskilda parametrar för kund kontakt i stället för CustomerContactDetail-objekt.</span><span class="sxs-lookup"><span data-stu-id="4dd97-154">Example 15: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-155">Exempel 16: skapa ett support ärende med begäran om 24 x 7 svar från Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd97-155">Example 16: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4dd97-156">Exempel 17: skapa ett support ärende för din kund åt dig om du är en KRYPTOGRAFIPROVIDER.</span><span class="sxs-lookup"><span data-stu-id="4dd97-156">Example 17: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="4dd97-157">KRYPTOGRAFIPROVIDERn ska först logga in i sin klient organisation och sedan logga in i kundens klient organisation enligt exemplet nedan.</span><span class="sxs-lookup"><span data-stu-id="4dd97-157">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="4dd97-158">De måste sedan använda-CSPHomeTenantId parameter för att ange deras hem klient-ID när du skapar ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="4dd97-158">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="4dd97-159">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dd97-159">PARAMETERS</span></span>

### <span data-ttu-id="4dd97-160">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="4dd97-160">-AdditionalEmailAddress</span></span>
<span data-ttu-id="4dd97-161">Ytterligare e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="4dd97-161">Additional email addresses.</span></span>
<span data-ttu-id="4dd97-162">E-postadresser som listas här kommer att kopieras efter eventuell korrespondens om support ärendet.</span><span class="sxs-lookup"><span data-stu-id="4dd97-162">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="4dd97-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dd97-163">-AsJob</span></span>
<span data-ttu-id="4dd97-164">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="4dd97-164">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4dd97-165">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="4dd97-165">-CSPHomeTenantId</span></span>
<span data-ttu-id="4dd97-166">Det här är hem klient organisations-ID: t för moln lösnings leverantören som försöker skapa ett support ärende för sin kund.</span><span class="sxs-lookup"><span data-stu-id="4dd97-166">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="4dd97-167">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="4dd97-167">-CustomerContactDetail</span></span>
<span data-ttu-id="4dd97-168">Kund kontakt uppgifter är associerade med SupportTicket-resursen.</span><span class="sxs-lookup"><span data-stu-id="4dd97-168">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="4dd97-169">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="4dd97-169">-CustomerCountry</span></span>
<span data-ttu-id="4dd97-170">Kund land.</span><span class="sxs-lookup"><span data-stu-id="4dd97-170">Customer country.</span></span>
<span data-ttu-id="4dd97-171">Detta måste vara en giltig ISO alpha-3 landkod (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="4dd97-171">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="4dd97-172">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="4dd97-172">-CustomerFirstName</span></span>
<span data-ttu-id="4dd97-173">Kund förnamn.</span><span class="sxs-lookup"><span data-stu-id="4dd97-173">Customer first name.</span></span>

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

### <span data-ttu-id="4dd97-174">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="4dd97-174">-CustomerLastName</span></span>
<span data-ttu-id="4dd97-175">Kund efter namn.</span><span class="sxs-lookup"><span data-stu-id="4dd97-175">Customer last name.</span></span>

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

### <span data-ttu-id="4dd97-176">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="4dd97-176">-CustomerPhoneNumber</span></span>
<span data-ttu-id="4dd97-177">Kund telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="4dd97-177">Customer phone number.</span></span>
<span data-ttu-id="4dd97-178">Det här är obligatoriskt om den rekommenderade kontakt metoden är telefon.</span><span class="sxs-lookup"><span data-stu-id="4dd97-178">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="4dd97-179">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="4dd97-179">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="4dd97-180">Peferred språk för anpassade.</span><span class="sxs-lookup"><span data-stu-id="4dd97-180">Peferred language of the custom.</span></span>
<span data-ttu-id="4dd97-181">Detta måste vara ett giltigt språk för fortion för något av de språk som stöds här https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="4dd97-181">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="4dd97-182">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="4dd97-182">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="4dd97-183">Anpassad tidszon för kunder.</span><span class="sxs-lookup"><span data-stu-id="4dd97-183">Customer preferred time zone.</span></span>
<span data-ttu-id="4dd97-184">Det måste vara ett giltigt System.TimeZoneInfo.Id-värde.</span><span class="sxs-lookup"><span data-stu-id="4dd97-184">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="4dd97-185">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="4dd97-185">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="4dd97-186">Kundens primära e-postadress.</span><span class="sxs-lookup"><span data-stu-id="4dd97-186">Customer primary email address.</span></span>

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

### <span data-ttu-id="4dd97-187">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd97-187">-DefaultProfile</span></span>
<span data-ttu-id="4dd97-188">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd97-188">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd97-189">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4dd97-189">-Description</span></span>
<span data-ttu-id="4dd97-190">Detaljerad beskrivning av frågan eller problemet.</span><span class="sxs-lookup"><span data-stu-id="4dd97-190">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="4dd97-191">-Namn</span><span class="sxs-lookup"><span data-stu-id="4dd97-191">-Name</span></span>
<span data-ttu-id="4dd97-192">Namnet på det support ärende som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="4dd97-192">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4dd97-193">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="4dd97-193">-PreferredContactMethod</span></span>
<span data-ttu-id="4dd97-194">Önskad kontakt metod.</span><span class="sxs-lookup"><span data-stu-id="4dd97-194">Preferred contact method.</span></span>

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

### <span data-ttu-id="4dd97-195">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="4dd97-195">-ProblemClassificationId</span></span>
<span data-ttu-id="4dd97-196">Varje Azure-tjänst har sin egen uppsättning med problem kategorier som kallas problem klassificering som motsvarar den typ av problem du har uppstått.</span><span class="sxs-lookup"><span data-stu-id="4dd97-196">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="4dd97-197">Den här parametern är ProblemClassification resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4dd97-197">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="4dd97-198">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="4dd97-198">-ProblemStartTime</span></span>
<span data-ttu-id="4dd97-199">Datum och tid när problemet startade.</span><span class="sxs-lookup"><span data-stu-id="4dd97-199">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="4dd97-200">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="4dd97-200">-QuotaTicketDetail</span></span>
<span data-ttu-id="4dd97-201">Ytterligare information för en kvot support.</span><span class="sxs-lookup"><span data-stu-id="4dd97-201">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="4dd97-202">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="4dd97-202">-Require24X7Response</span></span>
<span data-ttu-id="4dd97-203">Anger om den här Supportens biljett kräver ett svar dygnet runt från Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd97-203">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="4dd97-204">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="4dd97-204">-Severity</span></span>
<span data-ttu-id="4dd97-205">Allvarlighets grad för support ärendet.</span><span class="sxs-lookup"><span data-stu-id="4dd97-205">Severity of the support ticket.</span></span>
<span data-ttu-id="4dd97-206">Detta indikerar hur brådskande ärendet är, som i sin tur bestämmer svars tiden enligt service nivå avtalet för det tekniska support abonnemang du har med Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd97-206">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="4dd97-207">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd97-207">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="4dd97-208">Det här är resurs-ID för Azure Service-resursen (till exempel: en virtuell dator resurs eller en HDInsight-resurs) som support ärendet skapas för.</span><span class="sxs-lookup"><span data-stu-id="4dd97-208">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="4dd97-209">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="4dd97-209">-Title</span></span>
<span data-ttu-id="4dd97-210">Titel på support ärende.</span><span class="sxs-lookup"><span data-stu-id="4dd97-210">Title of support ticket.</span></span>

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

### <span data-ttu-id="4dd97-211">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4dd97-211">-Confirm</span></span>
<span data-ttu-id="4dd97-212">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dd97-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd97-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd97-213">-WhatIf</span></span>
<span data-ttu-id="4dd97-214">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4dd97-214">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd97-215">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4dd97-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd97-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd97-216">CommonParameters</span></span>
<span data-ttu-id="4dd97-217">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd97-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd97-218">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dd97-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd97-219">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dd97-219">INPUTS</span></span>

### <span data-ttu-id="4dd97-220">Ingen</span><span class="sxs-lookup"><span data-stu-id="4dd97-220">None</span></span>

## <span data-ttu-id="4dd97-221">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dd97-221">OUTPUTS</span></span>

### <span data-ttu-id="4dd97-222">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4dd97-222">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="4dd97-223">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dd97-223">NOTES</span></span>

## <span data-ttu-id="4dd97-224">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dd97-224">RELATED LINKS</span></span>
