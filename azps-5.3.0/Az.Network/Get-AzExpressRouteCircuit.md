---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522441"
---
# <span data-ttu-id="47b5d-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47b5d-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="47b5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="47b5d-103">Hämtar en Azure ExpressRoute-krets från Azure.</span><span class="sxs-lookup"><span data-stu-id="47b5d-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="47b5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47b5d-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="47b5d-106">Cmdleten **Get-AzExpressRouteCircuit** används för att hämta ett ExpressRoute-kretskort från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="47b5d-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="47b5d-107">Det kretsar som returneras kan användas som indata för andra cmdlets som fungerar på ExpressRoute-kretsar.</span><span class="sxs-lookup"><span data-stu-id="47b5d-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="47b5d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47b5d-108">EXAMPLES</span></span>

### <span data-ttu-id="47b5d-109">Exempel 1: skaffa ExpressRoute-kretsen</span><span class="sxs-lookup"><span data-stu-id="47b5d-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="47b5d-110">Skaffa en specifik ExpressRoute-krets med namnet "testrg" och ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="47b5d-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="47b5d-111">Exempel 2: lista de ExpressRoutea kretsarna med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="47b5d-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="47b5d-112">Få alla ExpressRoute-kretsar vars namn börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="47b5d-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="47b5d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47b5d-113">PARAMETERS</span></span>

### <span data-ttu-id="47b5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b5d-114">-DefaultProfile</span></span>
<span data-ttu-id="47b5d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47b5d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47b5d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="47b5d-116">-Name</span></span>
<span data-ttu-id="47b5d-117">Namnet på ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="47b5d-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="47b5d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b5d-118">-ResourceGroupName</span></span>
<span data-ttu-id="47b5d-119">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="47b5d-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="47b5d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b5d-120">CommonParameters</span></span>
<span data-ttu-id="47b5d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b5d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b5d-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b5d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b5d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47b5d-123">INPUTS</span></span>

### <span data-ttu-id="47b5d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="47b5d-124">System.String</span></span>

## <span data-ttu-id="47b5d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47b5d-125">OUTPUTS</span></span>

### <span data-ttu-id="47b5d-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47b5d-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="47b5d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47b5d-127">NOTES</span></span>

## <span data-ttu-id="47b5d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47b5d-128">RELATED LINKS</span></span>

[<span data-ttu-id="47b5d-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47b5d-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="47b5d-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47b5d-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="47b5d-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47b5d-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="47b5d-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47b5d-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
