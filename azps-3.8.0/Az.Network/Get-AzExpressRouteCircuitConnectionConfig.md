---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091110"
---
# <span data-ttu-id="e5dd0-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e5dd0-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="e5dd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dd0-103">Hämtar en konfiguration för ExpressRoute-kretsen kopplad till privat peering på ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="e5dd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5dd0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5dd0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="e5dd0-106">Cmdleten **Get-AzExpressRouteCircuitConnectionConfig** hämtar konfigurationen för en krets anslutning som är kopplad till privat peering för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e5dd0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5dd0-107">EXAMPLES</span></span>

### <span data-ttu-id="e5dd0-108">Exempel 1: Visa konfigurationen för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="e5dd0-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="e5dd0-109">Exempel 2: skaffa en kabel anslutning som är kopplad till en ExpressRoute-krets med rör</span><span class="sxs-lookup"><span data-stu-id="e5dd0-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="e5dd0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5dd0-110">PARAMETERS</span></span>

### <span data-ttu-id="e5dd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dd0-111">-DefaultProfile</span></span>
<span data-ttu-id="e5dd0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5dd0-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5dd0-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e5dd0-114">Det ExpressRoute-krets-objekt som innehåller kretsen.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="e5dd0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5dd0-115">-Name</span></span>
<span data-ttu-id="e5dd0-116">Namnet på den krets som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dd0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dd0-117">CommonParameters</span></span>
<span data-ttu-id="e5dd0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5dd0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dd0-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5dd0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dd0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5dd0-120">INPUTS</span></span>

### <span data-ttu-id="e5dd0-121">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5dd0-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e5dd0-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5dd0-122">OUTPUTS</span></span>

### <span data-ttu-id="e5dd0-123">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="e5dd0-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="e5dd0-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5dd0-124">NOTES</span></span>

## <span data-ttu-id="e5dd0-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5dd0-125">RELATED LINKS</span></span>

[<span data-ttu-id="e5dd0-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5dd0-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e5dd0-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e5dd0-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e5dd0-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e5dd0-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e5dd0-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e5dd0-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e5dd0-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e5dd0-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)