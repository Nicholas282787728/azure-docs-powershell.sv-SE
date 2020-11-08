---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089075"
---
# <span data-ttu-id="9532e-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9532e-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9532e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9532e-102">SYNOPSIS</span></span>
<span data-ttu-id="9532e-103">Ändrar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9532e-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="9532e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9532e-104">SYNTAX</span></span>

### <span data-ttu-id="9532e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9532e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9532e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9532e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9532e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9532e-107">DESCRIPTION</span></span>
<span data-ttu-id="9532e-108">Cmdleten **set-AzApplicationGatewayIPConfiguration** ändrar en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9532e-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="9532e-109">En IP-konfiguration innehåller det undernät där en Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="9532e-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="9532e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9532e-110">EXAMPLES</span></span>

### <span data-ttu-id="9532e-111">Exempel 1: uppdatera en IP-konfiguration för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="9532e-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="9532e-112">Det första kommandot hämtar det virtuella nätverk som heter VNet01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="9532e-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="9532e-113">Med det andra kommandot får du en under näts konfiguration som heter Subnet01 med $VNet och lagrar den i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="9532e-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="9532e-114">Det tredje kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="9532e-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9532e-115">Kommandot tillbaka anger IP-konfigurationen för den Programgateway som lagras i $AppGw till den under näts konfiguration som lagras i $Subnet.</span><span class="sxs-lookup"><span data-stu-id="9532e-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="9532e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9532e-116">PARAMETERS</span></span>

### <span data-ttu-id="9532e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9532e-117">-ApplicationGateway</span></span>
<span data-ttu-id="9532e-118">Anger ett Application Gateway-objekt som denna cmdlet associerar en IP-konfiguration med.</span><span class="sxs-lookup"><span data-stu-id="9532e-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="9532e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9532e-119">-DefaultProfile</span></span>
<span data-ttu-id="9532e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9532e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9532e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9532e-121">-Name</span></span>
<span data-ttu-id="9532e-122">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9532e-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="9532e-123">-Undernät</span><span class="sxs-lookup"><span data-stu-id="9532e-123">-Subnet</span></span>
<span data-ttu-id="9532e-124">Anger under nätet.</span><span class="sxs-lookup"><span data-stu-id="9532e-124">Specifies the subnet.</span></span>
<span data-ttu-id="9532e-125">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="9532e-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="9532e-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9532e-126">-SubnetId</span></span>
<span data-ttu-id="9532e-127">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="9532e-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="9532e-128">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="9532e-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="9532e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9532e-129">CommonParameters</span></span>
<span data-ttu-id="9532e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9532e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9532e-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9532e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9532e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9532e-132">INPUTS</span></span>

### <span data-ttu-id="9532e-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9532e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9532e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9532e-134">OUTPUTS</span></span>

### <span data-ttu-id="9532e-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9532e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9532e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9532e-136">NOTES</span></span>

## <span data-ttu-id="9532e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9532e-137">RELATED LINKS</span></span>

[<span data-ttu-id="9532e-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9532e-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9532e-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9532e-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9532e-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9532e-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9532e-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9532e-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9532e-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9532e-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


