---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416411"
---
# <span data-ttu-id="81b28-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81b28-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="81b28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81b28-102">SYNOPSIS</span></span>
<span data-ttu-id="81b28-103">Ändrar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="81b28-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="81b28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81b28-104">SYNTAX</span></span>

### <span data-ttu-id="81b28-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81b28-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81b28-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="81b28-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81b28-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81b28-107">DESCRIPTION</span></span>
<span data-ttu-id="81b28-108">Cmdleten **set-AzApplicationGatewayIPConfiguration** ändrar en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="81b28-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="81b28-109">En IP-konfiguration innehåller det undernät där en Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="81b28-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="81b28-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81b28-110">EXAMPLES</span></span>

### <span data-ttu-id="81b28-111">Exempel 1: uppdatera en IP-konfiguration för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="81b28-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="81b28-112">Det första kommandot hämtar det virtuella nätverk som heter VNet01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="81b28-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="81b28-113">Med det andra kommandot får du en under näts konfiguration som heter Subnet01 med $VNet och lagrar den i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="81b28-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="81b28-114">Det tredje kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="81b28-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="81b28-115">Kommandot tillbaka anger IP-konfigurationen för den Programgateway som lagras i $AppGw till den under näts konfiguration som lagras i $Subnet.</span><span class="sxs-lookup"><span data-stu-id="81b28-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="81b28-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81b28-116">PARAMETERS</span></span>

### <span data-ttu-id="81b28-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81b28-117">-ApplicationGateway</span></span>
<span data-ttu-id="81b28-118">Anger ett Application Gateway-objekt som denna cmdlet associerar en IP-konfiguration med.</span><span class="sxs-lookup"><span data-stu-id="81b28-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="81b28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b28-119">-DefaultProfile</span></span>
<span data-ttu-id="81b28-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81b28-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b28-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="81b28-121">-Name</span></span>
<span data-ttu-id="81b28-122">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="81b28-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="81b28-123">-Undernät</span><span class="sxs-lookup"><span data-stu-id="81b28-123">-Subnet</span></span>
<span data-ttu-id="81b28-124">Anger under nätet.</span><span class="sxs-lookup"><span data-stu-id="81b28-124">Specifies the subnet.</span></span>
<span data-ttu-id="81b28-125">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="81b28-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="81b28-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="81b28-126">-SubnetId</span></span>
<span data-ttu-id="81b28-127">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="81b28-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="81b28-128">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="81b28-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="81b28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b28-129">CommonParameters</span></span>
<span data-ttu-id="81b28-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b28-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b28-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b28-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81b28-132">INPUTS</span></span>

### <span data-ttu-id="81b28-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81b28-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81b28-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81b28-134">OUTPUTS</span></span>

### <span data-ttu-id="81b28-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81b28-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81b28-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81b28-136">NOTES</span></span>

## <span data-ttu-id="81b28-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81b28-137">RELATED LINKS</span></span>

[<span data-ttu-id="81b28-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81b28-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="81b28-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81b28-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="81b28-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81b28-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="81b28-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81b28-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="81b28-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81b28-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


