---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: a9751806760a8e2265737e72d726fb491191fa5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581096"
---
# <span data-ttu-id="3e59b-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e59b-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3e59b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e59b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e59b-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3e59b-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e59b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e59b-104">SYNTAX</span></span>

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
 [-EnableHttp2] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e59b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e59b-105">DESCRIPTION</span></span>
<span data-ttu-id="3e59b-106">Cmdleten **New-AzureRmApplicationGateway** skapar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3e59b-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="3e59b-107">En Programgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="3e59b-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="3e59b-108">En resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3e59b-108">A resource group.</span></span>
- <span data-ttu-id="3e59b-109">Ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="3e59b-109">A virtual network.</span></span>
- <span data-ttu-id="3e59b-110">Backend-serverpoolen med IP-adresser till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="3e59b-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="3e59b-111">Backend-inställningar för serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-111">Back-end server pool settings.</span></span> <span data-ttu-id="3e59b-112">Varje pool har inställningar som port, protokoll och cookie-baserad tillhörighet, som tillämpas på alla servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="3e59b-113">Front-IP-adresser, som är de IP-adresser som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="3e59b-114">En front-IP-adress kan vara en offentlig IP-adress eller en intern IP-adress.</span><span class="sxs-lookup"><span data-stu-id="3e59b-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="3e59b-115">Front portar, vilka är de offentliga portar som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="3e59b-116">Trafik som träffar dessa portar omdirigeras till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="3e59b-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="3e59b-117">En regel för anslutningsbegäran som binder lyssnaren och backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="3e59b-118">Regeln definierar vilken backend-server som trafiken ska omdirigeras till när den träffar en viss lyssnare.</span><span class="sxs-lookup"><span data-stu-id="3e59b-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="3e59b-119">En lyssnare har frontend-port, front-end IP Address, Protocol (HTTP eller HTTPS) och SSL (Secure Sockets Layer), certifikat namn (om du konfigurerar SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="3e59b-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="3e59b-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e59b-120">EXAMPLES</span></span>

### <span data-ttu-id="3e59b-121">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3e59b-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="3e59b-122">I följande exempel skapas en Programgateway genom att först skapa en resurs grupp och ett virtuellt nätverk:</span><span class="sxs-lookup"><span data-stu-id="3e59b-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="3e59b-123">Backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="3e59b-123">A back-end server pool</span></span>
- <span data-ttu-id="3e59b-124">Server poolinställningarna</span><span class="sxs-lookup"><span data-stu-id="3e59b-124">Back-end server pool settings</span></span>
- <span data-ttu-id="3e59b-125">Front portar</span><span class="sxs-lookup"><span data-stu-id="3e59b-125">Front-end ports</span></span>
- <span data-ttu-id="3e59b-126">Front-IP-adresser</span><span class="sxs-lookup"><span data-stu-id="3e59b-126">Front-end IP addresses</span></span>
- <span data-ttu-id="3e59b-127">En regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="3e59b-127">A request routing rule</span></span>

<span data-ttu-id="3e59b-128">De här fyra kommandona skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="3e59b-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="3e59b-129">Det första kommandot skapar en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3e59b-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="3e59b-130">Det andra kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="3e59b-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="3e59b-131">Det tredje kommandot verifierar nät konfiguration och det fjärde kommandot verifierar att det virtuella nätverket har skapats.</span><span class="sxs-lookup"><span data-stu-id="3e59b-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="3e59b-132">Med följande kommandon skapas programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="3e59b-133">Det första kommandot skapar en IP-konfiguration med namnet GatewayIp01 för under nätet som skapades.</span><span class="sxs-lookup"><span data-stu-id="3e59b-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="3e59b-134">Det andra kommandot skapar en backend-grupppool med namnet Pool01 med en lista över backend-IP-adresser och lagrar poolen i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="3e59b-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="3e59b-135">Det tredje kommandot skapar inställningarna för backend-serverpoolen och lagrar inställningarna i $PoolSetting variabeln.</span><span class="sxs-lookup"><span data-stu-id="3e59b-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="3e59b-136">Med kommandot tillbaka skapar du en front port på port 80, namnger den FrontEndPort01 och lagrar porten i $FrontEndPort variabel.</span><span class="sxs-lookup"><span data-stu-id="3e59b-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="3e59b-137">Det femte kommandot skapar en offentlig IP-adress genom att använda New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="3e59b-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="3e59b-138">Det sjätte kommandot skapar en front-IP-konfiguration med $PublicIp, namnger den FrontEndPortConfig01 och lagrar den i $FrontEndIpConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3e59b-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="3e59b-139">Med det sjunde kommandot skapas en lyssnare med den tidigare skapade $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="3e59b-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="3e59b-140">Med kommandot åtto skapas en regel för lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3e59b-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="3e59b-141">Med det nionde kommandot anges SKU.</span><span class="sxs-lookup"><span data-stu-id="3e59b-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="3e59b-142">Det tionde kommandot skapar en gateway med de objekt som anges med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="3e59b-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="3e59b-143">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e59b-143">PARAMETERS</span></span>

