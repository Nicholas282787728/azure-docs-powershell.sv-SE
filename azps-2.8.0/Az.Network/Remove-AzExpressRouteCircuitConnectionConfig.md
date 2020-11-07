---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918094"
---
# <span data-ttu-id="c1216-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1216-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="c1216-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1216-102">SYNOPSIS</span></span>
<span data-ttu-id="c1216-103">Tar bort en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c1216-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="c1216-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1216-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1216-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1216-105">DESCRIPTION</span></span>
<span data-ttu-id="c1216-106">Cmdleten **Remove-AzExpressRouteCircuitConnectionConfig** tar bort en konfiguration för ExpressRoute-anslutning som är kopplad till en given ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="c1216-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="c1216-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1216-107">EXAMPLES</span></span>

### <span data-ttu-id="c1216-108">Exempel 1: ta bort en kabel anslutnings konfiguration från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="c1216-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c1216-109">Exempel 2: ta bort en anslutnings konfiguration för en krets med ledning från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="c1216-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="c1216-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1216-110">PARAMETERS</span></span>

### <span data-ttu-id="c1216-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1216-111">-DefaultProfile</span></span>
<span data-ttu-id="c1216-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1216-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1216-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1216-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c1216-114">ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c1216-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c1216-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1216-115">-Name</span></span>
<span data-ttu-id="c1216-116">Namnet på den krets som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c1216-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="c1216-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1216-117">-Confirm</span></span>
<span data-ttu-id="c1216-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1216-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1216-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1216-119">-WhatIf</span></span>
<span data-ttu-id="c1216-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1216-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1216-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1216-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1216-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1216-122">CommonParameters</span></span>
<span data-ttu-id="c1216-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1216-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1216-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1216-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1216-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1216-125">INPUTS</span></span>

### <span data-ttu-id="c1216-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1216-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c1216-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1216-127">OUTPUTS</span></span>

### <span data-ttu-id="c1216-128">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1216-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c1216-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1216-129">NOTES</span></span>

## <span data-ttu-id="c1216-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1216-130">RELATED LINKS</span></span>

[<span data-ttu-id="c1216-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1216-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c1216-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1216-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1216-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1216-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1216-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1216-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1216-135">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1216-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1216-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1216-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="c1216-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1216-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)