---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922037"
---
# <span data-ttu-id="6a5ae-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6a5ae-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="6a5ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5ae-103">Tar bort en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6a5ae-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="6a5ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a5ae-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a5ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="6a5ae-106">Cmdleten **Remove-AzExpressRouteCircuitPeeringConfig** tar bort en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6a5ae-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="6a5ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="6a5ae-108">Exempel 1: ta bort en peering-konfiguration från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="6a5ae-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="6a5ae-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a5ae-109">PARAMETERS</span></span>

### <span data-ttu-id="6a5ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5ae-110">-DefaultProfile</span></span>
<span data-ttu-id="6a5ae-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5ae-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ae-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a5ae-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6a5ae-113">ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6a5ae-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ae-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a5ae-114">-Name</span></span>
<span data-ttu-id="6a5ae-115">Namnet på peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6a5ae-115">The name of the peering configuration to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ae-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="6a5ae-116">-PeerAddressType</span></span>
<span data-ttu-id="6a5ae-117">Peering-adress familjen</span><span class="sxs-lookup"><span data-stu-id="6a5ae-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5ae-118">CommonParameters</span></span>
<span data-ttu-id="6a5ae-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a5ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5ae-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a5ae-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5ae-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a5ae-121">INPUTS</span></span>

### <span data-ttu-id="6a5ae-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a5ae-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="6a5ae-123">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6a5ae-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="6a5ae-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a5ae-124">OUTPUTS</span></span>

### <span data-ttu-id="6a5ae-125">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a5ae-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6a5ae-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a5ae-126">NOTES</span></span>

## <span data-ttu-id="6a5ae-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a5ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="6a5ae-128">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6a5ae-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="6a5ae-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a5ae-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="6a5ae-130">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6a5ae-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="6a5ae-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a5ae-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
