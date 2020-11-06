---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 9d221f5ff25e43a750f939f80eae7a7878eacc44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577156"
---
# <span data-ttu-id="8877e-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8877e-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="8877e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8877e-102">SYNOPSIS</span></span>
<span data-ttu-id="8877e-103">Hämtar en routningstabell från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="8877e-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8877e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8877e-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8877e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8877e-105">DESCRIPTION</span></span>
<span data-ttu-id="8877e-106">Cmdleten **Get-AzureRmExpressRouteCircuitRouteTable** hämtar en detaljerad vägkälla för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="8877e-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="8877e-107">Routningstabellen visar alla vägar eller kan filtreras för att Visa vägar för en viss peering-typ.</span><span class="sxs-lookup"><span data-stu-id="8877e-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="8877e-108">Du kan använda routningstabellen för att validera din konfiguration och anslutnings barhet för din peering.</span><span class="sxs-lookup"><span data-stu-id="8877e-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="8877e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8877e-109">EXAMPLES</span></span>

### <span data-ttu-id="8877e-110">Exempel 1: Visa routningstabellen för den primära sökvägen</span><span class="sxs-lookup"><span data-stu-id="8877e-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="8877e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8877e-111">PARAMETERS</span></span>

### <span data-ttu-id="8877e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8877e-112">-DefaultProfile</span></span>
<span data-ttu-id="8877e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8877e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8877e-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="8877e-114">-DevicePath</span></span>
<span data-ttu-id="8877e-115">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8877e-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8877e-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="8877e-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="8877e-117">Namnet på den ExpressRoute-krets som unders öks.</span><span class="sxs-lookup"><span data-stu-id="8877e-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="8877e-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8877e-118">-PeeringType</span></span>
<span data-ttu-id="8877e-119">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8877e-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8877e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8877e-120">-ResourceGroupName</span></span>
<span data-ttu-id="8877e-121">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="8877e-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="8877e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8877e-122">CommonParameters</span></span>
<span data-ttu-id="8877e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8877e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8877e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8877e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8877e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8877e-125">INPUTS</span></span>

### <span data-ttu-id="8877e-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="8877e-126">None</span></span>
<span data-ttu-id="8877e-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8877e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8877e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8877e-128">OUTPUTS</span></span>

### <span data-ttu-id="8877e-129">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="8877e-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="8877e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8877e-130">NOTES</span></span>

## <span data-ttu-id="8877e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8877e-131">RELATED LINKS</span></span>

[<span data-ttu-id="8877e-132">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8877e-132">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="8877e-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8877e-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="8877e-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="8877e-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
