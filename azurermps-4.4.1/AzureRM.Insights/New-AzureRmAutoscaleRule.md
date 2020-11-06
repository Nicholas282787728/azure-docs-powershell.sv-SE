---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584724"
---
# <span data-ttu-id="a010d-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="a010d-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="a010d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a010d-102">SYNOPSIS</span></span>
<span data-ttu-id="a010d-103">Skapar en Autoskala-regel.</span><span class="sxs-lookup"><span data-stu-id="a010d-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a010d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a010d-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a010d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a010d-105">DESCRIPTION</span></span>
<span data-ttu-id="a010d-106">Cmdleten **New-AzureRmAutoscaleRule** skapar en AutoScale-regel.</span><span class="sxs-lookup"><span data-stu-id="a010d-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="a010d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a010d-107">EXAMPLES</span></span>

### <span data-ttu-id="a010d-108">Exempel 1: skapa en regel</span><span class="sxs-lookup"><span data-stu-id="a010d-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="a010d-109">Det här kommandot skapar en regel.</span><span class="sxs-lookup"><span data-stu-id="a010d-109">This command creates a rule.</span></span>

### <span data-ttu-id="a010d-110">Exempel 2: skapa två regler</span><span class="sxs-lookup"><span data-stu-id="a010d-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="a010d-111">Det första kommandot skapar en regel för begär måttet och lagrar det sedan i $Rule 1-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a010d-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="a010d-112">Det andra kommandot skapar en andra regel för det begärda måttet och lagrar det sedan i $Rule 2-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a010d-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="a010d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a010d-113">PARAMETERS</span></span>

### <span data-ttu-id="a010d-114">-MetricName</span><span class="sxs-lookup"><span data-stu-id="a010d-114">-MetricName</span></span>
<span data-ttu-id="a010d-115">Anger namnet på måttet.</span><span class="sxs-lookup"><span data-stu-id="a010d-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="a010d-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="a010d-116">-MetricResourceId</span></span>
<span data-ttu-id="a010d-117">Anger mått resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a010d-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="a010d-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="a010d-118">-MetricStatistic</span></span>
<span data-ttu-id="a010d-119">Anger Mät statistik.</span><span class="sxs-lookup"><span data-stu-id="a010d-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="a010d-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a010d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a010d-121">Medel</span><span class="sxs-lookup"><span data-stu-id="a010d-121">Average</span></span>
- <span data-ttu-id="a010d-122">Minst</span><span class="sxs-lookup"><span data-stu-id="a010d-122">Min</span></span>
- <span data-ttu-id="a010d-123">Värdet</span><span class="sxs-lookup"><span data-stu-id="a010d-123">Max</span></span>
- <span data-ttu-id="a010d-124">Totala</span><span class="sxs-lookup"><span data-stu-id="a010d-124">Sum</span></span>

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

### <span data-ttu-id="a010d-125">-Operatör</span><span class="sxs-lookup"><span data-stu-id="a010d-125">-Operator</span></span>
<span data-ttu-id="a010d-126">Anger operatorn.</span><span class="sxs-lookup"><span data-stu-id="a010d-126">Specifies the operator.</span></span>
<span data-ttu-id="a010d-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a010d-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a010d-128">Är lika med</span><span class="sxs-lookup"><span data-stu-id="a010d-128">Equals</span></span>
- <span data-ttu-id="a010d-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="a010d-129">NotEquals</span></span>
- <span data-ttu-id="a010d-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="a010d-130">GreaterThan</span></span>
- <span data-ttu-id="a010d-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="a010d-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="a010d-132">Mindreän</span><span class="sxs-lookup"><span data-stu-id="a010d-132">LessThan</span></span>
- <span data-ttu-id="a010d-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="a010d-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="a010d-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="a010d-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="a010d-135">Anger den automatiska skalnings åtgärden cooldown.</span><span class="sxs-lookup"><span data-stu-id="a010d-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="a010d-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="a010d-136">-ScaleActionDirection</span></span>
<span data-ttu-id="a010d-137">Anger riktningen för skalnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a010d-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="a010d-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a010d-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a010d-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="a010d-139">None</span></span>
- <span data-ttu-id="a010d-140">Fler</span><span class="sxs-lookup"><span data-stu-id="a010d-140">Increase</span></span>
- <span data-ttu-id="a010d-141">Minska</span><span class="sxs-lookup"><span data-stu-id="a010d-141">Decrease</span></span>

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

### <span data-ttu-id="a010d-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="a010d-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="a010d-143">Anger skalnings typen.</span><span class="sxs-lookup"><span data-stu-id="a010d-143">Specifies the scale type.</span></span>
<span data-ttu-id="a010d-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a010d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a010d-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="a010d-145">ChangeSize</span></span>
- <span data-ttu-id="a010d-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="a010d-146">ChangeCount</span></span>
- <span data-ttu-id="a010d-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="a010d-147">PercentChangeCount</span></span>
- <span data-ttu-id="a010d-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="a010d-148">ExactCount</span></span>

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

### <span data-ttu-id="a010d-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="a010d-149">-ScaleActionValue</span></span>
<span data-ttu-id="a010d-150">Anger åtgärd svärdet.</span><span class="sxs-lookup"><span data-stu-id="a010d-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="a010d-151">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="a010d-151">-Threshold</span></span>
<span data-ttu-id="a010d-152">Anger tröskelvärdet för Metric-värdet.</span><span class="sxs-lookup"><span data-stu-id="a010d-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="a010d-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="a010d-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="a010d-154">Anger tids mängds operator.</span><span class="sxs-lookup"><span data-stu-id="a010d-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="a010d-155">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a010d-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a010d-156">Medel</span><span class="sxs-lookup"><span data-stu-id="a010d-156">Average</span></span>
- <span data-ttu-id="a010d-157">Få</span><span class="sxs-lookup"><span data-stu-id="a010d-157">Minimum</span></span>
- <span data-ttu-id="a010d-158">Maximal</span><span class="sxs-lookup"><span data-stu-id="a010d-158">Maximum</span></span>
- <span data-ttu-id="a010d-159">Senast</span><span class="sxs-lookup"><span data-stu-id="a010d-159">Last</span></span>
- <span data-ttu-id="a010d-160">Totalt antal</span><span class="sxs-lookup"><span data-stu-id="a010d-160">Total, Count</span></span>

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

### <span data-ttu-id="a010d-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="a010d-161">-TimeGrain</span></span>
<span data-ttu-id="a010d-162">Anger tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="a010d-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="a010d-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="a010d-163">-TimeWindow</span></span>
<span data-ttu-id="a010d-164">Anger tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="a010d-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="a010d-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a010d-165">-DefaultProfile</span></span>
<span data-ttu-id="a010d-166">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a010d-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a010d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a010d-167">CommonParameters</span></span>
<span data-ttu-id="a010d-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a010d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a010d-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a010d-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a010d-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a010d-170">INPUTS</span></span>

## <span data-ttu-id="a010d-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a010d-171">OUTPUTS</span></span>

### <span data-ttu-id="a010d-172">Microsoft. Azure. Management. Monitoring. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="a010d-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="a010d-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a010d-173">NOTES</span></span>

## <span data-ttu-id="a010d-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a010d-174">RELATED LINKS</span></span>

[<span data-ttu-id="a010d-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a010d-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="a010d-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="a010d-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="a010d-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a010d-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="a010d-178">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="a010d-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="a010d-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a010d-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


