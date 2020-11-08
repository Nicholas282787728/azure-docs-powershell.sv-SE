---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262625"
---
# <span data-ttu-id="f6392-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f6392-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="f6392-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6392-102">SYNOPSIS</span></span>
<span data-ttu-id="f6392-103">Lägger till en peering-konfiguration till en ExpressRoute-kors anslutning.</span><span class="sxs-lookup"><span data-stu-id="f6392-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="f6392-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6392-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6392-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6392-105">DESCRIPTION</span></span>
<span data-ttu-id="f6392-106">Cmdleten **Add-AzExpressRouteCrossConnectionPeering** lägger till en peering-konfiguration till en ExpressRoute-kors anslutning.</span><span class="sxs-lookup"><span data-stu-id="f6392-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="f6392-107">Observera att när du har kört **Add-AzExpressRouteCrossConnectionPeering** måste du anropa Set-AzExpressRouteCrossConnection cmdlet för att aktivera konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f6392-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="f6392-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6392-108">EXAMPLES</span></span>

### <span data-ttu-id="f6392-109">Exempel 1: lägga till en peer-dator till en befintlig ExpressRoute-kors anslutning</span><span class="sxs-lookup"><span data-stu-id="f6392-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="f6392-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6392-110">PARAMETERS</span></span>

### <span data-ttu-id="f6392-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6392-111">-DefaultProfile</span></span>
<span data-ttu-id="f6392-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6392-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6392-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f6392-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f6392-114">ExpressRoute kors anslutningen ändras.</span><span class="sxs-lookup"><span data-stu-id="f6392-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="f6392-115">Detta Azure-objekt returneras av cmdlet **Get-AzExpressRouteCrossConnection** .</span><span class="sxs-lookup"><span data-stu-id="f6392-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6392-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f6392-116">-Force</span></span>
<span data-ttu-id="f6392-117">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="f6392-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f6392-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="f6392-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="f6392-119">För en PeeringType av MicrosoftPeering måste du ange en lista över alla de prefix du planerar att annonsera under BGP-sessionen.</span><span class="sxs-lookup"><span data-stu-id="f6392-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="f6392-120">Endast offentliga IP-adressprefix accepteras.</span><span class="sxs-lookup"><span data-stu-id="f6392-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="f6392-121">Du kan skicka en kommaseparerad lista om du planerar att skicka en uppsättning prefix.</span><span class="sxs-lookup"><span data-stu-id="f6392-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="f6392-122">De här prefixen måste vara registrerade i ett register namn för routning (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="f6392-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="f6392-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="f6392-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="f6392-124">Om du annonserar prefix som inte är registrerade för peering som-nummer kan du ange det som-nummer som de är registrerade i.</span><span class="sxs-lookup"><span data-stu-id="f6392-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="f6392-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="f6392-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="f6392-126">Namnet på routningstabellen (RIR/IRR) där AS-numret och prefixen är registrerade.</span><span class="sxs-lookup"><span data-stu-id="f6392-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="f6392-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6392-127">-Name</span></span>
<span data-ttu-id="f6392-128">Namnet på den peering-relation som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f6392-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="f6392-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f6392-129">-PeerAddressType</span></span>
<span data-ttu-id="f6392-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f6392-130">PeerAddressType</span></span>

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

### <span data-ttu-id="f6392-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="f6392-131">-PeerASN</span></span>
<span data-ttu-id="f6392-132">AS-numret för din ExpressRoute-kors anslutning.</span><span class="sxs-lookup"><span data-stu-id="f6392-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="f6392-133">Det måste vara ett offentligt ASN när PeeringType är AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="f6392-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="f6392-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f6392-134">-PeeringType</span></span>
<span data-ttu-id="f6392-135">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f6392-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f6392-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f6392-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="f6392-137">Det här är IP-adressintervallet för den primära Dirigerings Sök vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="f6392-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="f6392-138">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="f6392-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f6392-139">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="f6392-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f6392-140">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="f6392-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="f6392-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f6392-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="f6392-142">Det här är IP-adressintervallet för den sekundära cirkulations vägen för den här peering relationen.</span><span class="sxs-lookup"><span data-stu-id="f6392-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="f6392-143">Det måste vara ett/30 CIDR-undernät.</span><span class="sxs-lookup"><span data-stu-id="f6392-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f6392-144">Den första udda numrerade adressen i det här under nätet ska kopplas till ditt routergränssnitt.</span><span class="sxs-lookup"><span data-stu-id="f6392-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f6392-145">Azure konfigurerar nästa jämna numrerade adress till Azure router-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="f6392-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="f6392-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f6392-146">-SharedKey</span></span>
<span data-ttu-id="f6392-147">Det här är en valfri MD5-hash som används som en i förväg delad administratör för peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f6392-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="f6392-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="f6392-148">-VlanId</span></span>
<span data-ttu-id="f6392-149">Det här är ID-numret för det VLAN som tilldelats den här peering.</span><span class="sxs-lookup"><span data-stu-id="f6392-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="f6392-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6392-150">-Confirm</span></span>
<span data-ttu-id="f6392-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6392-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6392-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6392-152">-WhatIf</span></span>
<span data-ttu-id="f6392-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6392-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6392-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6392-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6392-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6392-155">CommonParameters</span></span>
<span data-ttu-id="f6392-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6392-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6392-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6392-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6392-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6392-158">INPUTS</span></span>

### <span data-ttu-id="f6392-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f6392-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="f6392-160">Parametern ' ExpressRouteCrossConnection ' godkänner värdet av typen ' PSExpressRouteCrossConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f6392-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="f6392-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6392-161">OUTPUTS</span></span>

### <span data-ttu-id="f6392-162">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f6392-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="f6392-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6392-163">NOTES</span></span>

## <span data-ttu-id="f6392-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6392-164">RELATED LINKS</span></span>

[<span data-ttu-id="f6392-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f6392-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="f6392-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f6392-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="f6392-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f6392-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="f6392-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f6392-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
