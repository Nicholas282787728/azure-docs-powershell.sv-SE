---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 12c920d0bacc6bd214e6ebe8d374a80d2b50a072
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089107"
---
# <span data-ttu-id="4aed9-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4aed9-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="4aed9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4aed9-102">SYNOPSIS</span></span>
<span data-ttu-id="4aed9-103">Hämtar ARP-tabellen från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="4aed9-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4aed9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4aed9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4aed9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4aed9-105">DESCRIPTION</span></span>
<span data-ttu-id="4aed9-106">Cmdleten **Get-AzExpressRouteCircuitARPTable** hämtar ARP-tabellen från båda gränssnitten av en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="4aed9-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="4aed9-107">ARP-tabellen tillhandahåller en mappning av IPv4-adress till MAC-adress för en viss peering.</span><span class="sxs-lookup"><span data-stu-id="4aed9-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="4aed9-108">Du kan använda ARP-tabellen för att verifiera nivå 2-konfiguration och anslutning.</span><span class="sxs-lookup"><span data-stu-id="4aed9-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="4aed9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4aed9-109">EXAMPLES</span></span>

### <span data-ttu-id="4aed9-110">Exempel 1: Visa ARP-tabellen för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="4aed9-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="4aed9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4aed9-111">PARAMETERS</span></span>

### <span data-ttu-id="4aed9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aed9-112">-DefaultProfile</span></span>
<span data-ttu-id="4aed9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4aed9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aed9-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="4aed9-114">-DevicePath</span></span>
<span data-ttu-id="4aed9-115">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="4aed9-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aed9-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="4aed9-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="4aed9-117">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="4aed9-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aed9-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4aed9-118">-PeeringType</span></span>
<span data-ttu-id="4aed9-119">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4aed9-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aed9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aed9-120">-ResourceGroupName</span></span>
<span data-ttu-id="4aed9-121">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="4aed9-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aed9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aed9-122">CommonParameters</span></span>
<span data-ttu-id="4aed9-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aed9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aed9-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aed9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aed9-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4aed9-125">INPUTS</span></span>

### <span data-ttu-id="4aed9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4aed9-126">System.String</span></span>

## <span data-ttu-id="4aed9-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4aed9-127">OUTPUTS</span></span>

### <span data-ttu-id="4aed9-128">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="4aed9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="4aed9-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4aed9-129">NOTES</span></span>

## <span data-ttu-id="4aed9-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4aed9-130">RELATED LINKS</span></span>

[<span data-ttu-id="4aed9-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4aed9-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="4aed9-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4aed9-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="4aed9-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="4aed9-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
