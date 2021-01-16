---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410595"
---
# <span data-ttu-id="53c2e-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="53c2e-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="53c2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="53c2e-103">Lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="53c2e-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="53c2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53c2e-104">SYNTAX</span></span>

### <span data-ttu-id="53c2e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53c2e-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53c2e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53c2e-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c2e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53c2e-107">DESCRIPTION</span></span>
<span data-ttu-id="53c2e-108">Cmdleten **Add-AzVirtualNetworkGatewayIpConfig** lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="53c2e-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="53c2e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53c2e-109">EXAMPLES</span></span>

### <span data-ttu-id="53c2e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53c2e-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="53c2e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53c2e-111">PARAMETERS</span></span>

### <span data-ttu-id="53c2e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c2e-112">-DefaultProfile</span></span>
<span data-ttu-id="53c2e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53c2e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53c2e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="53c2e-114">-Name</span></span>
<span data-ttu-id="53c2e-115">Anger namnet på gatewayens IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="53c2e-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="53c2e-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="53c2e-116">-PrivateIpAddress</span></span>
<span data-ttu-id="53c2e-117">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="53c2e-117">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c2e-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53c2e-118">-PublicIpAddress</span></span>
<span data-ttu-id="53c2e-119">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="53c2e-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c2e-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="53c2e-120">-PublicIpAddressId</span></span>
<span data-ttu-id="53c2e-121">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="53c2e-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c2e-122">-Undernät</span><span class="sxs-lookup"><span data-stu-id="53c2e-122">-Subnet</span></span>
<span data-ttu-id="53c2e-123">Anger ett **PSSubnet** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53c2e-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c2e-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="53c2e-124">-SubnetId</span></span>
<span data-ttu-id="53c2e-125">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="53c2e-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c2e-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="53c2e-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="53c2e-127">Anger ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53c2e-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="53c2e-128">Denna cmdlet ändrar det **PSVirtualNetworkGateway** -objekt som du anger.</span><span class="sxs-lookup"><span data-stu-id="53c2e-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="53c2e-129">Du kan använda Get-AzVirtualNetworkGateway cmdlet för att hämta ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53c2e-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="53c2e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53c2e-130">-Confirm</span></span>
<span data-ttu-id="53c2e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53c2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c2e-132">-WhatIf</span></span>
<span data-ttu-id="53c2e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53c2e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c2e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53c2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c2e-135">CommonParameters</span></span>
<span data-ttu-id="53c2e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c2e-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c2e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c2e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53c2e-138">INPUTS</span></span>

### <span data-ttu-id="53c2e-139">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="53c2e-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="53c2e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53c2e-140">OUTPUTS</span></span>

### <span data-ttu-id="53c2e-141">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="53c2e-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="53c2e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53c2e-142">NOTES</span></span>

## <span data-ttu-id="53c2e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53c2e-143">RELATED LINKS</span></span>

[<span data-ttu-id="53c2e-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="53c2e-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="53c2e-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="53c2e-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="53c2e-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="53c2e-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
