---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262991"
---
# <span data-ttu-id="37087-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="37087-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="37087-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37087-102">SYNOPSIS</span></span>
<span data-ttu-id="37087-103">Skapar en Autoskala-regel.</span><span class="sxs-lookup"><span data-stu-id="37087-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="37087-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37087-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37087-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37087-105">DESCRIPTION</span></span>
<span data-ttu-id="37087-106">Cmdleten **New-AzAutoscaleRule** skapar en AutoScale-regel.</span><span class="sxs-lookup"><span data-stu-id="37087-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="37087-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37087-107">EXAMPLES</span></span>

### <span data-ttu-id="37087-108">Exempel 1: skapa en regel</span><span class="sxs-lookup"><span data-stu-id="37087-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="37087-109">Det här kommandot skapar en regel.</span><span class="sxs-lookup"><span data-stu-id="37087-109">This command creates a rule.</span></span>

### <span data-ttu-id="37087-110">Exempel 2: skapa två regler</span><span class="sxs-lookup"><span data-stu-id="37087-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="37087-111">Det första kommandot skapar en regel för begär måttet och lagrar det sedan i $Rule 1-variabeln.</span><span class="sxs-lookup"><span data-stu-id="37087-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="37087-112">Det andra kommandot skapar en andra regel för det begärda måttet och lagrar det sedan i $Rule 2-variabeln.</span><span class="sxs-lookup"><span data-stu-id="37087-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="37087-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="37087-113">Example 3</span></span>

<span data-ttu-id="37087-114">Skapar en Autoskala-regel.</span><span class="sxs-lookup"><span data-stu-id="37087-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="37087-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="37087-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="37087-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37087-116">PARAMETERS</span></span>

### <span data-ttu-id="37087-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37087-117">-DefaultProfile</span></span>
<span data-ttu-id="37087-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="37087-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37087-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="37087-119">-MetricName</span></span>
<span data-ttu-id="37087-120">Anger namnet på måttet.</span><span class="sxs-lookup"><span data-stu-id="37087-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="37087-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="37087-121">-MetricResourceId</span></span>
<span data-ttu-id="37087-122">Anger mått resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="37087-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="37087-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="37087-123">-MetricStatistic</span></span>
<span data-ttu-id="37087-124">Anger Mät statistik.</span><span class="sxs-lookup"><span data-stu-id="37087-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="37087-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="37087-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37087-126">Medel</span><span class="sxs-lookup"><span data-stu-id="37087-126">Average</span></span>
- <span data-ttu-id="37087-127">Minst</span><span class="sxs-lookup"><span data-stu-id="37087-127">Min</span></span>
- <span data-ttu-id="37087-128">Värdet</span><span class="sxs-lookup"><span data-stu-id="37087-128">Max</span></span>
- <span data-ttu-id="37087-129">Totala</span><span class="sxs-lookup"><span data-stu-id="37087-129">Sum</span></span>

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

### <span data-ttu-id="37087-130">-Operatör</span><span class="sxs-lookup"><span data-stu-id="37087-130">-Operator</span></span>
<span data-ttu-id="37087-131">Anger operatorn.</span><span class="sxs-lookup"><span data-stu-id="37087-131">Specifies the operator.</span></span>
<span data-ttu-id="37087-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="37087-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37087-133">Är lika med</span><span class="sxs-lookup"><span data-stu-id="37087-133">Equals</span></span>
- <span data-ttu-id="37087-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="37087-134">NotEquals</span></span>
- <span data-ttu-id="37087-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="37087-135">GreaterThan</span></span>
- <span data-ttu-id="37087-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="37087-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="37087-137">Mindreän</span><span class="sxs-lookup"><span data-stu-id="37087-137">LessThan</span></span>
- <span data-ttu-id="37087-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="37087-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="37087-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="37087-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="37087-140">Anger den automatiska skalnings åtgärden cooldown.</span><span class="sxs-lookup"><span data-stu-id="37087-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="37087-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="37087-141">-ScaleActionDirection</span></span>
<span data-ttu-id="37087-142">Anger riktningen för skalnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="37087-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="37087-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="37087-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37087-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="37087-144">None</span></span>
- <span data-ttu-id="37087-145">Fler</span><span class="sxs-lookup"><span data-stu-id="37087-145">Increase</span></span>
- <span data-ttu-id="37087-146">Minska</span><span class="sxs-lookup"><span data-stu-id="37087-146">Decrease</span></span>

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

