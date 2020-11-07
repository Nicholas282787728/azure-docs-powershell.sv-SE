---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755494"
---
# <span data-ttu-id="2552c-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="2552c-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="2552c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2552c-102">SYNOPSIS</span></span>
<span data-ttu-id="2552c-103">Hämtar metriska värden för en resurs.</span><span class="sxs-lookup"><span data-stu-id="2552c-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2552c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2552c-104">SYNTAX</span></span>

### <span data-ttu-id="2552c-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="2552c-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2552c-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="2552c-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2552c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2552c-107">DESCRIPTION</span></span>
<span data-ttu-id="2552c-108">Cmdleten **Get-AzureRmMetric** hämtar metriska värden för en viss resurs.</span><span class="sxs-lookup"><span data-stu-id="2552c-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="2552c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2552c-109">EXAMPLES</span></span>

### <span data-ttu-id="2552c-110">Exempel 1: få ett mått med summerad utmatning</span><span class="sxs-lookup"><span data-stu-id="2552c-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="2552c-111">Det här kommandot får metriska värden för website3 med klock slaget 1 minut.</span><span class="sxs-lookup"><span data-stu-id="2552c-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="2552c-112">Exempel 2: få ett mått med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="2552c-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="2552c-113">Det här kommandot får metriska värden för website3 med klock slaget 1 minut.</span><span class="sxs-lookup"><span data-stu-id="2552c-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="2552c-114">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="2552c-114">The output is detailed.</span></span>

### <span data-ttu-id="2552c-115">Exempel 3: få detaljerad information om ett visst mått</span><span class="sxs-lookup"><span data-stu-id="2552c-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="2552c-116">Det här kommandot får detaljerad information om begär Anden.</span><span class="sxs-lookup"><span data-stu-id="2552c-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="2552c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2552c-117">PARAMETERS</span></span>

### <span data-ttu-id="2552c-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="2552c-118">-AggregationType</span></span>
<span data-ttu-id="2552c-119">Agg regerings typen för frågan</span><span class="sxs-lookup"><span data-stu-id="2552c-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2552c-120">-DefaultProfile</span></span>
<span data-ttu-id="2552c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2552c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2552c-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="2552c-122">-DetailedOutput</span></span>
<span data-ttu-id="2552c-123">Anger att den här cmdleten visar detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="2552c-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="2552c-124">Utdata sammanfattas som standard.</span><span class="sxs-lookup"><span data-stu-id="2552c-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-125">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="2552c-125">-EndTime</span></span>
<span data-ttu-id="2552c-126">Anger slut tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="2552c-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="2552c-127">Standardinställningen är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="2552c-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2552c-128">-MetricName</span></span>
<span data-ttu-id="2552c-129">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="2552c-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2552c-130">-ResourceId</span></span>
<span data-ttu-id="2552c-131">Anger måttets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2552c-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2552c-132">-StartTime</span></span>
<span data-ttu-id="2552c-133">Anger start tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="2552c-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="2552c-134">Standardvärdet är den aktuella lokala tiden minus en timme.</span><span class="sxs-lookup"><span data-stu-id="2552c-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-135">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="2552c-135">-TimeGrain</span></span>
<span data-ttu-id="2552c-136">Anger tidskornigt för måttet som ett **TimeSpan** -objekt i formatet hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="2552c-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2552c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2552c-137">CommonParameters</span></span>
<span data-ttu-id="2552c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2552c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2552c-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2552c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2552c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2552c-140">INPUTS</span></span>

### <span data-ttu-id="2552c-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="2552c-141">None</span></span>
<span data-ttu-id="2552c-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2552c-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2552c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2552c-143">OUTPUTS</span></span>

### <span data-ttu-id="2552c-144">Microsoft. Azure. commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="2552c-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="2552c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2552c-145">NOTES</span></span>

## <span data-ttu-id="2552c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2552c-146">RELATED LINKS</span></span>

[<span data-ttu-id="2552c-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="2552c-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


