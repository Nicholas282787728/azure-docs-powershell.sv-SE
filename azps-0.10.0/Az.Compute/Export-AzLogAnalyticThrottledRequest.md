---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925261"
---
# <span data-ttu-id="925ba-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="925ba-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="925ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="925ba-102">SYNOPSIS</span></span>
<span data-ttu-id="925ba-103">Exportera loggar som visar totalt antal begränsade API-begäranden för detta abonnemang i det angivna tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="925ba-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="925ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="925ba-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="925ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="925ba-105">DESCRIPTION</span></span>
<span data-ttu-id="925ba-106">Detta exporterar totalt antal begränsade Microsoft. Compute API-samtal.</span><span class="sxs-lookup"><span data-stu-id="925ba-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="925ba-107">Loggarna kan aggregeras ytterligare med tre alternativ: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="925ba-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="925ba-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="925ba-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="925ba-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="925ba-109">EXAMPLES</span></span>

### <span data-ttu-id="925ba-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="925ba-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="925ba-111">Det här kommandot lagrar det totala antalet Microsoft. Compute API-samtal mellan 2018-02-20T17:54:14 och 2018-02-22T17:54:17 tum angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="925ba-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="925ba-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="925ba-112">PARAMETERS</span></span>

### <span data-ttu-id="925ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="925ba-113">-AsJob</span></span>
<span data-ttu-id="925ba-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="925ba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="925ba-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="925ba-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="925ba-116">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="925ba-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="925ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925ba-117">-DefaultProfile</span></span>
<span data-ttu-id="925ba-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="925ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="925ba-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="925ba-119">-FromTime</span></span>
<span data-ttu-id="925ba-120">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="925ba-120">From time of the query</span></span>

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

### <span data-ttu-id="925ba-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="925ba-121">-GroupByOperationName</span></span>
<span data-ttu-id="925ba-122">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="925ba-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="925ba-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="925ba-123">-GroupByResourceName</span></span>
<span data-ttu-id="925ba-124">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="925ba-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="925ba-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="925ba-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="925ba-126">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="925ba-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="925ba-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="925ba-127">-Location</span></span>
<span data-ttu-id="925ba-128">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="925ba-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="925ba-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="925ba-129">-ToTime</span></span>
<span data-ttu-id="925ba-130">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="925ba-130">To time of the query</span></span>

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

### <span data-ttu-id="925ba-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="925ba-131">-Confirm</span></span>
<span data-ttu-id="925ba-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="925ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="925ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="925ba-133">-WhatIf</span></span>
<span data-ttu-id="925ba-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="925ba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="925ba-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="925ba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="925ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925ba-136">CommonParameters</span></span>
<span data-ttu-id="925ba-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="925ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925ba-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="925ba-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925ba-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="925ba-139">INPUTS</span></span>

### <span data-ttu-id="925ba-140">System. String</span><span class="sxs-lookup"><span data-stu-id="925ba-140">System.String</span></span>

## <span data-ttu-id="925ba-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="925ba-141">OUTPUTS</span></span>

### <span data-ttu-id="925ba-142">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="925ba-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="925ba-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="925ba-143">NOTES</span></span>

## <span data-ttu-id="925ba-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="925ba-144">RELATED LINKS</span></span>