### <span data-ttu-id="37087-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="37087-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="37087-148">Anger skalnings typen.</span><span class="sxs-lookup"><span data-stu-id="37087-148">Specifies the scale type.</span></span>
<span data-ttu-id="37087-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="37087-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37087-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="37087-150">ChangeSize</span></span>
- <span data-ttu-id="37087-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="37087-151">ChangeCount</span></span>
- <span data-ttu-id="37087-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="37087-152">PercentChangeCount</span></span>
- <span data-ttu-id="37087-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="37087-153">ExactCount</span></span>

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

### <span data-ttu-id="37087-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="37087-154">-ScaleActionValue</span></span>
<span data-ttu-id="37087-155">Anger åtgärd svärdet.</span><span class="sxs-lookup"><span data-stu-id="37087-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="37087-156">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="37087-156">-Threshold</span></span>
<span data-ttu-id="37087-157">Anger tröskelvärdet för Metric-värdet.</span><span class="sxs-lookup"><span data-stu-id="37087-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="37087-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="37087-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="37087-159">Anger tids mängds operator.</span><span class="sxs-lookup"><span data-stu-id="37087-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="37087-160">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="37087-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37087-161">Medel</span><span class="sxs-lookup"><span data-stu-id="37087-161">Average</span></span>
- <span data-ttu-id="37087-162">Få</span><span class="sxs-lookup"><span data-stu-id="37087-162">Minimum</span></span>
- <span data-ttu-id="37087-163">Maximal</span><span class="sxs-lookup"><span data-stu-id="37087-163">Maximum</span></span>
- <span data-ttu-id="37087-164">Senast</span><span class="sxs-lookup"><span data-stu-id="37087-164">Last</span></span>
- <span data-ttu-id="37087-165">Totalt antal</span><span class="sxs-lookup"><span data-stu-id="37087-165">Total, Count</span></span>

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

### <span data-ttu-id="37087-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="37087-166">-TimeGrain</span></span>
<span data-ttu-id="37087-167">Anger tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="37087-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="37087-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="37087-168">-TimeWindow</span></span>
<span data-ttu-id="37087-169">Anger tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="37087-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="37087-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37087-170">CommonParameters</span></span>
<span data-ttu-id="37087-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37087-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37087-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37087-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37087-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37087-173">INPUTS</span></span>

### <span data-ttu-id="37087-174">System. String</span><span class="sxs-lookup"><span data-stu-id="37087-174">System.String</span></span>

### <span data-ttu-id="37087-175">Microsoft. Azure. Management. Monitoring. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="37087-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="37087-176">Microsoft. Azure. Management. Monitoring. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="37087-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="37087-177">System. Double</span><span class="sxs-lookup"><span data-stu-id="37087-177">System.Double</span></span>

### <span data-ttu-id="37087-178">Microsoft. Azure. Management. Monitoring. Management. Models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="37087-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="37087-179">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="37087-179">System.TimeSpan</span></span>

### <span data-ttu-id="37087-180">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="37087-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="37087-181">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="37087-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="37087-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37087-182">OUTPUTS</span></span>

### <span data-ttu-id="37087-183">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="37087-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="37087-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37087-184">NOTES</span></span>

## <span data-ttu-id="37087-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37087-185">RELATED LINKS</span></span>

[<span data-ttu-id="37087-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37087-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="37087-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="37087-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="37087-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37087-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="37087-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="37087-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="37087-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37087-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


