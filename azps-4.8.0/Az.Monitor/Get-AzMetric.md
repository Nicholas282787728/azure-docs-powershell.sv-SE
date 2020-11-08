---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102229"
---
# <span data-ttu-id="ab462-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ab462-101">Get-AzMetric</span></span>

## <span data-ttu-id="ab462-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab462-102">SYNOPSIS</span></span>
<span data-ttu-id="ab462-103">Hämtar metriska värden för en resurs.</span><span class="sxs-lookup"><span data-stu-id="ab462-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="ab462-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab462-104">SYNTAX</span></span>

### <span data-ttu-id="ab462-105">GetWithDefaultParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="ab462-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab462-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="ab462-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab462-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab462-107">DESCRIPTION</span></span>
<span data-ttu-id="ab462-108">Cmdleten **Get-AzMetric** hämtar metriska värden för en viss resurs.</span><span class="sxs-lookup"><span data-stu-id="ab462-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="ab462-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab462-109">EXAMPLES</span></span>

### <span data-ttu-id="ab462-110">Exempel 1: få ett mått med summerad utmatning</span><span class="sxs-lookup"><span data-stu-id="ab462-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="ab462-111">Det här kommandot får metriska värden för website3 med klock slaget 1 minut.</span><span class="sxs-lookup"><span data-stu-id="ab462-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="ab462-112">Exempel 2: få ett mått med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="ab462-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="ab462-113">Det här kommandot får metriska värden för website3 med klock slaget 1 minut.</span><span class="sxs-lookup"><span data-stu-id="ab462-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="ab462-114">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="ab462-114">The output is detailed.</span></span>

### <span data-ttu-id="ab462-115">Exempel 3: få detaljerad information om ett visst mått</span><span class="sxs-lookup"><span data-stu-id="ab462-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="ab462-116">Det här kommandot får detaljerad information om begär Anden.</span><span class="sxs-lookup"><span data-stu-id="ab462-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="ab462-117">Exempel 4: få summerad utdata för ett angivet mått med angivet dimensions filter</span><span class="sxs-lookup"><span data-stu-id="ab462-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="ab462-118">Det här kommandot får sammanfattade utdata för PageViews mått med angivet dimensions filter och agg regerings typen.</span><span class="sxs-lookup"><span data-stu-id="ab462-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="ab462-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab462-119">PARAMETERS</span></span>

### <span data-ttu-id="ab462-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="ab462-120">-AggregationType</span></span>
<span data-ttu-id="ab462-121">Agg regerings typen för frågan</span><span class="sxs-lookup"><span data-stu-id="ab462-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab462-122">-DefaultProfile</span></span>
<span data-ttu-id="ab462-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab462-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab462-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="ab462-124">-DetailedOutput</span></span>
<span data-ttu-id="ab462-125">Anger att den här cmdleten visar detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="ab462-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="ab462-126">Utdata sammanfattas som standard.</span><span class="sxs-lookup"><span data-stu-id="ab462-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="ab462-127">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="ab462-127">-EndTime</span></span>
<span data-ttu-id="ab462-128">Anger slut tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="ab462-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="ab462-129">Standardinställningen är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="ab462-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="ab462-130">-MetricFilter</span></span>
<span data-ttu-id="ab462-131">Anger mått dimension filtret för att fråga efter mått för.</span><span class="sxs-lookup"><span data-stu-id="ab462-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ab462-132">-MetricName</span></span>
<span data-ttu-id="ab462-133">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="ab462-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ab462-134">-MetricNamespace</span></span>
<span data-ttu-id="ab462-135">Anger mått namn området för att fråga efter mått för.</span><span class="sxs-lookup"><span data-stu-id="ab462-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ab462-136">-OrderBy</span></span>
<span data-ttu-id="ab462-137">Anger den agg regering som ska användas för sortering av resultat och sorteringens riktning (exempel: Summa ASC).</span><span class="sxs-lookup"><span data-stu-id="ab462-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab462-138">-ResourceId</span></span>
<span data-ttu-id="ab462-139">Anger måttets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ab462-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="ab462-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="ab462-140">-ResultType</span></span>
<span data-ttu-id="ab462-141">Anger vilken resultat typ som ska returneras (metadata eller data).</span><span class="sxs-lookup"><span data-stu-id="ab462-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ab462-142">-StartTime</span></span>
<span data-ttu-id="ab462-143">Anger start tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="ab462-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="ab462-144">Standardvärdet är den aktuella lokala tiden minus en timme.</span><span class="sxs-lookup"><span data-stu-id="ab462-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ab462-145">-TimeGrain</span></span>
<span data-ttu-id="ab462-146">Anger tidskornigt för måttet som ett **TimeSpan** -objekt i formatet hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="ab462-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-147">-Överst</span><span class="sxs-lookup"><span data-stu-id="ab462-147">-Top</span></span>
<span data-ttu-id="ab462-148">Anger det maximala antalet poster som ska hämtas (standard: 10), som ska anges med $filter.</span><span class="sxs-lookup"><span data-stu-id="ab462-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab462-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab462-149">CommonParameters</span></span>
<span data-ttu-id="ab462-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab462-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab462-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab462-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab462-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab462-152">INPUTS</span></span>

### <span data-ttu-id="ab462-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ab462-153">System.String</span></span>

### <span data-ttu-id="ab462-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ab462-154">System.TimeSpan</span></span>

### <span data-ttu-id="ab462-155">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Models. AggregationType, Microsoft. Azure. Management. Monitor, version = 0.21.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ab462-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ab462-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ab462-156">System.DateTime</span></span>

### <span data-ttu-id="ab462-157">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab462-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ab462-158">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. modelers. ResultType, Microsoft. Azure. Management. Monitor, version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ab462-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ab462-159">System. string []</span><span class="sxs-lookup"><span data-stu-id="ab462-159">System.String[]</span></span>

### <span data-ttu-id="ab462-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab462-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab462-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab462-161">OUTPUTS</span></span>

### <span data-ttu-id="ab462-162">Microsoft. Azure. commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="ab462-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="ab462-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab462-163">NOTES</span></span>

<span data-ttu-id="ab462-164">Mer information om de mät värden som stöds finns i: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="ab462-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="ab462-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab462-165">RELATED LINKS</span></span>

<span data-ttu-id="ab462-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="ab462-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


