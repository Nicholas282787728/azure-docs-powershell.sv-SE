---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748295"
---
# <span data-ttu-id="13a6e-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="13a6e-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="13a6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="13a6e-103">Hämtar en lista ExpressRoute tjänste leverantörer och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="13a6e-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="13a6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13a6e-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13a6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13a6e-105">DESCRIPTION</span></span>
<span data-ttu-id="13a6e-106">Cmdleten **Get-AzExpressRouteServiceProvider** hämtar en List ExpressRoute och deras attribut.</span><span class="sxs-lookup"><span data-stu-id="13a6e-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="13a6e-107">Attribut inkluderar alternativ för plats och bandbredd.</span><span class="sxs-lookup"><span data-stu-id="13a6e-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="13a6e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13a6e-108">EXAMPLES</span></span>

### <span data-ttu-id="13a6e-109">Exempel 1: skaffa en lista över tjänste leverantörer med platser i "Silicon dal"</span><span class="sxs-lookup"><span data-stu-id="13a6e-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="13a6e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13a6e-110">PARAMETERS</span></span>

### <span data-ttu-id="13a6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a6e-111">-DefaultProfile</span></span>
<span data-ttu-id="13a6e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13a6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13a6e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a6e-113">CommonParameters</span></span>
<span data-ttu-id="13a6e-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a6e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a6e-115">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13a6e-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a6e-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13a6e-116">INPUTS</span></span>

### <span data-ttu-id="13a6e-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="13a6e-117">None</span></span>

## <span data-ttu-id="13a6e-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13a6e-118">OUTPUTS</span></span>

### <span data-ttu-id="13a6e-119">Microsoft. Azure. commands. Networks. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="13a6e-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="13a6e-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13a6e-120">NOTES</span></span>

## <span data-ttu-id="13a6e-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13a6e-121">RELATED LINKS</span></span>

[<span data-ttu-id="13a6e-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="13a6e-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="13a6e-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="13a6e-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="13a6e-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="13a6e-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="13a6e-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="13a6e-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)