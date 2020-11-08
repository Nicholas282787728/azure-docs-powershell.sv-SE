---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
ms.openlocfilehash: bdfb86eb53221466beca2566d8ea446072ea33d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929390"
---
# <span data-ttu-id="a78df-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a78df-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="a78df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a78df-102">SYNOPSIS</span></span>
<span data-ttu-id="a78df-103">Hämtar ARP-tabellen från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="a78df-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a78df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a78df-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a78df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a78df-105">DESCRIPTION</span></span>
<span data-ttu-id="a78df-106">Cmdleten **Get-AzureRmExpressRouteCircuitARPTable** hämtar ARP-tabellen från båda gränssnitten av en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="a78df-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="a78df-107">ARP-tabellen tillhandahåller en mappning av IPv4-adress till MAC-adress för en viss peering.</span><span class="sxs-lookup"><span data-stu-id="a78df-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="a78df-108">Du kan använda ARP-tabellen för att verifiera nivå 2-konfiguration och anslutning.</span><span class="sxs-lookup"><span data-stu-id="a78df-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="a78df-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a78df-109">EXAMPLES</span></span>

### <span data-ttu-id="a78df-110">Exempel 1: Visa ARP-tabellen för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="a78df-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="a78df-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a78df-111">PARAMETERS</span></span>

### <span data-ttu-id="a78df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78df-112">-DefaultProfile</span></span>
<span data-ttu-id="a78df-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a78df-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a78df-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a78df-114">-DevicePath</span></span>
<span data-ttu-id="a78df-115">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a78df-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78df-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a78df-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a78df-117">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="a78df-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a78df-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a78df-118">-PeeringType</span></span>
<span data-ttu-id="a78df-119">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a78df-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a78df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78df-120">-ResourceGroupName</span></span>
<span data-ttu-id="a78df-121">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="a78df-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a78df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78df-122">CommonParameters</span></span>
<span data-ttu-id="a78df-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78df-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a78df-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78df-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a78df-125">INPUTS</span></span>

## <span data-ttu-id="a78df-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a78df-126">OUTPUTS</span></span>

### <span data-ttu-id="a78df-127">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="a78df-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="a78df-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a78df-128">NOTES</span></span>

## <span data-ttu-id="a78df-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a78df-129">RELATED LINKS</span></span>

[<span data-ttu-id="a78df-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a78df-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a78df-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a78df-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="a78df-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a78df-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)