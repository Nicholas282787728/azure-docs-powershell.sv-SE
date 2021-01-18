---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522702"
---
# <span data-ttu-id="da832-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="da832-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="da832-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da832-102">SYNOPSIS</span></span>
<span data-ttu-id="da832-103">Skapa eller uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="da832-103">Create or update a host pool.</span></span>

## <span data-ttu-id="da832-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da832-104">SYNTAX</span></span>

### <span data-ttu-id="da832-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="da832-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da832-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="da832-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da832-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da832-107">DESCRIPTION</span></span>
<span data-ttu-id="da832-108">Skapa eller uppdatera en adresspool.</span><span class="sxs-lookup"><span data-stu-id="da832-108">Create or update a host pool.</span></span>

## <span data-ttu-id="da832-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da832-109">EXAMPLES</span></span>

### <span data-ttu-id="da832-110">Exempel 1: skapa ett virtuellt skriv bord i Windows med ett HostPool</span><span class="sxs-lookup"><span data-stu-id="da832-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="da832-111">Det här kommandot skapar en Windows Virtual Desktop-HostPool i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="da832-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="da832-112">Exempel 1: skapa ett virtuellt skriv bord i Windows med ett HostPool</span><span class="sxs-lookup"><span data-stu-id="da832-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="da832-113">Det här kommandot skapar en Windows Virtual Desktop-HostPool i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="da832-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="da832-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da832-114">PARAMETERS</span></span>

### <span data-ttu-id="da832-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="da832-115">-CustomRdpProperty</span></span>
<span data-ttu-id="da832-116">Anpassad RDP-egenskap för HostPool.</span><span class="sxs-lookup"><span data-stu-id="da832-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da832-117">-DefaultProfile</span></span>
<span data-ttu-id="da832-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da832-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da832-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="da832-119">-Description</span></span>
<span data-ttu-id="da832-120">Beskrivning av HostPool.</span><span class="sxs-lookup"><span data-stu-id="da832-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="da832-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="da832-122">Namn på Skriv bords appen</span><span class="sxs-lookup"><span data-stu-id="da832-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="da832-123">-ExpirationTime</span></span>
<span data-ttu-id="da832-124">Upphört att gälla.</span><span class="sxs-lookup"><span data-stu-id="da832-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="da832-125">-FriendlyName</span></span>
<span data-ttu-id="da832-126">Eget namn på HostPool.</span><span class="sxs-lookup"><span data-stu-id="da832-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="da832-127">-HostPoolType</span></span>
<span data-ttu-id="da832-128">HostPool typ för skriv bord.</span><span class="sxs-lookup"><span data-stu-id="da832-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="da832-129">-LoadBalancerType</span></span>
<span data-ttu-id="da832-130">Typen av belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="da832-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="da832-131">-Location</span></span>
<span data-ttu-id="da832-132">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="da832-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="da832-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="da832-133">-MaxSessionLimit</span></span>
<span data-ttu-id="da832-134">Maximal sessionsgräns för HostPool.</span><span class="sxs-lookup"><span data-stu-id="da832-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="da832-135">-Name</span></span>
<span data-ttu-id="da832-136">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="da832-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="da832-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="da832-138">PersonalDesktopAssignment typ för HostPool.</span><span class="sxs-lookup"><span data-stu-id="da832-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="da832-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="da832-140">Typen av grupp för önskat program, standard för Skriv bords program grupp</span><span class="sxs-lookup"><span data-stu-id="da832-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="da832-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="da832-142">Registrerings-token Base64-kodad sträng.</span><span class="sxs-lookup"><span data-stu-id="da832-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="da832-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="da832-144">Typen av ominställning av token.</span><span class="sxs-lookup"><span data-stu-id="da832-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da832-145">-ResourceGroupName</span></span>
<span data-ttu-id="da832-146">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="da832-146">The name of the resource group.</span></span>
<span data-ttu-id="da832-147">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="da832-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="da832-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="da832-148">-Ring</span></span>
<span data-ttu-id="da832-149">Ring numret för HostPool.</span><span class="sxs-lookup"><span data-stu-id="da832-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="da832-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="da832-151">URL till Customer ADFS Server för att signera WVD SSO-certifikat.</span><span class="sxs-lookup"><span data-stu-id="da832-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="da832-152">-SsoClientId</span></span>
<span data-ttu-id="da832-153">ClientId för den registrerade förlitande parten som används för att utfärda WVD SSO-certifikat.</span><span class="sxs-lookup"><span data-stu-id="da832-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="da832-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="da832-155">Sökväg till Azure-nyckel valv lagrar den hemlighet som används för kommunikation till AD FS.</span><span class="sxs-lookup"><span data-stu-id="da832-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="da832-156">-SsoContext</span></span>
<span data-ttu-id="da832-157">Sökväg till nyckel valv som innehåller ssoContext-hemlighet.</span><span class="sxs-lookup"><span data-stu-id="da832-157">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="da832-158">-SsoSecretType</span></span>
<span data-ttu-id="da832-159">Typen av enkel inloggnings typ.</span><span class="sxs-lookup"><span data-stu-id="da832-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="da832-160">-StartVMOnConnect</span></span>
<span data-ttu-id="da832-161">Flaggan för att aktivera/inaktivera StartVMOnConnect funktionen.</span><span class="sxs-lookup"><span data-stu-id="da832-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da832-162">-SubscriptionId</span></span>
<span data-ttu-id="da832-163">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da832-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="da832-164">-Tagg</span><span class="sxs-lookup"><span data-stu-id="da832-164">-Tag</span></span>
<span data-ttu-id="da832-165">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="da832-165">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="da832-166">-ValidationEnvironment</span></span>
<span data-ttu-id="da832-167">Är verifierings miljö.</span><span class="sxs-lookup"><span data-stu-id="da832-167">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="da832-168">-VMTemplate</span></span>
<span data-ttu-id="da832-169">Mall för virtuell dator för sessionhosts konfiguration i hostpool.</span><span class="sxs-lookup"><span data-stu-id="da832-169">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da832-170">-WorkspaceName</span></span>
<span data-ttu-id="da832-171">Namn på arbets ytan</span><span class="sxs-lookup"><span data-stu-id="da832-171">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da832-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da832-172">-Confirm</span></span>
<span data-ttu-id="da832-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da832-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da832-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da832-174">-WhatIf</span></span>
<span data-ttu-id="da832-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da832-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da832-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da832-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da832-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da832-177">CommonParameters</span></span>
<span data-ttu-id="da832-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da832-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da832-179">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da832-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da832-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da832-180">INPUTS</span></span>

## <span data-ttu-id="da832-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da832-181">OUTPUTS</span></span>

### <span data-ttu-id="da832-182">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="da832-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="da832-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da832-183">NOTES</span></span>

<span data-ttu-id="da832-184">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da832-184">ALIASES</span></span>

## <span data-ttu-id="da832-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da832-185">RELATED LINKS</span></span>

