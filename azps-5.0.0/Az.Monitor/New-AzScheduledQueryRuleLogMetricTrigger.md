---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270520"
---
# <span data-ttu-id="caa05-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="caa05-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="caa05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="caa05-102">SYNOPSIS</span></span>
<span data-ttu-id="caa05-103">Skapar ett objekt av typen log-utlösare.</span><span class="sxs-lookup"><span data-stu-id="caa05-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="caa05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="caa05-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="caa05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="caa05-105">DESCRIPTION</span></span>
<span data-ttu-id="caa05-106">Skapar ett objekt av typen log-utlösare och är valfritt.</span><span class="sxs-lookup"><span data-stu-id="caa05-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="caa05-107">Det här är utlösnings villkoret för regeln för metriska frågor som ska användas när du behöver ange mått typen för en avisering.</span><span class="sxs-lookup"><span data-stu-id="caa05-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="caa05-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="caa05-108">EXAMPLES</span></span>

### <span data-ttu-id="caa05-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="caa05-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="caa05-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="caa05-110">PARAMETERS</span></span>

### <span data-ttu-id="caa05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa05-111">-DefaultProfile</span></span>
<span data-ttu-id="caa05-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="caa05-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caa05-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="caa05-113">-MetricColumn</span></span>
<span data-ttu-id="caa05-114">Kolumn där mått värde aggregeras.</span><span class="sxs-lookup"><span data-stu-id="caa05-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="caa05-115">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="caa05-115">The input is not validated.</span></span> <span data-ttu-id="caa05-116">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="caa05-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="caa05-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="caa05-117">-MetricTriggerType</span></span>
<span data-ttu-id="caa05-118">Typ av mått utlösare.</span><span class="sxs-lookup"><span data-stu-id="caa05-118">The metric trigger type.</span></span>
<span data-ttu-id="caa05-119">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="caa05-119">The input is not validated.</span></span> <span data-ttu-id="caa05-120">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="caa05-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="caa05-121">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="caa05-121">-Threshold</span></span>
<span data-ttu-id="caa05-122">Mät tröskel värde: i följd, totalt.</span><span class="sxs-lookup"><span data-stu-id="caa05-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="caa05-123">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="caa05-123">The input is not validated.</span></span> <span data-ttu-id="caa05-124">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="caa05-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa05-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="caa05-125">-ThresholdOperator</span></span>
<span data-ttu-id="caa05-126">Mät operatorn för mått: GreaterThan, mindreän, Equal.</span><span class="sxs-lookup"><span data-stu-id="caa05-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="caa05-127">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="caa05-127">The input is not validated.</span></span> <span data-ttu-id="caa05-128">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="caa05-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="caa05-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa05-129">CommonParameters</span></span>
<span data-ttu-id="caa05-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa05-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa05-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="caa05-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa05-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="caa05-132">INPUTS</span></span>

### <span data-ttu-id="caa05-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="caa05-133">None</span></span>

## <span data-ttu-id="caa05-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="caa05-134">OUTPUTS</span></span>

### <span data-ttu-id="caa05-135">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="caa05-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="caa05-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="caa05-136">NOTES</span></span>

## <span data-ttu-id="caa05-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="caa05-137">RELATED LINKS</span></span>
