---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: d88468647b02f2de3c5aba81d6829a6931df5750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758290"
---
# <span data-ttu-id="5a665-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a665-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="5a665-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a665-102">SYNOPSIS</span></span>
<span data-ttu-id="5a665-103">Hämtar en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a665-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a665-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a665-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a665-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a665-105">DESCRIPTION</span></span>
<span data-ttu-id="5a665-106">Cmdleten **Get-AzureRmExpressRouteCircuitPeeringConfig** hämtar konfigurationen för en peering-relation för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="5a665-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="5a665-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a665-107">EXAMPLES</span></span>

### <span data-ttu-id="5a665-108">Exempel 1: Visa peering-konfigurationen för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="5a665-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="5a665-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a665-109">PARAMETERS</span></span>

### <span data-ttu-id="5a665-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a665-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5a665-111">Det ExpressRoute-krets-objekt som innehåller peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5a665-111">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="5a665-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a665-112">-Name</span></span>
<span data-ttu-id="5a665-113">Namnet på den peering-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="5a665-113">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="5a665-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a665-114">-DefaultProfile</span></span>
<span data-ttu-id="5a665-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a665-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a665-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a665-116">CommonParameters</span></span>
<span data-ttu-id="5a665-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a665-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a665-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a665-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a665-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a665-119">INPUTS</span></span>

### <span data-ttu-id="5a665-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a665-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5a665-121">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5a665-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="5a665-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a665-122">OUTPUTS</span></span>

### <span data-ttu-id="5a665-123">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="5a665-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="5a665-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a665-124">NOTES</span></span>

## <span data-ttu-id="5a665-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a665-125">RELATED LINKS</span></span>

[<span data-ttu-id="5a665-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a665-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5a665-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a665-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5a665-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a665-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5a665-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a665-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
