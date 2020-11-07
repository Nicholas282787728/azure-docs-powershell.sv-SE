---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756507"
---
# <span data-ttu-id="229f5-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="229f5-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="229f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="229f5-102">SYNOPSIS</span></span>
<span data-ttu-id="229f5-103">Skapar en Autoskala-regel.</span><span class="sxs-lookup"><span data-stu-id="229f5-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="229f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="229f5-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="229f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="229f5-105">DESCRIPTION</span></span>
<span data-ttu-id="229f5-106">Cmdleten **New-AzureRmAutoscaleRule** skapar en AutoScale-regel.</span><span class="sxs-lookup"><span data-stu-id="229f5-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="229f5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="229f5-107">EXAMPLES</span></span>

### <span data-ttu-id="229f5-108">Exempel 1: skapa en regel</span><span class="sxs-lookup"><span data-stu-id="229f5-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="229f5-109">Det här kommandot skapar en regel.</span><span class="sxs-lookup"><span data-stu-id="229f5-109">This command creates a rule.</span></span>

### <span data-ttu-id="229f5-110">Exempel 2: skapa två regler</span><span class="sxs-lookup"><span data-stu-id="229f5-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="229f5-111">Det första kommandot skapar en regel för begär måttet och lagrar det sedan i $Rule 1-variabeln.</span><span class="sxs-lookup"><span data-stu-id="229f5-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="229f5-112">Det andra kommandot skapar en andra regel för det begärda måttet och lagrar det sedan i $Rule 2-variabeln.</span><span class="sxs-lookup"><span data-stu-id="229f5-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="229f5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="229f5-113">PARAMETERS</span></span>

### <span data-ttu-id="229f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229f5-114">-DefaultProfile</span></span>
<span data-ttu-id="229f5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="229f5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="229f5-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="229f5-116">-MetricName</span></span>
<span data-ttu-id="229f5-117">Anger namnet på måttet.</span><span class="sxs-lookup"><span data-stu-id="229f5-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="229f5-118">-MetricResourceId</span></span>
<span data-ttu-id="229f5-119">Anger mått resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="229f5-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="229f5-120">-MetricStatistic</span></span>
<span data-ttu-id="229f5-121">Anger Mät statistik.</span><span class="sxs-lookup"><span data-stu-id="229f5-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="229f5-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="229f5-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="229f5-123">Medel</span><span class="sxs-lookup"><span data-stu-id="229f5-123">Average</span></span>
- <span data-ttu-id="229f5-124">Minst</span><span class="sxs-lookup"><span data-stu-id="229f5-124">Min</span></span>
- <span data-ttu-id="229f5-125">Värdet</span><span class="sxs-lookup"><span data-stu-id="229f5-125">Max</span></span>
- <span data-ttu-id="229f5-126">Totala</span><span class="sxs-lookup"><span data-stu-id="229f5-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-127">-Operatör</span><span class="sxs-lookup"><span data-stu-id="229f5-127">-Operator</span></span>
<span data-ttu-id="229f5-128">Anger operatorn.</span><span class="sxs-lookup"><span data-stu-id="229f5-128">Specifies the operator.</span></span>
<span data-ttu-id="229f5-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="229f5-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="229f5-130">Är lika med</span><span class="sxs-lookup"><span data-stu-id="229f5-130">Equals</span></span>
- <span data-ttu-id="229f5-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="229f5-131">NotEquals</span></span>
- <span data-ttu-id="229f5-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="229f5-132">GreaterThan</span></span>
- <span data-ttu-id="229f5-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="229f5-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="229f5-134">Mindreän</span><span class="sxs-lookup"><span data-stu-id="229f5-134">LessThan</span></span>
- <span data-ttu-id="229f5-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="229f5-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="229f5-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="229f5-137">Anger den automatiska skalnings åtgärden cooldown.</span><span class="sxs-lookup"><span data-stu-id="229f5-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="229f5-138">-ScaleActionDirection</span></span>
<span data-ttu-id="229f5-139">Anger riktningen för skalnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="229f5-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="229f5-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="229f5-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="229f5-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="229f5-141">None</span></span>
- <span data-ttu-id="229f5-142">Fler</span><span class="sxs-lookup"><span data-stu-id="229f5-142">Increase</span></span>
- <span data-ttu-id="229f5-143">Minska</span><span class="sxs-lookup"><span data-stu-id="229f5-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="229f5-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="229f5-145">Anger skalnings typen.</span><span class="sxs-lookup"><span data-stu-id="229f5-145">Specifies the scale type.</span></span>
<span data-ttu-id="229f5-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="229f5-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="229f5-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="229f5-147">ChangeSize</span></span>
- <span data-ttu-id="229f5-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="229f5-148">ChangeCount</span></span>
- <span data-ttu-id="229f5-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="229f5-149">PercentChangeCount</span></span>
- <span data-ttu-id="229f5-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="229f5-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="229f5-151">-ScaleActionValue</span></span>
<span data-ttu-id="229f5-152">Anger åtgärd svärdet.</span><span class="sxs-lookup"><span data-stu-id="229f5-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-153">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="229f5-153">-Threshold</span></span>
<span data-ttu-id="229f5-154">Anger tröskelvärdet för Metric-värdet.</span><span class="sxs-lookup"><span data-stu-id="229f5-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="229f5-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="229f5-156">Anger tids mängds operator.</span><span class="sxs-lookup"><span data-stu-id="229f5-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="229f5-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="229f5-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="229f5-158">Medel</span><span class="sxs-lookup"><span data-stu-id="229f5-158">Average</span></span>
- <span data-ttu-id="229f5-159">Få</span><span class="sxs-lookup"><span data-stu-id="229f5-159">Minimum</span></span>
- <span data-ttu-id="229f5-160">Maximal</span><span class="sxs-lookup"><span data-stu-id="229f5-160">Maximum</span></span>
- <span data-ttu-id="229f5-161">Senast</span><span class="sxs-lookup"><span data-stu-id="229f5-161">Last</span></span>
- <span data-ttu-id="229f5-162">Totalt antal</span><span class="sxs-lookup"><span data-stu-id="229f5-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="229f5-163">-TimeGrain</span></span>
<span data-ttu-id="229f5-164">Anger tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="229f5-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="229f5-165">-TimeWindow</span></span>
<span data-ttu-id="229f5-166">Anger tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="229f5-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229f5-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229f5-167">CommonParameters</span></span>
<span data-ttu-id="229f5-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229f5-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229f5-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229f5-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229f5-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="229f5-170">INPUTS</span></span>

### <span data-ttu-id="229f5-171">Ingen</span><span class="sxs-lookup"><span data-stu-id="229f5-171">None</span></span>
<span data-ttu-id="229f5-172">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="229f5-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="229f5-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="229f5-173">OUTPUTS</span></span>

### <span data-ttu-id="229f5-174">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="229f5-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="229f5-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="229f5-175">NOTES</span></span>

## <span data-ttu-id="229f5-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="229f5-176">RELATED LINKS</span></span>

[<span data-ttu-id="229f5-177">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="229f5-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="229f5-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="229f5-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="229f5-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="229f5-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="229f5-180">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="229f5-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="229f5-181">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="229f5-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


