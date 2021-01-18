---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520228"
---
# <span data-ttu-id="017e2-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="017e2-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="017e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="017e2-102">SYNOPSIS</span></span>
<span data-ttu-id="017e2-103">Skapar en princip regel för data Lake Analytics för en specifik AAD-enhet.</span><span class="sxs-lookup"><span data-stu-id="017e2-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="017e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="017e2-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="017e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="017e2-105">DESCRIPTION</span></span>
<span data-ttu-id="017e2-106">Den **nya-AzDataLakeAnalyticsComputePolicy** skapar den angivna beräknings princip regeln för en specifik AAD-enhet i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="017e2-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="017e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="017e2-107">EXAMPLES</span></span>

### <span data-ttu-id="017e2-108">Exempel 1: skapa en beräknings princip med bara en regel</span><span class="sxs-lookup"><span data-stu-id="017e2-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="017e2-109">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för användaren med ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" som säkerställer att de inte kan skicka jobb med mer än 5 analys enheter.</span><span class="sxs-lookup"><span data-stu-id="017e2-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="017e2-110">Exempel 2: skapa en beräknings princip med båda reglerna</span><span class="sxs-lookup"><span data-stu-id="017e2-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="017e2-111">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för användaren med ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" som säkerställer att de inte kan skicka jobb med mer än 5 analys enheter eller med högre prioritet än 100</span><span class="sxs-lookup"><span data-stu-id="017e2-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="017e2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="017e2-112">PARAMETERS</span></span>

### <span data-ttu-id="017e2-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="017e2-113">-Account</span></span>
<span data-ttu-id="017e2-114">Namnet på kontot som principen ska läggas till för.</span><span class="sxs-lookup"><span data-stu-id="017e2-114">Name of the account to add the compute policy to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017e2-115">-DefaultProfile</span></span>
<span data-ttu-id="017e2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="017e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="017e2-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="017e2-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="017e2-118">Högsta tillåtna analys enheter per jobb för den här policyn.</span><span class="sxs-lookup"><span data-stu-id="017e2-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="017e2-119">Antingen den här, MinPriorityPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="017e2-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="017e2-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="017e2-121">Den högsta prioritet som stöds per jobb för den här principen.</span><span class="sxs-lookup"><span data-stu-id="017e2-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="017e2-122">Antingen den här, MaxAnalyticsUnitsPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="017e2-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="017e2-123">-Name</span></span>
<span data-ttu-id="017e2-124">Namnet på den beräknings princip som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="017e2-124">Name of the compute policy to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="017e2-125">-ObjectId</span></span>
<span data-ttu-id="017e2-126">Azure Active Directory-objekt-ID: t för den användare eller grupp som principen ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="017e2-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="017e2-127">-ObjectType</span></span>
<span data-ttu-id="017e2-128">Objekt typen Azure Active Directory för det objekt-ID som skickades.</span><span class="sxs-lookup"><span data-stu-id="017e2-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="017e2-130">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="017e2-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="017e2-131">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="017e2-131">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017e2-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="017e2-132">-Confirm</span></span>
<span data-ttu-id="017e2-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="017e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="017e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="017e2-134">-WhatIf</span></span>
<span data-ttu-id="017e2-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="017e2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="017e2-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="017e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="017e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017e2-137">CommonParameters</span></span>
<span data-ttu-id="017e2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="017e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017e2-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="017e2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017e2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="017e2-140">INPUTS</span></span>

### <span data-ttu-id="017e2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="017e2-141">System.String</span></span>

### <span data-ttu-id="017e2-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="017e2-142">System.Guid</span></span>

### <span data-ttu-id="017e2-143">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="017e2-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="017e2-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="017e2-144">OUTPUTS</span></span>

### <span data-ttu-id="017e2-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="017e2-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="017e2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="017e2-146">NOTES</span></span>

## <span data-ttu-id="017e2-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="017e2-147">RELATED LINKS</span></span>
