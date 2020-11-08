---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260702"
---
# <span data-ttu-id="f62d6-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f62d6-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f62d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f62d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f62d6-103">Ändrar en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f62d6-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="f62d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f62d6-104">SYNTAX</span></span>

### <span data-ttu-id="f62d6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f62d6-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f62d6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f62d6-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f62d6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f62d6-107">DESCRIPTION</span></span>
<span data-ttu-id="f62d6-108">Cmdleten **set-AzApplicationGatewayFrontendIPConfig** uppdaterar en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f62d6-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="f62d6-109">En Programgateway stöder två typer av front-IP-adresser:</span><span class="sxs-lookup"><span data-stu-id="f62d6-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="f62d6-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="f62d6-110">Public IP addresses</span></span>
- <span data-ttu-id="f62d6-111">Privata IP-adresser som konfigurationen använder intern belastnings utjämning (ILB) för en Programgateway får ha högst en offentlig IP-adress och en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="f62d6-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="f62d6-112">En offentlig IP-adress och en privat IP-adress bör läggas till separat som front-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f62d6-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="f62d6-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f62d6-113">EXAMPLES</span></span>

### <span data-ttu-id="f62d6-114">Exempel 1: Ange en offentlig IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f62d6-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="f62d6-115">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="f62d6-116">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f62d6-117">Det tredje kommandot uppdaterar front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f62d6-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="f62d6-118">Exempel 2: Ange en statisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f62d6-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="f62d6-119">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f62d6-120">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f62d6-121">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f62d6-122">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="f62d6-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="f62d6-123">Exempel 3: Ange en dynamisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f62d6-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="f62d6-124">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f62d6-125">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f62d6-126">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f62d6-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f62d6-127">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="f62d6-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="f62d6-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f62d6-128">PARAMETERS</span></span>

### <span data-ttu-id="f62d6-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f62d6-129">-ApplicationGateway</span></span>
<span data-ttu-id="f62d6-130">Anger ett objekt för Application Gateway där du kan ändra front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f62d6-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="f62d6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62d6-131">-DefaultProfile</span></span>
<span data-ttu-id="f62d6-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f62d6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62d6-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="f62d6-133">-Name</span></span>
<span data-ttu-id="f62d6-134">Anger namnet på den frontend-IP-konfiguration som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f62d6-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f62d6-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="f62d6-135">-PrivateIPAddress</span></span>
<span data-ttu-id="f62d6-136">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="f62d6-136">Specifies the private IP address.</span></span>
<span data-ttu-id="f62d6-137">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="f62d6-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="f62d6-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f62d6-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="f62d6-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f62d6-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62d6-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f62d6-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="f62d6-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f62d6-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="f62d6-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="f62d6-142">-PublicIPAddress</span></span>
<span data-ttu-id="f62d6-143">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="f62d6-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="f62d6-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="f62d6-144">-PublicIPAddressId</span></span>
<span data-ttu-id="f62d6-145">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="f62d6-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="f62d6-146">-Undernät</span><span class="sxs-lookup"><span data-stu-id="f62d6-146">-Subnet</span></span>
<span data-ttu-id="f62d6-147">Anger det undernät som Application Gateway använder.</span><span class="sxs-lookup"><span data-stu-id="f62d6-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="f62d6-148">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="f62d6-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="f62d6-149">Om *PrivateIPAddress* -adressen anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="f62d6-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="f62d6-150">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f62d6-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f62d6-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f62d6-151">-SubnetId</span></span>
<span data-ttu-id="f62d6-152">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="f62d6-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="f62d6-153">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="f62d6-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="f62d6-154">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="f62d6-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="f62d6-155">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f62d6-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f62d6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62d6-156">CommonParameters</span></span>
<span data-ttu-id="f62d6-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62d6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62d6-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f62d6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62d6-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f62d6-159">INPUTS</span></span>

### <span data-ttu-id="f62d6-160">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f62d6-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f62d6-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f62d6-161">OUTPUTS</span></span>

### <span data-ttu-id="f62d6-162">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f62d6-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f62d6-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f62d6-163">NOTES</span></span>

## <span data-ttu-id="f62d6-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f62d6-164">RELATED LINKS</span></span>

[<span data-ttu-id="f62d6-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f62d6-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f62d6-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f62d6-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f62d6-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f62d6-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f62d6-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f62d6-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f62d6-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f62d6-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


