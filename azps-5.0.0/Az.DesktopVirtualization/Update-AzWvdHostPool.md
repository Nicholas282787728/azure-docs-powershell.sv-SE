---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270851"
---
# <span data-ttu-id="212fd-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="212fd-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="212fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="212fd-102">SYNOPSIS</span></span>
<span data-ttu-id="212fd-103">Uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="212fd-103">Update a host pool.</span></span>

## <span data-ttu-id="212fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="212fd-104">SYNTAX</span></span>

### <span data-ttu-id="212fd-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="212fd-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="212fd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="212fd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="212fd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="212fd-107">DESCRIPTION</span></span>
<span data-ttu-id="212fd-108">Uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="212fd-108">Update a host pool.</span></span>

## <span data-ttu-id="212fd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="212fd-109">EXAMPLES</span></span>

### <span data-ttu-id="212fd-110">Exempel 1: uppdatera en Windows Virtual Desktop-HostPool efter namn</span><span class="sxs-lookup"><span data-stu-id="212fd-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="212fd-111">Det här kommandot uppdaterar en Windows Virtual Desktop-HostPool i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="212fd-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="212fd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="212fd-112">PARAMETERS</span></span>

### <span data-ttu-id="212fd-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="212fd-113">-CustomRdpProperty</span></span>
<span data-ttu-id="212fd-114">Anpassad RDP-egenskap för HostPool.</span><span class="sxs-lookup"><span data-stu-id="212fd-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="212fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212fd-115">-DefaultProfile</span></span>
<span data-ttu-id="212fd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="212fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="212fd-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="212fd-117">-Description</span></span>
<span data-ttu-id="212fd-118">Beskrivning av HostPool.</span><span class="sxs-lookup"><span data-stu-id="212fd-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="212fd-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="212fd-119">-FriendlyName</span></span>
<span data-ttu-id="212fd-120">Eget namn på HostPool.</span><span class="sxs-lookup"><span data-stu-id="212fd-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="212fd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="212fd-121">-InputObject</span></span>
<span data-ttu-id="212fd-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="212fd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="212fd-123">-LoadBalancerType</span></span>
<span data-ttu-id="212fd-124">Typen av belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="212fd-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="212fd-125">-MaxSessionLimit</span></span>
<span data-ttu-id="212fd-126">Maximal sessionsgräns för HostPool.</span><span class="sxs-lookup"><span data-stu-id="212fd-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="212fd-127">-Name</span></span>
<span data-ttu-id="212fd-128">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="212fd-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="212fd-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="212fd-130">PersonalDesktopAssignment typ för HostPool.</span><span class="sxs-lookup"><span data-stu-id="212fd-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="212fd-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="212fd-132">Typen av grupp för önskat program, standard för Skriv bords program grupp</span><span class="sxs-lookup"><span data-stu-id="212fd-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="212fd-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="212fd-134">Upphört att gälla.</span><span class="sxs-lookup"><span data-stu-id="212fd-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="212fd-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="212fd-136">Typen av ominställning av token.</span><span class="sxs-lookup"><span data-stu-id="212fd-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212fd-137">-ResourceGroupName</span></span>
<span data-ttu-id="212fd-138">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="212fd-138">The name of the resource group.</span></span>
<span data-ttu-id="212fd-139">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="212fd-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="212fd-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="212fd-140">-Ring</span></span>
<span data-ttu-id="212fd-141">Ring numret för HostPool.</span><span class="sxs-lookup"><span data-stu-id="212fd-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212fd-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="212fd-142">-SsoContext</span></span>
<span data-ttu-id="212fd-143">Sökväg till nyckel valv som innehåller ssoContext-hemlighet.</span><span class="sxs-lookup"><span data-stu-id="212fd-143">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="212fd-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="212fd-144">-SubscriptionId</span></span>
<span data-ttu-id="212fd-145">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="212fd-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="212fd-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="212fd-146">-Tag</span></span>
<span data-ttu-id="212fd-147">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="212fd-147">tags to be updated</span></span>

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

### <span data-ttu-id="212fd-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="212fd-148">-ValidationEnvironment</span></span>
<span data-ttu-id="212fd-149">Är verifierings miljö.</span><span class="sxs-lookup"><span data-stu-id="212fd-149">Is validation environment.</span></span>

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

### <span data-ttu-id="212fd-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="212fd-150">-Confirm</span></span>
<span data-ttu-id="212fd-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="212fd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212fd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212fd-152">-WhatIf</span></span>
<span data-ttu-id="212fd-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="212fd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212fd-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="212fd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="212fd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212fd-155">CommonParameters</span></span>
<span data-ttu-id="212fd-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212fd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212fd-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="212fd-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212fd-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="212fd-158">INPUTS</span></span>

### <span data-ttu-id="212fd-159">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="212fd-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="212fd-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="212fd-160">OUTPUTS</span></span>

### <span data-ttu-id="212fd-161">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="212fd-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="212fd-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="212fd-162">NOTES</span></span>

<span data-ttu-id="212fd-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="212fd-163">ALIASES</span></span>

<span data-ttu-id="212fd-164">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="212fd-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="212fd-165">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="212fd-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="212fd-166">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="212fd-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="212fd-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="212fd-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="212fd-168">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="212fd-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="212fd-169">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="212fd-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="212fd-170">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="212fd-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="212fd-171">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="212fd-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="212fd-172">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="212fd-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="212fd-173">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="212fd-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="212fd-174">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="212fd-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="212fd-175">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="212fd-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="212fd-176">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="212fd-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="212fd-177">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="212fd-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="212fd-178">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="212fd-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="212fd-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="212fd-179">RELATED LINKS</span></span>

