---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2ce0cb130e6c4d25d4b076d06224364011ced2b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584156"
---
# <span data-ttu-id="e9471-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9471-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e9471-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9471-102">SYNOPSIS</span></span>
<span data-ttu-id="e9471-103">Lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e9471-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9471-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9471-104">SYNTAX</span></span>

### <span data-ttu-id="e9471-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9471-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9471-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e9471-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9471-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9471-107">DESCRIPTION</span></span>
<span data-ttu-id="e9471-108">Cmdleten **Add-AzureRmApplicationGatewayIPConfiguration** lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e9471-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="e9471-109">IP-konfigurationer innehåller det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="e9471-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="e9471-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9471-110">EXAMPLES</span></span>

### <span data-ttu-id="e9471-111">Exempel 1: lägga till en virtuell nätverks konfiguration i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="e9471-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="e9471-112">Det första kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e9471-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="e9471-113">Det andra kommandot skapar ett undernät med det skapade virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="e9471-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="e9471-114">Det tredje kommandot får programgatewayen och lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="e9471-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e9471-115">Med kommandot fouth lägger du till IP-konfigurationen till den Programgateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e9471-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e9471-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9471-116">PARAMETERS</span></span>

### <span data-ttu-id="e9471-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9471-117">-ApplicationGateway</span></span>
<span data-ttu-id="e9471-118">Anger den Programgateway som denna cmdlet lägger till en IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="e9471-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9471-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9471-119">-DefaultProfile</span></span>
<span data-ttu-id="e9471-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9471-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9471-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9471-121">-Name</span></span>
<span data-ttu-id="e9471-122">Anger namnet på den IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e9471-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="e9471-123">-Undernät</span><span class="sxs-lookup"><span data-stu-id="e9471-123">-Subnet</span></span>
<span data-ttu-id="e9471-124">Anger ett undernät.</span><span class="sxs-lookup"><span data-stu-id="e9471-124">Specifies a subnet.</span></span>
<span data-ttu-id="e9471-125">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="e9471-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e9471-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e9471-126">-SubnetId</span></span>
<span data-ttu-id="e9471-127">Anger ett nät-ID.</span><span class="sxs-lookup"><span data-stu-id="e9471-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="e9471-128">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="e9471-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e9471-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9471-129">CommonParameters</span></span>
<span data-ttu-id="e9471-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9471-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9471-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9471-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9471-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9471-132">INPUTS</span></span>

### <span data-ttu-id="e9471-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9471-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e9471-134">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9471-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e9471-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9471-135">OUTPUTS</span></span>

### <span data-ttu-id="e9471-136">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9471-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9471-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9471-137">NOTES</span></span>

## <span data-ttu-id="e9471-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9471-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9471-139">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9471-139">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e9471-140">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9471-140">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e9471-141">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9471-141">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e9471-142">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9471-142">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


