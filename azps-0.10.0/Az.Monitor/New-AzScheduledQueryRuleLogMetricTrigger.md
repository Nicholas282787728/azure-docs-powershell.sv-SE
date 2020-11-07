---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922542"
---
# <span data-ttu-id="23b8f-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="23b8f-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="23b8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="23b8f-103">Skapar ett objekt av typen log-utlösare</span><span class="sxs-lookup"><span data-stu-id="23b8f-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="23b8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23b8f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23b8f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="23b8f-106">Skapar ett objekt av typen log-utlösare och är valfritt.</span><span class="sxs-lookup"><span data-stu-id="23b8f-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="23b8f-107">Det här är utlösnings villkoret för regeln för metriska frågor som ska användas när du behöver ange mått typen för en avisering.</span><span class="sxs-lookup"><span data-stu-id="23b8f-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="23b8f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23b8f-108">EXAMPLES</span></span>

### <span data-ttu-id="23b8f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23b8f-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="23b8f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="23b8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b8f-111">-DefaultProfile</span></span>
<span data-ttu-id="23b8f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23b8f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b8f-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="23b8f-113">-MetricColumn</span></span>
<span data-ttu-id="23b8f-114">Kolumn där metriskt värde aggregeras</span><span class="sxs-lookup"><span data-stu-id="23b8f-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="23b8f-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="23b8f-115">-MetricTriggerType</span></span>
<span data-ttu-id="23b8f-116">Typ av mått utlösare</span><span class="sxs-lookup"><span data-stu-id="23b8f-116">The metric trigger type</span></span>

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

### <span data-ttu-id="23b8f-117">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="23b8f-117">-Threshold</span></span>
<span data-ttu-id="23b8f-118">Värdet för Mät värde</span><span class="sxs-lookup"><span data-stu-id="23b8f-118">The metric threshold value</span></span>

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

### <span data-ttu-id="23b8f-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="23b8f-119">-ThresholdOperator</span></span>
<span data-ttu-id="23b8f-120">Mät operatorn för mått: GreaterThan, mindreän, Equal</span><span class="sxs-lookup"><span data-stu-id="23b8f-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="23b8f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b8f-121">CommonParameters</span></span>
<span data-ttu-id="23b8f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b8f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b8f-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23b8f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b8f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23b8f-124">INPUTS</span></span>

### <span data-ttu-id="23b8f-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="23b8f-125">None</span></span>

## <span data-ttu-id="23b8f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23b8f-126">OUTPUTS</span></span>

### <span data-ttu-id="23b8f-127">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="23b8f-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="23b8f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23b8f-128">NOTES</span></span>

## <span data-ttu-id="23b8f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23b8f-129">RELATED LINKS</span></span>
