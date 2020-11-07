---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929393"
---
# <span data-ttu-id="9fbe7-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fbe7-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="9fbe7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fbe7-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbe7-103">Hämtar en Azure ExpressRoute-krets från Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fbe7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fbe7-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fbe7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fbe7-105">DESCRIPTION</span></span>
<span data-ttu-id="9fbe7-106">Cmdleten **Get-AzureRmExpressRouteCircuit** används för att hämta ett ExpressRoute-kretskort från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="9fbe7-107">Det kretsar som returneras kan användas som indata för andra cmdlets som fungerar på ExpressRoute-kretsar.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="9fbe7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fbe7-108">EXAMPLES</span></span>

### <span data-ttu-id="9fbe7-109">Exempel 1: få ExpressRoute-kretsen att tas bort</span><span class="sxs-lookup"><span data-stu-id="9fbe7-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="9fbe7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fbe7-110">PARAMETERS</span></span>

### <span data-ttu-id="9fbe7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbe7-111">-DefaultProfile</span></span>
<span data-ttu-id="9fbe7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fbe7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9fbe7-113">-Name</span></span>
<span data-ttu-id="9fbe7-114">Namnet på ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbe7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbe7-115">-ResourceGroupName</span></span>
<span data-ttu-id="9fbe7-116">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbe7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbe7-117">CommonParameters</span></span>
<span data-ttu-id="9fbe7-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbe7-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbe7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbe7-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fbe7-120">INPUTS</span></span>

## <span data-ttu-id="9fbe7-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fbe7-121">OUTPUTS</span></span>

### <span data-ttu-id="9fbe7-122">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fbe7-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9fbe7-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fbe7-123">NOTES</span></span>

## <span data-ttu-id="9fbe7-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fbe7-124">RELATED LINKS</span></span>

[<span data-ttu-id="9fbe7-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fbe7-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9fbe7-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fbe7-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9fbe7-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fbe7-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9fbe7-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fbe7-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
