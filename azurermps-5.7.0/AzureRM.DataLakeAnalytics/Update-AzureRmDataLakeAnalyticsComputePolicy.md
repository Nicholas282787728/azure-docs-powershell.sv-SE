---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 176a23a1909d5e7d1498add0e394311703106a7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578203"
---
# <span data-ttu-id="0fd43-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="0fd43-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="0fd43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fd43-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd43-103">Uppdaterar en policy regel för beräkning av data Lake Analytics för en specifik AAD-enhet.</span><span class="sxs-lookup"><span data-stu-id="0fd43-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fd43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fd43-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fd43-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd43-106">**Update-AzureRmDataLakeAnalyticsComputePolicy** uppdaterar den angivna beräknings princip regeln för en viss AAD-enhet i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="0fd43-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0fd43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fd43-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd43-108">Exempel 1: uppdatera en regel i en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="0fd43-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="0fd43-109">Det här kommandot uppdaterar principen "policy" i kontot "contosoadla" för att se till att användaren inte kan skicka jobb med mer än 5 analys enheter.</span><span class="sxs-lookup"><span data-stu-id="0fd43-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="0fd43-110">Exempel 2: skapa en beräknings princip med båda regel uppdateringar</span><span class="sxs-lookup"><span data-stu-id="0fd43-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="0fd43-111">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för att se till att användaren inte kan skicka jobb med mer än 5 Analytics-enheter eller med en högre prioritet än 100</span><span class="sxs-lookup"><span data-stu-id="0fd43-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="0fd43-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fd43-112">PARAMETERS</span></span>

### <span data-ttu-id="0fd43-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="0fd43-113">-Account</span></span>
<span data-ttu-id="0fd43-114">Namnet på kontot som principen ska uppdateras i.</span><span class="sxs-lookup"><span data-stu-id="0fd43-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="0fd43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd43-115">-DefaultProfile</span></span>
<span data-ttu-id="0fd43-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0fd43-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fd43-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="0fd43-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="0fd43-118">Högsta tillåtna analys enheter per jobb för den här policyn.</span><span class="sxs-lookup"><span data-stu-id="0fd43-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="0fd43-119">Antingen den här, MinPriorityPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="0fd43-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="0fd43-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="0fd43-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="0fd43-121">Den högsta prioritet som stöds per jobb för den här principen.</span><span class="sxs-lookup"><span data-stu-id="0fd43-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="0fd43-122">Antingen den här, MaxAnalyticsUnitsPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="0fd43-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="0fd43-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fd43-123">-Name</span></span>
<span data-ttu-id="0fd43-124">Namnet på den beräknings princip som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="0fd43-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="0fd43-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd43-125">-ResourceGroupName</span></span>
<span data-ttu-id="0fd43-126">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="0fd43-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="0fd43-127">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="0fd43-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="0fd43-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fd43-128">-Confirm</span></span>
<span data-ttu-id="0fd43-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fd43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd43-130">-WhatIf</span></span>
<span data-ttu-id="0fd43-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fd43-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fd43-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fd43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd43-133">CommonParameters</span></span>
<span data-ttu-id="0fd43-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd43-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd43-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fd43-136">INPUTS</span></span>

### <span data-ttu-id="0fd43-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd43-137">System.String</span></span>
<span data-ttu-id="0fd43-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0fd43-138">System.Int32</span></span>

## <span data-ttu-id="0fd43-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fd43-139">OUTPUTS</span></span>

### <span data-ttu-id="0fd43-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="0fd43-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="0fd43-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fd43-141">NOTES</span></span>

## <span data-ttu-id="0fd43-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fd43-142">RELATED LINKS</span></span>

