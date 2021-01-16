---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400619"
---
# <span data-ttu-id="757b4-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="757b4-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="757b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="757b4-102">SYNOPSIS</span></span>
<span data-ttu-id="757b4-103">Tar bort en IP-konfiguration från en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="757b4-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="757b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="757b4-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="757b4-105">DESCRIPTION</span></span>
<span data-ttu-id="757b4-106">Tar bort en IP-konfiguration från en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="757b4-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="757b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="757b4-107">EXAMPLES</span></span>

### <span data-ttu-id="757b4-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="757b4-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="757b4-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="757b4-109">PARAMETERS</span></span>

### <span data-ttu-id="757b4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757b4-110">-DefaultProfile</span></span>
<span data-ttu-id="757b4-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="757b4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="757b4-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="757b4-112">-Name</span></span>
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

### <span data-ttu-id="757b4-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="757b4-113">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="757b4-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="757b4-114">-Confirm</span></span>
<span data-ttu-id="757b4-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="757b4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757b4-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757b4-116">-WhatIf</span></span>
<span data-ttu-id="757b4-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="757b4-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757b4-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="757b4-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757b4-119">CommonParameters</span></span>
<span data-ttu-id="757b4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757b4-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757b4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757b4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="757b4-122">INPUTS</span></span>

### <span data-ttu-id="757b4-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="757b4-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="757b4-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="757b4-124">OUTPUTS</span></span>

### <span data-ttu-id="757b4-125">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="757b4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="757b4-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="757b4-126">NOTES</span></span>

## <span data-ttu-id="757b4-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="757b4-127">RELATED LINKS</span></span>

[<span data-ttu-id="757b4-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="757b4-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="757b4-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="757b4-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
