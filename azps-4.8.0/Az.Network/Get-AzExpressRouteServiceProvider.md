---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261876"
---
# <span data-ttu-id="3912d-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="3912d-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="3912d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3912d-102">SYNOPSIS</span></span>
<span data-ttu-id="3912d-103">Hämtar en lista ExpressRoute tjänste leverantörer och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="3912d-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="3912d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3912d-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3912d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3912d-105">DESCRIPTION</span></span>
<span data-ttu-id="3912d-106">Cmdleten **Get-AzExpressRouteServiceProvider** hämtar en List ExpressRoute och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="3912d-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="3912d-107">Attribut inkluderar alternativ för plats och bandbredd.</span><span class="sxs-lookup"><span data-stu-id="3912d-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="3912d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3912d-108">EXAMPLES</span></span>

### <span data-ttu-id="3912d-109">Exempel 1: skaffa en lista över tjänste leverantörer med platser i "Silicon dal"</span><span class="sxs-lookup"><span data-stu-id="3912d-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="3912d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3912d-110">PARAMETERS</span></span>

### <span data-ttu-id="3912d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3912d-111">-DefaultProfile</span></span>
<span data-ttu-id="3912d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3912d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3912d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3912d-113">CommonParameters</span></span>
<span data-ttu-id="3912d-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3912d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3912d-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3912d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3912d-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3912d-116">INPUTS</span></span>

### <span data-ttu-id="3912d-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="3912d-117">None</span></span>

## <span data-ttu-id="3912d-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3912d-118">OUTPUTS</span></span>

### <span data-ttu-id="3912d-119">Microsoft. Azure. commands. Networks. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="3912d-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="3912d-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3912d-120">NOTES</span></span>

## <span data-ttu-id="3912d-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3912d-121">RELATED LINKS</span></span>

[<span data-ttu-id="3912d-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3912d-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="3912d-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3912d-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="3912d-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3912d-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="3912d-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="3912d-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
