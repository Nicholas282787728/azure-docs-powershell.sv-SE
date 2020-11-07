---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926034"
---
# <span data-ttu-id="7c1fc-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7c1fc-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="7c1fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c1fc-102">SYNOPSIS</span></span> 
<span data-ttu-id="7c1fc-103">Koppla från angivna anslutna VPN-klientanslutningar med en given virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="7c1fc-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="7c1fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c1fc-104">SYNTAX</span></span>
### <span data-ttu-id="7c1fc-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="7c1fc-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="7c1fc-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7c1fc-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="7c1fc-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7c1fc-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="7c1fc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c1fc-108">DESCRIPTION</span></span>
<span data-ttu-id="7c1fc-109">Med cmdleten **Koppla från-AzVirtualNetworkGatewayVpnConnection** kan du koppla från angiven ansluten VPN-klientkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7c1fc-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="7c1fc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c1fc-110">EXAMPLES</span></span>

### <span data-ttu-id="7c1fc-111">Exempel</span><span class="sxs-lookup"><span data-stu-id="7c1fc-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="7c1fc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c1fc-112">PARAMETERS</span></span>

### <span data-ttu-id="7c1fc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1fc-113">-ResourceGroupName</span></span>
<span data-ttu-id="7c1fc-114">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7c1fc-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1fc-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7c1fc-115">-ResourceName</span></span>
<span data-ttu-id="7c1fc-116">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7c1fc-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1fc-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c1fc-117">-ResourceId</span></span>
<span data-ttu-id="7c1fc-118">Resurs-ID för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7c1fc-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1fc-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="7c1fc-119">-VpnConnectionId</span></span>
<span data-ttu-id="7c1fc-120">ID för VPN-anslutning</span><span class="sxs-lookup"><span data-stu-id="7c1fc-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1fc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c1fc-121">-InputObject</span></span>
<span data-ttu-id="7c1fc-122">Objekt för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7c1fc-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1fc-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c1fc-123">-AsJob</span></span>
<span data-ttu-id="7c1fc-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7c1fc-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c1fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1fc-125">CommonParameters</span></span>
<span data-ttu-id="7c1fc-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c1fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1fc-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c1fc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1fc-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c1fc-128">INPUTS</span></span>

### <span data-ttu-id="7c1fc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7c1fc-129">System.String</span></span>

## <span data-ttu-id="7c1fc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c1fc-130">OUTPUTS</span></span>

### <span data-ttu-id="7c1fc-131">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7c1fc-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7c1fc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c1fc-132">NOTES</span></span>

## <span data-ttu-id="7c1fc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c1fc-133">RELATED LINKS</span></span>
