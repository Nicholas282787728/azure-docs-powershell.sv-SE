---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320643"
---
# <span data-ttu-id="6767e-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="6767e-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="6767e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6767e-102">SYNOPSIS</span></span>
<span data-ttu-id="6767e-103">Uppdaterar en policy regel för beräkning av data Lake Analytics för en specifik AAD-enhet.</span><span class="sxs-lookup"><span data-stu-id="6767e-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="6767e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6767e-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6767e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6767e-105">DESCRIPTION</span></span>
<span data-ttu-id="6767e-106">**Update-AzDataLakeAnalyticsComputePolicy** uppdaterar den angivna beräknings princip regeln för en viss AAD-enhet i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="6767e-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6767e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6767e-107">EXAMPLES</span></span>

### <span data-ttu-id="6767e-108">Exempel 1: uppdatera en regel i en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="6767e-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="6767e-109">Det här kommandot uppdaterar principen "policy" i kontot "contosoadla" för att se till att användaren inte kan skicka jobb med mer än 5 analys enheter.</span><span class="sxs-lookup"><span data-stu-id="6767e-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="6767e-110">Exempel 2: skapa en beräknings princip med båda regel uppdateringar</span><span class="sxs-lookup"><span data-stu-id="6767e-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="6767e-111">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för att se till att användaren inte kan skicka jobb med mer än 5 Analytics-enheter eller med en högre prioritet än 100</span><span class="sxs-lookup"><span data-stu-id="6767e-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="6767e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6767e-112">PARAMETERS</span></span>

### <span data-ttu-id="6767e-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="6767e-113">-Account</span></span>
<span data-ttu-id="6767e-114">Namnet på kontot som principen ska uppdateras i.</span><span class="sxs-lookup"><span data-stu-id="6767e-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="6767e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6767e-115">-DefaultProfile</span></span>
<span data-ttu-id="6767e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6767e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6767e-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="6767e-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="6767e-118">Högsta tillåtna analys enheter per jobb för den här policyn.</span><span class="sxs-lookup"><span data-stu-id="6767e-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="6767e-119">Antingen den här, MinPriorityPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="6767e-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="6767e-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="6767e-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="6767e-121">Den högsta prioritet som stöds per jobb för den här principen.</span><span class="sxs-lookup"><span data-stu-id="6767e-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="6767e-122">Antingen den här, MaxAnalyticsUnitsPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="6767e-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="6767e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6767e-123">-Name</span></span>
<span data-ttu-id="6767e-124">Namnet på den beräknings princip som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="6767e-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="6767e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6767e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6767e-126">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="6767e-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="6767e-127">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="6767e-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="6767e-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6767e-128">-Confirm</span></span>
<span data-ttu-id="6767e-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6767e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6767e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6767e-130">-WhatIf</span></span>
<span data-ttu-id="6767e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6767e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6767e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6767e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6767e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6767e-133">CommonParameters</span></span>
<span data-ttu-id="6767e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6767e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6767e-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6767e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6767e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6767e-136">INPUTS</span></span>

### <span data-ttu-id="6767e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6767e-137">System.String</span></span>

### <span data-ttu-id="6767e-138">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6767e-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6767e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6767e-139">OUTPUTS</span></span>

### <span data-ttu-id="6767e-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="6767e-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="6767e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6767e-141">NOTES</span></span>

## <span data-ttu-id="6767e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6767e-142">RELATED LINKS</span></span>