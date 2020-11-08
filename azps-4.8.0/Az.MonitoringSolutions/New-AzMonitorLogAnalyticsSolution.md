---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259510"
---
# <span data-ttu-id="4666e-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="4666e-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="4666e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4666e-102">SYNOPSIS</span></span>
<span data-ttu-id="4666e-103">Skapar en logganalys-lösning.</span><span class="sxs-lookup"><span data-stu-id="4666e-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="4666e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4666e-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4666e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4666e-105">DESCRIPTION</span></span>
<span data-ttu-id="4666e-106">Skapar en logganalys-lösning.</span><span class="sxs-lookup"><span data-stu-id="4666e-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="4666e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4666e-107">EXAMPLES</span></span>

### <span data-ttu-id="4666e-108">Exempel 1: skapa en övervaka logganalys-lösning för logganalys-arbetsytan</span><span class="sxs-lookup"><span data-stu-id="4666e-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="4666e-109">Med det här kommandot skapas en monitor-lösning för logganalys-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="4666e-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="4666e-110">Vanliga typer är:</span><span class="sxs-lookup"><span data-stu-id="4666e-110">Commonly used types are:</span></span>

| <span data-ttu-id="4666e-111">Format</span><span class="sxs-lookup"><span data-stu-id="4666e-111">Type</span></span> | <span data-ttu-id="4666e-112">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="4666e-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="4666e-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="4666e-113">SecurityCenterFree</span></span> |  <span data-ttu-id="4666e-114">Azure Security Center – gratis version</span><span class="sxs-lookup"><span data-stu-id="4666e-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="4666e-115">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="4666e-115">Security</span></span> | <span data-ttu-id="4666e-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="4666e-116">Azure Security Center</span></span> |
| <span data-ttu-id="4666e-117">Updates</span><span class="sxs-lookup"><span data-stu-id="4666e-117">Updates</span></span> | <span data-ttu-id="4666e-118">Uppdaterings hantering</span><span class="sxs-lookup"><span data-stu-id="4666e-118">Update Management</span></span> |
| <span data-ttu-id="4666e-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="4666e-119">ContainerInsights</span></span> | <span data-ttu-id="4666e-120">Azure Monitor för behållare</span><span class="sxs-lookup"><span data-stu-id="4666e-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="4666e-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="4666e-121">ServiceMap</span></span> | <span data-ttu-id="4666e-122">Tjänst karta</span><span class="sxs-lookup"><span data-stu-id="4666e-122">Service Map</span></span> |
| <span data-ttu-id="4666e-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="4666e-123">AzureActivity</span></span> | <span data-ttu-id="4666e-124">Aktivitets logg analys</span><span class="sxs-lookup"><span data-stu-id="4666e-124">Activity log analytics</span></span> |
| <span data-ttu-id="4666e-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="4666e-125">ChangeTracking</span></span> | <span data-ttu-id="4666e-126">Spåra ändringar och lager</span><span class="sxs-lookup"><span data-stu-id="4666e-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="4666e-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="4666e-127">VMInsights</span></span> | <span data-ttu-id="4666e-128">Azure Monitor för virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="4666e-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="4666e-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="4666e-129">SecurityInsights</span></span> | <span data-ttu-id="4666e-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="4666e-130">Azure Sentinel</span></span> |
| <span data-ttu-id="4666e-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="4666e-131">NetworkMonitoring</span></span> | <span data-ttu-id="4666e-132">Övervakaren för nätverks prestanda</span><span class="sxs-lookup"><span data-stu-id="4666e-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="4666e-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="4666e-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="4666e-134">Utvärdering av SQL-sårbarhet</span><span class="sxs-lookup"><span data-stu-id="4666e-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="4666e-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4666e-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="4666e-136">Avancerat skydd för SQL</span><span class="sxs-lookup"><span data-stu-id="4666e-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="4666e-137">Antimalware</span><span class="sxs-lookup"><span data-stu-id="4666e-137">AntiMalware</span></span> | <span data-ttu-id="4666e-138">Utvärdering mot skadlig program vara</span><span class="sxs-lookup"><span data-stu-id="4666e-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="4666e-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="4666e-139">AzureAutomation</span></span> | <span data-ttu-id="4666e-140">Automatiserings hybrid arbetare</span><span class="sxs-lookup"><span data-stu-id="4666e-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="4666e-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="4666e-141">LogicAppsManagement</span></span> | <span data-ttu-id="4666e-142">Hantering av logiska appar</span><span class="sxs-lookup"><span data-stu-id="4666e-142">Logic Apps Management</span></span> |
| <span data-ttu-id="4666e-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="4666e-143">SQLDataClassification</span></span> | <span data-ttu-id="4666e-144">& klassificering av SQL-dataidentifiering</span><span class="sxs-lookup"><span data-stu-id="4666e-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="4666e-145">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4666e-145">PARAMETERS</span></span>

### <span data-ttu-id="4666e-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4666e-146">-DefaultProfile</span></span>
<span data-ttu-id="4666e-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4666e-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4666e-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="4666e-148">-Location</span></span>
<span data-ttu-id="4666e-149">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="4666e-149">Resource location.</span></span>
<span data-ttu-id="4666e-150">Måste vara samma som den analytiska arbets ytan för logg analys.</span><span class="sxs-lookup"><span data-stu-id="4666e-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="4666e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4666e-151">-ResourceGroupName</span></span>
<span data-ttu-id="4666e-152">Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4666e-152">The name of the resource group to get.</span></span>
<span data-ttu-id="4666e-153">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4666e-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4666e-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4666e-154">-SubscriptionId</span></span>
<span data-ttu-id="4666e-155">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4666e-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4666e-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4666e-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4666e-157">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4666e-157">-Tag</span></span>
<span data-ttu-id="4666e-158">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="4666e-158">Resource tags</span></span>

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

### <span data-ttu-id="4666e-159">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4666e-159">-Type</span></span>
<span data-ttu-id="4666e-160">Typ av lösning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4666e-160">Type of the solution to be created.</span></span>
<span data-ttu-id="4666e-161">Till exempel "container".</span><span class="sxs-lookup"><span data-stu-id="4666e-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4666e-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="4666e-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="4666e-163">Azure Resource ID för arbets ytan där lösningen distribueras/aktive ras.</span><span class="sxs-lookup"><span data-stu-id="4666e-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="4666e-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4666e-164">-Confirm</span></span>
<span data-ttu-id="4666e-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4666e-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4666e-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4666e-166">-WhatIf</span></span>
<span data-ttu-id="4666e-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4666e-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4666e-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4666e-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4666e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4666e-169">CommonParameters</span></span>
<span data-ttu-id="4666e-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4666e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4666e-171">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4666e-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4666e-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4666e-172">INPUTS</span></span>

## <span data-ttu-id="4666e-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4666e-173">OUTPUTS</span></span>

### <span data-ttu-id="4666e-174">Microsoft. Azure. PowerShell. cmdletar. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="4666e-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="4666e-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4666e-175">NOTES</span></span>

<span data-ttu-id="4666e-176">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4666e-176">ALIASES</span></span>

## <span data-ttu-id="4666e-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4666e-177">RELATED LINKS</span></span>



[<span data-ttu-id="4666e-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4666e-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

