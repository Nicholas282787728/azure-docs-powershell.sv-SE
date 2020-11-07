---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: fad4a56f9fb4d46ac1b9ab9878760e46f8a20746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755606"
---
# <span data-ttu-id="1912a-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1912a-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1912a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1912a-102">SYNOPSIS</span></span>
<span data-ttu-id="1912a-103">Skapar en princip regel för data Lake Analytics för en specifik AAD-enhet.</span><span class="sxs-lookup"><span data-stu-id="1912a-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1912a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1912a-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1912a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1912a-105">DESCRIPTION</span></span>
<span data-ttu-id="1912a-106">Den **nya-AzureRmDataLakeAnalyticsComputePolicy** skapar den angivna beräknings princip regeln för en specifik AAD-enhet i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="1912a-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1912a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1912a-107">EXAMPLES</span></span>

### <span data-ttu-id="1912a-108">Exempel 1: skapa en beräknings princip med bara en regel</span><span class="sxs-lookup"><span data-stu-id="1912a-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="1912a-109">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för användaren med ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" som säkerställer att de inte kan skicka jobb med mer än 5 analys enheter.</span><span class="sxs-lookup"><span data-stu-id="1912a-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="1912a-110">Exempel 2: skapa en beräknings princip med båda reglerna</span><span class="sxs-lookup"><span data-stu-id="1912a-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="1912a-111">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för användaren med ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" som säkerställer att de inte kan skicka jobb med mer än 5 analys enheter eller med högre prioritet än 100</span><span class="sxs-lookup"><span data-stu-id="1912a-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="1912a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1912a-112">PARAMETERS</span></span>

### <span data-ttu-id="1912a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="1912a-113">-Account</span></span>
<span data-ttu-id="1912a-114">Namnet på kontot som principen ska läggas till för.</span><span class="sxs-lookup"><span data-stu-id="1912a-114">Name of the account to add the compute policy to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1912a-115">-DefaultProfile</span></span>
<span data-ttu-id="1912a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1912a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="1912a-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="1912a-118">Högsta tillåtna analys enheter per jobb för den här policyn.</span><span class="sxs-lookup"><span data-stu-id="1912a-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="1912a-119">Antingen den här, MinPriorityPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="1912a-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="1912a-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="1912a-121">Den högsta prioritet som stöds per jobb för den här principen.</span><span class="sxs-lookup"><span data-stu-id="1912a-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="1912a-122">Antingen den här, MaxAnalyticsUnitsPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="1912a-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1912a-123">-Name</span></span>
<span data-ttu-id="1912a-124">Namnet på den beräknings princip som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="1912a-124">Name of the compute policy to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1912a-125">-ObjectId</span></span>
<span data-ttu-id="1912a-126">Azure Active Directory-objekt-ID: t för den användare eller grupp som principen ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="1912a-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="1912a-127">-ObjectType</span></span>
<span data-ttu-id="1912a-128">Objekt typen Azure Active Directory för det objekt-ID som skickades.</span><span class="sxs-lookup"><span data-stu-id="1912a-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1912a-129">-ResourceGroupName</span></span>
<span data-ttu-id="1912a-130">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="1912a-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1912a-131">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1912a-131">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1912a-132">-Confirm</span></span>
<span data-ttu-id="1912a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1912a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1912a-134">-WhatIf</span></span>
<span data-ttu-id="1912a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1912a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1912a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1912a-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1912a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1912a-137">CommonParameters</span></span>
<span data-ttu-id="1912a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1912a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1912a-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1912a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1912a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1912a-140">INPUTS</span></span>

### <span data-ttu-id="1912a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1912a-141">System.String</span></span>
<span data-ttu-id="1912a-142">System. GUID system. Int32</span><span class="sxs-lookup"><span data-stu-id="1912a-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="1912a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1912a-143">OUTPUTS</span></span>

### <span data-ttu-id="1912a-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1912a-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1912a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1912a-145">NOTES</span></span>

## <span data-ttu-id="1912a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1912a-146">RELATED LINKS</span></span>

