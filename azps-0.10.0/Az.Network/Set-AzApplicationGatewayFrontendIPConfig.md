---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e85976f77ece9af89ecd532ff0a3236039abb9fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924273"
---
# <span data-ttu-id="bdefc-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdefc-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="bdefc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdefc-102">SYNOPSIS</span></span>
<span data-ttu-id="bdefc-103">Ändrar en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="bdefc-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="bdefc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdefc-104">SYNTAX</span></span>

### <span data-ttu-id="bdefc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bdefc-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdefc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bdefc-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdefc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdefc-107">DESCRIPTION</span></span>
<span data-ttu-id="bdefc-108">Cmdleten **set-AzApplicationGatewayFrontendIPConfig** uppdaterar en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bdefc-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="bdefc-109">En Programgateway stöder två typer av front-IP-adresser:</span><span class="sxs-lookup"><span data-stu-id="bdefc-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="bdefc-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="bdefc-110">Public IP addresses</span></span>
- <span data-ttu-id="bdefc-111">Privata IP-adresser för vilka konfigurationen använder intern belastnings utjämning (ILB)</span><span class="sxs-lookup"><span data-stu-id="bdefc-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="bdefc-112">En Programgateway får högst ha en offentlig IP-adress och en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="bdefc-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="bdefc-113">En offentlig IP-adress och en privat IP-adress bör läggas till separat som front-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="bdefc-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="bdefc-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdefc-114">EXAMPLES</span></span>

### <span data-ttu-id="bdefc-115">Exempel 1: Ange en offentlig IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="bdefc-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="bdefc-116">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="bdefc-117">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bdefc-118">Det tredje kommandot uppdaterar front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="bdefc-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="bdefc-119">Exempel 2: Ange en statisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="bdefc-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="bdefc-120">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="bdefc-121">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="bdefc-122">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bdefc-123">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="bdefc-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="bdefc-124">Exempel 3: Ange en dynamisk privat IP som front-IP för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="bdefc-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="bdefc-125">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="bdefc-126">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="bdefc-127">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="bdefc-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bdefc-128">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="bdefc-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="bdefc-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdefc-129">PARAMETERS</span></span>

### <span data-ttu-id="bdefc-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdefc-130">-ApplicationGateway</span></span>
<span data-ttu-id="bdefc-131">Anger ett objekt för Application Gateway där du kan ändra front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bdefc-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="bdefc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdefc-132">-DefaultProfile</span></span>
<span data-ttu-id="bdefc-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdefc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdefc-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="bdefc-134">-Name</span></span>
<span data-ttu-id="bdefc-135">Anger namnet på den frontend-IP-konfiguration som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="bdefc-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bdefc-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="bdefc-136">-PrivateIPAddress</span></span>
<span data-ttu-id="bdefc-137">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="bdefc-137">Specifies the private IP address.</span></span>
<span data-ttu-id="bdefc-138">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="bdefc-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="bdefc-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="bdefc-139">-PublicIPAddress</span></span>
<span data-ttu-id="bdefc-140">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="bdefc-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="bdefc-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="bdefc-141">-PublicIPAddressId</span></span>
<span data-ttu-id="bdefc-142">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="bdefc-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="bdefc-143">-Undernät</span><span class="sxs-lookup"><span data-stu-id="bdefc-143">-Subnet</span></span>
<span data-ttu-id="bdefc-144">Anger det undernät som Application Gateway använder.</span><span class="sxs-lookup"><span data-stu-id="bdefc-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="bdefc-145">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="bdefc-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="bdefc-146">Om *PrivateIPAddress* -adressen anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="bdefc-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="bdefc-147">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="bdefc-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="bdefc-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bdefc-148">-SubnetId</span></span>
<span data-ttu-id="bdefc-149">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="bdefc-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="bdefc-150">Ange den här parametern om gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="bdefc-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="bdefc-151">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="bdefc-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="bdefc-152">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="bdefc-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="bdefc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdefc-153">CommonParameters</span></span>
<span data-ttu-id="bdefc-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdefc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdefc-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdefc-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdefc-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdefc-156">INPUTS</span></span>

### <span data-ttu-id="bdefc-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bdefc-157">System.String</span></span>

## <span data-ttu-id="bdefc-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdefc-158">OUTPUTS</span></span>

### <span data-ttu-id="bdefc-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdefc-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bdefc-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdefc-160">NOTES</span></span>

## <span data-ttu-id="bdefc-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdefc-161">RELATED LINKS</span></span>

[<span data-ttu-id="bdefc-162">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdefc-162">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bdefc-163">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdefc-163">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bdefc-164">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdefc-164">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bdefc-165">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdefc-165">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bdefc-166">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdefc-166">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


