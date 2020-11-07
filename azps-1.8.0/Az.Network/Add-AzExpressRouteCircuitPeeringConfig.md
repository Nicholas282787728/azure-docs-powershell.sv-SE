---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b7b28c9d2b1dd687759ae75db64039cbfb6d5d9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748445"
---
# <span data-ttu-id="b14d9-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b14d9-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b14d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b14d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b14d9-103">Lägger till en peering-konfiguration till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="b14d9-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b14d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b14d9-104">SYNTAX</span></span>

### <span data-ttu-id="b14d9-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="b14d9-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b14d9-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="b14d9-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b14d9-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="b14d9-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b14d9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b14d9-108">DESCRIPTION</span></span>
<span data-ttu-id="b14d9-109">Cmdleten **Add-AzExpressRouteCircuitPeeringConfig** lägger till en peering-konfiguration till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="b14d9-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="b14d9-110">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="b14d9-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="b14d9-111">Observera att när du har kört **Add-AzExpressRouteCircuitPeeringConfig** måste du anropa Set-AzExpressRouteCircuit cmdlet för att aktivera konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b14d9-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="b14d9-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b14d9-112">EXAMPLES</span></span>

### <span data-ttu-id="b14d9-113">Exempel 1: lägga till en peer för en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="b14d9-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="b14d9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b14d9-114">PARAMETERS</span></span>

### <span data-ttu-id="b14d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14d9-115">-DefaultProfile</span></span>
<span data-ttu-id="b14d9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b14d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b14d9-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b14d9-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b14d9-118">ExpressRoute-kretsen ändras.</span><span class="sxs-lookup"><span data-stu-id="b14d9-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="b14d9-119">Detta Azure-objekt returneras av cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="b14d9-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="b14d9-120">-LegacyMode</span></span>
<span data-ttu-id="b14d9-121">Det äldre läget för peering</span><span class="sxs-lookup"><span data-stu-id="b14d9-121">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="b14d9-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="b14d9-123">För en PeeringType av MicrosoftPeering måste du ange en lista över alla de prefix du planerar att annonsera under BGP-sessionen.</span><span class="sxs-lookup"><span data-stu-id="b14d9-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="b14d9-124">Endast offentliga IP-adressprefix accepteras.</span><span class="sxs-lookup"><span data-stu-id="b14d9-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="b14d9-125">Du kan skicka en kommaseparerad lista om du planerar att skicka en uppsättning prefix.</span><span class="sxs-lookup"><span data-stu-id="b14d9-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="b14d9-126">De här prefixen måste vara registrerade i ett register namn för routning (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="b14d9-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="b14d9-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="b14d9-128">Om du annonserar prefix som inte är registrerade för peering som-nummer kan du ange det som-nummer som de är registrerade i.</span><span class="sxs-lookup"><span data-stu-id="b14d9-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="b14d9-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="b14d9-130">Namnet på routningstabellen (RIR/IRR) där AS-numret och prefixen är registrerade.</span><span class="sxs-lookup"><span data-stu-id="b14d9-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="b14d9-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="b14d9-131">-Name</span></span>
<span data-ttu-id="b14d9-132">Namnet på den peering-relation som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="b14d9-132">The name of the peering relationship to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b14d9-133">-PeerAddressType</span></span>
<span data-ttu-id="b14d9-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b14d9-134">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="b14d9-135">-PeerASN</span></span>
<span data-ttu-id="b14d9-136">AS-numret för din ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="b14d9-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="b14d9-137">Det måste vara ett offentligt ASN när PeeringType är AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="b14d9-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b14d9-138">-PeeringType</span></span>
<span data-ttu-id="b14d9-139">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b14d9-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b14d9-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="b14d9-141">Det här är IP-adressintervallet för den primära Dirigerings Sök vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="b14d9-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="b14d9-142">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="b14d9-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b14d9-143">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b14d9-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b14d9-144">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="b14d9-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b14d9-145">-RouteFilter</span></span>
<span data-ttu-id="b14d9-146">Det här är ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="b14d9-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="b14d9-147">-RouteFilterId</span></span>
<span data-ttu-id="b14d9-148">Det här är resurs-ID för ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="b14d9-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b14d9-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="b14d9-150">Det här är IP-adressintervallet för den sekundära cirkulations vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="b14d9-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="b14d9-151">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="b14d9-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b14d9-152">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b14d9-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b14d9-153">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="b14d9-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b14d9-154">-SharedKey</span></span>
<span data-ttu-id="b14d9-155">Det här är en valfri MD5-hash som används som en i förväg delad administratör för peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b14d9-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="b14d9-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="b14d9-156">-VlanId</span></span>
<span data-ttu-id="b14d9-157">Det här är ID-numret för det VLAN som tilldelats den här peering.</span><span class="sxs-lookup"><span data-stu-id="b14d9-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14d9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14d9-158">CommonParameters</span></span>
<span data-ttu-id="b14d9-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b14d9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14d9-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b14d9-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14d9-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b14d9-161">INPUTS</span></span>

### <span data-ttu-id="b14d9-162">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b14d9-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="b14d9-163">System. String</span><span class="sxs-lookup"><span data-stu-id="b14d9-163">System.String</span></span>

### <span data-ttu-id="b14d9-164">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b14d9-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="b14d9-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b14d9-165">System.Boolean</span></span>

## <span data-ttu-id="b14d9-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b14d9-166">OUTPUTS</span></span>

### <span data-ttu-id="b14d9-167">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b14d9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b14d9-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b14d9-168">NOTES</span></span>

## <span data-ttu-id="b14d9-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b14d9-169">RELATED LINKS</span></span>

[<span data-ttu-id="b14d9-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b14d9-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b14d9-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b14d9-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b14d9-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b14d9-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b14d9-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b14d9-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
