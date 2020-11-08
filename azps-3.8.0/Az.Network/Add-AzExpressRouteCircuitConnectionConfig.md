---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089352"
---
# <span data-ttu-id="dde37-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dde37-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="dde37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dde37-102">SYNOPSIS</span></span>
<span data-ttu-id="dde37-103">Lägger till en konfiguration för en kabel anslutning för privat peering av en ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="dde37-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="dde37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dde37-104">SYNTAX</span></span>

### <span data-ttu-id="dde37-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="dde37-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dde37-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dde37-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde37-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dde37-107">DESCRIPTION</span></span>
<span data-ttu-id="dde37-108">Cmdleten **Add-AzExpressRouteCircuitConnectionConfig** lägger till en anslutnings konfiguration för en privat peering för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="dde37-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="dde37-109">Det gör att du kan använda två olika ExpressRoute-kretsar mellan regioner och abonnemang. Observera att när du har kört **Add-AzExpressRouteCircuitConnectionConfig** måste du anropa Set-AzExpressRouteCircuit cmdlet för att aktivera konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="dde37-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="dde37-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dde37-110">EXAMPLES</span></span>

### <span data-ttu-id="dde37-111">Exempel 1: lägga till en resurs i en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="dde37-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="dde37-112">Exempel 2: lägga till en kabel anslutning med hjälp av ledningar till en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="dde37-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="dde37-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dde37-113">PARAMETERS</span></span>

### <span data-ttu-id="dde37-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dde37-114">-AddressPrefix</span></span>
<span data-ttu-id="dde37-115">Ett minimum/29 kund adress utrymme för att skapa VxLan-tunnlar mellan ExpressRoute-kretsar för IPv4-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="dde37-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="dde37-116">eller ett minimum av/125 kund adress utrymme för att skapa VxLan-tunnlar mellan ExpressRoute-kretsar för IPv6-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="dde37-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="dde37-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="dde37-117">-AddressPrefixType</span></span>
<span data-ttu-id="dde37-118">Det här anger den adress familj som adressprefix ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="dde37-118">This specifies the Address Family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde37-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="dde37-119">-AuthorizationKey</span></span>
<span data-ttu-id="dde37-120">Auktoriseringsregel för flödes kretsen peer Express i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dde37-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="dde37-121">Auktorisering på peer-kretsen kan skapas med befintliga kommandon.</span><span class="sxs-lookup"><span data-stu-id="dde37-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="dde37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde37-122">-DefaultProfile</span></span>
<span data-ttu-id="dde37-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dde37-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde37-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dde37-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="dde37-125">ExpressRoute-kretsen ändras.</span><span class="sxs-lookup"><span data-stu-id="dde37-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="dde37-126">Detta Azure-objekt returneras av cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="dde37-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="dde37-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="dde37-127">-Name</span></span>
<span data-ttu-id="dde37-128">Namnet på den resurs som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="dde37-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="dde37-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="dde37-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="dde37-130">Resurs-ID för privat peering för fjärranslutna kretsar som kommer att användas med den aktuella kretsen.</span><span class="sxs-lookup"><span data-stu-id="dde37-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="dde37-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dde37-131">-Confirm</span></span>
<span data-ttu-id="dde37-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dde37-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde37-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde37-133">-WhatIf</span></span>
<span data-ttu-id="dde37-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dde37-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dde37-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dde37-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde37-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde37-136">CommonParameters</span></span>
<span data-ttu-id="dde37-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde37-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde37-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde37-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde37-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dde37-139">INPUTS</span></span>

### <span data-ttu-id="dde37-140">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dde37-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="dde37-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dde37-141">System.String</span></span>

## <span data-ttu-id="dde37-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dde37-142">OUTPUTS</span></span>

### <span data-ttu-id="dde37-143">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dde37-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="dde37-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dde37-144">NOTES</span></span>

## <span data-ttu-id="dde37-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dde37-145">RELATED LINKS</span></span>

[<span data-ttu-id="dde37-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dde37-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dde37-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dde37-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dde37-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dde37-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dde37-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dde37-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="dde37-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dde37-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)