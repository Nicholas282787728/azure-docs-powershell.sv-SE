---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 9e9718f23a262b8a914ef88aa1ad1bb97fc36fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755697"
---
# <span data-ttu-id="6d6d6-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6d6d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6d6-103">Konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d6d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d6d6-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d6d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="6d6d6-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnection** konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="6d6d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d6d6-107">EXAMPLES</span></span>

### <span data-ttu-id="6d6d6-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="6d6d6-108">Example 1:</span></span>
```
$conn = Get-AzureRmVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

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

## <span data-ttu-id="6d6d6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d6d6-109">PARAMETERS</span></span>

### <span data-ttu-id="6d6d6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d6d6-110">-AsJob</span></span>
<span data-ttu-id="6d6d6-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6d6d6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d6d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6d6-112">-DefaultProfile</span></span>
<span data-ttu-id="6d6d6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d6d6-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6d6d6-114">-EnableBgp</span></span>
<span data-ttu-id="6d6d6-115">Om en BGP-session ska användas över en VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="6d6d6-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="6d6d6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6d6d6-116">-Force</span></span>
<span data-ttu-id="6d6d6-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d6d6-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="6d6d6-118">-IpsecPolicies</span></span>
<span data-ttu-id="6d6d6-119">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="6d6d6-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6d6d6-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6d6d6-121">Om du ska använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="6d6d6-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="6d6d6-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="6d6d6-123">Anger det PSVirtualNetworkGatewayConnection-objekt som denna cmdlet använder för att ändra anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="6d6d6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d6d6-124">-Confirm</span></span>
<span data-ttu-id="6d6d6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6d6-126">-WhatIf</span></span>
<span data-ttu-id="6d6d6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6d6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d6d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6d6-129">CommonParameters</span></span>
<span data-ttu-id="6d6d6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d6d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6d6-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d6d6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6d6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d6d6-132">INPUTS</span></span>

### <span data-ttu-id="6d6d6-133">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="6d6d6-134">Parametrar: VirtualNetworkGatewayConnection (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d6d6-134">Parameters: VirtualNetworkGatewayConnection (ByValue)</span></span>

### <span data-ttu-id="6d6d6-135">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6d6d6-135">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6d6d6-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6d6d6-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6d6d6-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d6d6-137">OUTPUTS</span></span>

### <span data-ttu-id="6d6d6-138">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6d6d6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d6d6-139">NOTES</span></span>

## <span data-ttu-id="6d6d6-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d6d6-140">RELATED LINKS</span></span>

[<span data-ttu-id="6d6d6-141">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-141">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6d6d6-142">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-142">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6d6d6-143">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d6d6-143">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

