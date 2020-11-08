---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c36c185ac2fecf1e4584c1bb1b2025ce3b431cf4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092527"
---
# <span data-ttu-id="0b39e-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0b39e-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0b39e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b39e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b39e-103">Skapar en front-IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0b39e-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="0b39e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b39e-104">SYNTAX</span></span>

### <span data-ttu-id="0b39e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b39e-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b39e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0b39e-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b39e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b39e-107">DESCRIPTION</span></span>
<span data-ttu-id="0b39e-108">Cmdleten **New-AzApplicationGatewayFrontendIPConfig** skapar en front-IP-konfiguration för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b39e-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="0b39e-109">En Programgateway stöder två typer av front-IP-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="0b39e-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="0b39e-110">Offentliga IP-adresser--privata IP-adresser med intern belastnings utjämning (ILB).</span><span class="sxs-lookup"><span data-stu-id="0b39e-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="0b39e-111">En Programgateway får högst ha en offentlig IP-adress och en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0b39e-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="0b39e-112">Den offentliga IP-adressen och den privata IP-adressen bör läggas till separat som front-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="0b39e-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="0b39e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b39e-113">EXAMPLES</span></span>

### <span data-ttu-id="0b39e-114">Exempel 1: skapa en front-IP-konfiguration med ett offentligt IP-adressresurs</span><span class="sxs-lookup"><span data-stu-id="0b39e-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="0b39e-115">Det första kommandot skapar ett offentligt IP-adressresurs och lagrar det i $PublicIP variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="0b39e-116">Det andra kommandot använder $PublicIP för att skapa en ny front-IP-konfiguration med namnet FrontEndIP01 och lagrar den i $FrontEnd-variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="0b39e-117">Exempel 2: skapa en statisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="0b39e-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="0b39e-118">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="0b39e-119">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="0b39e-120">Det tredje kommandot skapar en front-IP-konfiguration med namnet FrontEndIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1 och lagrar sedan in den i $FrontEnd variabel.</span><span class="sxs-lookup"><span data-stu-id="0b39e-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="0b39e-121">Exempel 3: skapa en dynamisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="0b39e-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="0b39e-122">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="0b39e-123">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="0b39e-124">Det tredje kommandot skapar en front-IP-konfiguration med namnet FrontEndIP03 med $Subnet från det andra kommandot och lagrar den i $FrontEnd-variabeln.</span><span class="sxs-lookup"><span data-stu-id="0b39e-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="0b39e-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b39e-125">PARAMETERS</span></span>

### <span data-ttu-id="0b39e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b39e-126">-DefaultProfile</span></span>
<span data-ttu-id="0b39e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b39e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b39e-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b39e-128">-Name</span></span>
<span data-ttu-id="0b39e-129">Anger namnet på den frontend-IP-konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="0b39e-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0b39e-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="0b39e-130">-PrivateIPAddress</span></span>
<span data-ttu-id="0b39e-131">Anger den privata IP-adressen som denna cmdlet associerar med front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="0b39e-132">Det här kan bara anges om ett undernät har angetts.</span><span class="sxs-lookup"><span data-stu-id="0b39e-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="0b39e-133">Denna IP har tilldelats statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="0b39e-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="0b39e-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="0b39e-134">-PublicIPAddress</span></span>
<span data-ttu-id="0b39e-135">Anger det offentliga IP-adressen som denna cmdlet associerar med front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="0b39e-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="0b39e-136">-PublicIPAddressId</span></span>
<span data-ttu-id="0b39e-137">Anger det offentliga IP-adress-ID som denna cmdlet associerar med front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="0b39e-138">-Undernät</span><span class="sxs-lookup"><span data-stu-id="0b39e-138">-Subnet</span></span>
<span data-ttu-id="0b39e-139">Anger det Subnet-objekt som denna cmdlet associerar med front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="0b39e-140">Om du anger den här parametern innebär det att gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0b39e-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="0b39e-141">Om parametern *PrivateIPAddress* anges ska den tillhöra det undernät som anges med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0b39e-141">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="0b39e-142">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="0b39e-143">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0b39e-143">-SubnetId</span></span>
<span data-ttu-id="0b39e-144">Anger det Subnet-ID som denna cmdlet associerar med front-IP-konfigurationen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="0b39e-145">Om du anger en *under näts* parameter innebär det att gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0b39e-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="0b39e-146">Om parametern *PrivateIPAddress* anges ska den tillhöra det undernät som anges av *Subnet*.</span><span class="sxs-lookup"><span data-stu-id="0b39e-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="0b39e-147">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0b39e-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="0b39e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b39e-148">CommonParameters</span></span>
<span data-ttu-id="0b39e-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b39e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b39e-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b39e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b39e-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b39e-151">INPUTS</span></span>

### <span data-ttu-id="0b39e-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="0b39e-152">None</span></span>

## <span data-ttu-id="0b39e-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b39e-153">OUTPUTS</span></span>

### <span data-ttu-id="0b39e-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b39e-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="0b39e-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b39e-155">NOTES</span></span>

## <span data-ttu-id="0b39e-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b39e-156">RELATED LINKS</span></span>

[<span data-ttu-id="0b39e-157">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0b39e-157">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0b39e-158">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0b39e-158">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0b39e-159">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0b39e-159">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0b39e-160">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0b39e-160">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


