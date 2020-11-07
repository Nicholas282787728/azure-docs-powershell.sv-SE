---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c7d60c3d2f69e7ea18bcd256d8ad4a943817769a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747906"
---
# <span data-ttu-id="05708-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="05708-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="05708-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05708-102">SYNOPSIS</span></span>
<span data-ttu-id="05708-103">Tar bort en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="05708-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="05708-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05708-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05708-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05708-105">DESCRIPTION</span></span>
<span data-ttu-id="05708-106">Cmdleten **Remove-AzExpressRouteCircuitPeeringConfig** tar bort en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="05708-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="05708-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05708-107">EXAMPLES</span></span>

### <span data-ttu-id="05708-108">Exempel 1: ta bort en peering-konfiguration från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="05708-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="05708-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05708-109">PARAMETERS</span></span>

### <span data-ttu-id="05708-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05708-110">-DefaultProfile</span></span>
<span data-ttu-id="05708-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05708-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05708-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05708-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="05708-113">ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="05708-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="05708-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="05708-114">-Name</span></span>
<span data-ttu-id="05708-115">Namnet på peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="05708-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="05708-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="05708-116">-PeerAddressType</span></span>
<span data-ttu-id="05708-117">Peering-adress familjen</span><span class="sxs-lookup"><span data-stu-id="05708-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05708-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05708-118">CommonParameters</span></span>
<span data-ttu-id="05708-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05708-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05708-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05708-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05708-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05708-121">INPUTS</span></span>

### <span data-ttu-id="05708-122">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05708-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="05708-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05708-123">OUTPUTS</span></span>

### <span data-ttu-id="05708-124">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05708-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="05708-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05708-125">NOTES</span></span>

## <span data-ttu-id="05708-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05708-126">RELATED LINKS</span></span>

[<span data-ttu-id="05708-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="05708-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="05708-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05708-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="05708-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="05708-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="05708-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05708-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
