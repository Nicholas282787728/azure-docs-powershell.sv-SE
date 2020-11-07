---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 9b07574a1d8895d8504660784bf3bafe4ed891bd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929717"
---
# <span data-ttu-id="114ac-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="114ac-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="114ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="114ac-102">SYNOPSIS</span></span>
<span data-ttu-id="114ac-103">Skapar en ny peering-konfiguration som ska läggas till i en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="114ac-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="114ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="114ac-104">SYNTAX</span></span>

### <span data-ttu-id="114ac-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="114ac-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="114ac-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="114ac-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="114ac-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="114ac-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="114ac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="114ac-108">DESCRIPTION</span></span>
<span data-ttu-id="114ac-109">Cmdleten **New-AzureRmExpressRouteCircuitPeeringConfig** lägger till en peering-konfiguration till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="114ac-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="114ac-110">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="114ac-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="114ac-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="114ac-111">EXAMPLES</span></span>

### <span data-ttu-id="114ac-112">Exempel 1: skapa en ny ExpressRoute-krets med en peering-konfiguration</span><span class="sxs-lookup"><span data-stu-id="114ac-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="114ac-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="114ac-113">PARAMETERS</span></span>

### <span data-ttu-id="114ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114ac-114">-DefaultProfile</span></span>
<span data-ttu-id="114ac-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="114ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="114ac-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="114ac-116">-LegacyMode</span></span>
<span data-ttu-id="114ac-117">Det äldre läget för peering</span><span class="sxs-lookup"><span data-stu-id="114ac-117">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="114ac-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="114ac-119">För en PeeringType av MicrosoftPeering måste du ange en lista över alla de prefix du planerar att annonsera under BGP-sessionen.</span><span class="sxs-lookup"><span data-stu-id="114ac-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="114ac-120">Endast offentliga IP-adressprefix accepteras.</span><span class="sxs-lookup"><span data-stu-id="114ac-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="114ac-121">Du kan skicka en kommaseparerad lista om du planerar att skicka en uppsättning prefix.</span><span class="sxs-lookup"><span data-stu-id="114ac-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="114ac-122">De här prefixen måste vara registrerade i ett register namn för routning (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="114ac-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="114ac-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="114ac-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="114ac-124">Om du annonserar prefix som inte är registrerade för peering som-nummer kan du ange det som-nummer som de är registrerade i.</span><span class="sxs-lookup"><span data-stu-id="114ac-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="114ac-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="114ac-126">Namnet på routningstabellen (RIR/IRR) där AS-numret och prefixen är registrerade.</span><span class="sxs-lookup"><span data-stu-id="114ac-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="114ac-127">-Name</span></span>
<span data-ttu-id="114ac-128">Namnet på den peering-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="114ac-128">The name of the peering configuration to be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="114ac-129">-PeerAddressType</span></span>
<span data-ttu-id="114ac-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="114ac-130">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="114ac-131">-PeerASN</span></span>
<span data-ttu-id="114ac-132">AS-numret för din ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="114ac-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="114ac-133">Det måste vara ett offentligt ASN när PeeringType är AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="114ac-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="114ac-134">-PeeringType</span></span>
<span data-ttu-id="114ac-135">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="114ac-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="114ac-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="114ac-137">Det här är IP-adressintervallet för den primära Dirigerings Sök vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="114ac-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="114ac-138">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="114ac-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="114ac-139">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="114ac-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="114ac-140">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="114ac-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="114ac-141">-RouteFilter</span></span>
<span data-ttu-id="114ac-142">Det här är ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="114ac-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="114ac-143">-RouteFilterId</span></span>
<span data-ttu-id="114ac-144">Det här är resurs-ID för ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="114ac-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="114ac-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="114ac-146">Det här är IP-adressintervallet för den sekundära cirkulations vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="114ac-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="114ac-147">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="114ac-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="114ac-148">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="114ac-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="114ac-149">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="114ac-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="114ac-150">-SharedKey</span></span>
<span data-ttu-id="114ac-151">Det här är en valfri MD5-hash som används som en i förväg delad administratör för peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="114ac-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="114ac-152">-VlanId</span></span>
<span data-ttu-id="114ac-153">Det här är ID-numret för det VLAN som tilldelats den här peering.</span><span class="sxs-lookup"><span data-stu-id="114ac-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114ac-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114ac-154">CommonParameters</span></span>
<span data-ttu-id="114ac-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114ac-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114ac-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114ac-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114ac-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="114ac-157">INPUTS</span></span>

## <span data-ttu-id="114ac-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="114ac-158">OUTPUTS</span></span>

### <span data-ttu-id="114ac-159">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="114ac-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="114ac-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="114ac-160">NOTES</span></span>

## <span data-ttu-id="114ac-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="114ac-161">RELATED LINKS</span></span>

[<span data-ttu-id="114ac-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="114ac-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="114ac-163">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="114ac-163">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="114ac-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="114ac-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="114ac-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="114ac-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
