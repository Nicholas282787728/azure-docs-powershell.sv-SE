---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090995"
---
# <span data-ttu-id="76bf5-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="76bf5-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="76bf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="76bf5-103">Visar en lista med BGP-peers för Azure-nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="76bf5-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="76bf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76bf5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76bf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="76bf5-106">Det här kommandot räknar upp BGP-peers en Azure virtuell nätverksgateway är konfigurerad för att vara peer med.</span><span class="sxs-lookup"><span data-stu-id="76bf5-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="76bf5-107">Statusen för varje peer ges också.</span><span class="sxs-lookup"><span data-stu-id="76bf5-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="76bf5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76bf5-108">EXAMPLES</span></span>

### <span data-ttu-id="76bf5-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76bf5-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="76bf5-110">Hämtar BGP-peers för den Azure Virtual Network gateway som heter gatewayName i resurs grupp resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76bf5-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="76bf5-111">I det här exemplet visas en ansluten BGP-peer med en IP på 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="76bf5-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="76bf5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76bf5-112">PARAMETERS</span></span>

### <span data-ttu-id="76bf5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76bf5-113">-AsJob</span></span>
<span data-ttu-id="76bf5-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="76bf5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76bf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76bf5-115">-DefaultProfile</span></span>
<span data-ttu-id="76bf5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76bf5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76bf5-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="76bf5-117">-Peer</span></span>
<span data-ttu-id="76bf5-118">IP för motparten för att hämta status för</span><span class="sxs-lookup"><span data-stu-id="76bf5-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="76bf5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76bf5-119">-ResourceGroupName</span></span>
<span data-ttu-id="76bf5-120">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="76bf5-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="76bf5-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="76bf5-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="76bf5-122">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="76bf5-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="76bf5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76bf5-123">CommonParameters</span></span>
<span data-ttu-id="76bf5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76bf5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76bf5-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76bf5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76bf5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76bf5-126">INPUTS</span></span>

### <span data-ttu-id="76bf5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="76bf5-127">System.String</span></span>

## <span data-ttu-id="76bf5-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76bf5-128">OUTPUTS</span></span>

### <span data-ttu-id="76bf5-129">Microsoft. Azure. commands. Networks. Models. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="76bf5-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="76bf5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76bf5-130">NOTES</span></span>

## <span data-ttu-id="76bf5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76bf5-131">RELATED LINKS</span></span>
