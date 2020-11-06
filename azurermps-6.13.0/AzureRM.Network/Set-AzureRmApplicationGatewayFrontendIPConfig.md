---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e5bbe82276cb356da1e5a66c45145c7daa1d8769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576862"
---
# <span data-ttu-id="82885-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="82885-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="82885-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82885-102">SYNOPSIS</span></span>
<span data-ttu-id="82885-103">Ändrar en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="82885-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82885-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82885-104">SYNTAX</span></span>

### <span data-ttu-id="82885-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="82885-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82885-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="82885-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82885-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82885-107">DESCRIPTION</span></span>
<span data-ttu-id="82885-108">Cmdleten **set-AzureRmApplicationGatewayFrontendIPConfig** uppdaterar en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="82885-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="82885-109">En Programgateway stöder två typer av front-IP-adresser:</span><span class="sxs-lookup"><span data-stu-id="82885-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="82885-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="82885-110">Public IP addresses</span></span>
- <span data-ttu-id="82885-111">Privata IP-adresser som konfigurationen använder intern belastnings utjämning (ILB) för en Programgateway får ha högst en offentlig IP-adress och en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="82885-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="82885-112">En offentlig IP-adress och en privat IP-adress bör läggas till separat som front-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="82885-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="82885-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82885-113">EXAMPLES</span></span>

### <span data-ttu-id="82885-114">Exempel 1: Ange en offentlig IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="82885-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="82885-115">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="82885-116">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82885-117">Det tredje kommandot uppdaterar front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="82885-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="82885-118">Exempel 2: Ange en statisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="82885-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="82885-119">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="82885-120">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="82885-121">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82885-122">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="82885-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="82885-123">Exempel 3: Ange en dynamisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="82885-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="82885-124">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="82885-125">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="82885-126">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="82885-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82885-127">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="82885-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="82885-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82885-128">PARAMETERS</span></span>

### <span data-ttu-id="82885-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82885-129">-ApplicationGateway</span></span>
<span data-ttu-id="82885-130">Anger ett objekt för Application Gateway där du kan ändra front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="82885-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="82885-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82885-131">-DefaultProfile</span></span>
<span data-ttu-id="82885-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82885-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82885-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="82885-133">-Name</span></span>
<span data-ttu-id="82885-134">Anger namnet på den frontend-IP-konfiguration som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="82885-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="82885-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="82885-135">-PrivateIPAddress</span></span>
<span data-ttu-id="82885-136">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="82885-136">Specifies the private IP address.</span></span>
<span data-ttu-id="82885-137">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="82885-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="82885-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="82885-138">-PublicIPAddress</span></span>
<span data-ttu-id="82885-139">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="82885-139">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="82885-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="82885-140">-PublicIPAddressId</span></span>
<span data-ttu-id="82885-141">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="82885-141">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="82885-142">-Undernät</span><span class="sxs-lookup"><span data-stu-id="82885-142">-Subnet</span></span>
<span data-ttu-id="82885-143">Anger det undernät som Application Gateway använder.</span><span class="sxs-lookup"><span data-stu-id="82885-143">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="82885-144">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="82885-144">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="82885-145">Om *PrivateIPAddress* -adressen anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="82885-145">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="82885-146">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="82885-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="82885-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="82885-147">-SubnetId</span></span>
<span data-ttu-id="82885-148">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="82885-148">Specifies the subnet ID.</span></span>
<span data-ttu-id="82885-149">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="82885-149">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="82885-150">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="82885-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="82885-151">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="82885-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="82885-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82885-152">CommonParameters</span></span>
<span data-ttu-id="82885-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82885-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82885-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82885-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82885-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82885-155">INPUTS</span></span>

### <span data-ttu-id="82885-156">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82885-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="82885-157">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82885-157">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="82885-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82885-158">OUTPUTS</span></span>

### <span data-ttu-id="82885-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82885-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82885-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82885-160">NOTES</span></span>

## <span data-ttu-id="82885-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82885-161">RELATED LINKS</span></span>

[<span data-ttu-id="82885-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="82885-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="82885-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="82885-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="82885-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="82885-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="82885-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="82885-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="82885-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="82885-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


