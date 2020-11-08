---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 30238f9466e87ab732b1b2b6d30bba26bcd4c83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092051"
---
# <span data-ttu-id="6ad56-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6ad56-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="6ad56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ad56-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad56-103">Lägger till en klient-IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6ad56-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="6ad56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ad56-104">SYNTAX</span></span>

### <span data-ttu-id="6ad56-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad56-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad56-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6ad56-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ad56-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ad56-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad56-108">Cmdleten **Add-AzApplicationGatewayFrontendIPConfig** lägger till en klient-IP-konfiguration i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6ad56-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="6ad56-109">En Programgateway stöder två typer av front-IP-konfigurationer:</span><span class="sxs-lookup"><span data-stu-id="6ad56-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="6ad56-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="6ad56-110">Public IP addresses</span></span>
- <span data-ttu-id="6ad56-111">Privata IP-adresser med intern belastnings utjämning (ILB) en Programgateway får ha högst en offentlig IP och en privat IP.</span><span class="sxs-lookup"><span data-stu-id="6ad56-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="6ad56-112">Lägg till en offentlig IP-adress och en privat IP-adress som separata frontend-adresser.</span><span class="sxs-lookup"><span data-stu-id="6ad56-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="6ad56-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ad56-113">EXAMPLES</span></span>

### <span data-ttu-id="6ad56-114">Exempel 1: lägga till en offentlig IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="6ad56-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="6ad56-115">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="6ad56-116">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6ad56-117">Det tredje kommandot lägger till front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="6ad56-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="6ad56-118">Exempel 2: lägga till en statisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="6ad56-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="6ad56-119">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="6ad56-120">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6ad56-121">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6ad56-122">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="6ad56-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="6ad56-123">Exempel 3: lägga till en dynamisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="6ad56-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="6ad56-124">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="6ad56-125">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6ad56-126">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="6ad56-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6ad56-127">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="6ad56-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="6ad56-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ad56-128">PARAMETERS</span></span>

### <span data-ttu-id="6ad56-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad56-129">-ApplicationGateway</span></span>
<span data-ttu-id="6ad56-130">Anger den Programgateway som denna cmdlet lägger till en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="6ad56-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6ad56-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad56-131">-DefaultProfile</span></span>
<span data-ttu-id="6ad56-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad56-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad56-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ad56-133">-Name</span></span>
<span data-ttu-id="6ad56-134">Anger namnet på den frontend-IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6ad56-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="6ad56-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="6ad56-135">-PrivateIPAddress</span></span>
<span data-ttu-id="6ad56-136">Anger den privata IP-adressen som ska läggas till som front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad56-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="6ad56-137">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="6ad56-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="6ad56-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="6ad56-138">-PublicIPAddress</span></span>
<span data-ttu-id="6ad56-139">Anger den offentliga IP-adressen som denna cmdlet lägger till som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad56-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="6ad56-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="6ad56-140">-PublicIPAddressId</span></span>
<span data-ttu-id="6ad56-141">Anger ID för den offentliga IP-adressen som denna cmdlet lägger till som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad56-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="6ad56-142">-Undernät</span><span class="sxs-lookup"><span data-stu-id="6ad56-142">-Subnet</span></span>
<span data-ttu-id="6ad56-143">Anger det undernät som denna cmdlet lägger till som front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6ad56-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="6ad56-144">Om du anger den här parametern innebär det att programgatewayen stöder en privat IP-baserad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6ad56-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="6ad56-145">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="6ad56-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="6ad56-146">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad56-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6ad56-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6ad56-147">-SubnetId</span></span>
<span data-ttu-id="6ad56-148">Anger det ID-nummer som denna cmdlet lägger till som front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6ad56-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="6ad56-149">Att skicka under nätverk innebär privat IP.</span><span class="sxs-lookup"><span data-stu-id="6ad56-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="6ad56-150">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="6ad56-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="6ad56-151">Annars hämtas en IP-adress från detta undernät dynamiskt som front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6ad56-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="6ad56-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad56-152">CommonParameters</span></span>
<span data-ttu-id="6ad56-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad56-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad56-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad56-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad56-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ad56-155">INPUTS</span></span>

### <span data-ttu-id="6ad56-156">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad56-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ad56-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ad56-157">OUTPUTS</span></span>

### <span data-ttu-id="6ad56-158">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad56-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ad56-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ad56-159">NOTES</span></span>

## <span data-ttu-id="6ad56-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ad56-160">RELATED LINKS</span></span>

[<span data-ttu-id="6ad56-161">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6ad56-161">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6ad56-162">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6ad56-162">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6ad56-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6ad56-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6ad56-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6ad56-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


