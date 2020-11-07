---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922297"
---
# <span data-ttu-id="e6db5-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6db5-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="e6db5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6db5-102">SYNOPSIS</span></span>
<span data-ttu-id="e6db5-103">Hämtar en Azure ExpressRoute-krets från Azure.</span><span class="sxs-lookup"><span data-stu-id="e6db5-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="e6db5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6db5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6db5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6db5-105">DESCRIPTION</span></span>
<span data-ttu-id="e6db5-106">Cmdleten **Get-AzExpressRouteCircuit** används för att hämta ett ExpressRoute-kretskort från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e6db5-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="e6db5-107">Det kretsar som returneras kan användas som indata för andra cmdlets som fungerar på ExpressRoute-kretsar.</span><span class="sxs-lookup"><span data-stu-id="e6db5-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="e6db5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6db5-108">EXAMPLES</span></span>

### <span data-ttu-id="e6db5-109">Exempel 1: få ExpressRoute-kretsen att tas bort</span><span class="sxs-lookup"><span data-stu-id="e6db5-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="e6db5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6db5-110">PARAMETERS</span></span>

### <span data-ttu-id="e6db5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6db5-111">-DefaultProfile</span></span>
<span data-ttu-id="e6db5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6db5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6db5-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6db5-113">-Name</span></span>
<span data-ttu-id="e6db5-114">Namnet på ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="e6db5-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e6db5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6db5-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6db5-116">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="e6db5-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e6db5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6db5-117">CommonParameters</span></span>
<span data-ttu-id="e6db5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6db5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6db5-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6db5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6db5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6db5-120">INPUTS</span></span>

## <span data-ttu-id="e6db5-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6db5-121">OUTPUTS</span></span>

### <span data-ttu-id="e6db5-122">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6db5-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e6db5-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6db5-123">NOTES</span></span>

## <span data-ttu-id="e6db5-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6db5-124">RELATED LINKS</span></span>

[<span data-ttu-id="e6db5-125">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6db5-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="e6db5-126">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6db5-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="e6db5-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6db5-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="e6db5-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6db5-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
