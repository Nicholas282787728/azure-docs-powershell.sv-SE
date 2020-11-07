---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: f92b211befbf019f46869f733fa012e74e72c327
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922216"
---
# <span data-ttu-id="0dddb-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="0dddb-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="0dddb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0dddb-102">SYNOPSIS</span></span>
<span data-ttu-id="0dddb-103">Visar en lista med BGP-peers för Azure-nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="0dddb-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="0dddb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0dddb-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dddb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0dddb-105">DESCRIPTION</span></span>
<span data-ttu-id="0dddb-106">Det här kommandot räknar upp BGP-peers en Azure virtuell nätverksgateway är konfigurerad för att vara peer med.</span><span class="sxs-lookup"><span data-stu-id="0dddb-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="0dddb-107">Statusen för varje peer ges också.</span><span class="sxs-lookup"><span data-stu-id="0dddb-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="0dddb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0dddb-108">EXAMPLES</span></span>

### <span data-ttu-id="0dddb-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0dddb-109">Example 1</span></span>
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

<span data-ttu-id="0dddb-110">Hämtar BGP-peers för den Azure Virtual Network gateway som heter gatewayName i resurs grupp resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0dddb-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="0dddb-111">I det här exemplet visas en ansluten BGP-peer med en IP på 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="0dddb-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="0dddb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0dddb-112">PARAMETERS</span></span>

### <span data-ttu-id="0dddb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dddb-113">-AsJob</span></span>
<span data-ttu-id="0dddb-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0dddb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dddb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dddb-115">-DefaultProfile</span></span>
<span data-ttu-id="0dddb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0dddb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dddb-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="0dddb-117">-Peer</span></span>
<span data-ttu-id="0dddb-118">IP för motparten för att hämta status för</span><span class="sxs-lookup"><span data-stu-id="0dddb-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="0dddb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dddb-119">-ResourceGroupName</span></span>
<span data-ttu-id="0dddb-120">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="0dddb-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="0dddb-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0dddb-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0dddb-122">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="0dddb-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="0dddb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dddb-123">CommonParameters</span></span>
<span data-ttu-id="0dddb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dddb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dddb-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dddb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dddb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0dddb-126">INPUTS</span></span>

### <span data-ttu-id="0dddb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0dddb-127">System.String</span></span>

## <span data-ttu-id="0dddb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0dddb-128">OUTPUTS</span></span>

### <span data-ttu-id="0dddb-129">Microsoft. Azure. commands. Network. Models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="0dddb-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="0dddb-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0dddb-130">NOTES</span></span>

## <span data-ttu-id="0dddb-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0dddb-131">RELATED LINKS</span></span>

