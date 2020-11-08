---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262151"
---
# <span data-ttu-id="38a37-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="38a37-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="38a37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38a37-102">SYNOPSIS</span></span>
<span data-ttu-id="38a37-103">Skapar ett lokalt villkors objekt som kan användas för att skapa en ny mått avisering</span><span class="sxs-lookup"><span data-stu-id="38a37-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="38a37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38a37-104">SYNTAX</span></span>

### <span data-ttu-id="38a37-105">StaticThresholdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="38a37-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a37-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38a37-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a37-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="38a37-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a37-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38a37-108">DESCRIPTION</span></span>
<span data-ttu-id="38a37-109">Cmdleten **New-AzMetricAlertRuleV2Criteria** skapar ett objekt för lokala mått som du kan använda som indata Add-AzMetricAlertRuleV2 cmdlet som skapar en ny regel för metrisk avisering.</span><span class="sxs-lookup"><span data-stu-id="38a37-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="38a37-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38a37-110">EXAMPLES</span></span>

### <span data-ttu-id="38a37-111">Exempel 1: skapa ett enkelt mått för aviseringar</span><span class="sxs-lookup"><span data-stu-id="38a37-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="38a37-112">Det här kommandot skapar ett enkelt mått för varnings aviseringar som kan användas i en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="38a37-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="38a37-113">Exempel 2: skapa ett villkor för dynamisk metrisk avisering</span><span class="sxs-lookup"><span data-stu-id="38a37-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="38a37-114">Det här kommandot skapar ett dynamiskt mått för aviserings villkor som kan användas i en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="38a37-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="38a37-115">Exempel 3: skapa ett mer komplext mått för statistik avisering</span><span class="sxs-lookup"><span data-stu-id="38a37-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="38a37-116">Med den här uppsättningen kommandon skapas ett mer komplext mått för statistik avisering, vilket inkluderar dimensions val</span><span class="sxs-lookup"><span data-stu-id="38a37-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="38a37-117">Exempel 4: skapa tillgänglighets villkor för en webtest</span><span class="sxs-lookup"><span data-stu-id="38a37-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="38a37-118">Det här kommandot skapar ett tillgänglighets villkor för webtest som kan användas i en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="38a37-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="38a37-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38a37-119">PARAMETERS</span></span>

### <span data-ttu-id="38a37-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="38a37-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="38a37-121">ID för Application Insights-resursen.</span><span class="sxs-lookup"><span data-stu-id="38a37-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a37-122">-DefaultProfile</span></span>
<span data-ttu-id="38a37-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38a37-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a37-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="38a37-124">-DimensionSelection</span></span>
<span data-ttu-id="38a37-125">Lista över dimensions villkor</span><span class="sxs-lookup"><span data-stu-id="38a37-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="38a37-126">-DynamicThreshold</span></span>
<span data-ttu-id="38a37-127">Switch parameter för att använda dynamisk tröskel typ</span><span class="sxs-lookup"><span data-stu-id="38a37-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="38a37-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="38a37-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="38a37-129">Totalt antal undersökta punkter</span><span class="sxs-lookup"><span data-stu-id="38a37-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="38a37-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="38a37-130">-FailedLocationCount</span></span>
<span data-ttu-id="38a37-131">Minsta antal misslyckade platser för att utlösa en avisering.</span><span class="sxs-lookup"><span data-stu-id="38a37-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="38a37-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="38a37-133">Parametern IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="38a37-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="38a37-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="38a37-134">-MetricName</span></span>
<span data-ttu-id="38a37-135">Mått namn för regel</span><span class="sxs-lookup"><span data-stu-id="38a37-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="38a37-136">-MetricNamespace</span></span>
<span data-ttu-id="38a37-137">Mått områdes namn</span><span class="sxs-lookup"><span data-stu-id="38a37-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-138">-Operatör</span><span class="sxs-lookup"><span data-stu-id="38a37-138">-Operator</span></span>
<span data-ttu-id="38a37-139">Operatorn regel villkor</span><span class="sxs-lookup"><span data-stu-id="38a37-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="38a37-140">-SkipMetricValidation</span></span>
<span data-ttu-id="38a37-141">Gör det möjligt att skapa en notifieringsregel på ett anpassat mått som ännu inte har utlevererats, genom att orsaka att mät verifieringen hoppas över</span><span class="sxs-lookup"><span data-stu-id="38a37-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-142">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="38a37-142">-Threshold</span></span>
<span data-ttu-id="38a37-143">Tröskelvärdet för regel villkor</span><span class="sxs-lookup"><span data-stu-id="38a37-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="38a37-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="38a37-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="38a37-145">Känslighet för regel villkor</span><span class="sxs-lookup"><span data-stu-id="38a37-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="38a37-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="38a37-146">-TimeAggregation</span></span>
<span data-ttu-id="38a37-147">Den mängd funktion som används för att lyfta upp flera metriska värden över fönster intervallet</span><span class="sxs-lookup"><span data-stu-id="38a37-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="38a37-148">-ViolationCount</span></span>
<span data-ttu-id="38a37-149">Det minsta antalet överträdelser som krävs inom det valda tidsfönstret för lookback krävs för att öka en avisering</span><span class="sxs-lookup"><span data-stu-id="38a37-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="38a37-150">-Webtest</span><span class="sxs-lookup"><span data-stu-id="38a37-150">-WebTest</span></span>
<span data-ttu-id="38a37-151">Byt parameter för användning av tillgänglighets villkors typ</span><span class="sxs-lookup"><span data-stu-id="38a37-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="38a37-152">-WebTestId</span></span>
<span data-ttu-id="38a37-153">ID för webb test för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="38a37-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a37-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a37-154">CommonParameters</span></span>
<span data-ttu-id="38a37-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a37-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a37-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a37-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a37-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38a37-157">INPUTS</span></span>

### <span data-ttu-id="38a37-158">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="38a37-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="38a37-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38a37-159">OUTPUTS</span></span>

### <span data-ttu-id="38a37-160">Microsoft. Azure. commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="38a37-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="38a37-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38a37-161">NOTES</span></span>

## <span data-ttu-id="38a37-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38a37-162">RELATED LINKS</span></span>
