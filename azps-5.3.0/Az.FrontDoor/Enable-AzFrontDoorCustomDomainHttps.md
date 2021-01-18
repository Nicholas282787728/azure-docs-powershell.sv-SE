---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520759"
---
# <span data-ttu-id="634c4-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="634c4-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="634c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="634c4-102">SYNOPSIS</span></span>
<span data-ttu-id="634c4-103">Aktivera HTTPS för en anpassad domän med certifikat för front luckan som hanteras eller med ett eget certifikat från Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="634c4-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="634c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="634c4-104">SYNTAX</span></span>

### <span data-ttu-id="634c4-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="634c4-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634c4-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="634c4-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="634c4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="634c4-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634c4-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="634c4-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634c4-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="634c4-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634c4-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="634c4-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="634c4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="634c4-111">DESCRIPTION</span></span>
<span data-ttu-id="634c4-112">**Enable-AzFrontDoorCustomDomainHttps** aktiverar HTTPS för en egen domän.</span><span class="sxs-lookup"><span data-stu-id="634c4-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="634c4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="634c4-113">EXAMPLES</span></span>

### <span data-ttu-id="634c4-114">Exempel 1: Aktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName med hanterat certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="634c4-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="634c4-115">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" som är en del av front dörren "frontdoor1" i resurs gruppen "resourcegroup1" med certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="634c4-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="634c4-116">Exempel 2: Aktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName med eget certifikat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="634c4-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="634c4-117">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" som är en del av front dörren "frontdoor1" i resurs gruppen "resourcegroup1" med certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="634c4-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="634c4-118">Exempel 3: Aktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt med front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="634c4-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="634c4-119">Aktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt med front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="634c4-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="634c4-120">Exempel 4: Aktivera HTTPS för en anpassad domän med resurs-ID genom att använda front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="634c4-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="634c4-121">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" med resurs-ID $resourceId med certifikat från Front dörren.</span><span class="sxs-lookup"><span data-stu-id="634c4-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="634c4-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="634c4-122">PARAMETERS</span></span>

### <span data-ttu-id="634c4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634c4-123">-DefaultProfile</span></span>
<span data-ttu-id="634c4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="634c4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="634c4-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="634c4-125">-FrontDoorName</span></span>
<span data-ttu-id="634c4-126">Namnet på front dörren.</span><span class="sxs-lookup"><span data-stu-id="634c4-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="634c4-127">-FrontendEndpointName</span></span>
<span data-ttu-id="634c4-128">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="634c4-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="634c4-129">-InputObject</span></span>
<span data-ttu-id="634c4-130">Den frontend-slutpunkt-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="634c4-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="634c4-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="634c4-132">Den minsta TLS-version som krävs från klienter för att upprätta en SSL-handskakning med front dörren.</span><span class="sxs-lookup"><span data-stu-id="634c4-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="634c4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="634c4-133">-ResourceGroupName</span></span>
<span data-ttu-id="634c4-134">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="634c4-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="634c4-135">-ResourceId</span></span>
<span data-ttu-id="634c4-136">Resurs-ID för front dörrens slut punkt för att aktivera https</span><span class="sxs-lookup"><span data-stu-id="634c4-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="634c4-137">-SecretName</span></span>
<span data-ttu-id="634c4-138">Namnet på den hemliga nyckel valv hemligheten som representerar det fullständiga certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="634c4-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="634c4-139">-SecretVersion</span></span>
<span data-ttu-id="634c4-140">Den version av nyckel valv hemligheten som representerar fullständigt certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="634c4-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="634c4-141">-VaultId</span></span>
<span data-ttu-id="634c4-142">Det valv-ID som innehåller SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="634c4-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="634c4-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="634c4-143">-Confirm</span></span>
<span data-ttu-id="634c4-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="634c4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="634c4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="634c4-145">-WhatIf</span></span>
<span data-ttu-id="634c4-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="634c4-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="634c4-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="634c4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="634c4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634c4-148">CommonParameters</span></span>
<span data-ttu-id="634c4-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="634c4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634c4-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="634c4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634c4-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="634c4-151">INPUTS</span></span>

### <span data-ttu-id="634c4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="634c4-152">System.String</span></span>
## <span data-ttu-id="634c4-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="634c4-153">OUTPUTS</span></span>

### <span data-ttu-id="634c4-154">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="634c4-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="634c4-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="634c4-155">NOTES</span></span>

## <span data-ttu-id="634c4-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="634c4-156">RELATED LINKS</span></span>
