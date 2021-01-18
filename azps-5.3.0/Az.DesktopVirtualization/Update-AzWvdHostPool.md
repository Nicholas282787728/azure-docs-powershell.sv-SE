---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523703"
---
# <span data-ttu-id="60d6b-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="60d6b-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="60d6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="60d6b-103">Uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-103">Update a host pool.</span></span>

## <span data-ttu-id="60d6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60d6b-104">SYNTAX</span></span>

### <span data-ttu-id="60d6b-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="60d6b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="60d6b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="60d6b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="60d6b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60d6b-107">DESCRIPTION</span></span>
<span data-ttu-id="60d6b-108">Uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-108">Update a host pool.</span></span>

## <span data-ttu-id="60d6b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60d6b-109">EXAMPLES</span></span>

### <span data-ttu-id="60d6b-110">Exempel 1: uppdatera en Windows Virtual Desktop-HostPool efter namn</span><span class="sxs-lookup"><span data-stu-id="60d6b-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="60d6b-111">Det här kommandot uppdaterar en Windows Virtual Desktop-HostPool i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="60d6b-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="60d6b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60d6b-112">PARAMETERS</span></span>

### <span data-ttu-id="60d6b-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="60d6b-113">-CustomRdpProperty</span></span>
<span data-ttu-id="60d6b-114">Anpassad RDP-egenskap för HostPool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="60d6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d6b-115">-DefaultProfile</span></span>
<span data-ttu-id="60d6b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60d6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60d6b-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="60d6b-117">-Description</span></span>
<span data-ttu-id="60d6b-118">Beskrivning av HostPool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="60d6b-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="60d6b-119">-FriendlyName</span></span>
<span data-ttu-id="60d6b-120">Eget namn på HostPool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="60d6b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60d6b-121">-InputObject</span></span>
<span data-ttu-id="60d6b-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="60d6b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60d6b-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="60d6b-123">-LoadBalancerType</span></span>
<span data-ttu-id="60d6b-124">Typen av belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="60d6b-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="60d6b-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="60d6b-125">-MaxSessionLimit</span></span>
<span data-ttu-id="60d6b-126">Maximal sessionsgräns för HostPool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="60d6b-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="60d6b-127">-Name</span></span>
<span data-ttu-id="60d6b-128">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="60d6b-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="60d6b-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="60d6b-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="60d6b-130">PersonalDesktopAssignment typ för HostPool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="60d6b-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="60d6b-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="60d6b-132">Typen av grupp för önskat program, standard för Skriv bords program grupp</span><span class="sxs-lookup"><span data-stu-id="60d6b-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="60d6b-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="60d6b-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="60d6b-134">Upphört att gälla.</span><span class="sxs-lookup"><span data-stu-id="60d6b-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="60d6b-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="60d6b-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="60d6b-136">Typen av ominställning av token.</span><span class="sxs-lookup"><span data-stu-id="60d6b-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="60d6b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d6b-137">-ResourceGroupName</span></span>
<span data-ttu-id="60d6b-138">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="60d6b-138">The name of the resource group.</span></span>
<span data-ttu-id="60d6b-139">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="60d6b-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="60d6b-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="60d6b-140">-Ring</span></span>
<span data-ttu-id="60d6b-141">Ring numret för HostPool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="60d6b-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="60d6b-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="60d6b-143">URL till Customer ADFS Server för att signera WVD SSO-certifikat.</span><span class="sxs-lookup"><span data-stu-id="60d6b-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="60d6b-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="60d6b-144">-SsoClientId</span></span>
<span data-ttu-id="60d6b-145">ClientId för den registrerade förlitande parten som används för att utfärda WVD SSO-certifikat.</span><span class="sxs-lookup"><span data-stu-id="60d6b-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="60d6b-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="60d6b-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="60d6b-147">Sökväg till Azure-nyckel valv lagrar den hemlighet som används för kommunikation till AD FS.</span><span class="sxs-lookup"><span data-stu-id="60d6b-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="60d6b-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="60d6b-148">-SsoContext</span></span>
<span data-ttu-id="60d6b-149">Sökväg till nyckel valv som innehåller ssoContext-hemlighet.</span><span class="sxs-lookup"><span data-stu-id="60d6b-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="60d6b-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="60d6b-150">-SsoSecretType</span></span>
<span data-ttu-id="60d6b-151">Typen av enkel inloggnings typ.</span><span class="sxs-lookup"><span data-stu-id="60d6b-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d6b-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="60d6b-152">-StartVMOnConnect</span></span>
<span data-ttu-id="60d6b-153">Flaggan för att aktivera/inaktivera StartVMOnConnect funktionen.</span><span class="sxs-lookup"><span data-stu-id="60d6b-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="60d6b-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60d6b-154">-SubscriptionId</span></span>
<span data-ttu-id="60d6b-155">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="60d6b-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="60d6b-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="60d6b-156">-Tag</span></span>
<span data-ttu-id="60d6b-157">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="60d6b-157">tags to be updated</span></span>

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

### <span data-ttu-id="60d6b-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="60d6b-158">-ValidationEnvironment</span></span>
<span data-ttu-id="60d6b-159">Är verifierings miljö.</span><span class="sxs-lookup"><span data-stu-id="60d6b-159">Is validation environment.</span></span>

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

### <span data-ttu-id="60d6b-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="60d6b-160">-VMTemplate</span></span>
<span data-ttu-id="60d6b-161">Mall för virtuell dator för sessionhosts konfiguration i hostpool.</span><span class="sxs-lookup"><span data-stu-id="60d6b-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="60d6b-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60d6b-162">-Confirm</span></span>
<span data-ttu-id="60d6b-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60d6b-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60d6b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60d6b-164">-WhatIf</span></span>
<span data-ttu-id="60d6b-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60d6b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60d6b-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60d6b-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60d6b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d6b-167">CommonParameters</span></span>
<span data-ttu-id="60d6b-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d6b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d6b-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60d6b-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d6b-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60d6b-170">INPUTS</span></span>

### <span data-ttu-id="60d6b-171">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="60d6b-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="60d6b-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60d6b-172">OUTPUTS</span></span>

### <span data-ttu-id="60d6b-173">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="60d6b-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="60d6b-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60d6b-174">NOTES</span></span>

<span data-ttu-id="60d6b-175">ALIAS</span><span class="sxs-lookup"><span data-stu-id="60d6b-175">ALIASES</span></span>

<span data-ttu-id="60d6b-176">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="60d6b-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60d6b-177">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="60d6b-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60d6b-178">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60d6b-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60d6b-179">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="60d6b-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60d6b-180">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="60d6b-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="60d6b-181">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="60d6b-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="60d6b-182">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="60d6b-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="60d6b-183">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="60d6b-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="60d6b-184">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="60d6b-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60d6b-185">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="60d6b-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="60d6b-186">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="60d6b-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="60d6b-187">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="60d6b-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="60d6b-188">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="60d6b-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="60d6b-189">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="60d6b-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="60d6b-190">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="60d6b-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="60d6b-191">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="60d6b-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="60d6b-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60d6b-192">RELATED LINKS</span></span>

