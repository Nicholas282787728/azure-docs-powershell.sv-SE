---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088117"
---
# <span data-ttu-id="7b43e-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7b43e-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7b43e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b43e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b43e-103">Skapar ett objekt av typen log-utlösare.</span><span class="sxs-lookup"><span data-stu-id="7b43e-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="7b43e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b43e-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b43e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b43e-105">DESCRIPTION</span></span>
<span data-ttu-id="7b43e-106">Skapar ett objekt av typen log-utlösare och är valfritt.</span><span class="sxs-lookup"><span data-stu-id="7b43e-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="7b43e-107">Det här är utlösnings villkoret för regeln för metriska frågor som ska användas när du behöver ange mått typen för en avisering.</span><span class="sxs-lookup"><span data-stu-id="7b43e-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="7b43e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b43e-108">EXAMPLES</span></span>

### <span data-ttu-id="7b43e-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b43e-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="7b43e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b43e-110">PARAMETERS</span></span>

### <span data-ttu-id="7b43e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b43e-111">-DefaultProfile</span></span>
<span data-ttu-id="7b43e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b43e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b43e-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="7b43e-113">-MetricColumn</span></span>
<span data-ttu-id="7b43e-114">Kolumn där mått värde aggregeras.</span><span class="sxs-lookup"><span data-stu-id="7b43e-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="7b43e-115">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="7b43e-115">The input is not validated.</span></span> <span data-ttu-id="7b43e-116">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="7b43e-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7b43e-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="7b43e-117">-MetricTriggerType</span></span>
<span data-ttu-id="7b43e-118">Typ av mått utlösare.</span><span class="sxs-lookup"><span data-stu-id="7b43e-118">The metric trigger type.</span></span>
<span data-ttu-id="7b43e-119">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="7b43e-119">The input is not validated.</span></span> <span data-ttu-id="7b43e-120">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="7b43e-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7b43e-121">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="7b43e-121">-Threshold</span></span>
<span data-ttu-id="7b43e-122">Mät tröskel värde: i följd, totalt.</span><span class="sxs-lookup"><span data-stu-id="7b43e-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="7b43e-123">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="7b43e-123">The input is not validated.</span></span> <span data-ttu-id="7b43e-124">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="7b43e-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7b43e-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="7b43e-125">-ThresholdOperator</span></span>
<span data-ttu-id="7b43e-126">Mät operatorn för mått: GreaterThan, mindreän, Equal.</span><span class="sxs-lookup"><span data-stu-id="7b43e-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="7b43e-127">Indata är inte verifierade.</span><span class="sxs-lookup"><span data-stu-id="7b43e-127">The input is not validated.</span></span> <span data-ttu-id="7b43e-128">Det verifieras först när New-AzScheduledQueryRule kallas.</span><span class="sxs-lookup"><span data-stu-id="7b43e-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7b43e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b43e-129">CommonParameters</span></span>
<span data-ttu-id="7b43e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b43e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b43e-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b43e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b43e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b43e-132">INPUTS</span></span>

### <span data-ttu-id="7b43e-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="7b43e-133">None</span></span>

## <span data-ttu-id="7b43e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b43e-134">OUTPUTS</span></span>

### <span data-ttu-id="7b43e-135">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7b43e-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7b43e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b43e-136">NOTES</span></span>

## <span data-ttu-id="7b43e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b43e-137">RELATED LINKS</span></span>
