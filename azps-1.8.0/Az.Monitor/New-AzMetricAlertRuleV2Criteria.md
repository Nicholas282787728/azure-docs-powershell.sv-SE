---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915610"
---
# <span data-ttu-id="fd9f3-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="fd9f3-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="fd9f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9f3-103">Skapar ett lokalt villkors objekt som kan användas för att skapa en ny mått avisering</span><span class="sxs-lookup"><span data-stu-id="fd9f3-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="fd9f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd9f3-104">SYNTAX</span></span>

### <span data-ttu-id="fd9f3-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9f3-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd9f3-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9f3-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd9f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd9f3-107">DESCRIPTION</span></span>
<span data-ttu-id="fd9f3-108">Cmdleten **New-AzMetricAlertRuleV2Criteria** skapar ett objekt för lokala mått som du kan använda som indata Add-AzMetricAlertRuleV2 cmdlet som skapar en ny regel för metrisk avisering.</span><span class="sxs-lookup"><span data-stu-id="fd9f3-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="fd9f3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd9f3-109">EXAMPLES</span></span>

### <span data-ttu-id="fd9f3-110">Exempel 1: skapa ett enkelt mått för aviseringar</span><span class="sxs-lookup"><span data-stu-id="fd9f3-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="fd9f3-111">Det här kommandot skapar ett enkelt mått för varnings aviseringar som kan användas i en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="fd9f3-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="fd9f3-112">Exempel 2: skapa ett mer komplext mått för statistik avisering</span><span class="sxs-lookup"><span data-stu-id="fd9f3-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="fd9f3-113">Med den här uppsättningen kommandon skapas ett mer komplext mått för statistik avisering, vilket inkluderar dimensions val</span><span class="sxs-lookup"><span data-stu-id="fd9f3-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="fd9f3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd9f3-114">PARAMETERS</span></span>

### <span data-ttu-id="fd9f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9f3-115">-DefaultProfile</span></span>
<span data-ttu-id="fd9f3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd9f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="fd9f3-117">-DimensionSelection</span></span>
<span data-ttu-id="fd9f3-118">Lista över dimensions villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="fd9f3-119">-DynamicThreshold</span></span>
<span data-ttu-id="fd9f3-120">Tröskelvärdet dynamiskt för regel villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="fd9f3-121">-FailingPeriod</span></span>
<span data-ttu-id="fd9f3-122">Den misslyckade perioden för regel villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="fd9f3-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="fd9f3-124">Parametern IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="fd9f3-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="fd9f3-125">-MetricName</span></span>
<span data-ttu-id="fd9f3-126">Mått namn för regel</span><span class="sxs-lookup"><span data-stu-id="fd9f3-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="fd9f3-127">-MetricNamespace</span></span>
<span data-ttu-id="fd9f3-128">Mått områdes namn</span><span class="sxs-lookup"><span data-stu-id="fd9f3-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-129">-Operatör</span><span class="sxs-lookup"><span data-stu-id="fd9f3-129">-Operator</span></span>
<span data-ttu-id="fd9f3-130">Operatorn regel villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-131">-Känslighet</span><span class="sxs-lookup"><span data-stu-id="fd9f3-131">-Sensitivity</span></span>
<span data-ttu-id="fd9f3-132">Känslighet för regel villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-133">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="fd9f3-133">-Threshold</span></span>
<span data-ttu-id="fd9f3-134">Tröskelvärdet för regel villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="fd9f3-135">-TimeAggregation</span></span>
<span data-ttu-id="fd9f3-136">Den mängd funktion som används för att lyfta upp flera metriska värden över fönster intervallet</span><span class="sxs-lookup"><span data-stu-id="fd9f3-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="fd9f3-137">-TotalPeriod</span></span>
<span data-ttu-id="fd9f3-138">Den totala perioden för regel villkor</span><span class="sxs-lookup"><span data-stu-id="fd9f3-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9f3-139">CommonParameters</span></span>
<span data-ttu-id="fd9f3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fd9f3-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd9f3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9f3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd9f3-142">INPUTS</span></span>

### <span data-ttu-id="fd9f3-143">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="fd9f3-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="fd9f3-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd9f3-144">OUTPUTS</span></span>

### <span data-ttu-id="fd9f3-145">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="fd9f3-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="fd9f3-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd9f3-146">NOTES</span></span>

## <span data-ttu-id="fd9f3-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd9f3-147">RELATED LINKS</span></span>
