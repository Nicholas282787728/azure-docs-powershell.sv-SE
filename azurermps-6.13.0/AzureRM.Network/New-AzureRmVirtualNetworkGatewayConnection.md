---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: a9ad0933ce42dc0d031d9ca44d9b5ff7b84d6b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580760"
---
# <span data-ttu-id="eb15b-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb15b-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="eb15b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb15b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb15b-103">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="eb15b-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb15b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb15b-104">SYNTAX</span></span>

### <span data-ttu-id="eb15b-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="eb15b-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb15b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb15b-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb15b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb15b-107">DESCRIPTION</span></span>
<span data-ttu-id="eb15b-108">Skapar VPN-anslutningen för webbplats-till-plats mellan virtuell nätverksgateway och lokala VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="eb15b-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="eb15b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb15b-109">EXAMPLES</span></span>

### <span data-ttu-id="eb15b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb15b-110">Example 1</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="eb15b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb15b-111">PARAMETERS</span></span>

### <span data-ttu-id="eb15b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb15b-112">-AsJob</span></span>
<span data-ttu-id="eb15b-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eb15b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb15b-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="eb15b-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="eb15b-115">-Läge</span><span class="sxs-lookup"><span data-stu-id="eb15b-115">-ConnectionType</span></span>

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

### <span data-ttu-id="eb15b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb15b-116">-DefaultProfile</span></span>
<span data-ttu-id="eb15b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb15b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb15b-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="eb15b-118">-EnableBgp</span></span>

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

### <span data-ttu-id="eb15b-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="eb15b-119">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input:  True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb15b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eb15b-120">-Force</span></span>

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

### <span data-ttu-id="eb15b-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="eb15b-121">-IpsecPolicies</span></span>
<span data-ttu-id="eb15b-122">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="eb15b-122">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb15b-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="eb15b-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="eb15b-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="eb15b-124">-Location</span></span>

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

### <span data-ttu-id="eb15b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb15b-125">-Name</span></span>

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

### <span data-ttu-id="eb15b-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="eb15b-126">-Peer</span></span>

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

### <span data-ttu-id="eb15b-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="eb15b-127">-PeerId</span></span>

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

### <span data-ttu-id="eb15b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb15b-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="eb15b-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="eb15b-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="eb15b-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="eb15b-130">-SharedKey</span></span>

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

### <span data-ttu-id="eb15b-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eb15b-131">-Tag</span></span>
<span data-ttu-id="eb15b-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eb15b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eb15b-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="eb15b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eb15b-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="eb15b-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="eb15b-135">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="eb15b-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="eb15b-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="eb15b-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="eb15b-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="eb15b-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="eb15b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb15b-138">-Confirm</span></span>
<span data-ttu-id="eb15b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb15b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb15b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb15b-140">-WhatIf</span></span>
<span data-ttu-id="eb15b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb15b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb15b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb15b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb15b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb15b-143">CommonParameters</span></span>
<span data-ttu-id="eb15b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb15b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb15b-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb15b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb15b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb15b-146">INPUTS</span></span>

### <span data-ttu-id="eb15b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="eb15b-147">System.String</span></span>

### <span data-ttu-id="eb15b-148">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eb15b-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="eb15b-149">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eb15b-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="eb15b-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="eb15b-150">System.Int32</span></span>

### <span data-ttu-id="eb15b-151">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="eb15b-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="eb15b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb15b-152">System.Boolean</span></span>

### <span data-ttu-id="eb15b-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="eb15b-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="eb15b-154">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eb15b-154">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eb15b-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb15b-155">OUTPUTS</span></span>

### <span data-ttu-id="eb15b-156">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb15b-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="eb15b-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb15b-157">NOTES</span></span>

## <span data-ttu-id="eb15b-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb15b-158">RELATED LINKS</span></span>

[<span data-ttu-id="eb15b-159">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb15b-159">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="eb15b-160">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb15b-160">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="eb15b-161">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb15b-161">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
