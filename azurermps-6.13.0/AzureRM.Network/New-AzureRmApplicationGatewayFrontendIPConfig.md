---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 6f2e9ea87b478c4992bdad6c2c20029bec90ac13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756393"
---
# <span data-ttu-id="ed266-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed266-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ed266-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed266-102">SYNOPSIS</span></span>
<span data-ttu-id="ed266-103">Skapar en front-IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ed266-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed266-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed266-104">SYNTAX</span></span>

### <span data-ttu-id="ed266-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed266-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed266-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ed266-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed266-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed266-107">DESCRIPTION</span></span>
<span data-ttu-id="ed266-108">Cmdleten **New-AzureRmApplicationGatewayFrontendIPConfig** skapar en front-IP-Configuraton för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ed266-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="ed266-109">En Programgateway stöder två typer av front-IP-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="ed266-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="ed266-110">Offentliga IP-adresser--privata IP-adresser med intern belastnings utjämning (ILB).</span><span class="sxs-lookup"><span data-stu-id="ed266-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="ed266-111">En Programgateway får högst ha en offentlig IP-adress och en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ed266-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="ed266-112">Den offentliga IP-adressen och den privata IP-adressen bör läggas till separat som front-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="ed266-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="ed266-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed266-113">EXAMPLES</span></span>

### <span data-ttu-id="ed266-114">Exempel 1: skapa en front-IP-konfiguration med ett offentligt IP-adressresurs</span><span class="sxs-lookup"><span data-stu-id="ed266-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="ed266-115">Det första kommandot skapar ett offentligt IP-adressresurs och lagrar det i $PublicIP variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="ed266-116">Det andra kommandot använder $PublicIP för att skapa en ny front-IP-konfiguration med namnet FrontEndIP01 och lagrar den i $FrontEnd-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="ed266-117">Exempel 2: skapa en statisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="ed266-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="ed266-118">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ed266-119">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ed266-120">Det tredje kommandot skapar en front-IP-konfiguration med namnet FrontEndIP02 via $Subnet från det andra kommandot och den privata IP-10.0.1.1 och lagrar sedan in den i $FrontEnd variabel.</span><span class="sxs-lookup"><span data-stu-id="ed266-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="ed266-121">Exempel 3: skapa en dynamisk privat IP som front-IP-adress</span><span class="sxs-lookup"><span data-stu-id="ed266-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="ed266-122">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ed266-123">Det andra kommandot får en under nätverks konfiguration med namnet Subnet01 med $VNet från det första kommandot och lagrar det i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ed266-124">Det tredje kommandot skapar en front-IP-konfiguration med namnet FrontEndIP03 med $Subnet från det andra kommandot och lagrar den i $FrontEnd-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed266-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="ed266-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed266-125">PARAMETERS</span></span>

### <span data-ttu-id="ed266-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed266-126">-DefaultProfile</span></span>
<span data-ttu-id="ed266-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed266-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed266-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed266-128">-Name</span></span>
<span data-ttu-id="ed266-129">Anger namnet på den frontend-IP-konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ed266-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ed266-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="ed266-130">-PrivateIPAddress</span></span>
<span data-ttu-id="ed266-131">Anger den privata IP-adressen som denna cmdlet associerar med front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="ed266-132">Det här kan bara anges om ett undernät har angetts.</span><span class="sxs-lookup"><span data-stu-id="ed266-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="ed266-133">Denna IP har tilldelats statiskt från under nätet.</span><span class="sxs-lookup"><span data-stu-id="ed266-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="ed266-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ed266-134">-PublicIPAddress</span></span>
<span data-ttu-id="ed266-135">Anger det offentliga IP-adressen som denna cmdlet associerar med front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ed266-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ed266-136">-PublicIPAddressId</span></span>
<span data-ttu-id="ed266-137">Anger det offentliga IP-adress-ID som denna cmdlet associerar med front-IP för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="ed266-138">-Undernät</span><span class="sxs-lookup"><span data-stu-id="ed266-138">-Subnet</span></span>
<span data-ttu-id="ed266-139">Anger det Subnet-objekt som denna cmdlet associerar med front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="ed266-140">Om du anger den här parametern innebär det att gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ed266-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="ed266-141">Om parametern *PrivateIPAddresss* anges ska den tillhöra det undernät som anges med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="ed266-141">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="ed266-142">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ed266-143">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ed266-143">-SubnetId</span></span>
<span data-ttu-id="ed266-144">Anger det Subnet-ID som denna cmdlet associerar med front-IP-konfigurationen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="ed266-145">Om du anger en *under näts* parameter innebär det att gatewayen använder en privat IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ed266-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="ed266-146">Om parametern *PrivateIPAddress* anges ska den tillhöra det undernät som anges av *Subnet*.</span><span class="sxs-lookup"><span data-stu-id="ed266-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="ed266-147">Om *PrivateIPAddress* inte anges hämtas en av IP-adresserna från detta undernät dynamiskt som front-IP-adress för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed266-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ed266-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed266-148">CommonParameters</span></span>
<span data-ttu-id="ed266-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed266-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed266-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed266-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed266-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed266-151">INPUTS</span></span>

### <span data-ttu-id="ed266-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="ed266-152">None</span></span>

## <span data-ttu-id="ed266-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed266-153">OUTPUTS</span></span>

### <span data-ttu-id="ed266-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed266-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="ed266-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed266-155">NOTES</span></span>

## <span data-ttu-id="ed266-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed266-156">RELATED LINKS</span></span>

[<span data-ttu-id="ed266-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed266-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ed266-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed266-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ed266-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed266-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ed266-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed266-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

