---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 759e0c9ad61a00ea7fb0c6caa4551634ef614759
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918430"
---
# <span data-ttu-id="770db-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="770db-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="770db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="770db-102">SYNOPSIS</span></span>
<span data-ttu-id="770db-103">Visar en lista över vägar som annonseras av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="770db-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="770db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="770db-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="770db-105">DESCRIPTION</span></span>
<span data-ttu-id="770db-106">Med IP för en BGP-peer räknas vägarna som annonseras till den motparten av den angivna Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="770db-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="770db-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="770db-107">EXAMPLES</span></span>

### <span data-ttu-id="770db-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="770db-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="770db-109">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName hämtas en lista över vägar som annonseras till BGP-motparten med IP-10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="770db-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="770db-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="770db-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="770db-111">För Azure Gateway med namnet gatewayName i resurs grupp resourceGroupName hämtas vägar som annonseras till den första BGP-peer i gatewayens lista över BGP-peers.</span><span class="sxs-lookup"><span data-stu-id="770db-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="770db-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="770db-112">PARAMETERS</span></span>

### <span data-ttu-id="770db-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="770db-113">-AsJob</span></span>
<span data-ttu-id="770db-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="770db-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="770db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770db-115">-DefaultProfile</span></span>
<span data-ttu-id="770db-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="770db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="770db-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="770db-117">-Peer</span></span>
<span data-ttu-id="770db-118">BGP peers IP-adress.</span><span class="sxs-lookup"><span data-stu-id="770db-118">BGP peer's IP address.</span></span> <span data-ttu-id="770db-119">Detta ska vara en IP-adress i det adresser som är tillgängligt från det virtuella Azure-nätverket som gatewayen distribueras i.</span><span class="sxs-lookup"><span data-stu-id="770db-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="770db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770db-120">-ResourceGroupName</span></span>
<span data-ttu-id="770db-121">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="770db-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="770db-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="770db-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="770db-123">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="770db-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="770db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770db-124">CommonParameters</span></span>
<span data-ttu-id="770db-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770db-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="770db-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770db-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="770db-127">INPUTS</span></span>

### <span data-ttu-id="770db-128">System. String</span><span class="sxs-lookup"><span data-stu-id="770db-128">System.String</span></span>

## <span data-ttu-id="770db-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="770db-129">OUTPUTS</span></span>

### <span data-ttu-id="770db-130">Microsoft. Azure. commands. Networks. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="770db-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="770db-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="770db-131">NOTES</span></span>
<span data-ttu-id="770db-132">Det här kommandot kan bara användas för virtuella Azure-gateways med BGP-aktiverade anslutningar.</span><span class="sxs-lookup"><span data-stu-id="770db-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="770db-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="770db-133">RELATED LINKS</span></span>
