---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: b6a7854d3ddf3c3d444418e08717577a8a2ac172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756331"
---
# <span data-ttu-id="e2e25-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2e25-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="e2e25-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2e25-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e25-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e2e25-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2e25-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2e25-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2e25-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2e25-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e25-106">Cmdleten **New-AzureRmApplicationGateway** skapar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e2e25-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="e2e25-107">En Programgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="e2e25-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="e2e25-108">En resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e2e25-108">A resource group.</span></span>
- <span data-ttu-id="e2e25-109">Ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e2e25-109">A virtual network.</span></span>
- <span data-ttu-id="e2e25-110">Backend-serverpoolen med IP-adresser till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="e2e25-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="e2e25-111">Backend-inställningar för serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-111">Back-end server pool settings.</span></span> <span data-ttu-id="e2e25-112">Varje pool har inställningar som port, protokoll och cookie-baserad tillhörighet, som tillämpas på alla servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="e2e25-113">Front-IP-adresser, som är de IP-adresser som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="e2e25-114">En front-IP-adress kan vara en offentlig IP-adress eller en intern IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e2e25-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="e2e25-115">Front portar, vilka är de offentliga portar som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="e2e25-116">Trafik som träffar dessa portar omdirigeras till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="e2e25-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="e2e25-117">En regel för anslutningsbegäran som binder lyssnaren och backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="e2e25-118">Regeln definierar vilken backend-server som trafiken ska omdirigeras till när den träffar en viss lyssnare.</span><span class="sxs-lookup"><span data-stu-id="e2e25-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="e2e25-119">En lyssnare har frontend-port, front-end IP Address, Protocol (HTTP eller HTTPS) och SSL (Secure Sockets Layer), certifikat namn (om du konfigurerar SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="e2e25-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="e2e25-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2e25-120">EXAMPLES</span></span>

### <span data-ttu-id="e2e25-121">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="e2e25-121">Example 1: Create an application gateway</span></span>
```
PS C:\>$ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} PS C:\>$Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet PS C:\>$GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name $PublicIpName -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name $listenerName  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $ FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="e2e25-122">I följande exempel skapas en Programgateway genom att först skapa en resurs grupp och ett virtuellt nätverk:</span><span class="sxs-lookup"><span data-stu-id="e2e25-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="e2e25-123">Backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="e2e25-123">A back-end server pool</span></span>
- <span data-ttu-id="e2e25-124">Server poolinställningarna</span><span class="sxs-lookup"><span data-stu-id="e2e25-124">Back-end server pool settings</span></span>
- <span data-ttu-id="e2e25-125">Front portar</span><span class="sxs-lookup"><span data-stu-id="e2e25-125">Front-end ports</span></span>
- <span data-ttu-id="e2e25-126">Front-IP-adresser</span><span class="sxs-lookup"><span data-stu-id="e2e25-126">Front-end IP addresses</span></span>
- <span data-ttu-id="e2e25-127">En regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="e2e25-127">A request routing rule</span></span>

<span data-ttu-id="e2e25-128">De här fyra kommandona skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e2e25-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="e2e25-129">Det första kommandot skapar en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e2e25-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="e2e25-130">Det andra kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e2e25-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="e2e25-131">Det tredje kommandot verifierar nät konfiguration och det fjärde kommandot verifierar att det virtuella nätverket har skapats.</span><span class="sxs-lookup"><span data-stu-id="e2e25-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="e2e25-132">Med följande kommandon skapas programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="e2e25-133">Det första kommandot skapar en IP-konfiguration med namnet GatewayIp01 för under nätet som skapades.</span><span class="sxs-lookup"><span data-stu-id="e2e25-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="e2e25-134">Det andra kommandot skapar en backend-grupppool med namnet Pool01 med en lista över backend-IP-adresser och lagrar poolen i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="e2e25-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="e2e25-135">Det tredje kommandot skapar inställningarna för backend-serverpoolen och lagrar inställningarna i $PoolSetting variabeln.</span><span class="sxs-lookup"><span data-stu-id="e2e25-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="e2e25-136">Med kommandot tillbaka skapar du en front port på port 80, namnger den FrontEndPort01 och lagrar porten i $FrontEndPort variabel.</span><span class="sxs-lookup"><span data-stu-id="e2e25-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="e2e25-137">Det femte kommandot skapar en offentlig IP-adress genom att använda New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="e2e25-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="e2e25-138">Det sjätte kommandot skapar en front-IP-konfiguration med $PublicIp, namnger den FrontEndPortConfig01 och lagrar den i $FrontEndIpConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="e2e25-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="e2e25-139">Med det sjunde kommandot skapas en lyssnare med den tidigare skapade $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="e2e25-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="e2e25-140">Med kommandot åtto skapas en regel för lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e2e25-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="e2e25-141">Med det nionde kommandot anges SKU.</span><span class="sxs-lookup"><span data-stu-id="e2e25-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="e2e25-142">Det tionde kommandot skapar en gateway med de objekt som anges med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="e2e25-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="e2e25-143">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2e25-143">PARAMETERS</span></span>

### <span data-ttu-id="e2e25-144">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e2e25-144">-AuthenticationCertificates</span></span>
<span data-ttu-id="e2e25-145">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-145">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-146">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="e2e25-146">-BackendAddressPools</span></span>
<span data-ttu-id="e2e25-147">Anger listan över backend-adresspooler för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-147">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-148">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="e2e25-148">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="e2e25-149">Anger listan över backend-HTTP-inställningar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-149">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-150">-Force</span><span class="sxs-lookup"><span data-stu-id="e2e25-150">-Force</span></span>
<span data-ttu-id="e2e25-151">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e2e25-151">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-152">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="e2e25-152">-FrontendIPConfigurations</span></span>
<span data-ttu-id="e2e25-153">Anger en lista med IP-konfigurationer för front-end för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-153">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-154">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="e2e25-154">-FrontendPorts</span></span>
<span data-ttu-id="e2e25-155">Anger en lista över front portar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-155">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-156">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="e2e25-156">-GatewayIPConfigurations</span></span>
<span data-ttu-id="e2e25-157">Anger en lista med IP-konfigurationer för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-157">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-158">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="e2e25-158">-HttpListeners</span></span>
<span data-ttu-id="e2e25-159">Anger en lista med HTTP-lyssnare för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-159">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-160">-Plats</span><span class="sxs-lookup"><span data-stu-id="e2e25-160">-Location</span></span>
<span data-ttu-id="e2e25-161">Anger i vilken region du vill skapa programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-161">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-162">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2e25-162">-Name</span></span>
<span data-ttu-id="e2e25-163">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-163">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-164">-Avsöks</span><span class="sxs-lookup"><span data-stu-id="e2e25-164">-Probes</span></span>
<span data-ttu-id="e2e25-165">Anger Avsök för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-165">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-166">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="e2e25-166">-RedirectConfigurations</span></span>
<span data-ttu-id="e2e25-167">Listan med konfiguration av omdirigering</span><span class="sxs-lookup"><span data-stu-id="e2e25-167">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-168">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="e2e25-168">-RequestRoutingRules</span></span>
<span data-ttu-id="e2e25-169">Anger en lista över routningsregler för anslutningsbegäran för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-169">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e25-170">-ResourceGroupName</span></span>
<span data-ttu-id="e2e25-171">Anger namnet på den resurs grupp där Application Gateway ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e2e25-171">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-172">-SKU</span><span class="sxs-lookup"><span data-stu-id="e2e25-172">-Sku</span></span>
<span data-ttu-id="e2e25-173">Anger SKU (lager behållning) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-173">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-174">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="e2e25-174">-SslCertificates</span></span>
<span data-ttu-id="e2e25-175">Anger listan över SSL-certifikat (Secure Sockets Layer) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-175">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-176">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="e2e25-176">-SslPolicy</span></span>
<span data-ttu-id="e2e25-177">Anger en SSL-princip för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-177">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-178">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e2e25-178">-Tag</span></span>
<span data-ttu-id="e2e25-179">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e2e25-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e2e25-180">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e2e25-180">For example:</span></span>

<span data-ttu-id="e2e25-181">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e2e25-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-182">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="e2e25-182">-UrlPathMaps</span></span>
<span data-ttu-id="e2e25-183">Anger URL-sökvägar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2e25-183">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-184">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2e25-184">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="e2e25-185">Anger en konfiguration för webb programs brand väggen (WAF).</span><span class="sxs-lookup"><span data-stu-id="e2e25-185">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="e2e25-186">Du kan använda Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet för att få en WAF.</span><span class="sxs-lookup"><span data-stu-id="e2e25-186">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2e25-187">-Confirm</span></span>
<span data-ttu-id="e2e25-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2e25-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e25-189">-WhatIf</span></span>
<span data-ttu-id="e2e25-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2e25-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e25-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2e25-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e25-192">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e25-192">-DefaultProfile</span></span>
<span data-ttu-id="e2e25-193">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e25-193">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e25-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e25-194">CommonParameters</span></span>
<span data-ttu-id="e2e25-195">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e25-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e25-196">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e25-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e25-197">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2e25-197">INPUTS</span></span>

## <span data-ttu-id="e2e25-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2e25-198">OUTPUTS</span></span>

### <span data-ttu-id="e2e25-199">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2e25-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2e25-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2e25-200">NOTES</span></span>

## <span data-ttu-id="e2e25-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2e25-201">RELATED LINKS</span></span>

[<span data-ttu-id="e2e25-202">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2e25-202">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2e25-203">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e2e25-203">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="e2e25-204">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e2e25-204">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e2e25-205">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e2e25-205">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e2e25-206">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e2e25-206">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="e2e25-207">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2e25-207">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e2e25-208">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2e25-208">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e2e25-209">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e2e25-209">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="e2e25-210">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e2e25-210">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e2e25-211">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e2e25-211">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
