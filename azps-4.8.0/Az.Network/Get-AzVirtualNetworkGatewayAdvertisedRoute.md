---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258262"
---
# <span data-ttu-id="7c5b9-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="7c5b9-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="7c5b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5b9-103">Visar en lista över vägar som annonseras av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="7c5b9-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="7c5b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c5b9-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c5b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5b9-106">Med IP för en BGP-peer räknas vägarna som annonseras till den motparten av den angivna Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="7c5b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c5b9-107">EXAMPLES</span></span>

### <span data-ttu-id="7c5b9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c5b9-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="7c5b9-109">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName hämtas en lista över vägar som annonseras till BGP-motparten med IP-10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="7c5b9-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="7c5b9-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7c5b9-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="7c5b9-111">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName hämtas vägar som annonseras till den första BGP-peer i gatewayens lista över BGP-peers.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="7c5b9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c5b9-112">PARAMETERS</span></span>

### <span data-ttu-id="7c5b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c5b9-113">-AsJob</span></span>
<span data-ttu-id="7c5b9-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7c5b9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c5b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5b9-115">-DefaultProfile</span></span>
<span data-ttu-id="7c5b9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c5b9-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="7c5b9-117">-Peer</span></span>
<span data-ttu-id="7c5b9-118">BGP peers IP-adress.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-118">BGP peer's IP address.</span></span> <span data-ttu-id="7c5b9-119">Detta ska vara en IP-adress i det adresser som är tillgängligt från det virtuella Azure-nätverket som gatewayen distribueras i.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="7c5b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c5b9-121">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7c5b9-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="7c5b9-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7c5b9-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7c5b9-123">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7c5b9-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="7c5b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5b9-124">CommonParameters</span></span>
<span data-ttu-id="7c5b9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5b9-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c5b9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5b9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c5b9-127">INPUTS</span></span>

### <span data-ttu-id="7c5b9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7c5b9-128">System.String</span></span>

## <span data-ttu-id="7c5b9-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c5b9-129">OUTPUTS</span></span>

### <span data-ttu-id="7c5b9-130">Microsoft. Azure. commands. Networks. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="7c5b9-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="7c5b9-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c5b9-131">NOTES</span></span>
<span data-ttu-id="7c5b9-132">Det här kommandot kan bara användas för virtuella Azure-gateways med BGP-aktiverade anslutningar.</span><span class="sxs-lookup"><span data-stu-id="7c5b9-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="7c5b9-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c5b9-133">RELATED LINKS</span></span>
