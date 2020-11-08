---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 7aede18c438faca196d696a69e7f7651edac132e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922086"
---
# <span data-ttu-id="441d5-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="441d5-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="441d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="441d5-102">SYNOPSIS</span></span>

## <span data-ttu-id="441d5-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="441d5-103">SYNTAX</span></span>

### <span data-ttu-id="441d5-104">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="441d5-104">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="441d5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="441d5-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="441d5-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="441d5-106">DESCRIPTION</span></span>

## <span data-ttu-id="441d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="441d5-107">EXAMPLES</span></span>

### <span data-ttu-id="441d5-108">9.1</span><span class="sxs-lookup"><span data-stu-id="441d5-108">1:</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="441d5-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="441d5-109">PARAMETERS</span></span>

### <span data-ttu-id="441d5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="441d5-110">-AsJob</span></span>
<span data-ttu-id="441d5-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="441d5-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="441d5-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-113">-Läge</span><span class="sxs-lookup"><span data-stu-id="441d5-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441d5-114">-DefaultProfile</span></span>
<span data-ttu-id="441d5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="441d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="441d5-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="441d5-116">-EnableBgp</span></span>
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

### <span data-ttu-id="441d5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="441d5-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="441d5-118">-IpsecPolicies</span></span>
<span data-ttu-id="441d5-119">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="441d5-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="441d5-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="441d5-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="441d5-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="441d5-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="441d5-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="441d5-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="441d5-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="441d5-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="441d5-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="441d5-128">-Tag</span></span>
<span data-ttu-id="441d5-129">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="441d5-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="441d5-130">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="441d5-130">For example:</span></span>

<span data-ttu-id="441d5-131">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="441d5-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="441d5-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="441d5-133">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="441d5-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="441d5-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="441d5-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="441d5-136">-Confirm</span></span>
<span data-ttu-id="441d5-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="441d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="441d5-138">-WhatIf</span></span>
<span data-ttu-id="441d5-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="441d5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="441d5-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="441d5-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441d5-141">CommonParameters</span></span>
<span data-ttu-id="441d5-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="441d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441d5-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="441d5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441d5-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="441d5-144">INPUTS</span></span>

## <span data-ttu-id="441d5-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="441d5-145">OUTPUTS</span></span>

### <span data-ttu-id="441d5-146">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="441d5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="441d5-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="441d5-147">NOTES</span></span>

## <span data-ttu-id="441d5-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="441d5-148">RELATED LINKS</span></span>

[<span data-ttu-id="441d5-149">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="441d5-149">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="441d5-150">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="441d5-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="441d5-151">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="441d5-151">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)