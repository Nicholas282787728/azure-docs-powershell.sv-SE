---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: ac588fe9a82209cfd56c08f750fcd35945bc8af1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922562"
---
# <span data-ttu-id="64824-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="64824-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="64824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64824-102">SYNOPSIS</span></span>
<span data-ttu-id="64824-103">Skapar en Autoskala-regel.</span><span class="sxs-lookup"><span data-stu-id="64824-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="64824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64824-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64824-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64824-105">DESCRIPTION</span></span>
<span data-ttu-id="64824-106">Cmdleten **New-AzAutoscaleRule** skapar en AutoScale-regel.</span><span class="sxs-lookup"><span data-stu-id="64824-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="64824-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64824-107">EXAMPLES</span></span>

### <span data-ttu-id="64824-108">Exempel 1: skapa en regel</span><span class="sxs-lookup"><span data-stu-id="64824-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="64824-109">Det här kommandot skapar en regel.</span><span class="sxs-lookup"><span data-stu-id="64824-109">This command creates a rule.</span></span>

### <span data-ttu-id="64824-110">Exempel 2: skapa två regler</span><span class="sxs-lookup"><span data-stu-id="64824-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="64824-111">Det första kommandot skapar en regel för begär måttet och lagrar det sedan i $Rule 1-variabeln.</span><span class="sxs-lookup"><span data-stu-id="64824-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="64824-112">Det andra kommandot skapar en andra regel för det begärda måttet och lagrar det sedan i $Rule 2-variabeln.</span><span class="sxs-lookup"><span data-stu-id="64824-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="64824-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64824-113">PARAMETERS</span></span>

### <span data-ttu-id="64824-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64824-114">-DefaultProfile</span></span>
<span data-ttu-id="64824-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="64824-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64824-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="64824-116">-MetricName</span></span>
<span data-ttu-id="64824-117">Anger namnet på måttet.</span><span class="sxs-lookup"><span data-stu-id="64824-117">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="64824-118">-MetricResourceId</span></span>
<span data-ttu-id="64824-119">Anger mått resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="64824-119">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="64824-120">-MetricStatistic</span></span>
<span data-ttu-id="64824-121">Anger Mät statistik.</span><span class="sxs-lookup"><span data-stu-id="64824-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="64824-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64824-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64824-123">Medel</span><span class="sxs-lookup"><span data-stu-id="64824-123">Average</span></span>
- <span data-ttu-id="64824-124">Minst</span><span class="sxs-lookup"><span data-stu-id="64824-124">Min</span></span>
- <span data-ttu-id="64824-125">Värdet</span><span class="sxs-lookup"><span data-stu-id="64824-125">Max</span></span>
- <span data-ttu-id="64824-126">Totala</span><span class="sxs-lookup"><span data-stu-id="64824-126">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-127">-Operatör</span><span class="sxs-lookup"><span data-stu-id="64824-127">-Operator</span></span>
<span data-ttu-id="64824-128">Anger operatorn.</span><span class="sxs-lookup"><span data-stu-id="64824-128">Specifies the operator.</span></span>
<span data-ttu-id="64824-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64824-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64824-130">Är lika med</span><span class="sxs-lookup"><span data-stu-id="64824-130">Equals</span></span>
- <span data-ttu-id="64824-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="64824-131">NotEquals</span></span>
- <span data-ttu-id="64824-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="64824-132">GreaterThan</span></span>
- <span data-ttu-id="64824-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="64824-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="64824-134">Mindreän</span><span class="sxs-lookup"><span data-stu-id="64824-134">LessThan</span></span>
- <span data-ttu-id="64824-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="64824-135">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="64824-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="64824-137">Anger den automatiska skalnings åtgärden cooldown.</span><span class="sxs-lookup"><span data-stu-id="64824-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="64824-138">-ScaleActionDirection</span></span>
<span data-ttu-id="64824-139">Anger riktningen för skalnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="64824-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="64824-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64824-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64824-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="64824-141">None</span></span>
- <span data-ttu-id="64824-142">Fler</span><span class="sxs-lookup"><span data-stu-id="64824-142">Increase</span></span>
- <span data-ttu-id="64824-143">Minska</span><span class="sxs-lookup"><span data-stu-id="64824-143">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="64824-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="64824-145">Anger skalnings typen.</span><span class="sxs-lookup"><span data-stu-id="64824-145">Specifies the scale type.</span></span>
<span data-ttu-id="64824-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64824-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64824-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="64824-147">ChangeSize</span></span>
- <span data-ttu-id="64824-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="64824-148">ChangeCount</span></span>
- <span data-ttu-id="64824-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="64824-149">PercentChangeCount</span></span>
- <span data-ttu-id="64824-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="64824-150">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="64824-151">-ScaleActionValue</span></span>
<span data-ttu-id="64824-152">Anger åtgärd svärdet.</span><span class="sxs-lookup"><span data-stu-id="64824-152">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-153">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="64824-153">-Threshold</span></span>
<span data-ttu-id="64824-154">Anger tröskelvärdet för Metric-värdet.</span><span class="sxs-lookup"><span data-stu-id="64824-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="64824-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="64824-156">Anger tids mängds operator.</span><span class="sxs-lookup"><span data-stu-id="64824-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="64824-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64824-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64824-158">Medel</span><span class="sxs-lookup"><span data-stu-id="64824-158">Average</span></span>
- <span data-ttu-id="64824-159">Få</span><span class="sxs-lookup"><span data-stu-id="64824-159">Minimum</span></span>
- <span data-ttu-id="64824-160">Maximal</span><span class="sxs-lookup"><span data-stu-id="64824-160">Maximum</span></span>
- <span data-ttu-id="64824-161">Senast</span><span class="sxs-lookup"><span data-stu-id="64824-161">Last</span></span>
- <span data-ttu-id="64824-162">Totalt antal</span><span class="sxs-lookup"><span data-stu-id="64824-162">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="64824-163">-TimeGrain</span></span>
<span data-ttu-id="64824-164">Anger tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="64824-164">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64824-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="64824-165">-TimeWindow</span></span>
<span data-ttu-id="64824-166">Anger tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="64824-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="64824-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64824-167">CommonParameters</span></span>
<span data-ttu-id="64824-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64824-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64824-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64824-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64824-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64824-170">INPUTS</span></span>

### <span data-ttu-id="64824-171">System. String</span><span class="sxs-lookup"><span data-stu-id="64824-171">System.String</span></span>

### <span data-ttu-id="64824-172">Microsoft. Azure. Management. Monitoring. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="64824-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="64824-173">Microsoft. Azure. Management. Monitoring. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="64824-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="64824-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="64824-174">System.Double</span></span>

### <span data-ttu-id="64824-175">Microsoft. Azure. Management. Monitoring. Management. Models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="64824-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="64824-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="64824-176">System.TimeSpan</span></span>

### <span data-ttu-id="64824-177">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="64824-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="64824-178">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="64824-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="64824-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64824-179">OUTPUTS</span></span>

### <span data-ttu-id="64824-180">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="64824-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="64824-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64824-181">NOTES</span></span>

## <span data-ttu-id="64824-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64824-182">RELATED LINKS</span></span>

[<span data-ttu-id="64824-183">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="64824-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="64824-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="64824-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="64824-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="64824-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="64824-186">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="64824-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="64824-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="64824-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


