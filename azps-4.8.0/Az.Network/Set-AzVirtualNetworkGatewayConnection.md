---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261780"
---
# <span data-ttu-id="d5a93-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d5a93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5a93-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a93-103">Konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="d5a93-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="d5a93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5a93-104">SYNTAX</span></span>

### <span data-ttu-id="d5a93-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d5a93-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a93-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d5a93-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a93-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5a93-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a93-108">Cmdleten **set-AzVirtualNetworkGatewayConnection** konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="d5a93-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="d5a93-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5a93-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a93-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="d5a93-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="d5a93-111">Exempel 2: lägga till/uppdatera taggar till en befintlig VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="d5a93-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5a93-112">PARAMETERS</span></span>

### <span data-ttu-id="d5a93-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5a93-113">-AsJob</span></span>
<span data-ttu-id="d5a93-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d5a93-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5a93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a93-115">-DefaultProfile</span></span>
<span data-ttu-id="d5a93-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a93-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d5a93-117">-EnableBgp</span></span>
<span data-ttu-id="d5a93-118">Om en BGP-session ska användas över en VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="d5a93-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a93-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5a93-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="d5a93-120">Tids gräns för timeout för dödbaserade peer-anslutningar</span><span class="sxs-lookup"><span data-stu-id="d5a93-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="d5a93-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d5a93-121">-Force</span></span>
<span data-ttu-id="d5a93-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d5a93-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5a93-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="d5a93-123">-IpsecPolicies</span></span>
<span data-ttu-id="d5a93-124">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="d5a93-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="d5a93-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d5a93-125">-Tag</span></span>
<span data-ttu-id="d5a93-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d5a93-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a93-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a93-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="d5a93-128">En lista över principer för trafik väljaren.</span><span class="sxs-lookup"><span data-stu-id="d5a93-128">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="d5a93-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5a93-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="d5a93-130">Om du vill använda PrivateIP för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="d5a93-130">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a93-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d5a93-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d5a93-132">Om du ska använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="d5a93-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a93-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="d5a93-134">Anger det PSVirtualNetworkGatewayConnection-objekt som denna cmdlet använder för att ändra anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d5a93-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a93-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5a93-135">-Confirm</span></span>
<span data-ttu-id="d5a93-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5a93-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a93-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a93-137">-WhatIf</span></span>
<span data-ttu-id="d5a93-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5a93-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a93-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5a93-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a93-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a93-140">CommonParameters</span></span>
<span data-ttu-id="d5a93-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a93-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a93-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a93-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a93-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5a93-143">INPUTS</span></span>

### <span data-ttu-id="d5a93-144">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="d5a93-145">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d5a93-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d5a93-146">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d5a93-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d5a93-147">Microsoft. Azure. commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="d5a93-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="d5a93-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5a93-148">OUTPUTS</span></span>

### <span data-ttu-id="d5a93-149">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d5a93-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5a93-150">NOTES</span></span>

## <span data-ttu-id="d5a93-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5a93-151">RELATED LINKS</span></span>

[<span data-ttu-id="d5a93-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d5a93-153">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d5a93-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5a93-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


