---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 17be83253d452b4c347154f8c0e392277287d0b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915709"
---
# <span data-ttu-id="a57d6-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a57d6-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="a57d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a57d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a57d6-103">Lägger till eller uppdaterar en v2-baserad notifieringsregel (icke-klassiskt).</span><span class="sxs-lookup"><span data-stu-id="a57d6-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="a57d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a57d6-104">SYNTAX</span></span>

### <span data-ttu-id="a57d6-105">CreateAlertByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="a57d6-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57d6-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="a57d6-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57d6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a57d6-107">DESCRIPTION</span></span>
<span data-ttu-id="a57d6-108">Lägger till eller uppdaterar en **v2-baserad notifieringsregel (icke-klassiskt)**.</span><span class="sxs-lookup"><span data-stu-id="a57d6-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="a57d6-109">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="a57d6-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="a57d6-110">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="a57d6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a57d6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a57d6-111">EXAMPLES</span></span>

### <span data-ttu-id="a57d6-112">Exempel 1: lägga till en regel för att varna på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a57d6-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="a57d6-113">Det här kommandot skapar en regel för att varna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a57d6-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="a57d6-114">$condition är utdata från New-AzMetricAlertRuleV2Criteria cmdlet och $act är utdata från New-AzActionGroup cmdlet</span><span class="sxs-lookup"><span data-stu-id="a57d6-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="a57d6-115">Exempel 2: lägga till en regel för notifieringsregler för alla virtuella datorer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="a57d6-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="a57d6-116">Det här kommandot skapar en metrisk varnings regel för alla virtuella datorer i prenumerationen som är i öster</span><span class="sxs-lookup"><span data-stu-id="a57d6-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="a57d6-117">Exempel 3: inaktivera en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="a57d6-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="a57d6-118">Det här kommandot inaktiverar en regel för metrisk avisering.</span><span class="sxs-lookup"><span data-stu-id="a57d6-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="a57d6-119">Här tar vi ledningar för Get-AzMetricAlertRuleV2 till Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a57d6-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="a57d6-120">Exempel 4: Lägg till en regel för att varna med dimensioner</span><span class="sxs-lookup"><span data-stu-id="a57d6-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :

```

<span data-ttu-id="a57d6-121">Om du vill skapa en mer komplex varnings regel som de som innefattar att välja dimensions värden eller ha flera villkor kan du använda cmdletarna New-AzMetricAlertRuleV2DimensionSelection och New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="a57d6-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="a57d6-122">Ovanstående uppsättning cmdletar skapar en regel för metriska varningar med dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a57d6-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>
## <span data-ttu-id="a57d6-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a57d6-123">PARAMETERS</span></span>

### <span data-ttu-id="a57d6-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="a57d6-124">-ActionGroup</span></span>
<span data-ttu-id="a57d6-125">Åtgärds gruppen för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-125">The Action Group for rule</span></span>

```yaml
Type: ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-126">-Villkor</span><span class="sxs-lookup"><span data-stu-id="a57d6-126">-Condition</span></span>
<span data-ttu-id="a57d6-127">Villkor för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-127">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a57d6-128">-Confirm</span></span>
<span data-ttu-id="a57d6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a57d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57d6-130">-DefaultProfile</span></span>
<span data-ttu-id="a57d6-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a57d6-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57d6-132">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a57d6-132">-Description</span></span>
<span data-ttu-id="a57d6-133">Beskrivning av varnings regeln för metriska enheter</span><span class="sxs-lookup"><span data-stu-id="a57d6-133">The description of the metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="a57d6-134">-DisableRule</span></span>
<span data-ttu-id="a57d6-135">Flaggan Disable Rule (status)</span><span class="sxs-lookup"><span data-stu-id="a57d6-135">The disable rule (status) flag</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-136">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="a57d6-136">-Frequency</span></span>
<span data-ttu-id="a57d6-137">Utvärderings frekvens för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-137">The evaluation frequency for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="a57d6-138">-Name</span></span>
<span data-ttu-id="a57d6-139">Namnet på varnings regeln för mått</span><span class="sxs-lookup"><span data-stu-id="a57d6-139">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57d6-140">-ResourceGroupName</span></span>
<span data-ttu-id="a57d6-141">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="a57d6-141">The Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-142">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="a57d6-142">-Severity</span></span>
<span data-ttu-id="a57d6-143">Allvarlighets graden för Metric-varningen</span><span class="sxs-lookup"><span data-stu-id="a57d6-143">The severity for the metric alert rule</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a57d6-144">-TargetResourceId</span></span>
<span data-ttu-id="a57d6-145">Mål resurs-ID för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-145">The target resource id for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="a57d6-146">-TargetResourceRegion</span></span>
<span data-ttu-id="a57d6-147">Mål resurs region för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-147">The target resource region for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="a57d6-148">-TargetResourceScope</span></span>
<span data-ttu-id="a57d6-149">Mål resurs omfattning för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-149">The target resource scope for rule</span></span>

```yaml
Type: String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="a57d6-150">-TargetResourceType</span></span>
<span data-ttu-id="a57d6-151">Mål resurs typen för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-151">The target resource type for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57d6-152">-WhatIf</span></span>
<span data-ttu-id="a57d6-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a57d6-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57d6-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a57d6-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-155">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="a57d6-155">-WindowSize</span></span>
<span data-ttu-id="a57d6-156">Fönster storlek för regel</span><span class="sxs-lookup"><span data-stu-id="a57d6-156">The window size for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57d6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57d6-157">CommonParameters</span></span>
<span data-ttu-id="a57d6-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57d6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a57d6-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57d6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57d6-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a57d6-160">INPUTS</span></span>

### <span data-ttu-id="a57d6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a57d6-161">System.String</span></span>

### <span data-ttu-id="a57d6-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="a57d6-162">System.TimeSpan</span></span>

### <span data-ttu-id="a57d6-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="a57d6-163">System.String[]</span></span>

### <span data-ttu-id="a57d6-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Insights. OutputClasses. PSMetricCriteria, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a57d6-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a57d6-165">Microsoft. Azure. Management. Monitoring. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="a57d6-165">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="a57d6-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a57d6-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a57d6-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a57d6-167">System.Int32</span></span>

## <span data-ttu-id="a57d6-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a57d6-168">OUTPUTS</span></span>

### <span data-ttu-id="a57d6-169">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a57d6-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="a57d6-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a57d6-170">NOTES</span></span>

## <span data-ttu-id="a57d6-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a57d6-171">RELATED LINKS</span></span>