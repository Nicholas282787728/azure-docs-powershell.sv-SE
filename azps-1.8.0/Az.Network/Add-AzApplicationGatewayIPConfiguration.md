---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c8dd9faf54d92f34b523292a8b25465978074ad5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753970"
---
# <span data-ttu-id="4cf2a-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cf2a-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4cf2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cf2a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf2a-103">Lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="4cf2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cf2a-104">SYNTAX</span></span>

### <span data-ttu-id="4cf2a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf2a-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf2a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4cf2a-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf2a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cf2a-107">DESCRIPTION</span></span>
<span data-ttu-id="4cf2a-108">Cmdleten **Add-AzApplicationGatewayIPConfiguration** lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="4cf2a-109">IP-konfigurationer innehåller det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="4cf2a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cf2a-110">EXAMPLES</span></span>

### <span data-ttu-id="4cf2a-111">Exempel 1: lägga till en virtuell nätverks konfiguration i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4cf2a-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="4cf2a-112">Det första kommandot får ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="4cf2a-113">Det andra kommandot får ett undernät med det skapade virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="4cf2a-114">Det tredje kommandot får programgatewayen och lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4cf2a-115">Med kommandot fouth lägger du till IP-konfigurationen till den Programgateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4cf2a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cf2a-116">PARAMETERS</span></span>

### <span data-ttu-id="4cf2a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4cf2a-117">-ApplicationGateway</span></span>
<span data-ttu-id="4cf2a-118">Anger den Programgateway som denna cmdlet lägger till en IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="4cf2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf2a-119">-DefaultProfile</span></span>
<span data-ttu-id="4cf2a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cf2a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cf2a-121">-Name</span></span>
<span data-ttu-id="4cf2a-122">Anger namnet på den IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="4cf2a-123">-Undernät</span><span class="sxs-lookup"><span data-stu-id="4cf2a-123">-Subnet</span></span>
<span data-ttu-id="4cf2a-124">Anger ett undernät.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-124">Specifies a subnet.</span></span>
<span data-ttu-id="4cf2a-125">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4cf2a-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4cf2a-126">-SubnetId</span></span>
<span data-ttu-id="4cf2a-127">Anger ett nät-ID.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="4cf2a-128">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4cf2a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf2a-129">CommonParameters</span></span>
<span data-ttu-id="4cf2a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf2a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf2a-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf2a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf2a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cf2a-132">INPUTS</span></span>

### <span data-ttu-id="4cf2a-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4cf2a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4cf2a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cf2a-134">OUTPUTS</span></span>

### <span data-ttu-id="4cf2a-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4cf2a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4cf2a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cf2a-136">NOTES</span></span>

## <span data-ttu-id="4cf2a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cf2a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4cf2a-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cf2a-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4cf2a-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cf2a-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4cf2a-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cf2a-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4cf2a-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cf2a-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


