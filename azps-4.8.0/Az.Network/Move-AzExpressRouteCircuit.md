---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262129"
---
# <span data-ttu-id="969c0-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="969c0-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="969c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="969c0-102">SYNOPSIS</span></span>
<span data-ttu-id="969c0-103">Flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="969c0-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="969c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="969c0-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="969c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="969c0-105">DESCRIPTION</span></span>
<span data-ttu-id="969c0-106">Cmdleten **Move-AzExpressRouteCircuit** flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="969c0-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="969c0-107">Efter flytten fungerar ExpressRoute-kretsen och fungerar på samma sätt som alla andra ExpressRoute-kretsar som skapas i resurs hanterarens distributions modell.</span><span class="sxs-lookup"><span data-stu-id="969c0-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="969c0-108">Krets länkar, virtuella nätverk och VPN-gateways flyttas inte genom den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="969c0-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="969c0-109">Resurserna måste omkonfigureras efter flytten.</span><span class="sxs-lookup"><span data-stu-id="969c0-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="969c0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="969c0-110">EXAMPLES</span></span>

### <span data-ttu-id="969c0-111">Exempel 1: flytta en ExpressRoute-krets till distributions modellen för resurs hantering</span><span class="sxs-lookup"><span data-stu-id="969c0-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="969c0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="969c0-112">PARAMETERS</span></span>

### <span data-ttu-id="969c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="969c0-113">-AsJob</span></span>
<span data-ttu-id="969c0-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="969c0-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969c0-115">-DefaultProfile</span></span>
<span data-ttu-id="969c0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="969c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="969c0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="969c0-117">-Force</span></span>
<span data-ttu-id="969c0-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="969c0-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="969c0-119">-Location</span></span>
<span data-ttu-id="969c0-120">Namnet på den Azure-plats där ExpressRoute-kretsen finns.</span><span class="sxs-lookup"><span data-stu-id="969c0-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="969c0-121">-Name</span></span>
<span data-ttu-id="969c0-122">Namnet på ExpressRoute-kretsen som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="969c0-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="969c0-124">Namnet på resurs gruppen som ska innehålla den ExpressRoute-krets som flyttas.</span><span class="sxs-lookup"><span data-stu-id="969c0-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="969c0-125">-ServiceKey</span></span>
<span data-ttu-id="969c0-126">Den tjänst som används av ExpressRoute-kretsen i den klassiska distributions modellen.</span><span class="sxs-lookup"><span data-stu-id="969c0-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="969c0-127">-Tag</span></span>
<span data-ttu-id="969c0-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="969c0-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="969c0-129">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="969c0-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="969c0-130">-Confirm</span></span>
<span data-ttu-id="969c0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="969c0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969c0-132">-WhatIf</span></span>
<span data-ttu-id="969c0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="969c0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969c0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="969c0-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969c0-135">CommonParameters</span></span>
<span data-ttu-id="969c0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969c0-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969c0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969c0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="969c0-138">INPUTS</span></span>

### <span data-ttu-id="969c0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="969c0-139">System.String</span></span>

### <span data-ttu-id="969c0-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="969c0-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="969c0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="969c0-141">OUTPUTS</span></span>

### <span data-ttu-id="969c0-142">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="969c0-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="969c0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="969c0-143">NOTES</span></span>

## <span data-ttu-id="969c0-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="969c0-144">RELATED LINKS</span></span>

[<span data-ttu-id="969c0-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="969c0-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="969c0-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="969c0-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="969c0-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="969c0-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="969c0-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="969c0-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
