---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392155"
---
# <span data-ttu-id="c2633-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c2633-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="c2633-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2633-102">SYNOPSIS</span></span>
<span data-ttu-id="c2633-103">Skapar en regel för loggnings avisering (regel för schemalagd fråga)</span><span class="sxs-lookup"><span data-stu-id="c2633-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="c2633-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2633-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2633-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2633-105">DESCRIPTION</span></span>
<span data-ttu-id="c2633-106">Skapar en regel för loggnings avisering (regel för schemalagd fråga)</span><span class="sxs-lookup"><span data-stu-id="c2633-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="c2633-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2633-107">EXAMPLES</span></span>

### <span data-ttu-id="c2633-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2633-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="c2633-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2633-109">PARAMETERS</span></span>

### <span data-ttu-id="c2633-110">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="c2633-110">-Action</span></span>
<span data-ttu-id="c2633-111">Varnings åtgärden för den schemalagda frågekomponenten</span><span class="sxs-lookup"><span data-stu-id="c2633-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2633-112">-AsJob</span></span>
<span data-ttu-id="c2633-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c2633-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2633-114">-DefaultProfile</span></span>
<span data-ttu-id="c2633-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2633-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2633-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c2633-116">-Description</span></span>
<span data-ttu-id="c2633-117">Beskrivning för den här aviseringen</span><span class="sxs-lookup"><span data-stu-id="c2633-117">The description for this alert</span></span>

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

### <span data-ttu-id="c2633-118">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="c2633-118">-Enabled</span></span>
<span data-ttu-id="c2633-119">Azure Alert State – giltiga värden-$true $false</span><span class="sxs-lookup"><span data-stu-id="c2633-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="c2633-120">-Location</span></span>
<span data-ttu-id="c2633-121">Aviseringens plats</span><span class="sxs-lookup"><span data-stu-id="c2633-121">The location for this alert</span></span>

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

### <span data-ttu-id="c2633-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2633-122">-Name</span></span>
<span data-ttu-id="c2633-123">Aviseringens namn</span><span class="sxs-lookup"><span data-stu-id="c2633-123">The alert name</span></span>

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

### <span data-ttu-id="c2633-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2633-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2633-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="c2633-125">The resource group name</span></span>

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

### <span data-ttu-id="c2633-126">– Schema</span><span class="sxs-lookup"><span data-stu-id="c2633-126">-Schedule</span></span>
<span data-ttu-id="c2633-127">Schemat för den schemalagda regeln</span><span class="sxs-lookup"><span data-stu-id="c2633-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-128">-Källa</span><span class="sxs-lookup"><span data-stu-id="c2633-128">-Source</span></span>
<span data-ttu-id="c2633-129">Den schemalagda frågekomponenten</span><span class="sxs-lookup"><span data-stu-id="c2633-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c2633-130">-Tag</span></span>
<span data-ttu-id="c2633-131">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="c2633-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2633-132">-Confirm</span></span>
<span data-ttu-id="c2633-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2633-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2633-134">-WhatIf</span></span>
<span data-ttu-id="c2633-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2633-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2633-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2633-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2633-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2633-137">CommonParameters</span></span>
<span data-ttu-id="c2633-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2633-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2633-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2633-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2633-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2633-140">INPUTS</span></span>

### <span data-ttu-id="c2633-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c2633-141">System.String</span></span>

## <span data-ttu-id="c2633-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2633-142">OUTPUTS</span></span>

### <span data-ttu-id="c2633-143">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c2633-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="c2633-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2633-144">NOTES</span></span>

## <span data-ttu-id="c2633-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2633-145">RELATED LINKS</span></span>
