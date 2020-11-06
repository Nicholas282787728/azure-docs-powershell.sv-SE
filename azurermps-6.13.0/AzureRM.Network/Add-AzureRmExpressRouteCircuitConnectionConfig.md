---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584152"
---
# <span data-ttu-id="a26ef-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a26ef-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="a26ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a26ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a26ef-103">Lägger till en konfiguration för en kabel anslutning för privat peering av en ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="a26ef-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a26ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a26ef-104">SYNTAX</span></span>

### <span data-ttu-id="a26ef-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a26ef-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a26ef-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a26ef-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a26ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a26ef-107">DESCRIPTION</span></span>
<span data-ttu-id="a26ef-108">Cmdleten **Add-AzureRmExpressRouteCircuitConnectionConfig** lägger till en anslutnings konfiguration för en privat peering för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="a26ef-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="a26ef-109">Det gör att du kan använda två olika ExpressRoute-kretsar mellan regioner och abonnemang. Observera att när du har kört **Add-AzureRmExpressRouteCircuitPeeringConfig** måste du anropa Set-AzureRmExpressRouteCircuit cmdlet för att aktivera konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a26ef-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="a26ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a26ef-110">EXAMPLES</span></span>

### <span data-ttu-id="a26ef-111">Exempel 1: lägga till en resurs i en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="a26ef-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="a26ef-112">Exempel 2: lägga till en kabel anslutning med hjälp av ledningar till en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="a26ef-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="a26ef-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a26ef-113">PARAMETERS</span></span>

### <span data-ttu-id="a26ef-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a26ef-114">-AddressPrefix</span></span>
<span data-ttu-id="a26ef-115">Ett minsta/29 kund adress utrymme för att skapa VxLan tunnlar mellan ExpressRoute-kretsar</span><span class="sxs-lookup"><span data-stu-id="a26ef-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ef-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a26ef-116">-AuthorizationKey</span></span>
<span data-ttu-id="a26ef-117">Auktoriseringsregel för flödes kretsen peer Express i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a26ef-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="a26ef-118">Auktorisering på peer-kretsen kan skapas med befintliga kommandon.</span><span class="sxs-lookup"><span data-stu-id="a26ef-118">Authorization on peer circuit can be created using existing commands.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26ef-119">-DefaultProfile</span></span>
<span data-ttu-id="a26ef-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a26ef-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a26ef-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a26ef-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a26ef-122">ExpressRoute-kretsen ändras.</span><span class="sxs-lookup"><span data-stu-id="a26ef-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="a26ef-123">Detta Azure-objekt returneras av cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="a26ef-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="a26ef-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a26ef-124">-Name</span></span>
<span data-ttu-id="a26ef-125">Namnet på den resurs som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a26ef-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="a26ef-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="a26ef-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="a26ef-127">Resurs-ID för privat peering för fjärranslutna kretsar som kommer att användas med den aktuella kretsen.</span><span class="sxs-lookup"><span data-stu-id="a26ef-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26ef-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a26ef-128">-Confirm</span></span>
<span data-ttu-id="a26ef-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a26ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a26ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a26ef-130">-WhatIf</span></span>
<span data-ttu-id="a26ef-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a26ef-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a26ef-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a26ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a26ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26ef-133">CommonParameters</span></span>
<span data-ttu-id="a26ef-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a26ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26ef-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a26ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26ef-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a26ef-136">INPUTS</span></span>

### <span data-ttu-id="a26ef-137">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a26ef-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="a26ef-138">Parametrar: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a26ef-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="a26ef-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a26ef-139">System.String</span></span>

## <span data-ttu-id="a26ef-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a26ef-140">OUTPUTS</span></span>

### <span data-ttu-id="a26ef-141">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a26ef-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a26ef-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a26ef-142">NOTES</span></span>

## <span data-ttu-id="a26ef-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a26ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="a26ef-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a26ef-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a26ef-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a26ef-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a26ef-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a26ef-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a26ef-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a26ef-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a26ef-148">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a26ef-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a26ef-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a26ef-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a26ef-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a26ef-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
