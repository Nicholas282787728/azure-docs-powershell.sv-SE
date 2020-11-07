---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 5042f7055c9d74dcabc01aa81169c9290816953c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922282"
---
# <span data-ttu-id="bcdbd-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bcdbd-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="bcdbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdbd-103">Hämtar en väg tabells Sammanfattning av en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="bcdbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcdbd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcdbd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcdbd-105">DESCRIPTION</span></span>
<span data-ttu-id="bcdbd-106">Cmdleten **Get-AzExpressRouteCircuitRouteTableSummary** returnerar en sammanfattning av BGP Neighbor-informationen för en viss kontext för routning.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="bcdbd-107">Den här informationen är användbar för att avgöra hur länge en routningsdomän har upprättats och antalet väg-prefix som annonseras av peering router.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="bcdbd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcdbd-108">EXAMPLES</span></span>

### <span data-ttu-id="bcdbd-109">Exempel 1: Visa väg översikten för den primära sökvägen</span><span class="sxs-lookup"><span data-stu-id="bcdbd-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="bcdbd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcdbd-110">PARAMETERS</span></span>

### <span data-ttu-id="bcdbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdbd-111">-DefaultProfile</span></span>
<span data-ttu-id="bcdbd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcdbd-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="bcdbd-113">-DevicePath</span></span>
<span data-ttu-id="bcdbd-114">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="bcdbd-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="bcdbd-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="bcdbd-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="bcdbd-116">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="bcdbd-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="bcdbd-117">-PeeringType</span></span>
<span data-ttu-id="bcdbd-118">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="bcdbd-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="bcdbd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdbd-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcdbd-120">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="bcdbd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdbd-121">CommonParameters</span></span>
<span data-ttu-id="bcdbd-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdbd-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcdbd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdbd-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcdbd-124">INPUTS</span></span>

## <span data-ttu-id="bcdbd-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcdbd-125">OUTPUTS</span></span>

### <span data-ttu-id="bcdbd-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="bcdbd-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="bcdbd-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcdbd-127">NOTES</span></span>

## <span data-ttu-id="bcdbd-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcdbd-128">RELATED LINKS</span></span>

[<span data-ttu-id="bcdbd-129">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bcdbd-129">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="bcdbd-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bcdbd-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="bcdbd-131">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="bcdbd-131">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
