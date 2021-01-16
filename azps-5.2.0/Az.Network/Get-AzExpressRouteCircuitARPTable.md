---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 1c59ef12964ddd022add01ae296b8ecac9ad0acd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387657"
---
# <span data-ttu-id="46bf5-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="46bf5-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="46bf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="46bf5-103">Hämtar ARP-tabellen från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="46bf5-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="46bf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46bf5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46bf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="46bf5-106">Cmdleten **Get-AzExpressRouteCircuitARPTable** hämtar ARP-tabellen från båda gränssnitten av en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="46bf5-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="46bf5-107">ARP-tabellen tillhandahåller en mappning av IPv4-adress till MAC-adress för en viss peering.</span><span class="sxs-lookup"><span data-stu-id="46bf5-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="46bf5-108">Du kan använda ARP-tabellen för att verifiera nivå 2-konfiguration och anslutning.</span><span class="sxs-lookup"><span data-stu-id="46bf5-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="46bf5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="46bf5-110">Exempel 1: Visa ARP-tabellen för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="46bf5-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="46bf5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46bf5-111">PARAMETERS</span></span>

### <span data-ttu-id="46bf5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bf5-112">-DefaultProfile</span></span>
<span data-ttu-id="46bf5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46bf5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46bf5-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="46bf5-114">-DevicePath</span></span>
<span data-ttu-id="46bf5-115">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="46bf5-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="46bf5-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="46bf5-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="46bf5-117">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="46bf5-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="46bf5-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="46bf5-118">-PeeringType</span></span>
<span data-ttu-id="46bf5-119">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="46bf5-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="46bf5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46bf5-120">-ResourceGroupName</span></span>
<span data-ttu-id="46bf5-121">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="46bf5-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="46bf5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bf5-122">CommonParameters</span></span>
<span data-ttu-id="46bf5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46bf5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bf5-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46bf5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bf5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46bf5-125">INPUTS</span></span>

### <span data-ttu-id="46bf5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="46bf5-126">System.String</span></span>

## <span data-ttu-id="46bf5-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46bf5-127">OUTPUTS</span></span>

### <span data-ttu-id="46bf5-128">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="46bf5-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="46bf5-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46bf5-129">NOTES</span></span>

## <span data-ttu-id="46bf5-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46bf5-130">RELATED LINKS</span></span>

[<span data-ttu-id="46bf5-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="46bf5-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="46bf5-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46bf5-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="46bf5-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="46bf5-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
