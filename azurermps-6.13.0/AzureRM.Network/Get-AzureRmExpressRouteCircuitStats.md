---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: d9978c50186b520d8e956dc20581d1ceb615b673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757855"
---
# <span data-ttu-id="5f8c9-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="5f8c9-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="5f8c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8c9-103">Får användnings statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f8c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f8c9-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f8c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f8c9-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8c9-106">Cmdleten **Get-AzureRmExpressRouteCircuitStats** hämtar trafik statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="5f8c9-107">Statistiken innehåller antalet byte som skickas och tas emot via både primära och sekundära vägar.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="5f8c9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f8c9-108">EXAMPLES</span></span>

### <span data-ttu-id="5f8c9-109">Exempel 1: Visa trafik statistik för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="5f8c9-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="5f8c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f8c9-110">PARAMETERS</span></span>

### <span data-ttu-id="5f8c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8c9-111">-DefaultProfile</span></span>
<span data-ttu-id="5f8c9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f8c9-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="5f8c9-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="5f8c9-114">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="5f8c9-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5f8c9-115">-PeeringType</span></span>
<span data-ttu-id="5f8c9-116">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5f8c9-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5f8c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f8c9-118">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="5f8c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8c9-119">CommonParameters</span></span>
<span data-ttu-id="5f8c9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8c9-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8c9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8c9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f8c9-122">INPUTS</span></span>

### <span data-ttu-id="5f8c9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5f8c9-123">System.String</span></span>

## <span data-ttu-id="5f8c9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f8c9-124">OUTPUTS</span></span>

### <span data-ttu-id="5f8c9-125">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="5f8c9-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="5f8c9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f8c9-126">NOTES</span></span>

## <span data-ttu-id="5f8c9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f8c9-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f8c9-128">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5f8c9-128">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5f8c9-129">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5f8c9-129">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="5f8c9-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5f8c9-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
