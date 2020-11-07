---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6edf891d693e0c1cb2143236d12e623fdd2b4a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744165"
---
# <span data-ttu-id="19bdf-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="19bdf-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="19bdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="19bdf-103">Aktivera HTTPS för en anpassad domän med certifikat för front luckan som hanteras eller med ett eget certifikat från Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="19bdf-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="19bdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19bdf-104">SYNTAX</span></span>

### <span data-ttu-id="19bdf-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="19bdf-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19bdf-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="19bdf-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19bdf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19bdf-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19bdf-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="19bdf-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19bdf-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19bdf-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19bdf-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="19bdf-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19bdf-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19bdf-111">DESCRIPTION</span></span>
<span data-ttu-id="19bdf-112">**Enable-AzFrontDoorCustomDomainHttps** aktiverar HTTPS för en egen domän.</span><span class="sxs-lookup"><span data-stu-id="19bdf-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="19bdf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19bdf-113">EXAMPLES</span></span>

### <span data-ttu-id="19bdf-114">Exempel 1: Aktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName med hanterat certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="19bdf-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="19bdf-115">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" som är en del av front dörren "frontdoor1" i resurs gruppen "resourcegroup1" med certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="19bdf-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="19bdf-116">Exempel 2: Aktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName med eget certifikat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="19bdf-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="19bdf-117">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" som är en del av front dörren "frontdoor1" i resurs gruppen "resourcegroup1" med certifikat för front dörren.</span><span class="sxs-lookup"><span data-stu-id="19bdf-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="19bdf-118">Exempel 3: Aktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt med front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="19bdf-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="19bdf-119">Aktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt med front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="19bdf-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="19bdf-120">Exempel 4: Aktivera HTTPS för en anpassad domän med resurs-ID genom att använda front dörrens hanterat certifikat.</span><span class="sxs-lookup"><span data-stu-id="19bdf-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="19bdf-121">Aktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" med resurs-ID $resourceId med certifikat från Front dörren.</span><span class="sxs-lookup"><span data-stu-id="19bdf-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="19bdf-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19bdf-122">PARAMETERS</span></span>

### <span data-ttu-id="19bdf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bdf-123">-DefaultProfile</span></span>
<span data-ttu-id="19bdf-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19bdf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19bdf-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="19bdf-125">-FrontDoorName</span></span>
<span data-ttu-id="19bdf-126">Namnet på front dörren.</span><span class="sxs-lookup"><span data-stu-id="19bdf-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="19bdf-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="19bdf-127">-FrontendEndpointName</span></span>
<span data-ttu-id="19bdf-128">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="19bdf-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="19bdf-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19bdf-129">-InputObject</span></span>
<span data-ttu-id="19bdf-130">Den frontend-slutpunkt-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="19bdf-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="19bdf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19bdf-131">-ResourceGroupName</span></span>
<span data-ttu-id="19bdf-132">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="19bdf-132">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="19bdf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19bdf-133">-ResourceId</span></span>
<span data-ttu-id="19bdf-134">Resurs-ID för front dörrens slut punkt för att aktivera https</span><span class="sxs-lookup"><span data-stu-id="19bdf-134">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="19bdf-135">-SecretName</span><span class="sxs-lookup"><span data-stu-id="19bdf-135">-SecretName</span></span>
<span data-ttu-id="19bdf-136">Namnet på den hemliga nyckel valv hemligheten som representerar det fullständiga certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="19bdf-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="19bdf-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="19bdf-137">-SecretVersion</span></span>
<span data-ttu-id="19bdf-138">Den version av nyckel valv hemligheten som representerar fullständigt certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="19bdf-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="19bdf-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="19bdf-139">-VaultId</span></span>
<span data-ttu-id="19bdf-140">Det valv-ID som innehåller SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="19bdf-140">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="19bdf-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19bdf-141">-Confirm</span></span>
<span data-ttu-id="19bdf-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19bdf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19bdf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19bdf-143">-WhatIf</span></span>
<span data-ttu-id="19bdf-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19bdf-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19bdf-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19bdf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19bdf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bdf-146">CommonParameters</span></span>
<span data-ttu-id="19bdf-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19bdf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bdf-148">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19bdf-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bdf-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19bdf-149">INPUTS</span></span>

### <span data-ttu-id="19bdf-150">System. String</span><span class="sxs-lookup"><span data-stu-id="19bdf-150">System.String</span></span>

## <span data-ttu-id="19bdf-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19bdf-151">OUTPUTS</span></span>

### <span data-ttu-id="19bdf-152">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="19bdf-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="19bdf-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19bdf-153">NOTES</span></span>

## <span data-ttu-id="19bdf-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19bdf-154">RELATED LINKS</span></span>
