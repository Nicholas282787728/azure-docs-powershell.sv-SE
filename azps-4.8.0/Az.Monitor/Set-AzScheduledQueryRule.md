---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262143"
---
# <span data-ttu-id="3e421-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3e421-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="3e421-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e421-102">SYNOPSIS</span></span>
<span data-ttu-id="3e421-103">Uppdaterar en loggnings varnings regel</span><span class="sxs-lookup"><span data-stu-id="3e421-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="3e421-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e421-104">SYNTAX</span></span>

### <span data-ttu-id="3e421-105">ByRuleName (standard)</span><span class="sxs-lookup"><span data-stu-id="3e421-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e421-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e421-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e421-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e421-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e421-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e421-108">DESCRIPTION</span></span>
<span data-ttu-id="3e421-109">Uppdaterar en loggnings varnings regel genom att ange semantik</span><span class="sxs-lookup"><span data-stu-id="3e421-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="3e421-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e421-110">EXAMPLES</span></span>

### <span data-ttu-id="3e421-111">Exempel 1: Ange som regel namn</span><span class="sxs-lookup"><span data-stu-id="3e421-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
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

### <span data-ttu-id="3e421-112">Exempel 2: uppsättning med indata-objekt</span><span class="sxs-lookup"><span data-stu-id="3e421-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
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

### <span data-ttu-id="3e421-113">Exempel 3: Ange resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3e421-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
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

## <span data-ttu-id="3e421-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e421-114">PARAMETERS</span></span>

### <span data-ttu-id="3e421-115">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="3e421-115">-Action</span></span>
<span data-ttu-id="3e421-116">Varnings åtgärden för den schemalagda frågekomponenten</span><span class="sxs-lookup"><span data-stu-id="3e421-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e421-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e421-117">-AsJob</span></span>
<span data-ttu-id="3e421-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e421-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e421-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e421-119">-DefaultProfile</span></span>
<span data-ttu-id="3e421-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e421-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e421-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3e421-121">-Description</span></span>
<span data-ttu-id="3e421-122">Beskrivning för den här aviseringen</span><span class="sxs-lookup"><span data-stu-id="3e421-122">The description for this alert</span></span>

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

### <span data-ttu-id="3e421-123">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="3e421-123">-Enabled</span></span>
<span data-ttu-id="3e421-124">Azure Alert State – giltiga värden-$true $false</span><span class="sxs-lookup"><span data-stu-id="3e421-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e421-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e421-125">-InputObject</span></span>
<span data-ttu-id="3e421-126">Resursen för regel för schemaläggning</span><span class="sxs-lookup"><span data-stu-id="3e421-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="3e421-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e421-127">-Location</span></span>
<span data-ttu-id="3e421-128">Aviseringens plats</span><span class="sxs-lookup"><span data-stu-id="3e421-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e421-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e421-129">-Name</span></span>
<span data-ttu-id="3e421-130">Aviseringens namn</span><span class="sxs-lookup"><span data-stu-id="3e421-130">The alert name</span></span>

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

### <span data-ttu-id="3e421-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e421-131">-ResourceGroupName</span></span>
<span data-ttu-id="3e421-132">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="3e421-132">The resource group name</span></span>

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

### <span data-ttu-id="3e421-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e421-133">-ResourceId</span></span>
<span data-ttu-id="3e421-134">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3e421-134">The resource Id</span></span>

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

### <span data-ttu-id="3e421-135">– Schema</span><span class="sxs-lookup"><span data-stu-id="3e421-135">-Schedule</span></span>
<span data-ttu-id="3e421-136">Schemat för den schemalagda regeln</span><span class="sxs-lookup"><span data-stu-id="3e421-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e421-137">-Källa</span><span class="sxs-lookup"><span data-stu-id="3e421-137">-Source</span></span>
<span data-ttu-id="3e421-138">Den schemalagda frågekomponenten</span><span class="sxs-lookup"><span data-stu-id="3e421-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e421-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3e421-139">-Tag</span></span>
<span data-ttu-id="3e421-140">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="3e421-140">Resource tags</span></span>

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

### <span data-ttu-id="3e421-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e421-141">-Confirm</span></span>
<span data-ttu-id="3e421-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e421-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e421-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e421-143">-WhatIf</span></span>
<span data-ttu-id="3e421-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e421-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e421-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e421-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e421-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e421-146">CommonParameters</span></span>
<span data-ttu-id="3e421-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e421-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e421-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e421-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e421-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e421-149">INPUTS</span></span>

### <span data-ttu-id="3e421-150">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3e421-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="3e421-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3e421-151">System.String</span></span>

### <span data-ttu-id="3e421-152">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3e421-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="3e421-153">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3e421-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="3e421-154">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3e421-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="3e421-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e421-155">OUTPUTS</span></span>

### <span data-ttu-id="3e421-156">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3e421-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="3e421-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e421-157">NOTES</span></span>

## <span data-ttu-id="3e421-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e421-158">RELATED LINKS</span></span>
