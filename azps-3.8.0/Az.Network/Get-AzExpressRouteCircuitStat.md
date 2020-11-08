---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091101"
---
# <span data-ttu-id="88b2d-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="88b2d-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="88b2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="88b2d-103">Får användnings statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="88b2d-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="88b2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88b2d-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="88b2d-106">Cmdleten **Get-AzExpressRouteCircuitStat** hämtar trafik statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="88b2d-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="88b2d-107">Statistiken innehåller antalet byte som skickas och tas emot via både primära och sekundära vägar.</span><span class="sxs-lookup"><span data-stu-id="88b2d-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="88b2d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88b2d-108">EXAMPLES</span></span>

### <span data-ttu-id="88b2d-109">Exempel 1: Visa trafik statistik för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="88b2d-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="88b2d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88b2d-110">PARAMETERS</span></span>

### <span data-ttu-id="88b2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b2d-111">-DefaultProfile</span></span>
<span data-ttu-id="88b2d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88b2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88b2d-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="88b2d-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="88b2d-114">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="88b2d-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="88b2d-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="88b2d-115">-PeeringType</span></span>
<span data-ttu-id="88b2d-116">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="88b2d-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="88b2d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b2d-117">-ResourceGroupName</span></span>
<span data-ttu-id="88b2d-118">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="88b2d-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="88b2d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b2d-119">CommonParameters</span></span>
<span data-ttu-id="88b2d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b2d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b2d-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b2d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b2d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88b2d-122">INPUTS</span></span>

### <span data-ttu-id="88b2d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="88b2d-123">System.String</span></span>

## <span data-ttu-id="88b2d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88b2d-124">OUTPUTS</span></span>

### <span data-ttu-id="88b2d-125">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="88b2d-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="88b2d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88b2d-126">NOTES</span></span>

## <span data-ttu-id="88b2d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88b2d-127">RELATED LINKS</span></span>

[<span data-ttu-id="88b2d-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="88b2d-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="88b2d-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="88b2d-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="88b2d-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="88b2d-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
