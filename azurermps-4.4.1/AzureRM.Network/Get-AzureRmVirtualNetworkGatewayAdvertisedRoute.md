---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: a9b8cd9f13de8c1c4e3a7f20a0ffe410211f8973
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755992"
---
# <span data-ttu-id="bcdb1-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="bcdb1-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="bcdb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcdb1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdb1-103">Visar en lista över vägar som annonseras av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="bcdb1-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcdb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcdb1-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcdb1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcdb1-105">DESCRIPTION</span></span>
<span data-ttu-id="bcdb1-106">Med IP för en BGP-peer räknas vägarna som annonseras till den motparten av den angivna Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="bcdb1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcdb1-107">EXAMPLES</span></span>

### <span data-ttu-id="bcdb1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bcdb1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="bcdb1-109">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName retrives en lista över vägar som annonseras till BGP-motparten med IP-10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="bcdb1-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="bcdb1-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bcdb1-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="bcdb1-111">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName hämtas vägar som annonseras till den första BGP-peer i gatewayens lista över BGP-peers.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="bcdb1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcdb1-112">PARAMETERS</span></span>

### <span data-ttu-id="bcdb1-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="bcdb1-113">-Peer</span></span>
<span data-ttu-id="bcdb1-114">BGP peers IP-adress.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-114">BGP peer's IP address.</span></span> <span data-ttu-id="bcdb1-115">Detta ska vara en IP-adress i det adresser som är tillgängligt från det virtuella Azure-nätverket som gatewayen distribueras i.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-115">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="bcdb1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdb1-116">-ResourceGroupName</span></span>
<span data-ttu-id="bcdb1-117">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="bcdb1-117">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="bcdb1-118">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bcdb1-118">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bcdb1-119">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="bcdb1-119">Virtual network gateway name</span></span>

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

### <span data-ttu-id="bcdb1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdb1-120">-DefaultProfile</span></span>
<span data-ttu-id="bcdb1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcdb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdb1-122">CommonParameters</span></span>
<span data-ttu-id="bcdb1-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdb1-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcdb1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdb1-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcdb1-125">INPUTS</span></span>

### <span data-ttu-id="bcdb1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bcdb1-126">System.String</span></span>

## <span data-ttu-id="bcdb1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcdb1-127">OUTPUTS</span></span>

### <span data-ttu-id="bcdb1-128">Microsoft. Azure. commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="bcdb1-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="bcdb1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcdb1-129">NOTES</span></span>
<span data-ttu-id="bcdb1-130">Det här kommandot kan bara användas för virtuella Azure-gateways med BGP-aktiverade anslutningar.</span><span class="sxs-lookup"><span data-stu-id="bcdb1-130">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="bcdb1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcdb1-131">RELATED LINKS</span></span>

