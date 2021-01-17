---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389268"
---
# <span data-ttu-id="700c6-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="700c6-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="700c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="700c6-102">SYNOPSIS</span></span>
<span data-ttu-id="700c6-103">Uppdaterar en anslutnings konfiguration för en anslutning som har skapats i privata peers för en ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="700c6-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="700c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="700c6-104">SYNTAX</span></span>

### <span data-ttu-id="700c6-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="700c6-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="700c6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="700c6-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="700c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="700c6-107">DESCRIPTION</span></span>
<span data-ttu-id="700c6-108">Cmdleten **set-AzExpressRouteCircuitConnectionConfig** uppdaterar en konfiguration för kretsar som har skapats i privat peering för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="700c6-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="700c6-109">Det gör att du kan använda två olika ExpressRoute-kretsar mellan regioner och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="700c6-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="700c6-110">Observera att innan du kör **set-AzExpressRouteCircuitConnectionConfig** måste du lägga till kabel anslutningen med **Add-AzExpressRouteCircuitConnectionConfig**.</span><span class="sxs-lookup"><span data-stu-id="700c6-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="700c6-111">När du har kört **set-AzExpressRouteCircuitPeeringConfig** måste du också anropa Set-AzExpressRouteCircuit cmdlet för att aktivera konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="700c6-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="700c6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="700c6-112">EXAMPLES</span></span>

### <span data-ttu-id="700c6-113">Exempel 1: uppdatera en resurs till en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="700c6-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="700c6-114">Exempel 2: Ange en anslutnings konfiguration för en krets med ledning till en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="700c6-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="700c6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="700c6-115">PARAMETERS</span></span>

### <span data-ttu-id="700c6-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="700c6-116">-AddressPrefix</span></span>
<span data-ttu-id="700c6-117">Ett minimum/29 kund adress utrymme för att skapa VxLan-tunnlar mellan ExpressRoute-kretsar för IPv4-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="700c6-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="700c6-118">eller ett minimum av/125 kund adress utrymme för att skapa VxLan-tunnlar mellan ExpressRoute-kretsar för IPv6-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="700c6-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="700c6-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="700c6-119">-AddressPrefixType</span></span>
<span data-ttu-id="700c6-120">Anger den adress familj som adressprefix ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="700c6-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="700c6-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="700c6-121">-AuthorizationKey</span></span>
<span data-ttu-id="700c6-122">Auktoriseringsregel för flödes kretsen peer Express i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="700c6-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="700c6-123">Auktorisering på peer-kretsen kan skapas med befintliga kommandon.</span><span class="sxs-lookup"><span data-stu-id="700c6-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="700c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="700c6-124">-DefaultProfile</span></span>
<span data-ttu-id="700c6-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="700c6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="700c6-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="700c6-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="700c6-127">ExpressRoute-kretsen ändras.</span><span class="sxs-lookup"><span data-stu-id="700c6-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="700c6-128">Detta Azure-objekt returneras av cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="700c6-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="700c6-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="700c6-129">-Name</span></span>
<span data-ttu-id="700c6-130">Namnet på den resurs som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="700c6-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="700c6-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="700c6-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="700c6-132">Resurs-ID för privat peering för fjärranslutna kretsar som kommer att användas med den aktuella kretsen.</span><span class="sxs-lookup"><span data-stu-id="700c6-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="700c6-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="700c6-133">-Confirm</span></span>
<span data-ttu-id="700c6-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="700c6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="700c6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="700c6-135">-WhatIf</span></span>
<span data-ttu-id="700c6-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="700c6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="700c6-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="700c6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="700c6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700c6-138">CommonParameters</span></span>
<span data-ttu-id="700c6-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="700c6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700c6-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="700c6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700c6-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="700c6-141">INPUTS</span></span>

### <span data-ttu-id="700c6-142">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="700c6-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="700c6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="700c6-143">System.String</span></span>

## <span data-ttu-id="700c6-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="700c6-144">OUTPUTS</span></span>

### <span data-ttu-id="700c6-145">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="700c6-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="700c6-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="700c6-146">NOTES</span></span>

## <span data-ttu-id="700c6-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="700c6-147">RELATED LINKS</span></span>

[<span data-ttu-id="700c6-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="700c6-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="700c6-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="700c6-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="700c6-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="700c6-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="700c6-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="700c6-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="700c6-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="700c6-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
