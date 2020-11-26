---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272630"
---
# <span data-ttu-id="5bd2a-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="5bd2a-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="5bd2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd2a-103">Uppdatera taggarna för en lösning.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="5bd2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bd2a-104">SYNTAX</span></span>

### <span data-ttu-id="5bd2a-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="5bd2a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5bd2a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5bd2a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5bd2a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bd2a-107">DESCRIPTION</span></span>
<span data-ttu-id="5bd2a-108">Uppdatera taggarna för en lösning.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="5bd2a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bd2a-109">EXAMPLES</span></span>

### <span data-ttu-id="5bd2a-110">Exempel 1: uppdatera en monitor logganalys-lösning efter namn</span><span class="sxs-lookup"><span data-stu-id="5bd2a-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="5bd2a-111">Det här kommandot uppdaterar en övervakarens logg analys med namn.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="5bd2a-112">Exempel 2: uppdatera en Monitoring Analytics-lösning efter objekt</span><span class="sxs-lookup"><span data-stu-id="5bd2a-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="5bd2a-113">Det här kommandot uppdaterar en övervaka logg analys med objekt.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="5bd2a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bd2a-114">PARAMETERS</span></span>

### <span data-ttu-id="5bd2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd2a-115">-DefaultProfile</span></span>
<span data-ttu-id="5bd2a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd2a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bd2a-117">-InputObject</span></span>
<span data-ttu-id="5bd2a-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd2a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5bd2a-119">-Name</span></span>
<span data-ttu-id="5bd2a-120">Namn på användar lösning.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd2a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd2a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bd2a-122">Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-122">The name of the resource group to get.</span></span>
<span data-ttu-id="5bd2a-123">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd2a-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5bd2a-124">-SubscriptionId</span></span>
<span data-ttu-id="5bd2a-125">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5bd2a-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd2a-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5bd2a-127">-Tag</span></span>
<span data-ttu-id="5bd2a-128">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="5bd2a-128">Resource tags</span></span>

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

### <span data-ttu-id="5bd2a-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5bd2a-129">-Confirm</span></span>
<span data-ttu-id="5bd2a-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd2a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd2a-131">-WhatIf</span></span>
<span data-ttu-id="5bd2a-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd2a-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd2a-134">CommonParameters</span></span>
<span data-ttu-id="5bd2a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd2a-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bd2a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd2a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bd2a-137">INPUTS</span></span>

### <span data-ttu-id="5bd2a-138">Microsoft. Azure. PowerShell. cmdletar. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="5bd2a-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="5bd2a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bd2a-139">OUTPUTS</span></span>

### <span data-ttu-id="5bd2a-140">Microsoft. Azure. PowerShell. cmdletar. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="5bd2a-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="5bd2a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bd2a-141">NOTES</span></span>

<span data-ttu-id="5bd2a-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5bd2a-142">ALIASES</span></span>

<span data-ttu-id="5bd2a-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5bd2a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5bd2a-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5bd2a-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5bd2a-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5bd2a-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5bd2a-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5bd2a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5bd2a-148">`[ManagementAssociationName <String>]`: Användar namnet ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="5bd2a-149">`[ManagementConfigurationName <String>]`: Konfigurations namn för användar hantering.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="5bd2a-150">`[ProviderName <String>]`: Leverantörens namn för den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="5bd2a-151">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="5bd2a-152">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="5bd2a-153">`[ResourceName <String>]`: Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="5bd2a-154">`[ResourceType <String>]`: Resurs typ för den överordnade resursen</span><span class="sxs-lookup"><span data-stu-id="5bd2a-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="5bd2a-155">`[SolutionName <String>]`: Användar lösningens namn.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="5bd2a-156">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5bd2a-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5bd2a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5bd2a-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bd2a-158">RELATED LINKS</span></span>
