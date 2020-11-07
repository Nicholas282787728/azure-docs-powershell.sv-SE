---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: bbf275b08421265130da898b670b46c95b15c34c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925258"
---
# <span data-ttu-id="e4d16-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="e4d16-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="e4d16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4d16-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d16-103">Exportera loggar som visar API-begäranden som gjorts av detta abonnemang i tidsfönstret för att Visa begränsnings aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e4d16-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="e4d16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4d16-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4d16-105">DESCRIPTION</span></span>
<span data-ttu-id="e4d16-106">Detta exporterar sammansatta nummer i Microsoft. Compute API-samtal avgränsade med lyckat, misslyckat eller begränsat visas i tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="e4d16-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="e4d16-107">Loggarna kan grupperas ytterligare med tre parametrar: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="e4d16-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="e4d16-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="e4d16-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="e4d16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4d16-109">EXAMPLES</span></span>

### <span data-ttu-id="e4d16-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e4d16-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="e4d16-111">Det här kommandot lagrar de aggregerade numren för Microsoft. Compute API-samtal avgränsade med lyckat, misslyckat eller begränsat mellan 2018 – 02-20T17:54:14 och 2018-02-22T17:54:17 i angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="e4d16-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="e4d16-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4d16-112">PARAMETERS</span></span>

### <span data-ttu-id="e4d16-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4d16-113">-AsJob</span></span>
<span data-ttu-id="e4d16-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e4d16-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="e4d16-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="e4d16-116">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="e4d16-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d16-117">-DefaultProfile</span></span>
<span data-ttu-id="e4d16-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d16-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="e4d16-119">-FromTime</span></span>
<span data-ttu-id="e4d16-120">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="e4d16-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="e4d16-121">-GroupByOperationName</span></span>
<span data-ttu-id="e4d16-122">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="e4d16-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="e4d16-123">-GroupByResourceName</span></span>
<span data-ttu-id="e4d16-124">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e4d16-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="e4d16-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="e4d16-126">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="e4d16-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="e4d16-127">-IntervalLength</span></span>
<span data-ttu-id="e4d16-128">Intervall värde i minuter som används för att skapa LogAnalytics samtals taxa.</span><span class="sxs-lookup"><span data-stu-id="e4d16-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="e4d16-129">-Location</span></span>
<span data-ttu-id="e4d16-130">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="e4d16-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="e4d16-131">-ToTime</span></span>
<span data-ttu-id="e4d16-132">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="e4d16-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d16-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4d16-133">-Confirm</span></span>
<span data-ttu-id="e4d16-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4d16-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d16-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d16-135">-WhatIf</span></span>
<span data-ttu-id="e4d16-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4d16-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d16-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4d16-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d16-138">CommonParameters</span></span>
<span data-ttu-id="e4d16-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d16-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d16-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d16-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4d16-141">INPUTS</span></span>

### <span data-ttu-id="e4d16-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e4d16-142">System.String</span></span>

## <span data-ttu-id="e4d16-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4d16-143">OUTPUTS</span></span>

### <span data-ttu-id="e4d16-144">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="e4d16-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="e4d16-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4d16-145">NOTES</span></span>

## <span data-ttu-id="e4d16-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4d16-146">RELATED LINKS</span></span>

