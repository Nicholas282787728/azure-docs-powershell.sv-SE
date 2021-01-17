---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: a6c7572808184f3c83037932f45d36c7af3ff7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398504"
---
# <span data-ttu-id="5cb24-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="5cb24-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="5cb24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cb24-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb24-103">Uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-103">Update a host pool.</span></span>

## <span data-ttu-id="5cb24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cb24-104">SYNTAX</span></span>

### <span data-ttu-id="5cb24-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="5cb24-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5cb24-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5cb24-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cb24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cb24-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb24-108">Uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-108">Update a host pool.</span></span>

## <span data-ttu-id="5cb24-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cb24-109">EXAMPLES</span></span>

### <span data-ttu-id="5cb24-110">Exempel 1: uppdatera en Windows Virtual Desktop-HostPool efter namn</span><span class="sxs-lookup"><span data-stu-id="5cb24-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="5cb24-111">Det här kommandot uppdaterar en Windows Virtual Desktop-HostPool i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5cb24-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="5cb24-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cb24-112">PARAMETERS</span></span>

### <span data-ttu-id="5cb24-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="5cb24-113">-CustomRdpProperty</span></span>
<span data-ttu-id="5cb24-114">Anpassad RDP-egenskap för HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="5cb24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb24-115">-DefaultProfile</span></span>
<span data-ttu-id="5cb24-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb24-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5cb24-117">-Description</span></span>
<span data-ttu-id="5cb24-118">Beskrivning av HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="5cb24-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5cb24-119">-FriendlyName</span></span>
<span data-ttu-id="5cb24-120">Eget namn på HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="5cb24-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cb24-121">-InputObject</span></span>
<span data-ttu-id="5cb24-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5cb24-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cb24-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="5cb24-123">-LoadBalancerType</span></span>
<span data-ttu-id="5cb24-124">Typen av belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5cb24-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="5cb24-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="5cb24-125">-MaxSessionLimit</span></span>
<span data-ttu-id="5cb24-126">Maximal sessionsgräns för HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="5cb24-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cb24-127">-Name</span></span>
<span data-ttu-id="5cb24-128">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5cb24-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5cb24-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="5cb24-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="5cb24-130">PersonalDesktopAssignment typ för HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="5cb24-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="5cb24-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="5cb24-132">Typen av grupp för önskat program, standard för Skriv bords program grupp</span><span class="sxs-lookup"><span data-stu-id="5cb24-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="5cb24-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="5cb24-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="5cb24-134">Upphört att gälla.</span><span class="sxs-lookup"><span data-stu-id="5cb24-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="5cb24-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="5cb24-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="5cb24-136">Typen av ominställning av token.</span><span class="sxs-lookup"><span data-stu-id="5cb24-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="5cb24-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb24-137">-ResourceGroupName</span></span>
<span data-ttu-id="5cb24-138">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5cb24-138">The name of the resource group.</span></span>
<span data-ttu-id="5cb24-139">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5cb24-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5cb24-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="5cb24-140">-Ring</span></span>
<span data-ttu-id="5cb24-141">Ring numret för HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="5cb24-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="5cb24-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="5cb24-143">URL till Customer ADFS Server för att signera WVD SSO-certifikat.</span><span class="sxs-lookup"><span data-stu-id="5cb24-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="5cb24-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="5cb24-144">-SsoClientId</span></span>
<span data-ttu-id="5cb24-145">ClientId för den registrerade förlitande parten som används för att utfärda WVD SSO-certifikat.</span><span class="sxs-lookup"><span data-stu-id="5cb24-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="5cb24-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="5cb24-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="5cb24-147">Sökväg till Azure-nyckel valv lagrar den hemlighet som används för kommunikation till AD FS.</span><span class="sxs-lookup"><span data-stu-id="5cb24-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="5cb24-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="5cb24-148">-SsoContext</span></span>
<span data-ttu-id="5cb24-149">Sökväg till nyckel valv som innehåller ssoContext-hemlighet.</span><span class="sxs-lookup"><span data-stu-id="5cb24-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="5cb24-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="5cb24-150">-SsoSecretType</span></span>
<span data-ttu-id="5cb24-151">Typen av enkel inloggnings typ.</span><span class="sxs-lookup"><span data-stu-id="5cb24-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="5cb24-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cb24-152">-SubscriptionId</span></span>
<span data-ttu-id="5cb24-153">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5cb24-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5cb24-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5cb24-154">-Tag</span></span>
<span data-ttu-id="5cb24-155">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="5cb24-155">tags to be updated</span></span>

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

### <span data-ttu-id="5cb24-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="5cb24-156">-ValidationEnvironment</span></span>
<span data-ttu-id="5cb24-157">Är verifierings miljö.</span><span class="sxs-lookup"><span data-stu-id="5cb24-157">Is validation environment.</span></span>

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

### <span data-ttu-id="5cb24-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="5cb24-158">-VMTemplate</span></span>
<span data-ttu-id="5cb24-159">Mall för virtuell dator för sessionhosts konfiguration i hostpool.</span><span class="sxs-lookup"><span data-stu-id="5cb24-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="5cb24-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5cb24-160">-Confirm</span></span>
<span data-ttu-id="5cb24-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cb24-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb24-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb24-162">-WhatIf</span></span>
<span data-ttu-id="5cb24-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5cb24-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb24-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5cb24-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb24-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb24-165">CommonParameters</span></span>
<span data-ttu-id="5cb24-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb24-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb24-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cb24-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb24-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cb24-168">INPUTS</span></span>

### <span data-ttu-id="5cb24-169">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5cb24-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5cb24-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cb24-170">OUTPUTS</span></span>

### <span data-ttu-id="5cb24-171">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="5cb24-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="5cb24-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cb24-172">NOTES</span></span>

<span data-ttu-id="5cb24-173">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5cb24-173">ALIASES</span></span>

<span data-ttu-id="5cb24-174">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5cb24-174">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cb24-175">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5cb24-175">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cb24-176">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cb24-176">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cb24-177">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5cb24-177">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cb24-178">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="5cb24-178">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5cb24-179">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="5cb24-179">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5cb24-180">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="5cb24-180">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5cb24-181">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5cb24-181">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5cb24-182">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5cb24-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cb24-183">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="5cb24-183">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5cb24-184">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5cb24-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5cb24-185">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5cb24-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="5cb24-186">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="5cb24-186">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5cb24-187">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="5cb24-187">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5cb24-188">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="5cb24-188">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5cb24-189">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="5cb24-189">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5cb24-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cb24-190">RELATED LINKS</span></span>

