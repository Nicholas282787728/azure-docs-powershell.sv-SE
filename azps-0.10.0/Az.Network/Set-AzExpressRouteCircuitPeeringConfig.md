---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 3a97562c775c901e8226d1dc5a0b9d090f8f70cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924229"
---
# <span data-ttu-id="61ce7-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61ce7-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="61ce7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="61ce7-103">Sparar en ändrad ExpressRoute peering-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="61ce7-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="61ce7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61ce7-104">SYNTAX</span></span>

### <span data-ttu-id="61ce7-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="61ce7-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61ce7-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="61ce7-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61ce7-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="61ce7-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61ce7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61ce7-108">DESCRIPTION</span></span>
<span data-ttu-id="61ce7-109">Cmdleten **set-AzExpressRouteCircuitPeeringConfig** sparar en ändrad ExpressRoute peering-konfiguration tillbaka till Azure.</span><span class="sxs-lookup"><span data-stu-id="61ce7-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="61ce7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61ce7-110">EXAMPLES</span></span>

### <span data-ttu-id="61ce7-111">Exempel 1: ändra en befintlig peering-konfiguration</span><span class="sxs-lookup"><span data-stu-id="61ce7-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="61ce7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61ce7-112">PARAMETERS</span></span>

### <span data-ttu-id="61ce7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ce7-113">-DefaultProfile</span></span>
<span data-ttu-id="61ce7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61ce7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61ce7-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61ce7-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="61ce7-116">Det ExpressRoute-kretskort som innehåller den peering-konfiguration som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="61ce7-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61ce7-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="61ce7-117">-LegacyMode</span></span>
<span data-ttu-id="61ce7-118">Det äldre läget för peering</span><span class="sxs-lookup"><span data-stu-id="61ce7-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="61ce7-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="61ce7-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="61ce7-120">För en PeeringType av MicrosoftPeering måste du ange en lista över alla de prefix du planerar att annonsera under BGP-sessionen.</span><span class="sxs-lookup"><span data-stu-id="61ce7-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="61ce7-121">Endast offentliga IP-adressprefix accepteras.</span><span class="sxs-lookup"><span data-stu-id="61ce7-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="61ce7-122">Du kan skicka en kommaseparerad lista om du planerar att skicka en uppsättning prefix.</span><span class="sxs-lookup"><span data-stu-id="61ce7-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="61ce7-123">De här prefixen måste vara registrerade i ett register namn för routning (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="61ce7-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="61ce7-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="61ce7-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="61ce7-125">Om du annonserar prefix som inte är registrerade för peering som-nummer kan du ange det som-nummer som de är registrerade i.</span><span class="sxs-lookup"><span data-stu-id="61ce7-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="61ce7-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="61ce7-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="61ce7-127">Namnet på routningstabellen (RIR/IRR) där AS-numret och prefixen är registrerade.</span><span class="sxs-lookup"><span data-stu-id="61ce7-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="61ce7-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="61ce7-128">-Name</span></span>
<span data-ttu-id="61ce7-129">Namnet på den peering-konfiguration som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="61ce7-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="61ce7-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="61ce7-130">-PeerAddressType</span></span>
<span data-ttu-id="61ce7-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="61ce7-131">PeerAddressType</span></span>

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

### <span data-ttu-id="61ce7-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="61ce7-132">-PeerASN</span></span>
<span data-ttu-id="61ce7-133">AS-numret för din ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="61ce7-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="61ce7-134">Det måste vara ett offentligt ASN när PeeringType är AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="61ce7-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="61ce7-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="61ce7-135">-PeeringType</span></span>
<span data-ttu-id="61ce7-136">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="61ce7-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="61ce7-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="61ce7-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="61ce7-138">Det här är IP-adressintervallet för den primära Dirigerings Sök vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="61ce7-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="61ce7-139">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="61ce7-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="61ce7-140">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="61ce7-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="61ce7-141">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="61ce7-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="61ce7-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="61ce7-142">-RouteFilter</span></span>
<span data-ttu-id="61ce7-143">Det här är ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="61ce7-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="61ce7-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="61ce7-144">-RouteFilterId</span></span>
<span data-ttu-id="61ce7-145">Det här är resurs-ID för ett befintligt RouteFilter-objekt.</span><span class="sxs-lookup"><span data-stu-id="61ce7-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="61ce7-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="61ce7-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="61ce7-147">Det här är IP-adressintervallet för den sekundära cirkulations vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="61ce7-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="61ce7-148">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="61ce7-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="61ce7-149">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="61ce7-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="61ce7-150">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="61ce7-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="61ce7-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="61ce7-151">-SharedKey</span></span>
<span data-ttu-id="61ce7-152">Det här är en valfri MD5-hash som används som en i förväg delad administratör för peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="61ce7-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="61ce7-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="61ce7-153">-VlanId</span></span>
<span data-ttu-id="61ce7-154">Det här är ID-numret för det VLAN som tilldelats den här peering.</span><span class="sxs-lookup"><span data-stu-id="61ce7-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="61ce7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ce7-155">CommonParameters</span></span>
<span data-ttu-id="61ce7-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ce7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ce7-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ce7-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ce7-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61ce7-158">INPUTS</span></span>

### <span data-ttu-id="61ce7-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61ce7-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="61ce7-160">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="61ce7-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="61ce7-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61ce7-161">OUTPUTS</span></span>

### <span data-ttu-id="61ce7-162">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61ce7-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="61ce7-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61ce7-163">NOTES</span></span>

## <span data-ttu-id="61ce7-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61ce7-164">RELATED LINKS</span></span>

[<span data-ttu-id="61ce7-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61ce7-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="61ce7-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61ce7-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="61ce7-167">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61ce7-167">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="61ce7-168">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61ce7-168">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
