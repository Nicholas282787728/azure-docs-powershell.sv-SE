---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422403"
---
# <span data-ttu-id="dfefb-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dfefb-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="dfefb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfefb-102">SYNOPSIS</span></span>
<span data-ttu-id="dfefb-103">Lägger till en klient-IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="dfefb-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="dfefb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfefb-104">SYNTAX</span></span>

### <span data-ttu-id="dfefb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfefb-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfefb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dfefb-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfefb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfefb-107">DESCRIPTION</span></span>
<span data-ttu-id="dfefb-108">Cmdleten **Add-AzApplicationGatewayFrontendIPConfig** lägger till en klient-IP-konfiguration i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="dfefb-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="dfefb-109">En Programgateway stöder två typer av front-IP-konfigurationer:</span><span class="sxs-lookup"><span data-stu-id="dfefb-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="dfefb-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="dfefb-110">Public IP addresses</span></span>
- <span data-ttu-id="dfefb-111">Privata IP-adresser med intern belastnings utjämning (ILB) en Programgateway får ha högst en offentlig IP och en privat IP.</span><span class="sxs-lookup"><span data-stu-id="dfefb-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="dfefb-112">Lägg till en offentlig IP-adress och en privat IP-adress som separata frontend-adresser.</span><span class="sxs-lookup"><span data-stu-id="dfefb-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="dfefb-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfefb-113">EXAMPLES</span></span>

### <span data-ttu-id="dfefb-114">Exempel 1: lägga till en offentlig IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="dfefb-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="dfefb-115">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="dfefb-116">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dfefb-117">Det tredje kommandot lägger till front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="dfefb-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="dfefb-118">Exempel 2: lägga till en statisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="dfefb-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="dfefb-119">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="dfefb-120">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="dfefb-121">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dfefb-122">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="dfefb-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="dfefb-123">Exempel 3: lägga till en dynamisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="dfefb-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="dfefb-124">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="dfefb-125">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="dfefb-126">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="dfefb-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dfefb-127">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="dfefb-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="dfefb-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfefb-128">PARAMETERS</span></span>

### <span data-ttu-id="dfefb-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfefb-129">-ApplicationGateway</span></span>
<span data-ttu-id="dfefb-130">Anger den Programgateway som denna cmdlet lägger till en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="dfefb-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="dfefb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfefb-131">-DefaultProfile</span></span>
<span data-ttu-id="dfefb-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfefb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfefb-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfefb-133">-Name</span></span>
<span data-ttu-id="dfefb-134">Anger namnet på den frontend-IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="dfefb-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="dfefb-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="dfefb-135">-PrivateIPAddress</span></span>
<span data-ttu-id="dfefb-136">Anger den privata IP-adressen som ska läggas till som front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dfefb-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="dfefb-137">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="dfefb-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="dfefb-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfefb-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="dfefb-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfefb-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="dfefb-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dfefb-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="dfefb-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dfefb-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="dfefb-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="dfefb-142">-PublicIPAddress</span></span>
<span data-ttu-id="dfefb-143">Anger den offentliga IP-adressen som denna cmdlet lägger till som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dfefb-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="dfefb-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="dfefb-144">-PublicIPAddressId</span></span>
<span data-ttu-id="dfefb-145">Anger ID för den offentliga IP-adressen som denna cmdlet lägger till som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dfefb-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="dfefb-146">-Undernät</span><span class="sxs-lookup"><span data-stu-id="dfefb-146">-Subnet</span></span>
<span data-ttu-id="dfefb-147">Anger det undernät som denna cmdlet lägger till som front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dfefb-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="dfefb-148">Om du anger den här parametern innebär det att programgatewayen stöder en privat IP-baserad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dfefb-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="dfefb-149">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="dfefb-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="dfefb-150">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dfefb-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="dfefb-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dfefb-151">-SubnetId</span></span>
<span data-ttu-id="dfefb-152">Anger det ID-nummer som denna cmdlet lägger till som front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dfefb-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="dfefb-153">Att skicka under nätverk innebär privat IP.</span><span class="sxs-lookup"><span data-stu-id="dfefb-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="dfefb-154">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="dfefb-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="dfefb-155">Annars hämtas en IP-adress från detta undernät dynamiskt som front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dfefb-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="dfefb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfefb-156">CommonParameters</span></span>
<span data-ttu-id="dfefb-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfefb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfefb-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfefb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfefb-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfefb-159">INPUTS</span></span>

### <span data-ttu-id="dfefb-160">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfefb-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dfefb-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfefb-161">OUTPUTS</span></span>

### <span data-ttu-id="dfefb-162">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfefb-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dfefb-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfefb-163">NOTES</span></span>

## <span data-ttu-id="dfefb-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfefb-164">RELATED LINKS</span></span>

[<span data-ttu-id="dfefb-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dfefb-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="dfefb-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dfefb-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="dfefb-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dfefb-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="dfefb-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="dfefb-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


