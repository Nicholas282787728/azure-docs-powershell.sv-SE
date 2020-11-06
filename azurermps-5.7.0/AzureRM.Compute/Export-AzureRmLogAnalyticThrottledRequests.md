---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: a8deadf4760950eebbec22626bca475439ab0b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577256"
---
# <span data-ttu-id="f5b48-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="f5b48-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="f5b48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5b48-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b48-103">Exportera loggar som visar totalt antal begränsade API-begäranden för detta abonnemang i det angivna tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="f5b48-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5b48-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5b48-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5b48-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b48-106">Detta exporterar totalt antal begränsade Microsoft. Compute API-samtal.</span><span class="sxs-lookup"><span data-stu-id="f5b48-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="f5b48-107">Loggarna kan aggregeras ytterligare med tre alternativ: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="f5b48-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="f5b48-108">Observera att den här cmdleten endast samlar in CRP-loggar.</span><span class="sxs-lookup"><span data-stu-id="f5b48-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="f5b48-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5b48-109">EXAMPLES</span></span>

### <span data-ttu-id="f5b48-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5b48-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="f5b48-111">Det här kommandot lagrar det totala antalet Microsoft. Compute API-samtal mellan 2018-02-20T17:54:14 och 2018-02-22T17:54:17 tum angiven SAS URI, aggregerad efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="f5b48-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="f5b48-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5b48-112">PARAMETERS</span></span>

### <span data-ttu-id="f5b48-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5b48-113">-AsJob</span></span>
<span data-ttu-id="f5b48-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f5b48-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5b48-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="f5b48-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="f5b48-116">SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.</span><span class="sxs-lookup"><span data-stu-id="f5b48-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="f5b48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b48-117">-DefaultProfile</span></span>
<span data-ttu-id="f5b48-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5b48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5b48-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="f5b48-119">-FromTime</span></span>
<span data-ttu-id="f5b48-120">Från tiden i frågan</span><span class="sxs-lookup"><span data-stu-id="f5b48-120">From time of the query</span></span>

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

### <span data-ttu-id="f5b48-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="f5b48-121">-GroupByOperationName</span></span>
<span data-ttu-id="f5b48-122">Gruppens frågeresultat efter åtgärds namn.</span><span class="sxs-lookup"><span data-stu-id="f5b48-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="f5b48-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="f5b48-123">-GroupByResourceName</span></span>
<span data-ttu-id="f5b48-124">Grupp frågans resultat efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f5b48-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="f5b48-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="f5b48-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="f5b48-126">Grupp frågans resultat efter begränsnings princip tillämpas.</span><span class="sxs-lookup"><span data-stu-id="f5b48-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="f5b48-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="f5b48-127">-Location</span></span>
<span data-ttu-id="f5b48-128">Den plats där loggen för loggning görs.</span><span class="sxs-lookup"><span data-stu-id="f5b48-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="f5b48-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="f5b48-129">-ToTime</span></span>
<span data-ttu-id="f5b48-130">Till tid i frågan</span><span class="sxs-lookup"><span data-stu-id="f5b48-130">To time of the query</span></span>

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

### <span data-ttu-id="f5b48-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5b48-131">-Confirm</span></span>
<span data-ttu-id="f5b48-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5b48-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5b48-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5b48-133">-WhatIf</span></span>
<span data-ttu-id="f5b48-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5b48-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5b48-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5b48-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5b48-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b48-136">CommonParameters</span></span>
<span data-ttu-id="f5b48-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b48-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b48-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b48-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b48-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5b48-139">INPUTS</span></span>

### <span data-ttu-id="f5b48-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f5b48-140">System.String</span></span>

## <span data-ttu-id="f5b48-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5b48-141">OUTPUTS</span></span>

### <span data-ttu-id="f5b48-142">Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="f5b48-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="f5b48-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5b48-143">NOTES</span></span>

## <span data-ttu-id="f5b48-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5b48-144">RELATED LINKS</span></span>
