---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523401"
---
# <span data-ttu-id="8e2fd-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8e2fd-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="8e2fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2fd-103">Hämtar en lista ExpressRoute tjänste leverantörer och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="8e2fd-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="8e2fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e2fd-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e2fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e2fd-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2fd-106">Cmdleten **Get-AzExpressRouteServiceProvider** hämtar en List ExpressRoute och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="8e2fd-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="8e2fd-107">Attribut inkluderar alternativ för plats och bandbredd.</span><span class="sxs-lookup"><span data-stu-id="8e2fd-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="8e2fd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e2fd-108">EXAMPLES</span></span>

### <span data-ttu-id="8e2fd-109">Exempel 1: skaffa en lista över tjänste leverantörer med platser i "Silicon dal"</span><span class="sxs-lookup"><span data-stu-id="8e2fd-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="8e2fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e2fd-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2fd-111">-DefaultProfile</span></span>
<span data-ttu-id="8e2fd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e2fd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2fd-113">CommonParameters</span></span>
<span data-ttu-id="8e2fd-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2fd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2fd-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e2fd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2fd-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e2fd-116">INPUTS</span></span>

### <span data-ttu-id="8e2fd-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="8e2fd-117">None</span></span>

## <span data-ttu-id="8e2fd-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e2fd-118">OUTPUTS</span></span>

### <span data-ttu-id="8e2fd-119">Microsoft. Azure. commands. Networks. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8e2fd-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="8e2fd-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e2fd-120">NOTES</span></span>

## <span data-ttu-id="8e2fd-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e2fd-121">RELATED LINKS</span></span>

[<span data-ttu-id="8e2fd-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8e2fd-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="8e2fd-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e2fd-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="8e2fd-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8e2fd-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="8e2fd-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="8e2fd-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
