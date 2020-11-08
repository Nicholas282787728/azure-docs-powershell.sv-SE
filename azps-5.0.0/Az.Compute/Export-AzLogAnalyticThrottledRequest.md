---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272432"
---
# <span data-ttu-id="25779-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="25779-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="25779-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25779-102">SYNOPSIS</span></span>
<span data-ttu-id="25779-103">Exportera loggar som visar totalt antal begränsade API-begäranden för detta abonnemang i det angivna tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="25779-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="25779-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25779-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25779-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25779-105">DESCRIPTION</span></span>
<span data-ttu-id="25779-106">Detta exporterar totalt antal begränsade Microsoft. Compute API-samtal.</span><span class="sxs-lookup"><span data-stu-id="25779-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="25779-107">Loggarna kan aggregeras ytterligare med tre alternativ: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="25779-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="25779-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="25779-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="25779-109">En översikt över API-begränsning för Compute Resource Provider finns i https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="25779-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="25779-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25779-110">EXAMPLES</span></span>

### <span data-ttu-id="25779-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25779-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="25779-112">Det här kommandot lagrar det totala antalet Microsoft. Compute API-samtal mellan 2018-02-20T17:54:14 och 2018-02-22T17:54:17 tum angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="25779-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="25779-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25779-113">PARAMETERS</span></span>

### <span data-ttu-id="25779-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25779-114">-AsJob</span></span>
<span data-ttu-id="25779-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="25779-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25779-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="25779-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="25779-117">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="25779-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25779-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25779-118">-DefaultProfile</span></span>
<span data-ttu-id="25779-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25779-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25779-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="25779-120">-FromTime</span></span>
<span data-ttu-id="25779-121">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="25779-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25779-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="25779-122">-GroupByOperationName</span></span>
<span data-ttu-id="25779-123">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="25779-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="25779-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="25779-124">-GroupByResourceName</span></span>
<span data-ttu-id="25779-125">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="25779-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="25779-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="25779-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="25779-127">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="25779-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="25779-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="25779-128">-Location</span></span>
<span data-ttu-id="25779-129">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="25779-129">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25779-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="25779-130">-NoWait</span></span>
<span data-ttu-id="25779-131">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="25779-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="25779-132">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="25779-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="25779-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="25779-133">-ToTime</span></span>
<span data-ttu-id="25779-134">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="25779-134">To time of the query</span></span>

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

### <span data-ttu-id="25779-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25779-135">-Confirm</span></span>
<span data-ttu-id="25779-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25779-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25779-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25779-137">-WhatIf</span></span>
<span data-ttu-id="25779-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25779-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25779-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25779-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25779-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25779-140">CommonParameters</span></span>
<span data-ttu-id="25779-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25779-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25779-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25779-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25779-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25779-143">INPUTS</span></span>

### <span data-ttu-id="25779-144">System. String</span><span class="sxs-lookup"><span data-stu-id="25779-144">System.String</span></span>

## <span data-ttu-id="25779-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25779-145">OUTPUTS</span></span>

### <span data-ttu-id="25779-146">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="25779-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="25779-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25779-147">NOTES</span></span>

## <span data-ttu-id="25779-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25779-148">RELATED LINKS</span></span>
