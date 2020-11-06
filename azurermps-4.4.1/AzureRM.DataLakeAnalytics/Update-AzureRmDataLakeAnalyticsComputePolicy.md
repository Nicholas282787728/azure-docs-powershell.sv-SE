---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583328"
---
# <span data-ttu-id="50f01-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="50f01-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="50f01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50f01-102">SYNOPSIS</span></span>
<span data-ttu-id="50f01-103">Uppdaterar en policy regel för beräkning av data Lake Analytics för en specifik AAD-enhet.</span><span class="sxs-lookup"><span data-stu-id="50f01-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50f01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50f01-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50f01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50f01-105">DESCRIPTION</span></span>
<span data-ttu-id="50f01-106">**Update-AzureRmDataLakeAnalyticsComputePolicy** uppdaterar den angivna beräknings princip regeln för en viss AAD-enhet i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="50f01-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="50f01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50f01-107">EXAMPLES</span></span>

### <span data-ttu-id="50f01-108">Exempel 1: uppdatera en regel i en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="50f01-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="50f01-109">Det här kommandot uppdaterar principen "policy" i kontot "contosoadla" för att säkerställa att användaren inte kan skicka jobb med mer än 5 parallellitet.</span><span class="sxs-lookup"><span data-stu-id="50f01-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="50f01-110">Exempel 2: skapa en beräknings princip med båda regel uppdateringar</span><span class="sxs-lookup"><span data-stu-id="50f01-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="50f01-111">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för att se till att användaren inte kan skicka jobb med mer än 5 parallellitet eller med en prioritet som är lägre än 100</span><span class="sxs-lookup"><span data-stu-id="50f01-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="50f01-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50f01-112">PARAMETERS</span></span>

### <span data-ttu-id="50f01-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="50f01-113">-Account</span></span>
<span data-ttu-id="50f01-114">Namnet på kontot som principen ska uppdateras i.</span><span class="sxs-lookup"><span data-stu-id="50f01-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="50f01-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="50f01-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="50f01-116">Den högsta graden av parallellitet per jobb för den här policyn.</span><span class="sxs-lookup"><span data-stu-id="50f01-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="50f01-117">Antingen den här, MinPriorityPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="50f01-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="50f01-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="50f01-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="50f01-119">Den högsta prioritet som stöds per jobb för den här principen.</span><span class="sxs-lookup"><span data-stu-id="50f01-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="50f01-120">Antingen den här, MaxDegreeOfParallelismPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="50f01-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="50f01-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="50f01-121">-Name</span></span>
<span data-ttu-id="50f01-122">Namnet på den beräknings princip som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="50f01-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="50f01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f01-123">-ResourceGroupName</span></span>
<span data-ttu-id="50f01-124">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="50f01-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="50f01-125">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="50f01-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="50f01-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50f01-126">-Confirm</span></span>
<span data-ttu-id="50f01-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50f01-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50f01-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f01-128">-WhatIf</span></span>
<span data-ttu-id="50f01-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50f01-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50f01-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50f01-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50f01-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f01-131">-DefaultProfile</span></span>
<span data-ttu-id="50f01-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50f01-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f01-133">CommonParameters</span></span>
<span data-ttu-id="50f01-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f01-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f01-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f01-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50f01-136">INPUTS</span></span>

### <span data-ttu-id="50f01-137">System. String</span><span class="sxs-lookup"><span data-stu-id="50f01-137">System.String</span></span>
<span data-ttu-id="50f01-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="50f01-138">System.Int32</span></span>

## <span data-ttu-id="50f01-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50f01-139">OUTPUTS</span></span>

### <span data-ttu-id="50f01-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="50f01-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="50f01-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50f01-141">NOTES</span></span>

## <span data-ttu-id="50f01-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50f01-142">RELATED LINKS</span></span>

