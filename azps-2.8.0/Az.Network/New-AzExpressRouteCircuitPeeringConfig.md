---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: a1bb490d81d2c4df92299c18eeb0e1a05a6760f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918305"
---
# <span data-ttu-id="ae328-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ae328-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ae328-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae328-102">SYNOPSIS</span></span>
<span data-ttu-id="ae328-103">Skapar en ny peering-konfiguration som ska läggas till i en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ae328-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ae328-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae328-104">SYNTAX</span></span>

### <span data-ttu-id="ae328-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ae328-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae328-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="ae328-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae328-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="ae328-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae328-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae328-108">DESCRIPTION</span></span>
<span data-ttu-id="ae328-109">Cmdleten **New-AzExpressRouteCircuitPeeringConfig** lägger till en peering-konfiguration till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ae328-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="ae328-110">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="ae328-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="ae328-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae328-111">EXAMPLES</span></span>

### <span data-ttu-id="ae328-112">Exempel 1: skapa en ny ExpressRoute-krets med en peering-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ae328-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

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
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="ae328-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae328-113">PARAMETERS</span></span>

### <span data-ttu-id="ae328-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae328-114">-DefaultProfile</span></span>
<span data-ttu-id="ae328-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae328-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae328-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="ae328-116">-LegacyMode</span></span>
<span data-ttu-id="ae328-117">Det äldre läget för peering</span><span class="sxs-lookup"><span data-stu-id="ae328-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="ae328-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="ae328-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="ae328-119">För en PeeringType av MicrosoftPeering måste du ange en lista över alla de prefix du planerar att annonsera under BGP-sessionen.</span><span class="sxs-lookup"><span data-stu-id="ae328-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ae328-120">Endast offentliga IP-adressprefix accepteras.</span><span class="sxs-lookup"><span data-stu-id="ae328-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ae328-121">Du kan skicka en kommaseparerad lista om du planerar att skicka en uppsättning prefix.</span><span class="sxs-lookup"><span data-stu-id="ae328-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ae328-122">De här prefixen måste vara registrerade i ett register namn för routning (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="ae328-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ae328-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ae328-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ae328-124">Om du annonserar prefix som inte är registrerade för peering som-nummer kan du ange det som-nummer som de är registrerade i.</span><span class="sxs-lookup"><span data-stu-id="ae328-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ae328-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ae328-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ae328-126">Namnet på routningstabellen (RIR/IRR) där AS-numret och prefixen är registrerade.</span><span class="sxs-lookup"><span data-stu-id="ae328-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ae328-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae328-127">-Name</span></span>
<span data-ttu-id="ae328-128">Namnet på den peering-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ae328-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="ae328-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ae328-129">-PeerAddressType</span></span>
<span data-ttu-id="ae328-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ae328-130">PeerAddressType</span></span>

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

### <span data-ttu-id="ae328-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="ae328-131">-PeerASN</span></span>
<span data-ttu-id="ae328-132">AS-numret för din ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ae328-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="ae328-133">Det måste vara ett offentligt ASN när PeeringType är AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="ae328-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ae328-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ae328-134">-PeeringType</span></span>
<span data-ttu-id="ae328-135">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ae328-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ae328-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ae328-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ae328-137">Det här är IP-adressintervallet för den primära Dirigerings Sök vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="ae328-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ae328-138">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="ae328-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ae328-139">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="ae328-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ae328-140">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="ae328-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ae328-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ae328-141">-RouteFilter</span></span>
<span data-ttu-id="ae328-142">Det här är ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="ae328-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ae328-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="ae328-143">-RouteFilterId</span></span>
<span data-ttu-id="ae328-144">Det här är resurs-ID för ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="ae328-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ae328-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ae328-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ae328-146">Det här är IP-adressintervallet för den sekundära cirkulations vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="ae328-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ae328-147">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="ae328-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ae328-148">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="ae328-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ae328-149">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="ae328-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ae328-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ae328-150">-SharedKey</span></span>
<span data-ttu-id="ae328-151">Det här är en valfri MD5-hash som används som en i förväg delad administratör för peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ae328-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ae328-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="ae328-152">-VlanId</span></span>
<span data-ttu-id="ae328-153">Det här är ID-numret för det VLAN som tilldelats den här peering.</span><span class="sxs-lookup"><span data-stu-id="ae328-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ae328-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae328-154">CommonParameters</span></span>
<span data-ttu-id="ae328-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae328-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae328-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae328-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae328-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae328-157">INPUTS</span></span>

### <span data-ttu-id="ae328-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ae328-158">System.String</span></span>

### <span data-ttu-id="ae328-159">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ae328-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="ae328-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae328-160">System.Boolean</span></span>

## <span data-ttu-id="ae328-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae328-161">OUTPUTS</span></span>

### <span data-ttu-id="ae328-162">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="ae328-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="ae328-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae328-163">NOTES</span></span>

## <span data-ttu-id="ae328-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae328-164">RELATED LINKS</span></span>

[<span data-ttu-id="ae328-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ae328-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ae328-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae328-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ae328-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ae328-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ae328-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae328-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
