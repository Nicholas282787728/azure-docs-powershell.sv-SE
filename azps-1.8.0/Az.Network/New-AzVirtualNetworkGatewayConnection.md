---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747986"
---
# <span data-ttu-id="6f90b-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6f90b-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6f90b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f90b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f90b-103">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="6f90b-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="6f90b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f90b-104">SYNTAX</span></span>

### <span data-ttu-id="6f90b-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="6f90b-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f90b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f90b-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f90b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f90b-107">DESCRIPTION</span></span>
<span data-ttu-id="6f90b-108">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="6f90b-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="6f90b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f90b-109">EXAMPLES</span></span>

### <span data-ttu-id="6f90b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f90b-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="6f90b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f90b-111">PARAMETERS</span></span>

### <span data-ttu-id="6f90b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f90b-112">-AsJob</span></span>
<span data-ttu-id="6f90b-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6f90b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f90b-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="6f90b-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="6f90b-115">-Läge</span><span class="sxs-lookup"><span data-stu-id="6f90b-115">-ConnectionType</span></span>

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

### <span data-ttu-id="6f90b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f90b-116">-DefaultProfile</span></span>
<span data-ttu-id="6f90b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f90b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f90b-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6f90b-118">-EnableBgp</span></span>

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

### <span data-ttu-id="6f90b-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="6f90b-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="6f90b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6f90b-120">-Force</span></span>

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

### <span data-ttu-id="6f90b-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="6f90b-121">-IpsecPolicies</span></span>
<span data-ttu-id="6f90b-122">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="6f90b-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="6f90b-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6f90b-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="6f90b-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="6f90b-124">-Location</span></span>

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

### <span data-ttu-id="6f90b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f90b-125">-Name</span></span>

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

### <span data-ttu-id="6f90b-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="6f90b-126">-Peer</span></span>

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

### <span data-ttu-id="6f90b-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="6f90b-127">-PeerId</span></span>

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

### <span data-ttu-id="6f90b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f90b-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="6f90b-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6f90b-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="6f90b-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6f90b-130">-SharedKey</span></span>

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

### <span data-ttu-id="6f90b-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6f90b-131">-Tag</span></span>
<span data-ttu-id="6f90b-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6f90b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6f90b-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6f90b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6f90b-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6f90b-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6f90b-135">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="6f90b-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="6f90b-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="6f90b-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="6f90b-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6f90b-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="6f90b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f90b-138">-Confirm</span></span>
<span data-ttu-id="6f90b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f90b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f90b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f90b-140">-WhatIf</span></span>
<span data-ttu-id="6f90b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f90b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f90b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f90b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f90b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f90b-143">CommonParameters</span></span>
<span data-ttu-id="6f90b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f90b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f90b-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f90b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f90b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f90b-146">INPUTS</span></span>

### <span data-ttu-id="6f90b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6f90b-147">System.String</span></span>

### <span data-ttu-id="6f90b-148">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f90b-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="6f90b-149">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f90b-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="6f90b-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6f90b-150">System.Int32</span></span>

### <span data-ttu-id="6f90b-151">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="6f90b-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="6f90b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f90b-152">System.Boolean</span></span>

### <span data-ttu-id="6f90b-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6f90b-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6f90b-154">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="6f90b-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="6f90b-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f90b-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f90b-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f90b-156">OUTPUTS</span></span>

### <span data-ttu-id="6f90b-157">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6f90b-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6f90b-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f90b-158">NOTES</span></span>

## <span data-ttu-id="6f90b-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f90b-159">RELATED LINKS</span></span>

[<span data-ttu-id="6f90b-160">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6f90b-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6f90b-161">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6f90b-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6f90b-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6f90b-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
