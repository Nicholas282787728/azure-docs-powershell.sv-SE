---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 590f4021fc935966e636ce92359449ea8632349a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757861"
---
# <span data-ttu-id="00f60-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="00f60-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="00f60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00f60-102">SYNOPSIS</span></span>
<span data-ttu-id="00f60-103">Hämtar en routningstabell från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="00f60-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00f60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00f60-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00f60-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00f60-105">DESCRIPTION</span></span>
<span data-ttu-id="00f60-106">Cmdleten **Get-AzureRmExpressRouteCircuitRouteTable** hämtar en detaljerad vägkälla för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="00f60-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="00f60-107">Routningstabellen visar alla vägar eller kan filtreras för att Visa vägar för en viss peering-typ.</span><span class="sxs-lookup"><span data-stu-id="00f60-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="00f60-108">Du kan använda routningstabellen för att validera din konfiguration och anslutnings barhet för din peering.</span><span class="sxs-lookup"><span data-stu-id="00f60-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="00f60-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00f60-109">EXAMPLES</span></span>

### <span data-ttu-id="00f60-110">Exempel 1: Visa routningstabellen för den primära sökvägen</span><span class="sxs-lookup"><span data-stu-id="00f60-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="00f60-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00f60-111">PARAMETERS</span></span>

### <span data-ttu-id="00f60-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f60-112">-DefaultProfile</span></span>
<span data-ttu-id="00f60-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00f60-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00f60-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="00f60-114">-DevicePath</span></span>
<span data-ttu-id="00f60-115">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="00f60-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="00f60-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="00f60-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="00f60-117">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="00f60-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="00f60-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="00f60-118">-PeeringType</span></span>
<span data-ttu-id="00f60-119">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="00f60-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="00f60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f60-120">-ResourceGroupName</span></span>
<span data-ttu-id="00f60-121">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="00f60-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="00f60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f60-122">CommonParameters</span></span>
<span data-ttu-id="00f60-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f60-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f60-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f60-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00f60-125">INPUTS</span></span>

### <span data-ttu-id="00f60-126">System. String</span><span class="sxs-lookup"><span data-stu-id="00f60-126">System.String</span></span>

## <span data-ttu-id="00f60-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00f60-127">OUTPUTS</span></span>

### <span data-ttu-id="00f60-128">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="00f60-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="00f60-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00f60-129">NOTES</span></span>

## <span data-ttu-id="00f60-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00f60-130">RELATED LINKS</span></span>

[<span data-ttu-id="00f60-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="00f60-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="00f60-132">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="00f60-132">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="00f60-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="00f60-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
