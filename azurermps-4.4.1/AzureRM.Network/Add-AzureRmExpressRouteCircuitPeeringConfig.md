---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585452"
---
# <span data-ttu-id="3e90c-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3e90c-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="3e90c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e90c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e90c-103">Lägger till en peering-konfiguration till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3e90c-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e90c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e90c-104">SYNTAX</span></span>

### <span data-ttu-id="3e90c-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="3e90c-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e90c-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="3e90c-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e90c-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="3e90c-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e90c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e90c-108">DESCRIPTION</span></span>
<span data-ttu-id="3e90c-109">Cmdleten **Add-AzureRmExpressRouteCircuitPeeringConfig** lägger till en peering-konfiguration till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3e90c-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="3e90c-110">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="3e90c-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3e90c-111">Observera att när du har kört **Add-AzureRmExpressRouteCircuitPeeringConfig** måste du anropa Set-AzureRmExpressRouteCircuit cmdlet för att aktivera konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="3e90c-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="3e90c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e90c-112">EXAMPLES</span></span>

### <span data-ttu-id="3e90c-113">Exempel 1: lägga till en peer för en befintlig ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="3e90c-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="3e90c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e90c-114">PARAMETERS</span></span>

### <span data-ttu-id="3e90c-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e90c-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3e90c-116">ExpressRoute-kretsen ändras.</span><span class="sxs-lookup"><span data-stu-id="3e90c-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3e90c-117">Detta Azure-objekt returneras av cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="3e90c-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="3e90c-118">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="3e90c-118">-LegacyMode</span></span>
<span data-ttu-id="3e90c-119">Det äldre läget för peering</span><span class="sxs-lookup"><span data-stu-id="3e90c-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="3e90c-120">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="3e90c-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="3e90c-121">För en PeeringType av MicrosoftPeering måste du ange en lista över alla de prefix du planerar att annonsera under BGP-sessionen.</span><span class="sxs-lookup"><span data-stu-id="3e90c-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="3e90c-122">Endast offentliga IP-adressprefix accepteras.</span><span class="sxs-lookup"><span data-stu-id="3e90c-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="3e90c-123">Du kan skicka en kommaseparerad lista om du planerar att skicka en uppsättning prefix.</span><span class="sxs-lookup"><span data-stu-id="3e90c-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="3e90c-124">De här prefixen måste vara registrerade i ett register namn för routning (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="3e90c-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e90c-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="3e90c-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="3e90c-126">Om du annonserar prefix som inte är registrerade för peering som-nummer kan du ange det som-nummer som de är registrerade i.</span><span class="sxs-lookup"><span data-stu-id="3e90c-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="3e90c-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="3e90c-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="3e90c-128">Namnet på routningstabellen (RIR/IRR) där AS-numret och prefixen är registrerade.</span><span class="sxs-lookup"><span data-stu-id="3e90c-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="3e90c-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e90c-129">-Name</span></span>
<span data-ttu-id="3e90c-130">Namnet på den peering-relation som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="3e90c-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="3e90c-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3e90c-131">-PeerAddressType</span></span>
<span data-ttu-id="3e90c-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3e90c-132">PeerAddressType</span></span>

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

### <span data-ttu-id="3e90c-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="3e90c-133">-PeerASN</span></span>
<span data-ttu-id="3e90c-134">AS-numret för din ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3e90c-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="3e90c-135">Det måste vara ett offentligt ASN när PeeringType är AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="3e90c-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="3e90c-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3e90c-136">-PeeringType</span></span>
<span data-ttu-id="3e90c-137">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3e90c-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3e90c-138">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3e90c-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="3e90c-139">Det här är IP-adressintervallet för den primära Dirigerings Sök vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="3e90c-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="3e90c-140">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="3e90c-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3e90c-141">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3e90c-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3e90c-142">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3e90c-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3e90c-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3e90c-143">-RouteFilter</span></span>
<span data-ttu-id="3e90c-144">Det här är ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="3e90c-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="3e90c-145">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="3e90c-145">-RouteFilterId</span></span>
<span data-ttu-id="3e90c-146">Det här är resurs-ID för ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="3e90c-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="3e90c-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3e90c-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="3e90c-148">Det här är IP-adressintervallet för den sekundära cirkulations vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="3e90c-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="3e90c-149">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="3e90c-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3e90c-150">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3e90c-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3e90c-151">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3e90c-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3e90c-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3e90c-152">-SharedKey</span></span>
<span data-ttu-id="3e90c-153">Det här är en valfri MD5-hash som används som en i förväg delad administratör för peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="3e90c-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="3e90c-154">-VlanId</span><span class="sxs-lookup"><span data-stu-id="3e90c-154">-VlanId</span></span>
<span data-ttu-id="3e90c-155">Det här är ID-numret för det VLAN som tilldelats den här peering.</span><span class="sxs-lookup"><span data-stu-id="3e90c-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="3e90c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e90c-156">-DefaultProfile</span></span>
<span data-ttu-id="3e90c-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e90c-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e90c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e90c-158">CommonParameters</span></span>
<span data-ttu-id="3e90c-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e90c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e90c-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e90c-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e90c-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e90c-161">INPUTS</span></span>

### <span data-ttu-id="3e90c-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e90c-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="3e90c-163">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3e90c-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="3e90c-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e90c-164">OUTPUTS</span></span>

### <span data-ttu-id="3e90c-165">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e90c-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3e90c-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e90c-166">NOTES</span></span>

## <span data-ttu-id="3e90c-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e90c-167">RELATED LINKS</span></span>

[<span data-ttu-id="3e90c-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e90c-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3e90c-169">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3e90c-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3e90c-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3e90c-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3e90c-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e90c-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
