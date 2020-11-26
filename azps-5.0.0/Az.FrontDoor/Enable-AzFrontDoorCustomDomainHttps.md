---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272293"
---
# <span data-ttu-id="a5b76-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="a5b76-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="a5b76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5b76-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b76-103">Aktivera HTTPS för en anpassad domän med certifikat för front luckan som hanteras eller med ett eget certifikat från Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a5b76-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="a5b76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5b76-104">SYNTAX</span></span>

### <span data-ttu-id="a5b76-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a5b76-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b76-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b76-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b76-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b76-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b76-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b76-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b76-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b76-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b76-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b76-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b76-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5b76-111">DESCRIPTION</span></span>
<span data-ttu-id="a5b76-112">**Enable-AzFrontDoorCustomDomainHttps** aktiverar HTTPS för en egen domän.</span><span class="sxs-lookup"><span data-stu-id="a5b76-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="a5b76-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5b76-113">EXAMPLES</span></span>

### <span data-ttu-id="a5b76-114">Exempel 1: Aktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName med hanterat certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="a5b76-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="a5b76-115">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" som är en del av front dörren "frontdoor1" i resurs gruppen "resourcegroup1" med certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="a5b76-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="a5b76-116">Exempel 2: Aktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName med eget certifikat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a5b76-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="a5b76-117">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" som är en del av front dörren "frontdoor1" i resurs gruppen "resourcegroup1" med certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="a5b76-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="a5b76-118">Exempel 3: Aktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt med front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="a5b76-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="a5b76-119">Aktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt med front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="a5b76-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="a5b76-120">Exempel 4: Aktivera HTTPS för en anpassad domän med resurs-ID genom att använda front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="a5b76-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="a5b76-121">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" med resurs-ID $resourceId med certifikat från Front dörren.</span><span class="sxs-lookup"><span data-stu-id="a5b76-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="a5b76-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5b76-122">PARAMETERS</span></span>

### <span data-ttu-id="a5b76-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b76-123">-DefaultProfile</span></span>
<span data-ttu-id="a5b76-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b76-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b76-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a5b76-125">-FrontDoorName</span></span>
<span data-ttu-id="a5b76-126">Namnet på front dörren.</span><span class="sxs-lookup"><span data-stu-id="a5b76-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="a5b76-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="a5b76-127">-FrontendEndpointName</span></span>
<span data-ttu-id="a5b76-128">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="a5b76-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="a5b76-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b76-129">-InputObject</span></span>
<span data-ttu-id="a5b76-130">Den frontend-slutpunkt-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a5b76-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="a5b76-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a5b76-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="a5b76-132">Den minsta TLS-version som krävs från klienter för att upprätta en SSL-handskakning med front dörren.</span><span class="sxs-lookup"><span data-stu-id="a5b76-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="a5b76-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b76-133">-ResourceGroupName</span></span>
<span data-ttu-id="a5b76-134">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="a5b76-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="a5b76-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b76-135">-ResourceId</span></span>
<span data-ttu-id="a5b76-136">Resurs-ID för front dörrens slut punkt för att aktivera https</span><span class="sxs-lookup"><span data-stu-id="a5b76-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="a5b76-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="a5b76-137">-SecretName</span></span>
<span data-ttu-id="a5b76-138">Namnet på den hemliga nyckel valv hemligheten som representerar det fullständiga certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="a5b76-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a5b76-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="a5b76-139">-SecretVersion</span></span>
<span data-ttu-id="a5b76-140">Den version av nyckel valv hemligheten som representerar fullständigt certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="a5b76-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a5b76-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a5b76-141">-VaultId</span></span>
<span data-ttu-id="a5b76-142">Det valv-ID som innehåller SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="a5b76-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="a5b76-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5b76-143">-Confirm</span></span>
<span data-ttu-id="a5b76-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5b76-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b76-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b76-145">-WhatIf</span></span>
<span data-ttu-id="a5b76-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5b76-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5b76-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5b76-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b76-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b76-148">CommonParameters</span></span>
<span data-ttu-id="a5b76-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b76-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b76-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5b76-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b76-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5b76-151">INPUTS</span></span>

### <span data-ttu-id="a5b76-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b76-152">System.String</span></span>
## <span data-ttu-id="a5b76-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5b76-153">OUTPUTS</span></span>

### <span data-ttu-id="a5b76-154">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5b76-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="a5b76-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5b76-155">NOTES</span></span>

## <span data-ttu-id="a5b76-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5b76-156">RELATED LINKS</span></span>