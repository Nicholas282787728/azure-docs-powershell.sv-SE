---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 4577eb4f105bca235e7b5e9feb0b0ef308298881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755489"
---
# <span data-ttu-id="471df-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="471df-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="471df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="471df-102">SYNOPSIS</span></span>
<span data-ttu-id="471df-103">Får användnings statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="471df-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="471df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="471df-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="471df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="471df-105">DESCRIPTION</span></span>
<span data-ttu-id="471df-106">Cmdleten **Get-AzureRmExpressRouteCircuitStats** hämtar trafik statistik för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="471df-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="471df-107">Statistiken innehåller antalet byte som skickas och tas emot via både primära och sekundära vägar.</span><span class="sxs-lookup"><span data-stu-id="471df-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="471df-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="471df-108">EXAMPLES</span></span>

### <span data-ttu-id="471df-109">Exempel 1: Visa trafik statistik för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="471df-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="471df-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="471df-110">PARAMETERS</span></span>

### <span data-ttu-id="471df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471df-111">-DefaultProfile</span></span>
<span data-ttu-id="471df-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="471df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471df-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="471df-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="471df-114">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="471df-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="471df-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="471df-115">-PeeringType</span></span>
<span data-ttu-id="471df-116">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="471df-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="471df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471df-117">-ResourceGroupName</span></span>
<span data-ttu-id="471df-118">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="471df-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="471df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471df-119">CommonParameters</span></span>
<span data-ttu-id="471df-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471df-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471df-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471df-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="471df-122">INPUTS</span></span>

### <span data-ttu-id="471df-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="471df-123">None</span></span>
<span data-ttu-id="471df-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="471df-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="471df-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="471df-125">OUTPUTS</span></span>

### <span data-ttu-id="471df-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="471df-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="471df-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="471df-127">NOTES</span></span>

## <span data-ttu-id="471df-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="471df-128">RELATED LINKS</span></span>

[<span data-ttu-id="471df-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="471df-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="471df-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="471df-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="471df-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="471df-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)