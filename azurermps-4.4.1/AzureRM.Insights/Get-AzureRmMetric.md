---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582436"
---
# <span data-ttu-id="74fdc-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="74fdc-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="74fdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="74fdc-103">Hämtar metriska värden för en resurs.</span><span class="sxs-lookup"><span data-stu-id="74fdc-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74fdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74fdc-104">SYNTAX</span></span>

### <span data-ttu-id="74fdc-105">Parametrar för Get-AzureRmMetric cmdlet i standard läget</span><span class="sxs-lookup"><span data-stu-id="74fdc-105">Parameters for Get-AzureRmMetric cmdlet in the default mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74fdc-106">Parametrar för Get-AzureRmMetric cmdlet i det fullständiga parameter uppsättnings läget</span><span class="sxs-lookup"><span data-stu-id="74fdc-106">Parameters for Get-AzureRmMetric cmdlet in the full param set mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74fdc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74fdc-107">DESCRIPTION</span></span>
<span data-ttu-id="74fdc-108">Cmdleten **Get-AzureRmMetric** hämtar metriska värden för en viss resurs.</span><span class="sxs-lookup"><span data-stu-id="74fdc-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="74fdc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74fdc-109">EXAMPLES</span></span>

### <span data-ttu-id="74fdc-110">Exempel 1: få ett mått med summerad utmatning</span><span class="sxs-lookup"><span data-stu-id="74fdc-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="74fdc-111">Det här kommandot får metriska värden för website3 med klock slaget 1 minut.</span><span class="sxs-lookup"><span data-stu-id="74fdc-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="74fdc-112">Exempel 2: få ett mått med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="74fdc-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="74fdc-113">Det här kommandot får metriska värden för website3 med klock slaget 1 minut.</span><span class="sxs-lookup"><span data-stu-id="74fdc-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="74fdc-114">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="74fdc-114">The output is detailed.</span></span>

### <span data-ttu-id="74fdc-115">Exempel 3: få detaljerad information om ett visst mått</span><span class="sxs-lookup"><span data-stu-id="74fdc-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="74fdc-116">Det här kommandot får detaljerad information om begär Anden.</span><span class="sxs-lookup"><span data-stu-id="74fdc-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="74fdc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74fdc-117">PARAMETERS</span></span>

### <span data-ttu-id="74fdc-118">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="74fdc-118">-DetailedOutput</span></span>
<span data-ttu-id="74fdc-119">Anger att den här cmdleten visar detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="74fdc-119">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="74fdc-120">Utdata sammanfattas som standard.</span><span class="sxs-lookup"><span data-stu-id="74fdc-120">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fdc-121">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="74fdc-121">-EndTime</span></span>
<span data-ttu-id="74fdc-122">Anger slut tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="74fdc-122">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="74fdc-123">Standardinställningen är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="74fdc-123">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fdc-124">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="74fdc-124">-MetricNames</span></span>
<span data-ttu-id="74fdc-125">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="74fdc-125">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fdc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74fdc-126">-ResourceId</span></span>
<span data-ttu-id="74fdc-127">Anger måttets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="74fdc-127">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="74fdc-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="74fdc-128">-StartTime</span></span>
<span data-ttu-id="74fdc-129">Anger start tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="74fdc-129">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="74fdc-130">Standardvärdet är den aktuella lokala tiden minus en timme.</span><span class="sxs-lookup"><span data-stu-id="74fdc-130">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fdc-131">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="74fdc-131">-TimeGrain</span></span>
<span data-ttu-id="74fdc-132">Anger tidskornigt för måttet som ett **TimeSpan** -objekt i formatet hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="74fdc-132">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fdc-133">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="74fdc-133">-AggregationType</span></span>
<span data-ttu-id="74fdc-134">Agg regerings typen för Quer</span><span class="sxs-lookup"><span data-stu-id="74fdc-134">The aggregation type of the quer</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fdc-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fdc-135">-DefaultProfile</span></span>
<span data-ttu-id="74fdc-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74fdc-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74fdc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fdc-137">CommonParameters</span></span>
<span data-ttu-id="74fdc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fdc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fdc-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fdc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fdc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74fdc-140">INPUTS</span></span>

## <span data-ttu-id="74fdc-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74fdc-141">OUTPUTS</span></span>

### <span data-ttu-id="74fdc-142">Microsoft. Azure. commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="74fdc-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="74fdc-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74fdc-143">NOTES</span></span>

## <span data-ttu-id="74fdc-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74fdc-144">RELATED LINKS</span></span>

[<span data-ttu-id="74fdc-145">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="74fdc-145">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


