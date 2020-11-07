---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 3c0178ebae2237730d7f0d11eb832a30988ffdb4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924389"
---
# <span data-ttu-id="76f7c-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="76f7c-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="76f7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="76f7c-103">Lägger till eller uppdaterar en v2-baserad notifieringsregel (icke-klassiskt).</span><span class="sxs-lookup"><span data-stu-id="76f7c-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="76f7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76f7c-104">SYNTAX</span></span>

### <span data-ttu-id="76f7c-105">CreateAlertByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="76f7c-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f7c-106">CreateAlertByResourceIdAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="76f7c-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f7c-107">CreateAlertByResourceIdAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="76f7c-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f7c-108">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="76f7c-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f7c-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="76f7c-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f7c-110">CreateAlertByScopesAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="76f7c-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76f7c-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76f7c-111">DESCRIPTION</span></span>
<span data-ttu-id="76f7c-112">Lägger till eller uppdaterar en **v2-baserad notifieringsregel (icke-klassiskt)**.</span><span class="sxs-lookup"><span data-stu-id="76f7c-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="76f7c-113">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="76f7c-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="76f7c-114">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="76f7c-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="76f7c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76f7c-115">EXAMPLES</span></span>

### <span data-ttu-id="76f7c-116">Exempel 1: lägga till en regel för att varna på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="76f7c-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="76f7c-117">Det här kommandot skapar en regel för att varna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="76f7c-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="76f7c-118">$condition är utdata från New-AzMetricAlertRuleV2Criteria cmdlet och $act är utdata från New-AzActionGroup cmdlet</span><span class="sxs-lookup"><span data-stu-id="76f7c-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="76f7c-119">Exempel 2: lägga till en regel för notifieringsregler för alla virtuella datorer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="76f7c-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="76f7c-120">Det här kommandot skapar en metrisk varnings regel för alla virtuella datorer i prenumerationen som är i öster</span><span class="sxs-lookup"><span data-stu-id="76f7c-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="76f7c-121">Exempel 3: inaktivera en regel för att varna</span><span class="sxs-lookup"><span data-stu-id="76f7c-121">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="76f7c-122">Det här kommandot inaktiverar en regel för metrisk avisering.</span><span class="sxs-lookup"><span data-stu-id="76f7c-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="76f7c-123">Här tar vi ledningar för Get-AzMetricAlertRuleV2 till Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="76f7c-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="76f7c-124">Exempel 4: Lägg till en regel för att varna med dimensioner</span><span class="sxs-lookup"><span data-stu-id="76f7c-124">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="76f7c-125">Om du vill skapa en mer komplex varnings regel som de som innefattar att välja dimensions värden eller ha flera villkor kan du använda cmdletarna New-AzMetricAlertRuleV2DimensionSelection och New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="76f7c-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="76f7c-126">Ovanstående uppsättning cmdletar skapar en regel för metriska varningar med dimensioner.</span><span class="sxs-lookup"><span data-stu-id="76f7c-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="76f7c-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76f7c-127">PARAMETERS</span></span>

### <span data-ttu-id="76f7c-128">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="76f7c-128">-ActionGroup</span></span>
<span data-ttu-id="76f7c-129">Åtgärds gruppen för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-130">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="76f7c-130">-ActionGroupId</span></span>
<span data-ttu-id="76f7c-131">Åtgärds grupp-ID för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-132">-Villkor</span><span class="sxs-lookup"><span data-stu-id="76f7c-132">-Condition</span></span>
<span data-ttu-id="76f7c-133">Villkor för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-133">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f7c-134">-DefaultProfile</span></span>
<span data-ttu-id="76f7c-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76f7c-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f7c-136">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="76f7c-136">-Description</span></span>
<span data-ttu-id="76f7c-137">Beskrivning av varnings regeln för metriska enheter</span><span class="sxs-lookup"><span data-stu-id="76f7c-137">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="76f7c-138">-DisableRule</span></span>
<span data-ttu-id="76f7c-139">Flaggan Disable Rule (status)</span><span class="sxs-lookup"><span data-stu-id="76f7c-139">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-140">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="76f7c-140">-Frequency</span></span>
<span data-ttu-id="76f7c-141">Utvärderings frekvens för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-141">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="76f7c-142">-Name</span></span>
<span data-ttu-id="76f7c-143">Namnet på varnings regeln för mått</span><span class="sxs-lookup"><span data-stu-id="76f7c-143">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f7c-144">-ResourceGroupName</span></span>
<span data-ttu-id="76f7c-145">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="76f7c-145">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-146">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="76f7c-146">-Severity</span></span>
<span data-ttu-id="76f7c-147">Allvarlighets graden för Metric-varningen</span><span class="sxs-lookup"><span data-stu-id="76f7c-147">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="76f7c-148">-TargetResourceId</span></span>
<span data-ttu-id="76f7c-149">Mål resurs-ID för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="76f7c-150">-TargetResourceRegion</span></span>
<span data-ttu-id="76f7c-151">Mål resurs region för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="76f7c-152">-TargetResourceScope</span></span>
<span data-ttu-id="76f7c-153">Mål resurs omfattning för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="76f7c-154">-TargetResourceType</span></span>
<span data-ttu-id="76f7c-155">Mål resurs typen för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-156">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="76f7c-156">-WindowSize</span></span>
<span data-ttu-id="76f7c-157">Fönster storlek för regel</span><span class="sxs-lookup"><span data-stu-id="76f7c-157">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f7c-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76f7c-158">-Confirm</span></span>
<span data-ttu-id="76f7c-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76f7c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f7c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f7c-160">-WhatIf</span></span>
<span data-ttu-id="76f7c-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76f7c-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f7c-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76f7c-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f7c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f7c-163">CommonParameters</span></span>
<span data-ttu-id="76f7c-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f7c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f7c-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76f7c-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f7c-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76f7c-166">INPUTS</span></span>

### <span data-ttu-id="76f7c-167">System. String</span><span class="sxs-lookup"><span data-stu-id="76f7c-167">System.String</span></span>

### <span data-ttu-id="76f7c-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="76f7c-168">System.TimeSpan</span></span>

### <span data-ttu-id="76f7c-169">System. string []</span><span class="sxs-lookup"><span data-stu-id="76f7c-169">System.String[]</span></span>

### <span data-ttu-id="76f7c-170">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="76f7c-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="76f7c-171">Microsoft. Azure. Management. Monitoring. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="76f7c-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="76f7c-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76f7c-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="76f7c-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="76f7c-173">System.Int32</span></span>

## <span data-ttu-id="76f7c-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76f7c-174">OUTPUTS</span></span>

### <span data-ttu-id="76f7c-175">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="76f7c-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="76f7c-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76f7c-176">NOTES</span></span>

## <span data-ttu-id="76f7c-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76f7c-177">RELATED LINKS</span></span>
