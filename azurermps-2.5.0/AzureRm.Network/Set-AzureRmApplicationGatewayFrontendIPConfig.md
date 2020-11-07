---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: abcf1665f6117d12ad99e48e8fd15d0a350c1d96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931157"
---
# <span data-ttu-id="72fc4-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="72fc4-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="72fc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="72fc4-103">Ändrar en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="72fc4-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72fc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72fc4-104">SYNTAX</span></span>

### <span data-ttu-id="72fc4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72fc4-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fc4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72fc4-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72fc4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72fc4-107">DESCRIPTION</span></span>
<span data-ttu-id="72fc4-108">Cmdleten **set-AzureRmApplicationGatewayFrontendIPConfig** uppdaterar en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="72fc4-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="72fc4-109">En Programgateway stöder två typer av front-IP-adresser:</span><span class="sxs-lookup"><span data-stu-id="72fc4-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="72fc4-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="72fc4-110">Public IP addresses</span></span>
- <span data-ttu-id="72fc4-111">Privata IP-adresser för vilka konfigurationen använder intern belastnings utjämning (ILB)</span><span class="sxs-lookup"><span data-stu-id="72fc4-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="72fc4-112">En Programgateway får högst ha en offentlig IP-adress och en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="72fc4-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="72fc4-113">En offentlig IP-adress och en privat IP-adress bör läggas till separat som front-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="72fc4-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="72fc4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72fc4-114">EXAMPLES</span></span>

### <span data-ttu-id="72fc4-115">Exempel 1: Ange en offentlig IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="72fc4-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="72fc4-116">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="72fc4-117">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="72fc4-118">Det tredje kommandot uppdaterar front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="72fc4-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="72fc4-119">Exempel 2: Ange en statisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="72fc4-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="72fc4-120">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="72fc4-121">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="72fc4-122">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="72fc4-123">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="72fc4-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="72fc4-124">Exempel 3: Ange en dynamisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="72fc4-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="72fc4-125">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="72fc4-126">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="72fc4-127">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="72fc4-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="72fc4-128">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="72fc4-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="72fc4-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72fc4-129">PARAMETERS</span></span>

### <span data-ttu-id="72fc4-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72fc4-130">-ApplicationGateway</span></span>
<span data-ttu-id="72fc4-131">Anger ett objekt för Application Gateway där du kan ändra front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="72fc4-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fc4-132">-DefaultProfile</span></span>
<span data-ttu-id="72fc4-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72fc4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72fc4-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="72fc4-134">-Name</span></span>
<span data-ttu-id="72fc4-135">Anger namnet på den frontend-IP-konfiguration som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="72fc4-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="72fc4-136">-PrivateIPAddress</span></span>
<span data-ttu-id="72fc4-137">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="72fc4-137">Specifies the private IP address.</span></span>
<span data-ttu-id="72fc4-138">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="72fc4-138">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="72fc4-139">-PublicIPAddress</span></span>
<span data-ttu-id="72fc4-140">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="72fc4-140">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="72fc4-141">-PublicIPAddressId</span></span>
<span data-ttu-id="72fc4-142">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="72fc4-142">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-143">-Undernät</span><span class="sxs-lookup"><span data-stu-id="72fc4-143">-Subnet</span></span>
<span data-ttu-id="72fc4-144">Anger det undernät som Application Gateway använder.</span><span class="sxs-lookup"><span data-stu-id="72fc4-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="72fc4-145">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="72fc4-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="72fc4-146">Om *PrivateIPAddress* -adressen anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="72fc4-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="72fc4-147">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="72fc4-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="72fc4-148">-SubnetId</span></span>
<span data-ttu-id="72fc4-149">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="72fc4-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="72fc4-150">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="72fc4-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="72fc4-151">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="72fc4-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="72fc4-152">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="72fc4-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fc4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fc4-153">CommonParameters</span></span>
<span data-ttu-id="72fc4-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fc4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fc4-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fc4-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fc4-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72fc4-156">INPUTS</span></span>

### <span data-ttu-id="72fc4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="72fc4-157">System.String</span></span>

## <span data-ttu-id="72fc4-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72fc4-158">OUTPUTS</span></span>

### <span data-ttu-id="72fc4-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72fc4-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72fc4-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72fc4-160">NOTES</span></span>

## <span data-ttu-id="72fc4-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72fc4-161">RELATED LINKS</span></span>

[<span data-ttu-id="72fc4-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="72fc4-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="72fc4-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="72fc4-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="72fc4-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="72fc4-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="72fc4-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="72fc4-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="72fc4-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="72fc4-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


