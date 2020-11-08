---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272054"
---
# <span data-ttu-id="1ce74-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1ce74-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1ce74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ce74-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce74-103">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="1ce74-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="1ce74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ce74-104">SYNTAX</span></span>

### <span data-ttu-id="1ce74-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="1ce74-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ce74-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ce74-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ce74-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ce74-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce74-108">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="1ce74-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="1ce74-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ce74-109">EXAMPLES</span></span>

### <span data-ttu-id="1ce74-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ce74-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="1ce74-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ce74-111">PARAMETERS</span></span>

### <span data-ttu-id="1ce74-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ce74-112">-AsJob</span></span>
<span data-ttu-id="1ce74-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1ce74-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ce74-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="1ce74-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="1ce74-115">-ConnectionProtocol</span></span>
<span data-ttu-id="1ce74-116">Gateway-anslutnings protokoll: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="1ce74-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-117">-Läge</span><span class="sxs-lookup"><span data-stu-id="1ce74-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce74-118">-DefaultProfile</span></span>
<span data-ttu-id="1ce74-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ce74-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce74-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="1ce74-120">-EnableBgp</span></span>

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

### <span data-ttu-id="1ce74-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="1ce74-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1ce74-122">-Force</span></span>

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

### <span data-ttu-id="1ce74-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="1ce74-123">-IpsecPolicies</span></span>
<span data-ttu-id="1ce74-124">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="1ce74-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="1ce74-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ce74-126">-Location</span></span>

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

### <span data-ttu-id="1ce74-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ce74-127">-Name</span></span>

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

### <span data-ttu-id="1ce74-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="1ce74-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="1ce74-129">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce74-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="1ce74-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="1ce74-131">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1ce74-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="1ce74-133">Tids gräns för timeout för dödbaserade peer-anslutningar</span><span class="sxs-lookup"><span data-stu-id="1ce74-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1ce74-134">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1ce74-135">-Tag</span></span>
<span data-ttu-id="1ce74-136">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1ce74-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ce74-137">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1ce74-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ce74-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="1ce74-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="1ce74-139">En lista över principer för trafik väljaren.</span><span class="sxs-lookup"><span data-stu-id="1ce74-139">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="1ce74-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="1ce74-141">Om du vill använda PrivateIP för denna VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="1ce74-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="1ce74-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="1ce74-143">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="1ce74-143">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="1ce74-144">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="1ce74-145">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce74-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ce74-146">-Confirm</span></span>
<span data-ttu-id="1ce74-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ce74-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce74-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce74-148">-WhatIf</span></span>
<span data-ttu-id="1ce74-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ce74-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce74-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ce74-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce74-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce74-151">CommonParameters</span></span>
<span data-ttu-id="1ce74-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce74-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce74-153">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce74-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce74-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ce74-154">INPUTS</span></span>

### <span data-ttu-id="1ce74-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1ce74-155">System.String</span></span>

### <span data-ttu-id="1ce74-156">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ce74-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1ce74-157">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ce74-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="1ce74-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1ce74-158">System.Int32</span></span>

### <span data-ttu-id="1ce74-159">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="1ce74-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="1ce74-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ce74-160">System.Boolean</span></span>

### <span data-ttu-id="1ce74-161">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1ce74-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1ce74-162">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="1ce74-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="1ce74-163">Microsoft. Azure. commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="1ce74-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="1ce74-164">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ce74-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ce74-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ce74-165">OUTPUTS</span></span>

### <span data-ttu-id="1ce74-166">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1ce74-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1ce74-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ce74-167">NOTES</span></span>

## <span data-ttu-id="1ce74-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ce74-168">RELATED LINKS</span></span>

[<span data-ttu-id="1ce74-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1ce74-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="1ce74-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1ce74-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="1ce74-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1ce74-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
