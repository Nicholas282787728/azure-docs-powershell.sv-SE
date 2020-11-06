---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: f565adcf308e9615374753a28992f572feda61ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576212"
---
# <span data-ttu-id="ea51a-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ea51a-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="ea51a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea51a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea51a-103">Flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ea51a-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea51a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea51a-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea51a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea51a-105">DESCRIPTION</span></span>
<span data-ttu-id="ea51a-106">Cmdleten **Move-AzureRmExpressRouteCircuit** flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ea51a-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="ea51a-107">Efter flytten fungerar ExpressRoute-kretsen och fungerar på samma sätt som alla andra ExpressRoute-kretsar som skapas i resurs hanterarens distributions modell.</span><span class="sxs-lookup"><span data-stu-id="ea51a-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="ea51a-108">Krets länkar, virtuella nätverk och VPN-gateways flyttas inte genom den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ea51a-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="ea51a-109">Resurserna måste omkonfigureras efter flytten.</span><span class="sxs-lookup"><span data-stu-id="ea51a-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="ea51a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea51a-110">EXAMPLES</span></span>

### <span data-ttu-id="ea51a-111">Exempel 1: flytta en ExpressRoute-krets till distributions modellen för resurs hantering</span><span class="sxs-lookup"><span data-stu-id="ea51a-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="ea51a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea51a-112">PARAMETERS</span></span>

### <span data-ttu-id="ea51a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea51a-113">-AsJob</span></span>
<span data-ttu-id="ea51a-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ea51a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea51a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea51a-115">-DefaultProfile</span></span>
<span data-ttu-id="ea51a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea51a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea51a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ea51a-117">-Force</span></span>
<span data-ttu-id="ea51a-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ea51a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea51a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="ea51a-119">-Location</span></span>
<span data-ttu-id="ea51a-120">Namnet på den Azure-plats där ExpressRoute-kretsen finns.</span><span class="sxs-lookup"><span data-stu-id="ea51a-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="ea51a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea51a-121">-Name</span></span>
<span data-ttu-id="ea51a-122">Namnet på ExpressRoute-kretsen som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="ea51a-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="ea51a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea51a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea51a-124">Namnet på resurs gruppen som ska innehålla den ExpressRoute-krets som flyttas.</span><span class="sxs-lookup"><span data-stu-id="ea51a-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="ea51a-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="ea51a-125">-ServiceKey</span></span>
<span data-ttu-id="ea51a-126">Den tjänst som används av ExpressRoute-kretsen i den klassiska distributions modellen.</span><span class="sxs-lookup"><span data-stu-id="ea51a-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="ea51a-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ea51a-127">-Tag</span></span>
<span data-ttu-id="ea51a-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ea51a-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea51a-129">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ea51a-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ea51a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea51a-130">-Confirm</span></span>
<span data-ttu-id="ea51a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea51a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea51a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea51a-132">-WhatIf</span></span>
<span data-ttu-id="ea51a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea51a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea51a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea51a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea51a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea51a-135">CommonParameters</span></span>
<span data-ttu-id="ea51a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea51a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea51a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea51a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea51a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea51a-138">INPUTS</span></span>

### <span data-ttu-id="ea51a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea51a-139">System.String</span></span>

### <span data-ttu-id="ea51a-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ea51a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ea51a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea51a-141">OUTPUTS</span></span>

### <span data-ttu-id="ea51a-142">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ea51a-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ea51a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea51a-143">NOTES</span></span>

## <span data-ttu-id="ea51a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea51a-144">RELATED LINKS</span></span>

[<span data-ttu-id="ea51a-145">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ea51a-145">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ea51a-146">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ea51a-146">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ea51a-147">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ea51a-147">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ea51a-148">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ea51a-148">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
