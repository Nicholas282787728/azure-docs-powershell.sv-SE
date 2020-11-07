---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
ms.openlocfilehash: 68579ea2adecbf7ad6a97fd11f4f32da9adeb48f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930989"
---
# <span data-ttu-id="79c2f-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="79c2f-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="79c2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="79c2f-103">Får användnings statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="79c2f-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79c2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79c2f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c2f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="79c2f-106">Cmdleten **Get-AzureRmExpressRouteCircuitStats** hämtar trafik statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="79c2f-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="79c2f-107">Statistiken innehåller antalet byte som skickas och tas emot via både primära och sekundära vägar.</span><span class="sxs-lookup"><span data-stu-id="79c2f-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="79c2f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79c2f-108">EXAMPLES</span></span>

### <span data-ttu-id="79c2f-109">Exempel 1: Visa trafik statistik för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="79c2f-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="79c2f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="79c2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c2f-111">-DefaultProfile</span></span>
<span data-ttu-id="79c2f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79c2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c2f-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="79c2f-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="79c2f-114">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="79c2f-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c2f-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="79c2f-115">-PeeringType</span></span>
<span data-ttu-id="79c2f-116">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="79c2f-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="79c2f-118">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="79c2f-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c2f-119">CommonParameters</span></span>
<span data-ttu-id="79c2f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c2f-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c2f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c2f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79c2f-122">INPUTS</span></span>

## <span data-ttu-id="79c2f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79c2f-123">OUTPUTS</span></span>

### <span data-ttu-id="79c2f-124">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="79c2f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="79c2f-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79c2f-125">NOTES</span></span>

## <span data-ttu-id="79c2f-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79c2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="79c2f-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="79c2f-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="79c2f-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c2f-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="79c2f-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="79c2f-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
