---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
ms.openlocfilehash: e98819ab7de961dacefea673ac43690ad260ac3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929506"
---
# <span data-ttu-id="e7811-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="e7811-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="e7811-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7811-102">SYNOPSIS</span></span>
<span data-ttu-id="e7811-103">Exportera loggar som visar totalt antal begränsade API-begäranden för detta abonnemang i det angivna tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="e7811-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7811-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7811-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7811-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7811-105">DESCRIPTION</span></span>
<span data-ttu-id="e7811-106">Detta exporterar totalt antal begränsade Microsoft. Compute API-samtal.</span><span class="sxs-lookup"><span data-stu-id="e7811-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="e7811-107">Loggarna kan aggregeras ytterligare med tre alternativ: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="e7811-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="e7811-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="e7811-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="e7811-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7811-109">EXAMPLES</span></span>

### <span data-ttu-id="e7811-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7811-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="e7811-111">Det här kommandot lagrar det totala antalet Microsoft. Compute API-samtal mellan 2018-02-20T17:54:14 och 2018-02-22T17:54:17 tum angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="e7811-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="e7811-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7811-112">PARAMETERS</span></span>

### <span data-ttu-id="e7811-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7811-113">-AsJob</span></span>
<span data-ttu-id="e7811-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e7811-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7811-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="e7811-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="e7811-116">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="e7811-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="e7811-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7811-117">-DefaultProfile</span></span>
<span data-ttu-id="e7811-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7811-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7811-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="e7811-119">-FromTime</span></span>
<span data-ttu-id="e7811-120">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="e7811-120">From time of the query</span></span>

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

### <span data-ttu-id="e7811-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="e7811-121">-GroupByOperationName</span></span>
<span data-ttu-id="e7811-122">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="e7811-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="e7811-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="e7811-123">-GroupByResourceName</span></span>
<span data-ttu-id="e7811-124">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e7811-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="e7811-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="e7811-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="e7811-126">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="e7811-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="e7811-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="e7811-127">-Location</span></span>
<span data-ttu-id="e7811-128">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="e7811-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="e7811-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="e7811-129">-ToTime</span></span>
<span data-ttu-id="e7811-130">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="e7811-130">To time of the query</span></span>

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

### <span data-ttu-id="e7811-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7811-131">-Confirm</span></span>
<span data-ttu-id="e7811-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7811-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7811-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7811-133">-WhatIf</span></span>
<span data-ttu-id="e7811-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7811-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7811-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7811-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7811-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7811-136">CommonParameters</span></span>
<span data-ttu-id="e7811-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7811-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7811-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7811-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7811-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7811-139">INPUTS</span></span>

### <span data-ttu-id="e7811-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e7811-140">System.String</span></span>

## <span data-ttu-id="e7811-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7811-141">OUTPUTS</span></span>

### <span data-ttu-id="e7811-142">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="e7811-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="e7811-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7811-143">NOTES</span></span>

## <span data-ttu-id="e7811-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7811-144">RELATED LINKS</span></span>

