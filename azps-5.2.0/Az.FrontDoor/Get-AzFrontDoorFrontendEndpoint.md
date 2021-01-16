---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407355"
---
# <span data-ttu-id="c2575-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2575-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="c2575-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2575-102">SYNOPSIS</span></span>
<span data-ttu-id="c2575-103">Skaffa en slut punkt för frontend-väckare.</span><span class="sxs-lookup"><span data-stu-id="c2575-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="c2575-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2575-104">SYNTAX</span></span>

### <span data-ttu-id="c2575-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2575-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2575-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2575-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2575-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2575-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2575-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2575-108">DESCRIPTION</span></span>
<span data-ttu-id="c2575-109">Cmdleten **Get-AzFrontDoorFrontendEndpoint** får alla befintliga frontend-slutpunkter i den aktuella resursen för front dörren som matchar angiven information.</span><span class="sxs-lookup"><span data-stu-id="c2575-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="c2575-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2575-110">EXAMPLES</span></span>

### <span data-ttu-id="c2575-111">Exempel 1: Hämta alla slut punkter för klient delen i front dörren "frontdoor1", som är en del av resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="c2575-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="c2575-112">Hämta alla slut punkter för klient delen i front dörren "frontdoor1" som är en del av resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="c2575-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="c2575-113">Exempel 2: Hämta slut punkt för klient delen med namnet "frontdoor1-azurefd-net" i front dörren "frontdoor1", som är en del av resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="c2575-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="c2575-114">Hämta klient delen med namn "frontdoor1-azurefd-net" i front dörren "frontdoor1", som är en del av resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="c2575-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="c2575-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2575-115">PARAMETERS</span></span>

### <span data-ttu-id="c2575-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2575-116">-DefaultProfile</span></span>
<span data-ttu-id="c2575-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2575-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2575-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c2575-118">-FrontDoorName</span></span>
<span data-ttu-id="c2575-119">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="c2575-119">Front Door name.</span></span>

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

### <span data-ttu-id="c2575-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="c2575-120">-FrontDoorObject</span></span>
<span data-ttu-id="c2575-121">FrontDoor-objektet.</span><span class="sxs-lookup"><span data-stu-id="c2575-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="c2575-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2575-122">-Name</span></span>
<span data-ttu-id="c2575-123">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="c2575-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="c2575-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2575-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2575-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c2575-125">The resource group name.</span></span>

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

### <span data-ttu-id="c2575-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2575-126">-ResourceId</span></span>
<span data-ttu-id="c2575-127">Resurs-ID för front dörren</span><span class="sxs-lookup"><span data-stu-id="c2575-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="c2575-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2575-128">CommonParameters</span></span>
<span data-ttu-id="c2575-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2575-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2575-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2575-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2575-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2575-131">INPUTS</span></span>

### <span data-ttu-id="c2575-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="c2575-132">None</span></span>

## <span data-ttu-id="c2575-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2575-133">OUTPUTS</span></span>

### <span data-ttu-id="c2575-134">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2575-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="c2575-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2575-135">NOTES</span></span>

## <span data-ttu-id="c2575-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2575-136">RELATED LINKS</span></span>
