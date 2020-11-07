---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 380a5f52a520f487e625663f7d84cbbc55564db5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756245"
---
# <span data-ttu-id="9b683-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b683-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="9b683-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b683-102">SYNOPSIS</span></span>
<span data-ttu-id="9b683-103">Hämtar en Azure ExpressRoute-krets från Azure.</span><span class="sxs-lookup"><span data-stu-id="9b683-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b683-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b683-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b683-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b683-105">DESCRIPTION</span></span>
<span data-ttu-id="9b683-106">Cmdleten **Get-AzureRmExpressRouteCircuit** används för att hämta ett ExpressRoute-kretskort från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9b683-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="9b683-107">Det kretsar som returneras kan användas som indata för andra cmdlets som fungerar på ExpressRoute-kretsar.</span><span class="sxs-lookup"><span data-stu-id="9b683-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="9b683-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b683-108">EXAMPLES</span></span>

### <span data-ttu-id="9b683-109">Exempel 1: få ExpressRoute-kretsen att tas bort</span><span class="sxs-lookup"><span data-stu-id="9b683-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="9b683-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b683-110">PARAMETERS</span></span>

### <span data-ttu-id="9b683-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b683-111">-DefaultProfile</span></span>
<span data-ttu-id="9b683-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b683-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b683-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b683-113">-Name</span></span>
<span data-ttu-id="9b683-114">Namnet på ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="9b683-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="9b683-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b683-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b683-116">Namnet på resurs gruppen som innehåller ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="9b683-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="9b683-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b683-117">CommonParameters</span></span>
<span data-ttu-id="9b683-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b683-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b683-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b683-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b683-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b683-120">INPUTS</span></span>

### <span data-ttu-id="9b683-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="9b683-121">None</span></span>
<span data-ttu-id="9b683-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9b683-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b683-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b683-123">OUTPUTS</span></span>

### <span data-ttu-id="9b683-124">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b683-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9b683-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b683-125">NOTES</span></span>

## <span data-ttu-id="9b683-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b683-126">RELATED LINKS</span></span>

[<span data-ttu-id="9b683-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b683-127">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9b683-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b683-128">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9b683-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b683-129">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9b683-130">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b683-130">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
