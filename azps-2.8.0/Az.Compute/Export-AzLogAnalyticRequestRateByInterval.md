---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 0c76a4fe34e99de8a0cb13759f7247ae3a643302
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745218"
---
# <span data-ttu-id="dcd65-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="dcd65-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="dcd65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcd65-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd65-103">Exportera loggar som visar API-begäranden som gjorts av detta abonnemang i tidsfönstret för att Visa begränsnings aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="dcd65-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="dcd65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcd65-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd65-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcd65-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd65-106">Exporterar statistik information om prenumerationens samtal till Microsoft. Compute API efter framgång, misslyckad eller begränsad status, i fördefinierade tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="dcd65-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="dcd65-107">Loggarna kan grupperas ytterligare med tre parametrar: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="dcd65-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="dcd65-108">Observera att den här cmdleten endast samlar in en Compute Resource Provider-loggar; Dessutom finns inte data om resurs typerna disk och ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="dcd65-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="dcd65-109">En översikt över API-begränsning för Compute Resource Provider finns i https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="dcd65-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="dcd65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcd65-110">EXAMPLES</span></span>

### <span data-ttu-id="dcd65-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dcd65-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="dcd65-112">Det här kommandot lagrar de aggregerade numren för Microsoft. Compute API-samtal avgränsade med lyckat, misslyckat eller begränsat mellan 2018 – 02-20T17:54:14 och 2018-02-22T17:54:17 i angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="dcd65-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="dcd65-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcd65-113">PARAMETERS</span></span>

### <span data-ttu-id="dcd65-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcd65-114">-AsJob</span></span>
<span data-ttu-id="dcd65-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dcd65-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcd65-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="dcd65-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="dcd65-117">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="dcd65-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="dcd65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd65-118">-DefaultProfile</span></span>
<span data-ttu-id="dcd65-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd65-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="dcd65-120">-FromTime</span></span>
<span data-ttu-id="dcd65-121">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="dcd65-121">From time of the query</span></span>

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

### <span data-ttu-id="dcd65-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="dcd65-122">-GroupByOperationName</span></span>
<span data-ttu-id="dcd65-123">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="dcd65-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="dcd65-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="dcd65-124">-GroupByResourceName</span></span>
<span data-ttu-id="dcd65-125">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="dcd65-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="dcd65-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="dcd65-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="dcd65-127">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="dcd65-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="dcd65-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="dcd65-128">-IntervalLength</span></span>
<span data-ttu-id="dcd65-129">Intervall värde i minuter som används för att skapa LogAnalytics samtals taxa.</span><span class="sxs-lookup"><span data-stu-id="dcd65-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd65-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="dcd65-130">-Location</span></span>
<span data-ttu-id="dcd65-131">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="dcd65-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="dcd65-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dcd65-132">-NoWait</span></span>
<span data-ttu-id="dcd65-133">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="dcd65-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="dcd65-134">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="dcd65-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="dcd65-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="dcd65-135">-ToTime</span></span>
<span data-ttu-id="dcd65-136">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="dcd65-136">To time of the query</span></span>

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

### <span data-ttu-id="dcd65-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dcd65-137">-Confirm</span></span>
<span data-ttu-id="dcd65-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dcd65-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd65-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd65-139">-WhatIf</span></span>
<span data-ttu-id="dcd65-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dcd65-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd65-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dcd65-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd65-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd65-142">CommonParameters</span></span>
<span data-ttu-id="dcd65-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd65-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd65-144">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcd65-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd65-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcd65-145">INPUTS</span></span>

### <span data-ttu-id="dcd65-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dcd65-146">System.String</span></span>

## <span data-ttu-id="dcd65-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcd65-147">OUTPUTS</span></span>

### <span data-ttu-id="dcd65-148">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="dcd65-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="dcd65-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcd65-149">NOTES</span></span>

## <span data-ttu-id="dcd65-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcd65-150">RELATED LINKS</span></span>
