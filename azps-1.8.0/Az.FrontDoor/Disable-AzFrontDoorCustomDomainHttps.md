---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 2f6b5635b029548f8d92917e0abfca18d5c0c415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916786"
---
# <span data-ttu-id="8e359-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="8e359-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="8e359-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e359-102">SYNOPSIS</span></span>
<span data-ttu-id="8e359-103">Inaktivera HTTPS för en anpassad domän</span><span class="sxs-lookup"><span data-stu-id="8e359-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="8e359-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e359-104">SYNTAX</span></span>

### <span data-ttu-id="8e359-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8e359-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e359-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e359-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e359-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e359-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e359-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e359-108">DESCRIPTION</span></span>
<span data-ttu-id="8e359-109">**Disable-AzFrontDoorCustomDomainHttps** inaktiverar https för en anpassad domän.</span><span class="sxs-lookup"><span data-stu-id="8e359-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="8e359-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e359-110">EXAMPLES</span></span>

### <span data-ttu-id="8e359-111">Exempel 1: inaktivera HTTPS för en anpassad domän med FrontDoorName och ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="8e359-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
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

<span data-ttu-id="8e359-112">Inaktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" med FrontDoorName som "frontdoor1" och ResourceGroupName som "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="8e359-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="8e359-113">Exempel 2: inaktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt.</span><span class="sxs-lookup"><span data-stu-id="8e359-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
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

<span data-ttu-id="8e359-114">Inaktivera HTTPS för en anpassad domän med PSFrontendEndpoint-objekt.</span><span class="sxs-lookup"><span data-stu-id="8e359-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="8e359-115">Exempel 3: inaktivera HTTPS för en anpassad domän med ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8e359-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
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

<span data-ttu-id="8e359-116">Inaktivera HTTPS för en anpassad domän "frontendpointname1-Custom-XYZ" med ResourceId som $resourceId.</span><span class="sxs-lookup"><span data-stu-id="8e359-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="8e359-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e359-117">PARAMETERS</span></span>

### <span data-ttu-id="8e359-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e359-118">-DefaultProfile</span></span>
<span data-ttu-id="8e359-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e359-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e359-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8e359-120">-FrontDoorName</span></span>
<span data-ttu-id="8e359-121">Namnet på front dörren.</span><span class="sxs-lookup"><span data-stu-id="8e359-121">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e359-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="8e359-122">-FrontendEndpointName</span></span>
<span data-ttu-id="8e359-123">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="8e359-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e359-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e359-124">-InputObject</span></span>
<span data-ttu-id="8e359-125">Den frontend-slutpunkt-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8e359-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e359-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e359-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e359-127">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="8e359-127">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e359-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e359-128">-ResourceId</span></span>
<span data-ttu-id="8e359-129">Resurs-ID för front dörrens slut punkt för att inaktivera https</span><span class="sxs-lookup"><span data-stu-id="8e359-129">Resource Id of the Front Door endpoint to disable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e359-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e359-130">-Confirm</span></span>
<span data-ttu-id="8e359-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e359-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e359-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e359-132">-WhatIf</span></span>
<span data-ttu-id="8e359-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e359-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e359-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e359-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e359-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e359-135">CommonParameters</span></span>
<span data-ttu-id="8e359-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e359-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e359-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e359-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e359-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e359-138">INPUTS</span></span>

### <span data-ttu-id="8e359-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8e359-139">System.String</span></span>

## <span data-ttu-id="8e359-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e359-140">OUTPUTS</span></span>

### <span data-ttu-id="8e359-141">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e359-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="8e359-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e359-142">NOTES</span></span>

## <span data-ttu-id="8e359-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e359-143">RELATED LINKS</span></span>
