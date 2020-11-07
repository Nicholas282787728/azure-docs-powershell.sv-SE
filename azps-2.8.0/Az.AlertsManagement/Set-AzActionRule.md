---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745905"
---
# <span data-ttu-id="40f87-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="40f87-101">Set-AzActionRule</span></span>

## <span data-ttu-id="40f87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40f87-102">SYNOPSIS</span></span>
<span data-ttu-id="40f87-103">Skapa eller uppdatera en åtgärds regel.</span><span class="sxs-lookup"><span data-stu-id="40f87-103">Create or update an action rule.</span></span>

## <span data-ttu-id="40f87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40f87-104">SYNTAX</span></span>

### <span data-ttu-id="40f87-105">BySimplifiedFormatDiagnosticsActionRule (standard)</span><span class="sxs-lookup"><span data-stu-id="40f87-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40f87-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="40f87-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40f87-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="40f87-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40f87-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="40f87-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40f87-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40f87-109">DESCRIPTION</span></span>
<span data-ttu-id="40f87-110">**Set-AzActionRule** skapar eller uppdaterar en åtgärds regel.</span><span class="sxs-lookup"><span data-stu-id="40f87-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="40f87-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40f87-111">EXAMPLES</span></span>

### <span data-ttu-id="40f87-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40f87-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="40f87-113">Denna cmdlet skapar en åtgärds regel för Supression.</span><span class="sxs-lookup"><span data-stu-id="40f87-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="40f87-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="40f87-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="40f87-115">Denna cmdlet skapar en åtgärds regel för gruppen åtgärd.</span><span class="sxs-lookup"><span data-stu-id="40f87-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="40f87-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="40f87-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="40f87-117">Denna cmdlet skapar en åtgärds regel för diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="40f87-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="40f87-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40f87-118">PARAMETERS</span></span>

### <span data-ttu-id="40f87-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="40f87-119">-ActionGroupId</span></span>
<span data-ttu-id="40f87-120">Åtgärds grupp-ID som ska meddelas.</span><span class="sxs-lookup"><span data-stu-id="40f87-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="40f87-121">-ActionRuleType</span></span>
<span data-ttu-id="40f87-122">JSON-format för åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="40f87-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-123">-AlertContextCondition</span></span>
<span data-ttu-id="40f87-124">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-125">Innehåller: smartgroups</span><span class="sxs-lookup"><span data-stu-id="40f87-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="40f87-127">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-128">Lika med:/abonnemang/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/leverantörer/Microsoft. insikter/metricAlerts/test-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="40f87-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f87-129">-DefaultProfile</span></span>
<span data-ttu-id="40f87-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40f87-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f87-131">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="40f87-131">-Description</span></span>
<span data-ttu-id="40f87-132">Beskrivning av åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="40f87-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-133">-DescriptionCondition</span></span>
<span data-ttu-id="40f87-134">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-135">Innehåller: test avisering</span><span class="sxs-lookup"><span data-stu-id="40f87-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40f87-136">-InputObject</span></span>
<span data-ttu-id="40f87-137">Resurs för åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="40f87-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-138">-MonitorCondition</span></span>
<span data-ttu-id="40f87-139">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-140">NotEquals: löst</span><span class="sxs-lookup"><span data-stu-id="40f87-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="40f87-142">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-143">Lika med: plattform, logg analys</span><span class="sxs-lookup"><span data-stu-id="40f87-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="40f87-144">-Name</span></span>
<span data-ttu-id="40f87-145">Namn på åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="40f87-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="40f87-146">-ReccurenceType</span></span>
<span data-ttu-id="40f87-147">Anger hur länge undersökning ska göras.</span><span class="sxs-lookup"><span data-stu-id="40f87-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="40f87-148">-ReccurentValue</span></span>
<span data-ttu-id="40f87-149">Reccurent-värden, om tillämpligt. För varje vecka – \[ 1, \] 3 för varje månad- \[ 1,3\]</span><span class="sxs-lookup"><span data-stu-id="40f87-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f87-150">-ResourceGroupName</span></span>
<span data-ttu-id="40f87-151">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="40f87-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-152">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="40f87-152">-Scope</span></span>
<span data-ttu-id="40f87-153">Kommaseparerad lista med värden</span><span class="sxs-lookup"><span data-stu-id="40f87-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-154">-SeverityCondition</span></span>
<span data-ttu-id="40f87-155">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-156">Är lika med: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="40f87-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-157">-Status</span><span class="sxs-lookup"><span data-stu-id="40f87-157">-Status</span></span>
<span data-ttu-id="40f87-158">Status för åtgärds regel.</span><span class="sxs-lookup"><span data-stu-id="40f87-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="40f87-159">-SuppressionEndTime</span></span>
<span data-ttu-id="40f87-160">Undertrycks slut tid.</span><span class="sxs-lookup"><span data-stu-id="40f87-160">Suppression End Time.</span></span>
<span data-ttu-id="40f87-161">Format 12/09/2018 06:00:00 + bör nämnas i händelse av Reccurent Supression schema-en gång, varje dag, varje vecka eller varje månad.</span><span class="sxs-lookup"><span data-stu-id="40f87-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="40f87-162">-SuppressionStartTime</span></span>
<span data-ttu-id="40f87-163">Undertrycks starts tiden.</span><span class="sxs-lookup"><span data-stu-id="40f87-163">Suppression Start Time.</span></span>
<span data-ttu-id="40f87-164">Format 12/09/2018 06:00:00 + bör nämnas i händelse av Reccurent Supression schema-en gång, varje dag, varje vecka eller varje månad.</span><span class="sxs-lookup"><span data-stu-id="40f87-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="40f87-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="40f87-166">Förväntat format-{ \< åtgärd \> : \< kommaavgränsad lista med värden \> } till exempel.</span><span class="sxs-lookup"><span data-stu-id="40f87-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="40f87-167">Innehåller: virtuella datorer, lagrings konto</span><span class="sxs-lookup"><span data-stu-id="40f87-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f87-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40f87-168">-Confirm</span></span>
<span data-ttu-id="40f87-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40f87-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f87-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f87-170">-WhatIf</span></span>
<span data-ttu-id="40f87-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40f87-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40f87-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40f87-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f87-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f87-173">CommonParameters</span></span>
<span data-ttu-id="40f87-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40f87-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f87-175">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40f87-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f87-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40f87-176">INPUTS</span></span>

### <span data-ttu-id="40f87-177">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="40f87-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="40f87-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40f87-178">OUTPUTS</span></span>

### <span data-ttu-id="40f87-179">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="40f87-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="40f87-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40f87-180">NOTES</span></span>

## <span data-ttu-id="40f87-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40f87-181">RELATED LINKS</span></span>
