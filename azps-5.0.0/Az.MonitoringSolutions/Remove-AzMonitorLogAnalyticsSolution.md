---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272631"
---
# <span data-ttu-id="781f2-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="781f2-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="781f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="781f2-102">SYNOPSIS</span></span>
<span data-ttu-id="781f2-103">Tar bort lösningen i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="781f2-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="781f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="781f2-104">SYNTAX</span></span>

### <span data-ttu-id="781f2-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="781f2-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="781f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="781f2-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="781f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="781f2-107">DESCRIPTION</span></span>
<span data-ttu-id="781f2-108">Tar bort lösningen i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="781f2-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="781f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="781f2-109">EXAMPLES</span></span>

### <span data-ttu-id="781f2-110">Exempel 1: ta bort en övervaka logganalys-lösning efter namn</span><span class="sxs-lookup"><span data-stu-id="781f2-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="781f2-111">Det här kommandot tar bort en övervaka logganalys-lösning efter namn.</span><span class="sxs-lookup"><span data-stu-id="781f2-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="781f2-112">Exempel 2: ta bort en övervaka logganalys-lösning efter objekt</span><span class="sxs-lookup"><span data-stu-id="781f2-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="781f2-113">Det här kommandot tar bort en övervaka logg analys med objekt.</span><span class="sxs-lookup"><span data-stu-id="781f2-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="781f2-114">Exempel 3: ta bort en monitor logganalys-lösning via pipeline</span><span class="sxs-lookup"><span data-stu-id="781f2-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="781f2-115">Det här kommandot tar bort en övervaka logg analys.</span><span class="sxs-lookup"><span data-stu-id="781f2-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="781f2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="781f2-116">PARAMETERS</span></span>

### <span data-ttu-id="781f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781f2-117">-DefaultProfile</span></span>
<span data-ttu-id="781f2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="781f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="781f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="781f2-119">-InputObject</span></span>
<span data-ttu-id="781f2-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="781f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="781f2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="781f2-121">-Name</span></span>
<span data-ttu-id="781f2-122">Namn på användar lösning.</span><span class="sxs-lookup"><span data-stu-id="781f2-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781f2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="781f2-123">-PassThru</span></span>
<span data-ttu-id="781f2-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="781f2-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="781f2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781f2-125">-ResourceGroupName</span></span>
<span data-ttu-id="781f2-126">Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="781f2-126">The name of the resource group to get.</span></span>
<span data-ttu-id="781f2-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="781f2-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781f2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="781f2-128">-SubscriptionId</span></span>
<span data-ttu-id="781f2-129">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="781f2-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="781f2-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="781f2-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781f2-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="781f2-131">-Confirm</span></span>
<span data-ttu-id="781f2-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="781f2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="781f2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="781f2-133">-WhatIf</span></span>
<span data-ttu-id="781f2-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="781f2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="781f2-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="781f2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="781f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781f2-136">CommonParameters</span></span>
<span data-ttu-id="781f2-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="781f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781f2-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="781f2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781f2-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="781f2-139">INPUTS</span></span>

### <span data-ttu-id="781f2-140">Microsoft. Azure. PowerShell. cmdletar. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="781f2-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="781f2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="781f2-141">OUTPUTS</span></span>

### <span data-ttu-id="781f2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="781f2-142">System.Boolean</span></span>

## <span data-ttu-id="781f2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="781f2-143">NOTES</span></span>

<span data-ttu-id="781f2-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="781f2-144">ALIASES</span></span>

<span data-ttu-id="781f2-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="781f2-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="781f2-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="781f2-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="781f2-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="781f2-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="781f2-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="781f2-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="781f2-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="781f2-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="781f2-150">`[ManagementAssociationName <String>]`: Användar namnet ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="781f2-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="781f2-151">`[ManagementConfigurationName <String>]`: Konfigurations namn för användar hantering.</span><span class="sxs-lookup"><span data-stu-id="781f2-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="781f2-152">`[ProviderName <String>]`: Leverantörens namn för den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="781f2-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="781f2-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="781f2-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="781f2-154">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="781f2-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="781f2-155">`[ResourceName <String>]`: Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="781f2-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="781f2-156">`[ResourceType <String>]`: Resurs typ för den överordnade resursen</span><span class="sxs-lookup"><span data-stu-id="781f2-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="781f2-157">`[SolutionName <String>]`: Användar lösningens namn.</span><span class="sxs-lookup"><span data-stu-id="781f2-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="781f2-158">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="781f2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="781f2-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="781f2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="781f2-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="781f2-160">RELATED LINKS</span></span>
