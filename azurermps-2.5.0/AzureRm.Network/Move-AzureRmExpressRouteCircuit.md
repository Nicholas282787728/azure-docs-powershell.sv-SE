---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929745"
---
# <span data-ttu-id="7de77-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7de77-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="7de77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7de77-102">SYNOPSIS</span></span>
<span data-ttu-id="7de77-103">Flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7de77-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7de77-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7de77-105">DESCRIPTION</span></span>
<span data-ttu-id="7de77-106">Cmdleten **Move-AzureRmExpressRouteCircuit** flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7de77-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="7de77-107">Efter flytten fungerar ExpressRoute-kretsen och fungerar på samma sätt som alla andra ExpressRoute-kretsar som skapas i resurs hanterarens distributions modell.</span><span class="sxs-lookup"><span data-stu-id="7de77-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="7de77-108">Krets länkar, virtuella nätverk och VPN-gateways flyttas inte genom den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7de77-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="7de77-109">Resurserna måste omkonfigureras efter flytten.</span><span class="sxs-lookup"><span data-stu-id="7de77-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="7de77-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7de77-110">EXAMPLES</span></span>

### <span data-ttu-id="7de77-111">Exempel 1: flytta en ExpressRoute-krets till distributions modellen för resurs hantering</span><span class="sxs-lookup"><span data-stu-id="7de77-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="7de77-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7de77-112">PARAMETERS</span></span>

### <span data-ttu-id="7de77-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7de77-113">-AsJob</span></span>
<span data-ttu-id="7de77-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7de77-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de77-115">-DefaultProfile</span></span>
<span data-ttu-id="7de77-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7de77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de77-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7de77-117">-Force</span></span>
<span data-ttu-id="7de77-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7de77-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="7de77-119">-Location</span></span>
<span data-ttu-id="7de77-120">Namnet på den Azure-plats där ExpressRoute-kretsen finns.</span><span class="sxs-lookup"><span data-stu-id="7de77-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7de77-121">-Name</span></span>
<span data-ttu-id="7de77-122">Namnet på ExpressRoute-kretsen som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="7de77-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de77-123">-ResourceGroupName</span></span>
<span data-ttu-id="7de77-124">Namnet på resurs gruppen som ska innehålla den ExpressRoute-krets som flyttas.</span><span class="sxs-lookup"><span data-stu-id="7de77-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="7de77-125">-ServiceKey</span></span>
<span data-ttu-id="7de77-126">Den tjänst som används av ExpressRoute-kretsen i den klassiska distributions modellen.</span><span class="sxs-lookup"><span data-stu-id="7de77-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7de77-127">-Tag</span></span>
<span data-ttu-id="7de77-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7de77-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7de77-129">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="7de77-129">For example:</span></span>

<span data-ttu-id="7de77-130">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7de77-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7de77-131">-Confirm</span></span>
<span data-ttu-id="7de77-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7de77-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de77-133">-WhatIf</span></span>
<span data-ttu-id="7de77-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7de77-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de77-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7de77-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de77-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de77-136">CommonParameters</span></span>
<span data-ttu-id="7de77-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de77-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de77-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de77-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de77-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7de77-139">INPUTS</span></span>

## <span data-ttu-id="7de77-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7de77-140">OUTPUTS</span></span>

### <span data-ttu-id="7de77-141">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7de77-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7de77-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7de77-142">NOTES</span></span>

## <span data-ttu-id="7de77-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7de77-143">RELATED LINKS</span></span>

[<span data-ttu-id="7de77-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7de77-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7de77-145">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7de77-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7de77-146">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7de77-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7de77-147">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7de77-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