### <span data-ttu-id="3e59b-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e59b-144">-AsJob</span></span>
<span data-ttu-id="3e59b-145">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e59b-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e59b-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="3e59b-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="3e59b-147">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="3e59b-148">-BackendAddressPools</span></span>
<span data-ttu-id="3e59b-149">Anger listan över backend-adresspooler för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="3e59b-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="3e59b-151">Anger listan över backend-HTTP-inställningar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e59b-152">-DefaultProfile</span></span>
<span data-ttu-id="3e59b-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e59b-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e59b-154">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="3e59b-154">-EnableHttp2</span></span>
<span data-ttu-id="3e59b-155">Om HTTP2 är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="3e59b-155">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e59b-156">-Force</span><span class="sxs-lookup"><span data-stu-id="3e59b-156">-Force</span></span>
<span data-ttu-id="3e59b-157">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3e59b-157">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e59b-158">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="3e59b-158">-FrontendIPConfigurations</span></span>
<span data-ttu-id="3e59b-159">Anger en lista med IP-konfigurationer för front-end för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-159">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-160">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="3e59b-160">-FrontendPorts</span></span>
<span data-ttu-id="3e59b-161">Anger en lista över front portar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-161">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-162">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="3e59b-162">-GatewayIPConfigurations</span></span>
<span data-ttu-id="3e59b-163">Anger en lista med IP-konfigurationer för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-163">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-164">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="3e59b-164">-HttpListeners</span></span>
<span data-ttu-id="3e59b-165">Anger en lista med HTTP-lyssnare för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-165">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-166">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e59b-166">-Location</span></span>
<span data-ttu-id="3e59b-167">Anger i vilken region du vill skapa programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-167">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-168">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e59b-168">-Name</span></span>
<span data-ttu-id="3e59b-169">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-169">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="3e59b-170">-Avsöks</span><span class="sxs-lookup"><span data-stu-id="3e59b-170">-Probes</span></span>
<span data-ttu-id="3e59b-171">Anger Avsök för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-171">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-172">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="3e59b-172">-RedirectConfigurations</span></span>
<span data-ttu-id="3e59b-173">Listan med konfiguration av omdirigering</span><span class="sxs-lookup"><span data-stu-id="3e59b-173">The list of redirect configuration</span></span>

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

### <span data-ttu-id="3e59b-174">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="3e59b-174">-RequestRoutingRules</span></span>
<span data-ttu-id="3e59b-175">Anger en lista över routningsregler för anslutningsbegäran för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-175">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e59b-176">-ResourceGroupName</span></span>
<span data-ttu-id="3e59b-177">Anger namnet på den resurs grupp där Application Gateway ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3e59b-177">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-178">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e59b-178">-Sku</span></span>
<span data-ttu-id="3e59b-179">Anger SKU (lager behållning) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-179">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-180">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="3e59b-180">-SslCertificates</span></span>
<span data-ttu-id="3e59b-181">Anger listan över SSL-certifikat (Secure Sockets Layer) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-181">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-182">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="3e59b-182">-SslPolicy</span></span>
<span data-ttu-id="3e59b-183">Anger en SSL-princip för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-183">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-184">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3e59b-184">-Tag</span></span>
<span data-ttu-id="3e59b-185">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3e59b-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3e59b-186">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3e59b-186">For example:</span></span>

<span data-ttu-id="3e59b-187">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3e59b-187">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3e59b-188">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="3e59b-188">-UrlPathMaps</span></span>
<span data-ttu-id="3e59b-189">Anger URL-sökvägar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3e59b-189">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="3e59b-190">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e59b-190">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="3e59b-191">Anger en konfiguration för webb programs brand väggen (WAF).</span><span class="sxs-lookup"><span data-stu-id="3e59b-191">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="3e59b-192">Du kan använda Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet för att få en WAF.</span><span class="sxs-lookup"><span data-stu-id="3e59b-192">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="3e59b-193">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e59b-193">-Confirm</span></span>
<span data-ttu-id="3e59b-194">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e59b-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e59b-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e59b-195">-WhatIf</span></span>
<span data-ttu-id="3e59b-196">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e59b-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e59b-197">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e59b-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e59b-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e59b-198">CommonParameters</span></span>
<span data-ttu-id="3e59b-199">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e59b-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e59b-200">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e59b-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e59b-201">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e59b-201">INPUTS</span></span>

### <span data-ttu-id="3e59b-202">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e59b-202">None</span></span>
<span data-ttu-id="3e59b-203">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3e59b-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e59b-204">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e59b-204">OUTPUTS</span></span>

### <span data-ttu-id="3e59b-205">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e59b-205">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e59b-206">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e59b-206">NOTES</span></span>

## <span data-ttu-id="3e59b-207">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e59b-207">RELATED LINKS</span></span>

[<span data-ttu-id="3e59b-208">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3e59b-208">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3e59b-209">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3e59b-209">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="3e59b-210">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3e59b-210">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3e59b-211">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3e59b-211">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3e59b-212">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3e59b-212">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="3e59b-213">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e59b-213">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3e59b-214">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e59b-214">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3e59b-215">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3e59b-215">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="3e59b-216">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3e59b-216">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="3e59b-217">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e59b-217">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
