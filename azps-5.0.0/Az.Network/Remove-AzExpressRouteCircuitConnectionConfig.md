---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272872"
---
# <span data-ttu-id="c8313-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c8313-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="c8313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8313-102">SYNOPSIS</span></span>
<span data-ttu-id="c8313-103">Tar bort en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c8313-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="c8313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8313-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8313-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8313-105">DESCRIPTION</span></span>
<span data-ttu-id="c8313-106">Cmdleten **Remove-AzExpressRouteCircuitConnectionConfig** tar bort en konfiguration för ExpressRoute-anslutning som är kopplad till en given ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="c8313-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="c8313-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8313-107">EXAMPLES</span></span>

### <span data-ttu-id="c8313-108">Exempel 1: ta bort en kabel anslutnings konfiguration från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="c8313-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c8313-109">Exempel 2: ta bort en anslutnings konfiguration för en krets med ledning från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="c8313-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="c8313-110">Exempel 3: ta bort en kabel anslutning från en ExpressRoute-krets för en viss adress familj</span><span class="sxs-lookup"><span data-stu-id="c8313-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c8313-111">Exempel 4: ta bort en kabel anslutnings konfiguration med hjälp av rör dragning från en ExpressRoute-krets för en viss adress familj</span><span class="sxs-lookup"><span data-stu-id="c8313-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="c8313-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8313-112">PARAMETERS</span></span>

### <span data-ttu-id="c8313-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8313-113">-DefaultProfile</span></span>
<span data-ttu-id="c8313-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8313-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8313-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8313-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c8313-116">ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c8313-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c8313-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8313-117">-Name</span></span>
<span data-ttu-id="c8313-118">Namnet på den krets som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c8313-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="c8313-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="c8313-119">-AddressPrefixType</span></span>
<span data-ttu-id="c8313-120">Anger den adress familjen som ska tas bort från config</span><span class="sxs-lookup"><span data-stu-id="c8313-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8313-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8313-121">-Confirm</span></span>
<span data-ttu-id="c8313-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8313-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8313-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8313-123">-WhatIf</span></span>
<span data-ttu-id="c8313-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8313-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8313-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8313-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8313-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8313-126">CommonParameters</span></span>
<span data-ttu-id="c8313-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8313-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8313-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8313-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8313-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8313-129">INPUTS</span></span>

### <span data-ttu-id="c8313-130">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8313-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c8313-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8313-131">OUTPUTS</span></span>

### <span data-ttu-id="c8313-132">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8313-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c8313-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8313-133">NOTES</span></span>

## <span data-ttu-id="c8313-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8313-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8313-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8313-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c8313-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c8313-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c8313-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c8313-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c8313-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c8313-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c8313-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c8313-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c8313-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8313-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="c8313-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8313-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)