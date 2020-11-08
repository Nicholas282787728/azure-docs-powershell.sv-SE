---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258228"
---
# <span data-ttu-id="7b9dc-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7b9dc-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7b9dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9dc-103">Skapar en IP-konfiguration för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7b9dc-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="7b9dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b9dc-104">SYNTAX</span></span>

### <span data-ttu-id="7b9dc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b9dc-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9dc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7b9dc-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9dc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b9dc-107">DESCRIPTION</span></span>
<span data-ttu-id="7b9dc-108">Cmdleten **New-AzVirtualNetworkGatewayIpConfig** skapar en konfiguration som är kopplad till en virtuell nätverksgateway med en (tidigare skapad) offentlig IP-adress baserat på Subnet-ID.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="7b9dc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b9dc-109">EXAMPLES</span></span>

### <span data-ttu-id="7b9dc-110">1: skapa en IP-konfiguration för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7b9dc-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="7b9dc-111">Konfigurerar en virtuell nätverksgateway med en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="7b9dc-112">Variabeln $myGWsubnet hämtas med cmdleten **Get-AzVirtualNetworkSubnetConfig** på "GatewaySubnet" i det virtuella nätverk som du tänker skapa en virtuell nätverksgateway för.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="7b9dc-113">Variabeln $myGWpip erhålls med hjälp av **New-AzPublicIpAddress** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="7b9dc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b9dc-114">PARAMETERS</span></span>

### <span data-ttu-id="7b9dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9dc-115">-DefaultProfile</span></span>
<span data-ttu-id="7b9dc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b9dc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b9dc-117">-Name</span></span>
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

### <span data-ttu-id="7b9dc-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b9dc-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="7b9dc-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b9dc-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="7b9dc-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7b9dc-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="7b9dc-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="7b9dc-121">-Subnet</span></span>
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

### <span data-ttu-id="7b9dc-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7b9dc-122">-SubnetId</span></span>
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

### <span data-ttu-id="7b9dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9dc-123">CommonParameters</span></span>
<span data-ttu-id="7b9dc-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9dc-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b9dc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9dc-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b9dc-126">INPUTS</span></span>

### <span data-ttu-id="7b9dc-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="7b9dc-127">None</span></span>

## <span data-ttu-id="7b9dc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b9dc-128">OUTPUTS</span></span>

### <span data-ttu-id="7b9dc-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b9dc-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="7b9dc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b9dc-130">NOTES</span></span>

## <span data-ttu-id="7b9dc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b9dc-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b9dc-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7b9dc-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="7b9dc-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7b9dc-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
