---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c25b311a4f99814c718ce825d61433d7c2fee192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919070"
---
# <span data-ttu-id="8040a-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8040a-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8040a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8040a-102">SYNOPSIS</span></span>
<span data-ttu-id="8040a-103">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="8040a-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="8040a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8040a-104">SYNTAX</span></span>

### <span data-ttu-id="8040a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="8040a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8040a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8040a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8040a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8040a-107">DESCRIPTION</span></span>
<span data-ttu-id="8040a-108">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="8040a-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="8040a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8040a-109">EXAMPLES</span></span>

### <span data-ttu-id="8040a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8040a-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="8040a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8040a-111">PARAMETERS</span></span>

### <span data-ttu-id="8040a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8040a-112">-AsJob</span></span>
<span data-ttu-id="8040a-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8040a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8040a-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="8040a-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="8040a-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="8040a-115">-ConnectionProtocol</span></span>
<span data-ttu-id="8040a-116">Gateway-anslutnings protokoll: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="8040a-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="8040a-117">-Läge</span><span class="sxs-lookup"><span data-stu-id="8040a-117">-ConnectionType</span></span>

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

### <span data-ttu-id="8040a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8040a-118">-DefaultProfile</span></span>
<span data-ttu-id="8040a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8040a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8040a-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="8040a-120">-EnableBgp</span></span>

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

### <span data-ttu-id="8040a-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="8040a-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="8040a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8040a-122">-Force</span></span>

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

### <span data-ttu-id="8040a-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="8040a-123">-IpsecPolicies</span></span>
<span data-ttu-id="8040a-124">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="8040a-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="8040a-125">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8040a-125">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="8040a-126">En lista över principer för trafik väljaren.</span><span class="sxs-lookup"><span data-stu-id="8040a-126">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="8040a-127">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="8040a-127">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="8040a-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="8040a-128">-Location</span></span>

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

### <span data-ttu-id="8040a-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="8040a-129">-Name</span></span>

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

### <span data-ttu-id="8040a-130">-Peer</span><span class="sxs-lookup"><span data-stu-id="8040a-130">-Peer</span></span>

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

### <span data-ttu-id="8040a-131">-PeerId</span><span class="sxs-lookup"><span data-stu-id="8040a-131">-PeerId</span></span>

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

### <span data-ttu-id="8040a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8040a-132">-ResourceGroupName</span></span>

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

### <span data-ttu-id="8040a-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="8040a-133">-RoutingWeight</span></span>

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

### <span data-ttu-id="8040a-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8040a-134">-SharedKey</span></span>

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

### <span data-ttu-id="8040a-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8040a-135">-Tag</span></span>
<span data-ttu-id="8040a-136">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8040a-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8040a-137">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="8040a-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8040a-138">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="8040a-138">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="8040a-139">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="8040a-139">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="8040a-140">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="8040a-140">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="8040a-141">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="8040a-141">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="8040a-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8040a-142">-Confirm</span></span>
<span data-ttu-id="8040a-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8040a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8040a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8040a-144">-WhatIf</span></span>
<span data-ttu-id="8040a-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8040a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8040a-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8040a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8040a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8040a-147">CommonParameters</span></span>
<span data-ttu-id="8040a-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8040a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8040a-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8040a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8040a-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8040a-150">INPUTS</span></span>

### <span data-ttu-id="8040a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8040a-151">System.String</span></span>

### <span data-ttu-id="8040a-152">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8040a-152">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8040a-153">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8040a-153">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="8040a-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8040a-154">System.Int32</span></span>

### <span data-ttu-id="8040a-155">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="8040a-155">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="8040a-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8040a-156">System.Boolean</span></span>

### <span data-ttu-id="8040a-157">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8040a-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8040a-158">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="8040a-158">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="8040a-159">Microsoft. Azure. commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="8040a-159">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="8040a-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8040a-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8040a-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8040a-161">OUTPUTS</span></span>

### <span data-ttu-id="8040a-162">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8040a-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8040a-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8040a-163">NOTES</span></span>

## <span data-ttu-id="8040a-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8040a-164">RELATED LINKS</span></span>

[<span data-ttu-id="8040a-165">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8040a-165">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8040a-166">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8040a-166">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8040a-167">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8040a-167">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
