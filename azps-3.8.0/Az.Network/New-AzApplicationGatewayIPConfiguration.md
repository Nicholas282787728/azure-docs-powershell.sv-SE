---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092528"
---
# <span data-ttu-id="ca654-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca654-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ca654-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca654-102">SYNOPSIS</span></span>
<span data-ttu-id="ca654-103">Skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca654-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="ca654-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca654-104">SYNTAX</span></span>

### <span data-ttu-id="ca654-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca654-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca654-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ca654-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca654-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca654-107">DESCRIPTION</span></span>
<span data-ttu-id="ca654-108">Cmdleten **New-AzApplicationGatewayIPConfiguration** skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca654-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="ca654-109">IP-konfigurationen innehåller det undernät då Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="ca654-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="ca654-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca654-110">EXAMPLES</span></span>

### <span data-ttu-id="ca654-111">Exempel 1: skapa en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca654-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="ca654-112">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ca654-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="ca654-113">Det andra kommandot får under nätets konfiguration för det undernät som det virtuella nätverket i föregående kommando tillhör och lagrar det i $Subnet variabeln.</span><span class="sxs-lookup"><span data-stu-id="ca654-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ca654-114">Det tredje kommandot skapar IP-konfigurationen med $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ca654-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="ca654-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca654-115">PARAMETERS</span></span>

### <span data-ttu-id="ca654-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca654-116">-DefaultProfile</span></span>
<span data-ttu-id="ca654-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca654-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca654-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca654-118">-Name</span></span>
<span data-ttu-id="ca654-119">Anger namnet på den IP-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ca654-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="ca654-120">-Undernät</span><span class="sxs-lookup"><span data-stu-id="ca654-120">-Subnet</span></span>
<span data-ttu-id="ca654-121">Anger ett under näts objekt.</span><span class="sxs-lookup"><span data-stu-id="ca654-121">Specifies the subnet object.</span></span>
<span data-ttu-id="ca654-122">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="ca654-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="ca654-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ca654-123">-SubnetId</span></span>
<span data-ttu-id="ca654-124">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="ca654-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="ca654-125">Det här är det undernät där programgatewayen distribueras.</span><span class="sxs-lookup"><span data-stu-id="ca654-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="ca654-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca654-126">CommonParameters</span></span>
<span data-ttu-id="ca654-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca654-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca654-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca654-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca654-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca654-129">INPUTS</span></span>

### <span data-ttu-id="ca654-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="ca654-130">None</span></span>

## <span data-ttu-id="ca654-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca654-131">OUTPUTS</span></span>

### <span data-ttu-id="ca654-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca654-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ca654-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca654-133">NOTES</span></span>

## <span data-ttu-id="ca654-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca654-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca654-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca654-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ca654-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca654-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ca654-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca654-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ca654-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca654-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

