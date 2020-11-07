---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 36cf08aa4cb201beac284ae2296dfa508bf4edba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574891"
---
# <span data-ttu-id="269c6-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="269c6-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="269c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="269c6-102">SYNOPSIS</span></span>
<span data-ttu-id="269c6-103">Tar bort en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="269c6-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="269c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="269c6-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="269c6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="269c6-105">DESCRIPTION</span></span>
<span data-ttu-id="269c6-106">Cmdleten **Remove-AzureRmExpressRouteCircuitPeeringConfig** tar bort en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="269c6-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="269c6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="269c6-107">EXAMPLES</span></span>

### <span data-ttu-id="269c6-108">Exempel 1: ta bort en peering-konfiguration från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="269c6-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="269c6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="269c6-109">PARAMETERS</span></span>

### <span data-ttu-id="269c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="269c6-110">-DefaultProfile</span></span>
<span data-ttu-id="269c6-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="269c6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="269c6-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="269c6-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="269c6-113">ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="269c6-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="269c6-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="269c6-114">-Name</span></span>
<span data-ttu-id="269c6-115">Namnet på peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="269c6-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="269c6-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="269c6-116">-PeerAddressType</span></span>
<span data-ttu-id="269c6-117">Peering-adress familjen</span><span class="sxs-lookup"><span data-stu-id="269c6-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="269c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269c6-118">CommonParameters</span></span>
<span data-ttu-id="269c6-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="269c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269c6-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="269c6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269c6-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="269c6-121">INPUTS</span></span>

### <span data-ttu-id="269c6-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="269c6-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="269c6-123">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="269c6-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="269c6-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="269c6-124">OUTPUTS</span></span>

### <span data-ttu-id="269c6-125">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="269c6-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="269c6-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="269c6-126">NOTES</span></span>

## <span data-ttu-id="269c6-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="269c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="269c6-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="269c6-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="269c6-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="269c6-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="269c6-130">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="269c6-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="269c6-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="269c6-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)