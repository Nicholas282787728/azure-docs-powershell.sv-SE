---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1d58fba402f292c0935fc10715e06b323353046c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925658"
---
# <span data-ttu-id="3188d-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3188d-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="3188d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3188d-102">SYNOPSIS</span></span>
<span data-ttu-id="3188d-103">Uppdaterar en loggnings varnings regel</span><span class="sxs-lookup"><span data-stu-id="3188d-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="3188d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3188d-104">SYNTAX</span></span>

### <span data-ttu-id="3188d-105">ByRuleName (standard)</span><span class="sxs-lookup"><span data-stu-id="3188d-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3188d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3188d-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3188d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3188d-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3188d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3188d-108">DESCRIPTION</span></span>
<span data-ttu-id="3188d-109">Uppdaterar en regel för loggnings varningar, uppdatering av endast "aktiverat"-egenskapen stöds av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="3188d-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="3188d-110">Om du vill uppdatera andra egenskaper läser du "Set-AzScheduledQueryRule".</span><span class="sxs-lookup"><span data-stu-id="3188d-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="3188d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3188d-111">EXAMPLES</span></span>

### <span data-ttu-id="3188d-112">Exempel 1 – uppdatera enligt regel namn</span><span class="sxs-lookup"><span data-stu-id="3188d-112">Example 1 - Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="3188d-113">Exempel 2 – uppdatera med indata-objekt</span><span class="sxs-lookup"><span data-stu-id="3188d-113">Example 2 - Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="3188d-114">Exempel 3 – uppdatera efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3188d-114">Example 3 - Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="3188d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3188d-115">PARAMETERS</span></span>

### <span data-ttu-id="3188d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3188d-116">-DefaultProfile</span></span>
<span data-ttu-id="3188d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3188d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3188d-118">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="3188d-118">-Enabled</span></span>
<span data-ttu-id="3188d-119">Azure Alert State – giltiga värden-$true $false</span><span class="sxs-lookup"><span data-stu-id="3188d-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="3188d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3188d-120">-InputObject</span></span>
<span data-ttu-id="3188d-121">Resursen för regel för schemaläggning</span><span class="sxs-lookup"><span data-stu-id="3188d-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3188d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3188d-122">-Name</span></span>
<span data-ttu-id="3188d-123">Aviseringens namn</span><span class="sxs-lookup"><span data-stu-id="3188d-123">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3188d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3188d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3188d-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="3188d-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3188d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3188d-126">-ResourceId</span></span>
<span data-ttu-id="3188d-127">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3188d-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3188d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3188d-128">-Confirm</span></span>
<span data-ttu-id="3188d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3188d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3188d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3188d-130">-WhatIf</span></span>
<span data-ttu-id="3188d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3188d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3188d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3188d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3188d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3188d-133">CommonParameters</span></span>
<span data-ttu-id="3188d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3188d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3188d-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3188d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3188d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3188d-136">INPUTS</span></span>

### <span data-ttu-id="3188d-137">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3188d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="3188d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3188d-138">System.String</span></span>

## <span data-ttu-id="3188d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3188d-139">OUTPUTS</span></span>

### <span data-ttu-id="3188d-140">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3188d-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="3188d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3188d-141">NOTES</span></span>

## <span data-ttu-id="3188d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3188d-142">RELATED LINKS</span></span>