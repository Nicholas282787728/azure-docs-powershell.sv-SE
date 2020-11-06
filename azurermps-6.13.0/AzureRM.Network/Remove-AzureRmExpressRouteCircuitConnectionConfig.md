---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576181"
---
# <span data-ttu-id="f0991-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0991-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f0991-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0991-102">SYNOPSIS</span></span>
<span data-ttu-id="f0991-103">Tar bort en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f0991-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0991-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0991-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0991-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0991-105">DESCRIPTION</span></span>
<span data-ttu-id="f0991-106">Cmdleten **Remove-AzureRmExpressRouteCircuitConnectionConfig** tar bort en konfiguration för ExpressRoute-anslutning som är kopplad till en given ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="f0991-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="f0991-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0991-107">EXAMPLES</span></span>

### <span data-ttu-id="f0991-108">Exempel 1: ta bort en kabel anslutnings konfiguration från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="f0991-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f0991-109">Exempel 2: ta bort en anslutnings konfiguration för en krets med ledning från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="f0991-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="f0991-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0991-110">PARAMETERS</span></span>

### <span data-ttu-id="f0991-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0991-111">-DefaultProfile</span></span>
<span data-ttu-id="f0991-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0991-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0991-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f0991-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f0991-114">ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f0991-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="f0991-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0991-115">-Name</span></span>
<span data-ttu-id="f0991-116">Namnet på den krets som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f0991-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="f0991-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0991-117">-Confirm</span></span>
<span data-ttu-id="f0991-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0991-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0991-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0991-119">-WhatIf</span></span>
<span data-ttu-id="f0991-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0991-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0991-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0991-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0991-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0991-122">CommonParameters</span></span>
<span data-ttu-id="f0991-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0991-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0991-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0991-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0991-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0991-125">INPUTS</span></span>

### <span data-ttu-id="f0991-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f0991-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="f0991-127">Parametrar: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0991-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="f0991-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0991-128">OUTPUTS</span></span>

### <span data-ttu-id="f0991-129">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f0991-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f0991-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0991-130">NOTES</span></span>

## <span data-ttu-id="f0991-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0991-131">RELATED LINKS</span></span>

[<span data-ttu-id="f0991-132">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f0991-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f0991-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0991-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f0991-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0991-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f0991-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0991-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f0991-136">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0991-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f0991-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f0991-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f0991-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f0991-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
