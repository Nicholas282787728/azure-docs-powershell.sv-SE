---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584947"
---
# <span data-ttu-id="eea78-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea78-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="eea78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eea78-102">SYNOPSIS</span></span>
<span data-ttu-id="eea78-103">Hämtar en konfiguration för ExpressRoute-kretsen kopplad till privat peering på ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="eea78-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eea78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eea78-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eea78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eea78-105">DESCRIPTION</span></span>
<span data-ttu-id="eea78-106">Cmdleten **Get-AzureRmExpressRouteCircuitConnectionConfig** hämtar konfigurationen för en krets anslutning som är kopplad till privat peering för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="eea78-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="eea78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eea78-107">EXAMPLES</span></span>

### <span data-ttu-id="eea78-108">Exempel 1: Visa konfigurationen för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="eea78-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="eea78-109">Exempel 2: skaffa en kabel anslutning som är kopplad till en ExpressRoute-krets med rör</span><span class="sxs-lookup"><span data-stu-id="eea78-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="eea78-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eea78-110">PARAMETERS</span></span>

### <span data-ttu-id="eea78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea78-111">-DefaultProfile</span></span>
<span data-ttu-id="eea78-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eea78-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea78-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eea78-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="eea78-114">Det ExpressRoute-krets-objekt som innehåller kretsen.</span><span class="sxs-lookup"><span data-stu-id="eea78-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea78-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="eea78-115">-Name</span></span>
<span data-ttu-id="eea78-116">Namnet på den krets som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="eea78-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea78-117">CommonParameters</span></span>
<span data-ttu-id="eea78-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea78-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea78-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea78-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eea78-120">INPUTS</span></span>

### <span data-ttu-id="eea78-121">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eea78-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="eea78-122">Parametrar: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eea78-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="eea78-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eea78-123">OUTPUTS</span></span>

### <span data-ttu-id="eea78-124">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="eea78-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="eea78-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eea78-125">NOTES</span></span>

## <span data-ttu-id="eea78-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eea78-126">RELATED LINKS</span></span>

[<span data-ttu-id="eea78-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eea78-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="eea78-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea78-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="eea78-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea78-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="eea78-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea78-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="eea78-131">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea78-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
