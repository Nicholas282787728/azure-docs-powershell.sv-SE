---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922286"
---
# <span data-ttu-id="59c69-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59c69-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="59c69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59c69-102">SYNOPSIS</span></span>
<span data-ttu-id="59c69-103">Hämtar en ExpressRoute-peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="59c69-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="59c69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59c69-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c69-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59c69-105">DESCRIPTION</span></span>
<span data-ttu-id="59c69-106">Cmdleten **Get-AzExpressRouteCircuitPeeringConfig** hämtar konfigurationen för en peering-relation för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="59c69-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="59c69-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59c69-107">EXAMPLES</span></span>

### <span data-ttu-id="59c69-108">Exempel 1: Visa peering-konfigurationen för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="59c69-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="59c69-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59c69-109">PARAMETERS</span></span>

### <span data-ttu-id="59c69-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c69-110">-DefaultProfile</span></span>
<span data-ttu-id="59c69-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59c69-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59c69-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59c69-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="59c69-113">Det ExpressRoute-krets-objekt som innehåller peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="59c69-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="59c69-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="59c69-114">-Name</span></span>
<span data-ttu-id="59c69-115">Namnet på den peering-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="59c69-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="59c69-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c69-116">CommonParameters</span></span>
<span data-ttu-id="59c69-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c69-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c69-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59c69-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c69-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59c69-119">INPUTS</span></span>

### <span data-ttu-id="59c69-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59c69-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="59c69-121">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="59c69-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="59c69-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59c69-122">OUTPUTS</span></span>

### <span data-ttu-id="59c69-123">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="59c69-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="59c69-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59c69-124">NOTES</span></span>

## <span data-ttu-id="59c69-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59c69-125">RELATED LINKS</span></span>

[<span data-ttu-id="59c69-126">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59c69-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="59c69-127">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59c69-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="59c69-128">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59c69-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="59c69-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59c69-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
