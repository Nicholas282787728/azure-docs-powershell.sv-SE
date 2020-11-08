---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918506"
---
# <span data-ttu-id="f2de6-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2de6-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f2de6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2de6-102">SYNOPSIS</span></span>
<span data-ttu-id="f2de6-103">Hämtar en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f2de6-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="f2de6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2de6-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2de6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2de6-105">DESCRIPTION</span></span>
<span data-ttu-id="f2de6-106">Cmdleten **Get-AzExpressRouteCircuitPeeringConfig** hämtar konfigurationen för en peering-relation för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="f2de6-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f2de6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2de6-107">EXAMPLES</span></span>

### <span data-ttu-id="f2de6-108">Exempel 1: Visa peering-konfigurationen för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="f2de6-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f2de6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2de6-109">PARAMETERS</span></span>

### <span data-ttu-id="f2de6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2de6-110">-DefaultProfile</span></span>
<span data-ttu-id="f2de6-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2de6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2de6-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2de6-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f2de6-113">Det ExpressRoute-krets-objekt som innehåller peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f2de6-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2de6-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2de6-114">-Name</span></span>
<span data-ttu-id="f2de6-115">Namnet på den peering-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f2de6-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="f2de6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2de6-116">CommonParameters</span></span>
<span data-ttu-id="f2de6-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2de6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2de6-118">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2de6-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2de6-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2de6-119">INPUTS</span></span>

### <span data-ttu-id="f2de6-120">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2de6-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f2de6-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2de6-121">OUTPUTS</span></span>

### <span data-ttu-id="f2de6-122">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f2de6-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f2de6-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2de6-123">NOTES</span></span>

## <span data-ttu-id="f2de6-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2de6-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2de6-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2de6-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f2de6-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2de6-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f2de6-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2de6-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f2de6-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2de6-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)