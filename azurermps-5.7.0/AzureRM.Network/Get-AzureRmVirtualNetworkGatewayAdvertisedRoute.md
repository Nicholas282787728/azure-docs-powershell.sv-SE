---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: aee420343d2ebe0a78fccd19395abd67262500a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578140"
---
# <span data-ttu-id="3f0ce-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="3f0ce-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="3f0ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0ce-103">Visar en lista över vägar som annonseras av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="3f0ce-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f0ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f0ce-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f0ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="3f0ce-106">Med IP för en BGP-peer räknas vägarna som annonseras till den motparten av den angivna Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="3f0ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="3f0ce-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f0ce-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="3f0ce-109">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName retrives en lista över vägar som annonseras till BGP-motparten med IP-10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="3f0ce-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="3f0ce-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f0ce-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="3f0ce-111">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName hämtas vägar som annonseras till den första BGP-peer i gatewayens lista över BGP-peers.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="3f0ce-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f0ce-112">PARAMETERS</span></span>

### <span data-ttu-id="3f0ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f0ce-113">-AsJob</span></span>
<span data-ttu-id="3f0ce-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3f0ce-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f0ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0ce-115">-DefaultProfile</span></span>
<span data-ttu-id="3f0ce-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f0ce-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="3f0ce-117">-Peer</span></span>
<span data-ttu-id="3f0ce-118">BGP peers IP-adress.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-118">BGP peer's IP address.</span></span> <span data-ttu-id="3f0ce-119">Detta ska vara en IP-adress i det adresser som är tillgängligt från det virtuella Azure-nätverket som gatewayen distribueras i.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="3f0ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f0ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f0ce-121">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3f0ce-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="3f0ce-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3f0ce-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3f0ce-123">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3f0ce-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="3f0ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0ce-124">CommonParameters</span></span>
<span data-ttu-id="3f0ce-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0ce-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f0ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0ce-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f0ce-127">INPUTS</span></span>

### <span data-ttu-id="3f0ce-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3f0ce-128">System.String</span></span>

## <span data-ttu-id="3f0ce-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f0ce-129">OUTPUTS</span></span>

### <span data-ttu-id="3f0ce-130">Microsoft. Azure. commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="3f0ce-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="3f0ce-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f0ce-131">NOTES</span></span>
<span data-ttu-id="3f0ce-132">Det här kommandot kan bara användas för virtuella Azure-gateways med BGP-aktiverade anslutningar.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="3f0ce-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f0ce-133">RELATED LINKS</span></span>
