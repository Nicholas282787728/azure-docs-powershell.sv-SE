---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: 0b4bdbcdb4a753943278b759d584bb034a717b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931242"
---
# <span data-ttu-id="75f75-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="75f75-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="75f75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75f75-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75f75-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75f75-103">SYNTAX</span></span>

### <span data-ttu-id="75f75-104">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="75f75-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f75-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="75f75-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f75-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75f75-106">DESCRIPTION</span></span>

## <span data-ttu-id="75f75-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75f75-107">EXAMPLES</span></span>

### <span data-ttu-id="75f75-108">9.1</span><span class="sxs-lookup"><span data-stu-id="75f75-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="75f75-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75f75-109">PARAMETERS</span></span>

### <span data-ttu-id="75f75-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75f75-110">-AsJob</span></span>
<span data-ttu-id="75f75-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="75f75-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75f75-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="75f75-112">-AuthorizationKey</span></span>
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

### <span data-ttu-id="75f75-113">-Läge</span><span class="sxs-lookup"><span data-stu-id="75f75-113">-ConnectionType</span></span>
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

### <span data-ttu-id="75f75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f75-114">-DefaultProfile</span></span>
<span data-ttu-id="75f75-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75f75-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f75-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="75f75-116">-EnableBgp</span></span>
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

### <span data-ttu-id="75f75-117">-Force</span><span class="sxs-lookup"><span data-stu-id="75f75-117">-Force</span></span>
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

### <span data-ttu-id="75f75-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="75f75-118">-IpsecPolicies</span></span>
<span data-ttu-id="75f75-119">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="75f75-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="75f75-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="75f75-120">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="75f75-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="75f75-121">-Location</span></span>
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

### <span data-ttu-id="75f75-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="75f75-122">-Name</span></span>
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

### <span data-ttu-id="75f75-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="75f75-123">-Peer</span></span>
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

### <span data-ttu-id="75f75-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="75f75-124">-PeerId</span></span>
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

### <span data-ttu-id="75f75-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f75-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="75f75-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="75f75-126">-RoutingWeight</span></span>
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

### <span data-ttu-id="75f75-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="75f75-127">-SharedKey</span></span>
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

### <span data-ttu-id="75f75-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="75f75-128">-Tag</span></span>
<span data-ttu-id="75f75-129">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="75f75-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75f75-130">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="75f75-130">For example:</span></span>

<span data-ttu-id="75f75-131">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="75f75-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75f75-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="75f75-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="75f75-133">Använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="75f75-133">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="75f75-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="75f75-134">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="75f75-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="75f75-135">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="75f75-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75f75-136">-Confirm</span></span>
<span data-ttu-id="75f75-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75f75-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f75-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f75-138">-WhatIf</span></span>
<span data-ttu-id="75f75-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75f75-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f75-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75f75-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f75-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f75-141">CommonParameters</span></span>
<span data-ttu-id="75f75-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f75-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f75-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f75-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f75-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75f75-144">INPUTS</span></span>

## <span data-ttu-id="75f75-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75f75-145">OUTPUTS</span></span>

### <span data-ttu-id="75f75-146">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="75f75-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="75f75-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75f75-147">NOTES</span></span>

## <span data-ttu-id="75f75-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75f75-148">RELATED LINKS</span></span>

[<span data-ttu-id="75f75-149">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="75f75-149">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="75f75-150">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="75f75-150">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="75f75-151">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="75f75-151">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
