---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 0c619b306d6dece23006d351f666637afe9f852a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574594"
---
# <span data-ttu-id="d2d4b-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d2d4b-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d2d4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2d4b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d4b-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2d4b-103">SYNTAX</span></span>

### <span data-ttu-id="d2d4b-104">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d2d4b-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d4b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d4b-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d4b-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2d4b-106">DESCRIPTION</span></span>

## <span data-ttu-id="d2d4b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="d2d4b-108">9.1</span><span class="sxs-lookup"><span data-stu-id="d2d4b-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="d2d4b-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2d4b-109">PARAMETERS</span></span>

### <span data-ttu-id="d2d4b-110">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="d2d4b-110">-AuthorizationKey</span></span>
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

### <span data-ttu-id="d2d4b-111">-Läge</span><span class="sxs-lookup"><span data-stu-id="d2d4b-111">-ConnectionType</span></span>
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

### <span data-ttu-id="d2d4b-112">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d2d4b-112">-EnableBgp</span></span>
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

### <span data-ttu-id="d2d4b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d2d4b-113">-Force</span></span>
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

### <span data-ttu-id="d2d4b-114">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="d2d4b-114">-IpsecPolicies</span></span>
<span data-ttu-id="d2d4b-115">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-115">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="d2d4b-116">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="d2d4b-116">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="d2d4b-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="d2d4b-117">-Location</span></span>
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

### <span data-ttu-id="d2d4b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2d4b-118">-Name</span></span>
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

### <span data-ttu-id="d2d4b-119">-Peer</span><span class="sxs-lookup"><span data-stu-id="d2d4b-119">-Peer</span></span>
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

### <span data-ttu-id="d2d4b-120">-PeerId</span><span class="sxs-lookup"><span data-stu-id="d2d4b-120">-PeerId</span></span>
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

### <span data-ttu-id="d2d4b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d4b-121">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d2d4b-122">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="d2d4b-122">-RoutingWeight</span></span>
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

### <span data-ttu-id="d2d4b-123">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d2d4b-123">-SharedKey</span></span>
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

### <span data-ttu-id="d2d4b-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d2d4b-124">-Tag</span></span>
<span data-ttu-id="d2d4b-125">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d2d4b-126">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d2d4b-126">For example:</span></span>

<span data-ttu-id="d2d4b-127">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d2d4b-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d2d4b-128">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d2d4b-128">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d2d4b-129">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="d2d4b-129">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="d2d4b-130">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="d2d4b-130">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="d2d4b-131">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="d2d4b-131">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="d2d4b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2d4b-132">-Confirm</span></span>
<span data-ttu-id="d2d4b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d4b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d4b-134">-WhatIf</span></span>
<span data-ttu-id="d2d4b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2d4b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d4b-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d4b-137">-DefaultProfile</span></span>
<span data-ttu-id="d2d4b-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d4b-139">CommonParameters</span></span>
<span data-ttu-id="d2d4b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d4b-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d4b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d4b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2d4b-142">INPUTS</span></span>

## <span data-ttu-id="d2d4b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2d4b-143">OUTPUTS</span></span>

### <span data-ttu-id="d2d4b-144">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d2d4b-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d2d4b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2d4b-145">NOTES</span></span>

## <span data-ttu-id="d2d4b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2d4b-146">RELATED LINKS</span></span>

[<span data-ttu-id="d2d4b-147">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d2d4b-147">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d2d4b-148">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d2d4b-148">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d2d4b-149">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d2d4b-149">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
