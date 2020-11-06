---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580540"
---
# <span data-ttu-id="09b26-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="09b26-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="09b26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09b26-102">SYNOPSIS</span></span>
<span data-ttu-id="09b26-103">Flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="09b26-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09b26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09b26-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09b26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09b26-105">DESCRIPTION</span></span>
<span data-ttu-id="09b26-106">Cmdleten **Move-AzureRmExpressRouteCircuit** flyttar en ExpressRoute-krets från den klassiska distributions modellen till distributions modellen för Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="09b26-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="09b26-107">Efter flytten fungerar ExpressRoute-kretsen och fungerar på samma sätt som alla andra ExpressRoute-kretsar som skapas i resurs hanterarens distributions modell.</span><span class="sxs-lookup"><span data-stu-id="09b26-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="09b26-108">Krets länkar, virtuella nätverk och VPN-gateways flyttas inte genom den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="09b26-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="09b26-109">Resurserna måste omkonfigureras efter flytten.</span><span class="sxs-lookup"><span data-stu-id="09b26-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="09b26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09b26-110">EXAMPLES</span></span>

### <span data-ttu-id="09b26-111">Exempel 1: flytta en ExpressRoute-krets till distributions modellen för resurs hantering</span><span class="sxs-lookup"><span data-stu-id="09b26-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="09b26-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09b26-112">PARAMETERS</span></span>

### <span data-ttu-id="09b26-113">-Force</span><span class="sxs-lookup"><span data-stu-id="09b26-113">-Force</span></span>
<span data-ttu-id="09b26-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="09b26-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09b26-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="09b26-115">-Location</span></span>
<span data-ttu-id="09b26-116">Namnet på den Azure-plats där ExpressRoute-kretsen finns.</span><span class="sxs-lookup"><span data-stu-id="09b26-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="09b26-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="09b26-117">-Name</span></span>
<span data-ttu-id="09b26-118">Namnet på ExpressRoute-kretsen som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="09b26-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="09b26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09b26-119">-ResourceGroupName</span></span>
<span data-ttu-id="09b26-120">Namnet på resurs gruppen som ska innehålla den ExpressRoute-krets som flyttas.</span><span class="sxs-lookup"><span data-stu-id="09b26-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="09b26-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="09b26-121">-ServiceKey</span></span>
<span data-ttu-id="09b26-122">Den tjänst som används av ExpressRoute-kretsen i den klassiska distributions modellen.</span><span class="sxs-lookup"><span data-stu-id="09b26-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="09b26-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="09b26-123">-Tag</span></span>
<span data-ttu-id="09b26-124">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="09b26-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="09b26-125">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="09b26-125">For example:</span></span>

<span data-ttu-id="09b26-126">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="09b26-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="09b26-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09b26-127">-Confirm</span></span>
<span data-ttu-id="09b26-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09b26-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09b26-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09b26-129">-WhatIf</span></span>
<span data-ttu-id="09b26-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09b26-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09b26-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09b26-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09b26-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b26-132">-DefaultProfile</span></span>
<span data-ttu-id="09b26-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09b26-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b26-134">CommonParameters</span></span>
<span data-ttu-id="09b26-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b26-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b26-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b26-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09b26-137">INPUTS</span></span>

## <span data-ttu-id="09b26-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09b26-138">OUTPUTS</span></span>

### <span data-ttu-id="09b26-139">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="09b26-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="09b26-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09b26-140">NOTES</span></span>

## <span data-ttu-id="09b26-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09b26-141">RELATED LINKS</span></span>

[<span data-ttu-id="09b26-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="09b26-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="09b26-143">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="09b26-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="09b26-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="09b26-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="09b26-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="09b26-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
