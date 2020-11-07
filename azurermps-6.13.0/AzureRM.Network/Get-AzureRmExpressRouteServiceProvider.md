---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: 0c7beb4bc53635a8bf4293abf50441b0f15b66b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757850"
---
# <span data-ttu-id="b609d-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b609d-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b609d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b609d-102">SYNOPSIS</span></span>
<span data-ttu-id="b609d-103">Hämtar en lista ExpressRoute tjänste leverantörer och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="b609d-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b609d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b609d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b609d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b609d-105">DESCRIPTION</span></span>
<span data-ttu-id="b609d-106">Cmdleten **Get-AzureRmExpressRouteServiceProvider** hämtar en List ExpressRoute och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="b609d-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="b609d-107">Attribut inkluderar alternativ för plats och bandbredd.</span><span class="sxs-lookup"><span data-stu-id="b609d-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="b609d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b609d-108">EXAMPLES</span></span>

### <span data-ttu-id="b609d-109">Exempel 1: skaffa en lista över tjänste leverantörer med platser i "Silicon dal"</span><span class="sxs-lookup"><span data-stu-id="b609d-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="b609d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b609d-110">PARAMETERS</span></span>

### <span data-ttu-id="b609d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b609d-111">-DefaultProfile</span></span>
<span data-ttu-id="b609d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b609d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b609d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b609d-113">CommonParameters</span></span>
<span data-ttu-id="b609d-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b609d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b609d-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b609d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b609d-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b609d-116">INPUTS</span></span>

### <span data-ttu-id="b609d-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="b609d-117">None</span></span>

## <span data-ttu-id="b609d-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b609d-118">OUTPUTS</span></span>

### <span data-ttu-id="b609d-119">Microsoft. Azure. commands. Networks. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b609d-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b609d-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b609d-120">NOTES</span></span>

## <span data-ttu-id="b609d-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b609d-121">RELATED LINKS</span></span>

[<span data-ttu-id="b609d-122">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b609d-122">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b609d-123">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b609d-123">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b609d-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b609d-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b609d-125">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="b609d-125">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)