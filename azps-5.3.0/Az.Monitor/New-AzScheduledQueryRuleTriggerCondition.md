---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522537"
---
# <span data-ttu-id="06699-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="06699-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="06699-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06699-102">SYNOPSIS</span></span>
<span data-ttu-id="06699-103">Skapar ett objekt av typen trigger villkor</span><span class="sxs-lookup"><span data-stu-id="06699-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="06699-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06699-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06699-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06699-105">DESCRIPTION</span></span>
<span data-ttu-id="06699-106">Skapar ett objekt av typen trigger villkor.</span><span class="sxs-lookup"><span data-stu-id="06699-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="06699-107">Det här objektet ska överföras till kommandot som skapar ett varnings objekt</span><span class="sxs-lookup"><span data-stu-id="06699-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="06699-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06699-108">EXAMPLES</span></span>

### <span data-ttu-id="06699-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06699-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="06699-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06699-110">PARAMETERS</span></span>

### <span data-ttu-id="06699-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06699-111">-DefaultProfile</span></span>
<span data-ttu-id="06699-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06699-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06699-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="06699-113">-MetricTrigger</span></span>
<span data-ttu-id="06699-114">Utlös ande villkor för regeln för metriska frågor</span><span class="sxs-lookup"><span data-stu-id="06699-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06699-115">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="06699-115">-Threshold</span></span>
<span data-ttu-id="06699-116">Tröskelvärde över vilken varning utlöses</span><span class="sxs-lookup"><span data-stu-id="06699-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="06699-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="06699-117">-ThresholdOperator</span></span>
<span data-ttu-id="06699-118">Tröskelvärdes operatör: GreaterThan, mindreän eller lika</span><span class="sxs-lookup"><span data-stu-id="06699-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="06699-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06699-119">CommonParameters</span></span>
<span data-ttu-id="06699-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06699-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06699-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06699-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06699-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06699-122">INPUTS</span></span>

### <span data-ttu-id="06699-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="06699-123">None</span></span>

## <span data-ttu-id="06699-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06699-124">OUTPUTS</span></span>

### <span data-ttu-id="06699-125">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="06699-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="06699-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06699-126">NOTES</span></span>

## <span data-ttu-id="06699-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06699-127">RELATED LINKS</span></span>
