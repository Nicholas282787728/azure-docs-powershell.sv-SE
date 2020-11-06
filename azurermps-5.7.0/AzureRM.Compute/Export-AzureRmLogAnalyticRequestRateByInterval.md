---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: b5e087bf42a2cb7f19980621c6dd0606471374d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577257"
---
# <span data-ttu-id="0ddce-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="0ddce-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="0ddce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ddce-102">SYNOPSIS</span></span>
<span data-ttu-id="0ddce-103">Exportera loggar som visar API-begäranden som gjorts av detta abonnemang i tidsfönstret för att Visa begränsnings aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="0ddce-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ddce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ddce-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ddce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ddce-105">DESCRIPTION</span></span>
<span data-ttu-id="0ddce-106">Detta exporterar sammansatta nummer i Microsoft. Compute API-samtal avgränsade med lyckat, misslyckat eller begränsat visas i tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="0ddce-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="0ddce-107">Loggarna kan grupperas ytterligare med tre parametrar: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="0ddce-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="0ddce-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="0ddce-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="0ddce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ddce-109">EXAMPLES</span></span>

### <span data-ttu-id="0ddce-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ddce-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="0ddce-111">Det här kommandot lagrar de aggregerade numren för Microsoft. Compute API-samtal avgränsade med lyckat, misslyckat eller begränsat mellan 2018 – 02-20T17:54:14 och 2018-02-22T17:54:17 i angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="0ddce-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="0ddce-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ddce-112">PARAMETERS</span></span>

### <span data-ttu-id="0ddce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ddce-113">-AsJob</span></span>
<span data-ttu-id="0ddce-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0ddce-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ddce-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="0ddce-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="0ddce-116">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="0ddce-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="0ddce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ddce-117">-DefaultProfile</span></span>
<span data-ttu-id="0ddce-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ddce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ddce-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="0ddce-119">-FromTime</span></span>
<span data-ttu-id="0ddce-120">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="0ddce-120">From time of the query</span></span>

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

### <span data-ttu-id="0ddce-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="0ddce-121">-GroupByOperationName</span></span>
<span data-ttu-id="0ddce-122">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="0ddce-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="0ddce-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="0ddce-123">-GroupByResourceName</span></span>
<span data-ttu-id="0ddce-124">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0ddce-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="0ddce-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="0ddce-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="0ddce-126">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="0ddce-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="0ddce-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="0ddce-127">-IntervalLength</span></span>
<span data-ttu-id="0ddce-128">Intervall värde i minuter som används för att skapa LogAnalytics samtals taxa.</span><span class="sxs-lookup"><span data-stu-id="0ddce-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="0ddce-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="0ddce-129">-Location</span></span>
<span data-ttu-id="0ddce-130">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="0ddce-130">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="0ddce-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="0ddce-131">-ToTime</span></span>
<span data-ttu-id="0ddce-132">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="0ddce-132">To time of the query</span></span>

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

### <span data-ttu-id="0ddce-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ddce-133">-Confirm</span></span>
<span data-ttu-id="0ddce-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ddce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ddce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ddce-135">-WhatIf</span></span>
<span data-ttu-id="0ddce-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ddce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ddce-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ddce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ddce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ddce-138">CommonParameters</span></span>
<span data-ttu-id="0ddce-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ddce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ddce-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ddce-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ddce-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ddce-141">INPUTS</span></span>

### <span data-ttu-id="0ddce-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0ddce-142">System.String</span></span>

## <span data-ttu-id="0ddce-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ddce-143">OUTPUTS</span></span>

### <span data-ttu-id="0ddce-144">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="0ddce-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="0ddce-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ddce-145">NOTES</span></span>

## <span data-ttu-id="0ddce-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ddce-146">RELATED LINKS</span></span>
