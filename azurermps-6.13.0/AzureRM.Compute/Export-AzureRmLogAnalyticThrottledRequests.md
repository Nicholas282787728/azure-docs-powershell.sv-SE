---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575314"
---
# <span data-ttu-id="a0cf9-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="a0cf9-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="a0cf9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cf9-103">Exportera loggar som visar totalt antal begränsade API-begäranden för detta abonnemang i det angivna tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0cf9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0cf9-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0cf9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cf9-106">Detta exporterar totalt antal begränsade Microsoft. Compute API-samtal.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="a0cf9-107">Loggarna kan aggregeras ytterligare med tre alternativ: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="a0cf9-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="a0cf9-109">En översikt över API-begränsning för Compute Resource Provider finns i https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="a0cf9-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="a0cf9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0cf9-110">EXAMPLES</span></span>

### <span data-ttu-id="a0cf9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a0cf9-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="a0cf9-112">Det här kommandot lagrar det totala antalet Microsoft. Compute API-samtal mellan 2018-02-20T17:54:14 och 2018-02-22T17:54:17 tum angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="a0cf9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0cf9-113">PARAMETERS</span></span>

### <span data-ttu-id="a0cf9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0cf9-114">-AsJob</span></span>
<span data-ttu-id="a0cf9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a0cf9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0cf9-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a0cf9-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="a0cf9-117">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cf9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cf9-118">-DefaultProfile</span></span>
<span data-ttu-id="a0cf9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0cf9-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="a0cf9-120">-FromTime</span></span>
<span data-ttu-id="a0cf9-121">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="a0cf9-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cf9-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="a0cf9-122">-GroupByOperationName</span></span>
<span data-ttu-id="a0cf9-123">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="a0cf9-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="a0cf9-124">-GroupByResourceName</span></span>
<span data-ttu-id="a0cf9-125">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="a0cf9-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="a0cf9-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="a0cf9-127">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="a0cf9-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="a0cf9-128">-Location</span></span>
<span data-ttu-id="a0cf9-129">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-129">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cf9-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="a0cf9-130">-ToTime</span></span>
<span data-ttu-id="a0cf9-131">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="a0cf9-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cf9-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0cf9-132">-Confirm</span></span>
<span data-ttu-id="a0cf9-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cf9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cf9-134">-WhatIf</span></span>
<span data-ttu-id="a0cf9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cf9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cf9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cf9-137">CommonParameters</span></span>
<span data-ttu-id="a0cf9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cf9-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cf9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cf9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0cf9-140">INPUTS</span></span>

### <span data-ttu-id="a0cf9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a0cf9-141">System.String</span></span>

## <span data-ttu-id="a0cf9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0cf9-142">OUTPUTS</span></span>

### <span data-ttu-id="a0cf9-143">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="a0cf9-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="a0cf9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0cf9-144">NOTES</span></span>

## <span data-ttu-id="a0cf9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0cf9-145">RELATED LINKS</span></span>
