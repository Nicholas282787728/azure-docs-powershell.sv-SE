---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 6e50269e98a942d425f914eed5cc0a75938d0e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088135"
---
# <span data-ttu-id="426d9-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="426d9-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="426d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="426d9-102">SYNOPSIS</span></span>
<span data-ttu-id="426d9-103">Skapar ett lokalt villkors objekt som kan användas för att skapa en ny mått avisering</span><span class="sxs-lookup"><span data-stu-id="426d9-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="426d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="426d9-104">SYNTAX</span></span>

### <span data-ttu-id="426d9-105">StaticThresholdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="426d9-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="426d9-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="426d9-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="426d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="426d9-107">DESCRIPTION</span></span>
<span data-ttu-id="426d9-108">Cmdleten **New-AzMetricAlertRuleV2Criteria** skapar ett objekt för lokala mått som du kan använda som indata Add-AzMetricAlertRuleV2 cmdlet som skapar en ny regel för metrisk avisering.</span><span class="sxs-lookup"><span data-stu-id="426d9-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="426d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="426d9-109">EXAMPLES</span></span>

### <span data-ttu-id="426d9-110">Exempel 1: skapa ett enkelt mått för aviseringar</span><span class="sxs-lookup"><span data-stu-id="426d9-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="426d9-111">Det här kommandot skapar ett enkelt mått för varnings aviseringar som kan användas i en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="426d9-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="426d9-112">Exempel 2: skapa ett villkor för dynamisk metrisk avisering</span><span class="sxs-lookup"><span data-stu-id="426d9-112">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="426d9-113">Det här kommandot skapar ett dynamiskt mått för aviserings villkor som kan användas i en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="426d9-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="426d9-114">Exempel 3: skapa ett mer komplext mått för statistik avisering</span><span class="sxs-lookup"><span data-stu-id="426d9-114">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="426d9-115">Med den här uppsättningen kommandon skapas ett mer komplext mått för statistik avisering, vilket inkluderar dimensions val</span><span class="sxs-lookup"><span data-stu-id="426d9-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="426d9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="426d9-116">PARAMETERS</span></span>

### <span data-ttu-id="426d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426d9-117">-DefaultProfile</span></span>
<span data-ttu-id="426d9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="426d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="426d9-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="426d9-119">-DimensionSelection</span></span>
<span data-ttu-id="426d9-120">Lista över dimensions villkor</span><span class="sxs-lookup"><span data-stu-id="426d9-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="426d9-121">-DynamicThreshold</span></span>
<span data-ttu-id="426d9-122">Switch parameter för att använda dynamisk tröskel typ</span><span class="sxs-lookup"><span data-stu-id="426d9-122">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="426d9-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="426d9-124">Totalt antal undersökta punkter</span><span class="sxs-lookup"><span data-stu-id="426d9-124">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="426d9-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="426d9-126">Parametern IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="426d9-126">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="426d9-127">-MetricName</span></span>
<span data-ttu-id="426d9-128">Mått namn för regel</span><span class="sxs-lookup"><span data-stu-id="426d9-128">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="426d9-129">-MetricNamespace</span></span>
<span data-ttu-id="426d9-130">Mått områdes namn</span><span class="sxs-lookup"><span data-stu-id="426d9-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-131">-Operatör</span><span class="sxs-lookup"><span data-stu-id="426d9-131">-Operator</span></span>
<span data-ttu-id="426d9-132">Operatorn regel villkor</span><span class="sxs-lookup"><span data-stu-id="426d9-132">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-133">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="426d9-133">-Threshold</span></span>
<span data-ttu-id="426d9-134">Tröskelvärdet för regel villkor</span><span class="sxs-lookup"><span data-stu-id="426d9-134">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="426d9-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="426d9-136">Känslighet för regel villkor</span><span class="sxs-lookup"><span data-stu-id="426d9-136">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="426d9-137">-TimeAggregation</span></span>
<span data-ttu-id="426d9-138">Den mängd funktion som används för att lyfta upp flera metriska värden över fönster intervallet</span><span class="sxs-lookup"><span data-stu-id="426d9-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="426d9-139">-ViolationCount</span></span>
<span data-ttu-id="426d9-140">Det minsta antalet överträdelser som krävs inom det valda tidsfönstret för lookback krävs för att öka en avisering</span><span class="sxs-lookup"><span data-stu-id="426d9-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426d9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426d9-141">CommonParameters</span></span>
<span data-ttu-id="426d9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426d9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426d9-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="426d9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426d9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="426d9-144">INPUTS</span></span>

### <span data-ttu-id="426d9-145">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="426d9-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="426d9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="426d9-146">OUTPUTS</span></span>

### <span data-ttu-id="426d9-147">Microsoft. Azure. commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="426d9-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="426d9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="426d9-148">NOTES</span></span>

## <span data-ttu-id="426d9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="426d9-149">RELATED LINKS</span></span>
