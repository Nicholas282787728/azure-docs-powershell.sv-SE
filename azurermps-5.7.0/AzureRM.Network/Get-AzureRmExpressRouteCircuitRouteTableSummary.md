---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 849fb653308537a3d37740a21ba8b488903406ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578144"
---
# <span data-ttu-id="3b5fa-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3b5fa-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="3b5fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5fa-103">Hämtar en väg tabells Sammanfattning av en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b5fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b5fa-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b5fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5fa-106">Cmdleten **Get-AzureRmExpressRouteCircuitRouteTableSummary** returnerar en sammanfattning av BGP Neighbor-informationen för en viss kontext för routning.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="3b5fa-107">Den här informationen är användbar för att avgöra hur länge en routningsdomän har upprättats och antalet väg-prefix som annonseras av peering router.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="3b5fa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b5fa-108">EXAMPLES</span></span>

### <span data-ttu-id="3b5fa-109">Exempel 1: Visa väg översikten för den primära sökvägen</span><span class="sxs-lookup"><span data-stu-id="3b5fa-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="3b5fa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b5fa-110">PARAMETERS</span></span>

### <span data-ttu-id="3b5fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5fa-111">-DefaultProfile</span></span>
<span data-ttu-id="3b5fa-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b5fa-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="3b5fa-113">-DevicePath</span></span>
<span data-ttu-id="3b5fa-114">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="3b5fa-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="3b5fa-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="3b5fa-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="3b5fa-116">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="3b5fa-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3b5fa-117">-PeeringType</span></span>
<span data-ttu-id="3b5fa-118">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3b5fa-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3b5fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="3b5fa-120">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="3b5fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5fa-121">CommonParameters</span></span>
<span data-ttu-id="3b5fa-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5fa-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5fa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5fa-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b5fa-124">INPUTS</span></span>

### <span data-ttu-id="3b5fa-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b5fa-125">None</span></span>
<span data-ttu-id="3b5fa-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3b5fa-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b5fa-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b5fa-127">OUTPUTS</span></span>

### <span data-ttu-id="3b5fa-128">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="3b5fa-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="3b5fa-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b5fa-129">NOTES</span></span>

## <span data-ttu-id="3b5fa-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b5fa-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b5fa-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3b5fa-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="3b5fa-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3b5fa-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="3b5fa-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="3b5fa-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
