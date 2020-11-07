---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 969d7c5f55d210cdff74066d08af50bbcc47181e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756157"
---
# <span data-ttu-id="b02de-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b02de-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="b02de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b02de-102">SYNOPSIS</span></span>
<span data-ttu-id="b02de-103">Hämtar en Azure ExpressRoute-krets från Azure.</span><span class="sxs-lookup"><span data-stu-id="b02de-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b02de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b02de-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b02de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b02de-105">DESCRIPTION</span></span>
<span data-ttu-id="b02de-106">Cmdleten **Get-AzureRmExpressRouteCircuit** används för att hämta ett ExpressRoute-kretskort från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b02de-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="b02de-107">Det kretsar som returneras kan användas som indata för andra cmdlets som fungerar på ExpressRoute-kretsar.</span><span class="sxs-lookup"><span data-stu-id="b02de-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="b02de-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b02de-108">EXAMPLES</span></span>

### <span data-ttu-id="b02de-109">Exempel 1: få ExpressRoute-kretsen att tas bort</span><span class="sxs-lookup"><span data-stu-id="b02de-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="b02de-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b02de-110">PARAMETERS</span></span>

### <span data-ttu-id="b02de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02de-111">-DefaultProfile</span></span>
<span data-ttu-id="b02de-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b02de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b02de-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b02de-113">-Name</span></span>
<span data-ttu-id="b02de-114">Namnet på ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="b02de-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02de-115">-ResourceGroupName</span></span>
<span data-ttu-id="b02de-116">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="b02de-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02de-117">CommonParameters</span></span>
<span data-ttu-id="b02de-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02de-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02de-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02de-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b02de-120">INPUTS</span></span>

### <span data-ttu-id="b02de-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b02de-121">System.String</span></span>

## <span data-ttu-id="b02de-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b02de-122">OUTPUTS</span></span>

### <span data-ttu-id="b02de-123">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b02de-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b02de-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b02de-124">NOTES</span></span>

## <span data-ttu-id="b02de-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b02de-125">RELATED LINKS</span></span>

[<span data-ttu-id="b02de-126">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b02de-126">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b02de-127">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b02de-127">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b02de-128">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b02de-128">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b02de-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b02de-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
