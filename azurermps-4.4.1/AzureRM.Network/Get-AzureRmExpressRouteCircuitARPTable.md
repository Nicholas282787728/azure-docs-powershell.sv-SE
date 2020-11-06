---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e306faae861b8f35bff3695dc4235394764621a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574597"
---
# <span data-ttu-id="75921-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="75921-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="75921-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75921-102">SYNOPSIS</span></span>
<span data-ttu-id="75921-103">Hämtar ARP-tabellen från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="75921-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75921-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75921-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75921-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75921-105">DESCRIPTION</span></span>
<span data-ttu-id="75921-106">Cmdleten **Get-AzureRmExpressRouteCircuitARPTable** hämtar ARP-tabellen från båda gränssnitten av en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="75921-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="75921-107">ARP-tabellen tillhandahåller en mappning av IPv4-adress till MAC-adress för en viss peering.</span><span class="sxs-lookup"><span data-stu-id="75921-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="75921-108">Du kan använda ARP-tabellen för att verifiera nivå 2-konfiguration och anslutning.</span><span class="sxs-lookup"><span data-stu-id="75921-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="75921-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75921-109">EXAMPLES</span></span>

### <span data-ttu-id="75921-110">Exempel 1: Visa ARP-tabellen för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="75921-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="75921-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75921-111">PARAMETERS</span></span>

### <span data-ttu-id="75921-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="75921-112">-DevicePath</span></span>
<span data-ttu-id="75921-113">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="75921-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="75921-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="75921-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="75921-115">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="75921-115">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="75921-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="75921-116">-PeeringType</span></span>
<span data-ttu-id="75921-117">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="75921-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75921-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75921-118">-ResourceGroupName</span></span>
<span data-ttu-id="75921-119">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="75921-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="75921-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75921-120">-DefaultProfile</span></span>
<span data-ttu-id="75921-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75921-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75921-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75921-122">CommonParameters</span></span>
<span data-ttu-id="75921-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75921-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75921-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75921-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75921-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75921-125">INPUTS</span></span>

## <span data-ttu-id="75921-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75921-126">OUTPUTS</span></span>

### <span data-ttu-id="75921-127">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="75921-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="75921-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75921-128">NOTES</span></span>

## <span data-ttu-id="75921-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75921-129">RELATED LINKS</span></span>

[<span data-ttu-id="75921-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="75921-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="75921-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="75921-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="75921-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="75921-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
