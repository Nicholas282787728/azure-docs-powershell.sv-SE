---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b00c3950140c0ebf158170a8ddd2396e62c2b2c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756376"
---
# <span data-ttu-id="f8bf4-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8bf4-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f8bf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bf4-103">Skapar en IP-konfiguration för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="f8bf4-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8bf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8bf4-104">SYNTAX</span></span>

### <span data-ttu-id="f8bf4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8bf4-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bf4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f8bf4-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8bf4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8bf4-107">DESCRIPTION</span></span>
<span data-ttu-id="f8bf4-108">Cmdleten **New-AzureRmVirtualNetworkGatewayIpConfig** skapar en konfiguration som är kopplad till en virtuell nätverksgateway med en (tidigare skapad) offentlig IP-adress baserat på Subnet-ID.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="f8bf4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-109">EXAMPLES</span></span>

### <span data-ttu-id="f8bf4-110">1: skapa en IP-konfiguration för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="f8bf4-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="f8bf4-111">Konfigurerar en virtuell nätverksgateway med en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="f8bf4-112">Variabeln $myGWsubnet hämtas med cmdleten **Get-AzureRmVirtualNetworkSubnetConfig** på "GatewaySubnet" i det virtuella nätverk som du tänker skapa en virtuell nätverksgateway för.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="f8bf4-113">Variabeln $myGWpip erhålls med hjälp av **New-AzureRmPublicIpAddress** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="f8bf4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8bf4-114">PARAMETERS</span></span>

### <span data-ttu-id="f8bf4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bf4-115">-DefaultProfile</span></span>
<span data-ttu-id="f8bf4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8bf4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8bf4-117">-Name</span></span>
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

### <span data-ttu-id="f8bf4-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8bf4-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="f8bf4-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8bf4-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="f8bf4-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f8bf4-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="f8bf4-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="f8bf4-121">-Subnet</span></span>
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

### <span data-ttu-id="f8bf4-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f8bf4-122">-SubnetId</span></span>
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

### <span data-ttu-id="f8bf4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bf4-123">CommonParameters</span></span>
<span data-ttu-id="f8bf4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bf4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8bf4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bf4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-126">INPUTS</span></span>

### <span data-ttu-id="f8bf4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8bf4-127">None</span></span>

## <span data-ttu-id="f8bf4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8bf4-128">OUTPUTS</span></span>

### <span data-ttu-id="f8bf4-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8bf4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="f8bf4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8bf4-130">NOTES</span></span>

## <span data-ttu-id="f8bf4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8bf4-131">RELATED LINKS</span></span>
