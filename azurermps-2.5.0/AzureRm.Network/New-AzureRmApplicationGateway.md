---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 73b72c6585fb4c7487b43dc99b3494cdc99bf7a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929746"
---
# <span data-ttu-id="80a86-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80a86-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="80a86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80a86-102">SYNOPSIS</span></span>
<span data-ttu-id="80a86-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="80a86-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80a86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80a86-104">SYNTAX</span></span>

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
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80a86-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80a86-105">DESCRIPTION</span></span>
<span data-ttu-id="80a86-106">Cmdleten **New-AzureRmApplicationGateway** skapar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="80a86-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="80a86-107">En Programgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="80a86-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="80a86-108">En resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="80a86-108">A resource group.</span></span>
- <span data-ttu-id="80a86-109">Ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="80a86-109">A virtual network.</span></span>
- <span data-ttu-id="80a86-110">Backend-serverpoolen med IP-adresser till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="80a86-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="80a86-111">Backend-inställningar för serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="80a86-111">Back-end server pool settings.</span></span> <span data-ttu-id="80a86-112">Varje pool har inställningar som port, protokoll och cookie-baserad tillhörighet, som tillämpas på alla servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="80a86-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="80a86-113">Front-IP-adresser, som är de IP-adresser som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="80a86-114">En front-IP-adress kan vara en offentlig IP-adress eller en intern IP-adress.</span><span class="sxs-lookup"><span data-stu-id="80a86-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="80a86-115">Front portar, vilka är de offentliga portar som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="80a86-116">Trafik som träffar dessa portar omdirigeras till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="80a86-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="80a86-117">En regel för anslutningsbegäran som binder lyssnaren och backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="80a86-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="80a86-118">Regeln definierar vilken backend-server som trafiken ska omdirigeras till när den träffar en viss lyssnare.</span><span class="sxs-lookup"><span data-stu-id="80a86-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="80a86-119">En lyssnare har frontend-port, front-end IP Address, Protocol (HTTP eller HTTPS) och SSL (Secure Sockets Layer), certifikat namn (om du konfigurerar SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="80a86-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="80a86-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80a86-120">EXAMPLES</span></span>

### <span data-ttu-id="80a86-121">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="80a86-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="80a86-122">I följande exempel skapas en Programgateway genom att först skapa en resurs grupp och ett virtuellt nätverk:</span><span class="sxs-lookup"><span data-stu-id="80a86-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="80a86-123">Backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="80a86-123">A back-end server pool</span></span>
- <span data-ttu-id="80a86-124">Server poolinställningarna</span><span class="sxs-lookup"><span data-stu-id="80a86-124">Back-end server pool settings</span></span>
- <span data-ttu-id="80a86-125">Front portar</span><span class="sxs-lookup"><span data-stu-id="80a86-125">Front-end ports</span></span>
- <span data-ttu-id="80a86-126">Front-IP-adresser</span><span class="sxs-lookup"><span data-stu-id="80a86-126">Front-end IP addresses</span></span>
- <span data-ttu-id="80a86-127">En regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="80a86-127">A request routing rule</span></span>

<span data-ttu-id="80a86-128">De här fyra kommandona skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="80a86-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="80a86-129">Det första kommandot skapar en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="80a86-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="80a86-130">Det andra kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="80a86-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="80a86-131">Det tredje kommandot verifierar nät konfiguration och det fjärde kommandot verifierar att det virtuella nätverket har skapats.</span><span class="sxs-lookup"><span data-stu-id="80a86-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="80a86-132">Med följande kommandon skapas programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="80a86-133">Det första kommandot skapar en IP-konfiguration med namnet GatewayIp01 för under nätet som skapades.</span><span class="sxs-lookup"><span data-stu-id="80a86-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="80a86-134">Det andra kommandot skapar en backend-grupppool med namnet Pool01 med en lista över backend-IP-adresser och lagrar poolen i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="80a86-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="80a86-135">Det tredje kommandot skapar inställningarna för backend-serverpoolen och lagrar inställningarna i $PoolSetting variabeln.</span><span class="sxs-lookup"><span data-stu-id="80a86-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="80a86-136">Med kommandot tillbaka skapar du en front port på port 80, namnger den FrontEndPort01 och lagrar porten i $FrontEndPort variabel.</span><span class="sxs-lookup"><span data-stu-id="80a86-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="80a86-137">Det femte kommandot skapar en offentlig IP-adress genom att använda New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="80a86-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="80a86-138">Det sjätte kommandot skapar en front-IP-konfiguration med $PublicIp, namnger den FrontEndPortConfig01 och lagrar den i $FrontEndIpConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="80a86-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="80a86-139">Med det sjunde kommandot skapas en lyssnare med den tidigare skapade $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="80a86-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="80a86-140">Med kommandot åtto skapas en regel för lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="80a86-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="80a86-141">Med det nionde kommandot anges SKU.</span><span class="sxs-lookup"><span data-stu-id="80a86-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="80a86-142">Det tionde kommandot skapar en gateway med de objekt som anges med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="80a86-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="80a86-143">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80a86-143">PARAMETERS</span></span>

### <span data-ttu-id="80a86-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80a86-144">-AsJob</span></span>
<span data-ttu-id="80a86-145">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="80a86-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="80a86-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="80a86-147">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="80a86-148">-BackendAddressPools</span></span>
<span data-ttu-id="80a86-149">Anger listan över backend-adresspooler för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="80a86-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="80a86-151">Anger listan över backend-HTTP-inställningar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a86-152">-DefaultProfile</span></span>
<span data-ttu-id="80a86-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80a86-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a86-154">-Force</span><span class="sxs-lookup"><span data-stu-id="80a86-154">-Force</span></span>
<span data-ttu-id="80a86-155">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="80a86-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="80a86-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="80a86-157">Anger en lista med IP-konfigurationer för front-end för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="80a86-158">-FrontendPorts</span></span>
<span data-ttu-id="80a86-159">Anger en lista över front portar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-159">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="80a86-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="80a86-161">Anger en lista med IP-konfigurationer för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-161">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="80a86-162">-HttpListeners</span></span>
<span data-ttu-id="80a86-163">Anger en lista med HTTP-lyssnare för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-164">-Plats</span><span class="sxs-lookup"><span data-stu-id="80a86-164">-Location</span></span>
<span data-ttu-id="80a86-165">Anger i vilken region du vill skapa programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-165">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-166">-Namn</span><span class="sxs-lookup"><span data-stu-id="80a86-166">-Name</span></span>
<span data-ttu-id="80a86-167">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-167">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-168">-Avsöks</span><span class="sxs-lookup"><span data-stu-id="80a86-168">-Probes</span></span>
<span data-ttu-id="80a86-169">Anger Avsök för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-169">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="80a86-170">-RedirectConfigurations</span></span>
<span data-ttu-id="80a86-171">Listan med konfiguration av omdirigering</span><span class="sxs-lookup"><span data-stu-id="80a86-171">The list of redirect configuration</span></span>

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

### <span data-ttu-id="80a86-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="80a86-172">-RequestRoutingRules</span></span>
<span data-ttu-id="80a86-173">Anger en lista över routningsregler för anslutningsbegäran för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-173">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a86-174">-ResourceGroupName</span></span>
<span data-ttu-id="80a86-175">Anger namnet på den resurs grupp där Application Gateway ska skapas.</span><span class="sxs-lookup"><span data-stu-id="80a86-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="80a86-176">-Sku</span></span>
<span data-ttu-id="80a86-177">Anger SKU (lager behållning) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="80a86-178">-SslCertificates</span></span>
<span data-ttu-id="80a86-179">Anger listan över SSL-certifikat (Secure Sockets Layer) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="80a86-180">-SslPolicy</span></span>
<span data-ttu-id="80a86-181">Anger en SSL-princip för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-181">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-182">-Tagg</span><span class="sxs-lookup"><span data-stu-id="80a86-182">-Tag</span></span>
<span data-ttu-id="80a86-183">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="80a86-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="80a86-184">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="80a86-184">For example:</span></span>

<span data-ttu-id="80a86-185">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="80a86-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="80a86-186">-UrlPathMaps</span></span>
<span data-ttu-id="80a86-187">Anger URL-sökvägar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="80a86-187">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="80a86-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="80a86-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="80a86-189">Anger en konfiguration för webb programs brand väggen (WAF).</span><span class="sxs-lookup"><span data-stu-id="80a86-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="80a86-190">Du kan använda Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet för att få en WAF.</span><span class="sxs-lookup"><span data-stu-id="80a86-190">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-191">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80a86-191">-Confirm</span></span>
<span data-ttu-id="80a86-192">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80a86-192">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a86-193">-WhatIf</span></span>
<span data-ttu-id="80a86-194">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80a86-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a86-195">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80a86-195">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a86-196">CommonParameters</span></span>
<span data-ttu-id="80a86-197">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a86-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a86-198">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a86-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a86-199">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80a86-199">INPUTS</span></span>

## <span data-ttu-id="80a86-200">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80a86-200">OUTPUTS</span></span>

### <span data-ttu-id="80a86-201">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80a86-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80a86-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80a86-202">NOTES</span></span>

## <span data-ttu-id="80a86-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80a86-203">RELATED LINKS</span></span>

[<span data-ttu-id="80a86-204">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="80a86-204">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="80a86-205">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="80a86-205">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="80a86-206">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="80a86-206">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="80a86-207">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80a86-207">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="80a86-208">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80a86-208">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="80a86-209">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80a86-209">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="80a86-210">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="80a86-210">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="80a86-211">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="80a86-211">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="80a86-212">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80a86-212">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="80a86-213">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="80a86-213">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
