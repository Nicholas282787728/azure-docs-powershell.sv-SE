---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 212af54a6b3484b81e0914bd82e8ff68553f30ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584651"
---
# <span data-ttu-id="09f38-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="09f38-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="09f38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09f38-102">SYNOPSIS</span></span>
<span data-ttu-id="09f38-103">Lägger till en klient-IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="09f38-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09f38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09f38-104">SYNTAX</span></span>

### <span data-ttu-id="09f38-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="09f38-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f38-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="09f38-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f38-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09f38-107">DESCRIPTION</span></span>
<span data-ttu-id="09f38-108">Cmdleten **Add-AzureRmApplicationGatewayFrontendIPConfig** lägger till en klient-IP-konfiguration i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="09f38-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="09f38-109">En Programgateway stöder två typer av front-IP-konfigurationer:</span><span class="sxs-lookup"><span data-stu-id="09f38-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="09f38-110">Offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="09f38-110">Public IP addresses</span></span>
- <span data-ttu-id="09f38-111">Privata IP-adresser med intern belastnings utjämning (ILB)</span><span class="sxs-lookup"><span data-stu-id="09f38-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="09f38-112">En Programgateway får ha högst en offentlig IP och en privat IP.</span><span class="sxs-lookup"><span data-stu-id="09f38-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="09f38-113">Lägg till en offentlig IP-adress och en privat IP-adress som separata frontend-adresser.</span><span class="sxs-lookup"><span data-stu-id="09f38-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="09f38-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09f38-114">EXAMPLES</span></span>

### <span data-ttu-id="09f38-115">Exempel 1: lägga till en offentlig IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="09f38-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="09f38-116">Det första kommandot skapar ett offentligt IP-adressprefix och lagrar det i $PublicIp variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="09f38-117">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="09f38-118">Det tredje kommandot lägger till front-IP-konfigurationen som heter FrontEndIp01, för gatewayen i $AppGw, med den adress som är lagrad i $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="09f38-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="09f38-119">Exempel 2: lägga till en statisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="09f38-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="09f38-120">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="09f38-121">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="09f38-122">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="09f38-123">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="09f38-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="09f38-124">Exempel 3: lägga till en dynamisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="09f38-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="09f38-125">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="09f38-126">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="09f38-127">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="09f38-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="09f38-128">Det fjärde kommandot lägger till en front-IP-konfiguration med namnet FrontendIP02 med hjälp av $Subnet från det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="09f38-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="09f38-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09f38-129">PARAMETERS</span></span>

### <span data-ttu-id="09f38-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09f38-130">-ApplicationGateway</span></span>
<span data-ttu-id="09f38-131">Anger den Programgateway som denna cmdlet lägger till en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="09f38-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="09f38-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="09f38-132">-Name</span></span>
<span data-ttu-id="09f38-133">Anger namnet på den frontend-IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="09f38-133">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="09f38-134">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="09f38-134">-PrivateIPAddress</span></span>
<span data-ttu-id="09f38-135">Anger den privata IP-adressen som ska läggas till som front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="09f38-135">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="09f38-136">Om det här alternativet anges tilldelas denna IP statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="09f38-136">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="09f38-137">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="09f38-137">-PublicIPAddress</span></span>
<span data-ttu-id="09f38-138">Anger den offentliga IP-adressen som denna cmdlet lägger till som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="09f38-138">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="09f38-139">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="09f38-139">-PublicIPAddressId</span></span>
<span data-ttu-id="09f38-140">Anger ID för den offentliga IP-adressen som denna cmdlet lägger till som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="09f38-140">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="09f38-141">-Undernät</span><span class="sxs-lookup"><span data-stu-id="09f38-141">-Subnet</span></span>
<span data-ttu-id="09f38-142">Anger det undernät som denna cmdlet lägger till som front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09f38-142">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="09f38-143">Om du anger den här parametern innebär det att programgatewayen stöder en privat IP-baserad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09f38-143">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="09f38-144">Om parametern *PrivateIPAddress* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="09f38-144">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="09f38-145">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="09f38-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="09f38-146">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="09f38-146">-SubnetId</span></span>
<span data-ttu-id="09f38-147">Anger det ID-nummer som denna cmdlet lägger till som front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09f38-147">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="09f38-148">Att skicka under nätverk innebär privat IP.</span><span class="sxs-lookup"><span data-stu-id="09f38-148">Passing subnet implies private IP.</span></span>
<span data-ttu-id="09f38-149">Om parametern *PrivateIPAddresss* anges ska den tillhöra detta undernät.</span><span class="sxs-lookup"><span data-stu-id="09f38-149">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="09f38-150">Annars hämtas en IP-adress från detta undernät dynamiskt som front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="09f38-150">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="09f38-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f38-151">-DefaultProfile</span></span>
<span data-ttu-id="09f38-152">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09f38-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f38-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f38-153">CommonParameters</span></span>
<span data-ttu-id="09f38-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f38-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f38-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f38-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f38-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09f38-156">INPUTS</span></span>

### <span data-ttu-id="09f38-157">System. String</span><span class="sxs-lookup"><span data-stu-id="09f38-157">System.String</span></span>

## <span data-ttu-id="09f38-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09f38-158">OUTPUTS</span></span>

### <span data-ttu-id="09f38-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09f38-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09f38-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09f38-160">NOTES</span></span>

## <span data-ttu-id="09f38-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09f38-161">RELATED LINKS</span></span>

[<span data-ttu-id="09f38-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="09f38-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="09f38-163">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="09f38-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="09f38-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="09f38-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="09f38-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="09f38-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

