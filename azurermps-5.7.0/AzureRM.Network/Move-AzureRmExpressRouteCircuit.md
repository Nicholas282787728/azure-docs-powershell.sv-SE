---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: d0fb9fb0c6fb27ff683fcbb2b3ae537d736189cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577143"
---
# <span data-ttu-id="b256a-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b256a-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="b256a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b256a-102">SYNOPSIS</span></span>
<span data-ttu-id="b256a-103">Flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b256a-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b256a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b256a-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b256a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b256a-105">DESCRIPTION</span></span>
<span data-ttu-id="b256a-106">Cmdleten **Move-AzureRmExpressRouteCircuit** flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b256a-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="b256a-107">Efter flytten fungerar ExpressRoute-kretsen och fungerar på samma sätt som alla andra ExpressRoute-kretsar som skapas i resurs hanterarens distributions modell.</span><span class="sxs-lookup"><span data-stu-id="b256a-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="b256a-108">Krets länkar, virtuella nätverk och VPN-gateways flyttas inte genom den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b256a-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="b256a-109">Resurserna måste omkonfigureras efter flytten.</span><span class="sxs-lookup"><span data-stu-id="b256a-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="b256a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b256a-110">EXAMPLES</span></span>

### <span data-ttu-id="b256a-111">Exempel 1: flytta en ExpressRoute-krets till distributions modellen för resurs hantering</span><span class="sxs-lookup"><span data-stu-id="b256a-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="b256a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b256a-112">PARAMETERS</span></span>

### <span data-ttu-id="b256a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b256a-113">-AsJob</span></span>
<span data-ttu-id="b256a-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b256a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b256a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b256a-115">-DefaultProfile</span></span>
<span data-ttu-id="b256a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b256a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b256a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b256a-117">-Force</span></span>
<span data-ttu-id="b256a-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b256a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b256a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="b256a-119">-Location</span></span>
<span data-ttu-id="b256a-120">Namnet på den Azure-plats där ExpressRoute-kretsen finns.</span><span class="sxs-lookup"><span data-stu-id="b256a-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="b256a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b256a-121">-Name</span></span>
<span data-ttu-id="b256a-122">Namnet på ExpressRoute-kretsen som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="b256a-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="b256a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b256a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b256a-124">Namnet på resurs gruppen som ska innehålla den ExpressRoute-krets som flyttas.</span><span class="sxs-lookup"><span data-stu-id="b256a-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="b256a-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="b256a-125">-ServiceKey</span></span>
<span data-ttu-id="b256a-126">Den tjänst som används av ExpressRoute-kretsen i den klassiska distributions modellen.</span><span class="sxs-lookup"><span data-stu-id="b256a-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="b256a-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b256a-127">-Tag</span></span>
<span data-ttu-id="b256a-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b256a-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b256a-129">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="b256a-129">For example:</span></span>

<span data-ttu-id="b256a-130">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b256a-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b256a-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b256a-131">-Confirm</span></span>
<span data-ttu-id="b256a-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b256a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b256a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b256a-133">-WhatIf</span></span>
<span data-ttu-id="b256a-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b256a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b256a-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b256a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b256a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b256a-136">CommonParameters</span></span>
<span data-ttu-id="b256a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b256a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b256a-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b256a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b256a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b256a-139">INPUTS</span></span>

### <span data-ttu-id="b256a-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="b256a-140">None</span></span>
<span data-ttu-id="b256a-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b256a-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b256a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b256a-142">OUTPUTS</span></span>

### <span data-ttu-id="b256a-143">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b256a-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b256a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b256a-144">NOTES</span></span>

## <span data-ttu-id="b256a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b256a-145">RELATED LINKS</span></span>

[<span data-ttu-id="b256a-146">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b256a-146">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b256a-147">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b256a-147">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b256a-148">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b256a-148">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b256a-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b256a-149">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
