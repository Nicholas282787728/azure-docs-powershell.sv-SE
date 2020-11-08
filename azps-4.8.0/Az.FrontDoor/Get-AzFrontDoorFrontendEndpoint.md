---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262683"
---
# <span data-ttu-id="bc3cf-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc3cf-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="bc3cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3cf-103">Skaffa en slut punkt för frontend-väckare.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="bc3cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc3cf-104">SYNTAX</span></span>

### <span data-ttu-id="bc3cf-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bc3cf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc3cf-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3cf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc3cf-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc3cf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc3cf-108">DESCRIPTION</span></span>
<span data-ttu-id="bc3cf-109">Cmdleten **Get-AzFrontDoorFrontendEndpoint** får alla befintliga frontend-slutpunkter i den aktuella resursen för front dörren som matchar angiven information.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="bc3cf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc3cf-110">EXAMPLES</span></span>

### <span data-ttu-id="bc3cf-111">Exempel 1: Hämta alla slut punkter för klient delen i front dörren "frontdoor1", som är en del av resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="bc3cf-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
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

<span data-ttu-id="bc3cf-112">Hämta alla slut punkter för klient delen i front dörren "frontdoor1" som är en del av resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="bc3cf-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="bc3cf-113">Exempel 2: Hämta slut punkt för klient delen med namnet "frontdoor1-azurefd-net" i front dörren "frontdoor1", som är en del av resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="bc3cf-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="bc3cf-114">Hämta klient delen med namn "frontdoor1-azurefd-net" i front dörren "frontdoor1", som är en del av resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="bc3cf-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="bc3cf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc3cf-115">PARAMETERS</span></span>

### <span data-ttu-id="bc3cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3cf-116">-DefaultProfile</span></span>
<span data-ttu-id="bc3cf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc3cf-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="bc3cf-118">-FrontDoorName</span></span>
<span data-ttu-id="bc3cf-119">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-119">Front Door name.</span></span>

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

### <span data-ttu-id="bc3cf-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="bc3cf-120">-FrontDoorObject</span></span>
<span data-ttu-id="bc3cf-121">FrontDoor-objektet.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3cf-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc3cf-122">-Name</span></span>
<span data-ttu-id="bc3cf-123">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc3cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc3cf-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-125">The resource group name.</span></span>

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

### <span data-ttu-id="bc3cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc3cf-126">-ResourceId</span></span>
<span data-ttu-id="bc3cf-127">Resurs-ID för front dörren</span><span class="sxs-lookup"><span data-stu-id="bc3cf-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="bc3cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3cf-128">CommonParameters</span></span>
<span data-ttu-id="bc3cf-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3cf-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc3cf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3cf-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc3cf-131">INPUTS</span></span>

### <span data-ttu-id="bc3cf-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="bc3cf-132">None</span></span>

## <span data-ttu-id="bc3cf-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc3cf-133">OUTPUTS</span></span>

### <span data-ttu-id="bc3cf-134">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc3cf-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="bc3cf-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc3cf-135">NOTES</span></span>

## <span data-ttu-id="bc3cf-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc3cf-136">RELATED LINKS</span></span>
