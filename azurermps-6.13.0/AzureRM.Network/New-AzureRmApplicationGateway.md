---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576210"
---
# <span data-ttu-id="6bd9b-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bd9b-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="6bd9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bd9b-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd9b-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bd9b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
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
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd9b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bd9b-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd9b-106">Cmdleten **New-AzureRmApplicationGateway** skapar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="6bd9b-107">En Programgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="6bd9b-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="6bd9b-108">En resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-108">A resource group.</span></span>
- <span data-ttu-id="6bd9b-109">Ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-109">A virtual network.</span></span>
- <span data-ttu-id="6bd9b-110">Backend-serverpoolen med IP-adresser till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="6bd9b-111">Backend-inställningar för serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-111">Back-end server pool settings.</span></span> <span data-ttu-id="6bd9b-112">Varje pool har inställningar som port, protokoll och cookie-baserad tillhörighet, som tillämpas på alla servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="6bd9b-113">Front-IP-adresser, som är de IP-adresser som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="6bd9b-114">En front-IP-adress kan vara en offentlig IP-adress eller en intern IP-adress.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="6bd9b-115">Front portar, vilka är de offentliga portar som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="6bd9b-116">Trafik som träffar dessa portar omdirigeras till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="6bd9b-117">En regel för anslutningsbegäran som binder lyssnaren och backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="6bd9b-118">Regeln definierar vilken backend-server som trafiken ska omdirigeras till när den träffar en viss lyssnare.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="6bd9b-119">En lyssnare har frontend-port, front-end IP Address, Protocol (HTTP eller HTTPS) och SSL (Secure Sockets Layer), certifikat namn (om du konfigurerar SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="6bd9b-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="6bd9b-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bd9b-120">EXAMPLES</span></span>

### <span data-ttu-id="6bd9b-121">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="6bd9b-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="6bd9b-122">I följande exempel skapas en Programgateway genom att först skapa en resurs grupp och ett virtuellt nätverk:</span><span class="sxs-lookup"><span data-stu-id="6bd9b-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="6bd9b-123">Backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="6bd9b-123">A back-end server pool</span></span>
- <span data-ttu-id="6bd9b-124">Server poolinställningarna</span><span class="sxs-lookup"><span data-stu-id="6bd9b-124">Back-end server pool settings</span></span>
- <span data-ttu-id="6bd9b-125">Front portar</span><span class="sxs-lookup"><span data-stu-id="6bd9b-125">Front-end ports</span></span>
- <span data-ttu-id="6bd9b-126">Front-IP-adresser</span><span class="sxs-lookup"><span data-stu-id="6bd9b-126">Front-end IP addresses</span></span>
- <span data-ttu-id="6bd9b-127">En regel för en anslutningsbegäran de fyra kommandona skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="6bd9b-128">Det första kommandot skapar en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="6bd9b-129">Det andra kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="6bd9b-130">Det tredje kommandot verifierar nät konfiguration och det fjärde kommandot verifierar att det virtuella nätverket har skapats.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="6bd9b-131">Med följande kommandon skapas programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="6bd9b-132">Det första kommandot skapar en IP-konfiguration med namnet GatewayIp01 för under nätet som skapades.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="6bd9b-133">Det andra kommandot skapar en backend-grupppool med namnet Pool01 med en lista över backend-IP-adresser och lagrar poolen i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="6bd9b-134">Det tredje kommandot skapar inställningarna för backend-serverpoolen och lagrar inställningarna i $PoolSetting variabeln.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="6bd9b-135">Med kommandot tillbaka skapar du en front port på port 80, namnger den FrontEndPort01 och lagrar porten i $FrontEndPort variabel.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="6bd9b-136">Det femte kommandot skapar en offentlig IP-adress genom att använda New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="6bd9b-137">Det sjätte kommandot skapar en front-IP-konfiguration med $PublicIp, namnger den FrontEndPortConfig01 och lagrar den i $FrontEndIpConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="6bd9b-138">Med det sjunde kommandot skapas en lyssnare med den tidigare skapade $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="6bd9b-139">Med kommandot åtto skapas en regel för lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="6bd9b-140">Med det nionde kommandot anges SKU.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="6bd9b-141">Det tionde kommandot skapar en gateway med de objekt som anges med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="6bd9b-142">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bd9b-142">PARAMETERS</span></span>

### <span data-ttu-id="6bd9b-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bd9b-143">-AsJob</span></span>
<span data-ttu-id="6bd9b-144">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6bd9b-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bd9b-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="6bd9b-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="6bd9b-146">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-146">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-147">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd9b-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="6bd9b-148">Autoskalans konfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd9b-148">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd9b-149">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="6bd9b-149">-BackendAddressPools</span></span>
<span data-ttu-id="6bd9b-150">Anger listan över backend-adresspooler för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-150">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="6bd9b-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="6bd9b-152">Anger listan över backend-HTTP-inställningar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd9b-153">-DefaultProfile</span></span>
<span data-ttu-id="6bd9b-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bd9b-155">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="6bd9b-155">-EnableFIPS</span></span>
<span data-ttu-id="6bd9b-156">Om FIPS är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-156">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="6bd9b-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="6bd9b-157">-EnableHttp2</span></span>
<span data-ttu-id="6bd9b-158">Om HTTP2 är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-158">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="6bd9b-159">-Force</span><span class="sxs-lookup"><span data-stu-id="6bd9b-159">-Force</span></span>
<span data-ttu-id="6bd9b-160">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-160">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6bd9b-161">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="6bd9b-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="6bd9b-162">Anger en lista med IP-konfigurationer för front-end för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-163">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="6bd9b-163">-FrontendPorts</span></span>
<span data-ttu-id="6bd9b-164">Anger en lista över front portar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-164">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-165">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="6bd9b-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="6bd9b-166">Anger en lista med IP-konfigurationer för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-166">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="6bd9b-167">-HttpListeners</span></span>
<span data-ttu-id="6bd9b-168">Anger en lista med HTTP-lyssnare för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-169">-Plats</span><span class="sxs-lookup"><span data-stu-id="6bd9b-169">-Location</span></span>
<span data-ttu-id="6bd9b-170">Anger i vilken region du vill skapa programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-170">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-171">-Namn</span><span class="sxs-lookup"><span data-stu-id="6bd9b-171">-Name</span></span>
<span data-ttu-id="6bd9b-172">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-172">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-173">-Avsöks</span><span class="sxs-lookup"><span data-stu-id="6bd9b-173">-Probes</span></span>
<span data-ttu-id="6bd9b-174">Anger Avsök för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-174">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-175">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="6bd9b-175">-RedirectConfigurations</span></span>
<span data-ttu-id="6bd9b-176">Listan med konfiguration av omdirigering</span><span class="sxs-lookup"><span data-stu-id="6bd9b-176">The list of redirect configuration</span></span>

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

### <span data-ttu-id="6bd9b-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="6bd9b-177">-RequestRoutingRules</span></span>
<span data-ttu-id="6bd9b-178">Anger en lista över routningsregler för anslutningsbegäran för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-178">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd9b-179">-ResourceGroupName</span></span>
<span data-ttu-id="6bd9b-180">Anger namnet på den resurs grupp där Application Gateway ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="6bd9b-181">-Sku</span></span>
<span data-ttu-id="6bd9b-182">Anger SKU (lager behållning) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="6bd9b-183">-SslCertificates</span></span>
<span data-ttu-id="6bd9b-184">Anger listan över SSL-certifikat (Secure Sockets Layer) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="6bd9b-185">-SslPolicy</span></span>
<span data-ttu-id="6bd9b-186">Anger en SSL-princip för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-186">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-187">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6bd9b-187">-Tag</span></span>
<span data-ttu-id="6bd9b-188">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6bd9b-189">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6bd9b-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6bd9b-190">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6bd9b-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="6bd9b-191">Listan över betrodda rot certifikat</span><span class="sxs-lookup"><span data-stu-id="6bd9b-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd9b-192">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="6bd9b-192">-UrlPathMaps</span></span>
<span data-ttu-id="6bd9b-193">Anger URL-sökvägar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-193">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="6bd9b-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd9b-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="6bd9b-195">Anger en konfiguration för webb programs brand väggen (WAF).</span><span class="sxs-lookup"><span data-stu-id="6bd9b-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="6bd9b-196">Du kan använda Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet för att få en WAF.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="6bd9b-197">-Zone</span><span class="sxs-lookup"><span data-stu-id="6bd9b-197">-Zone</span></span>
<span data-ttu-id="6bd9b-198">En lista över tillgänglighets zoner som betecknar var Application Gateway måste komma från.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd9b-199">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6bd9b-199">-Confirm</span></span>
<span data-ttu-id="6bd9b-200">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd9b-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd9b-201">-WhatIf</span></span>
<span data-ttu-id="6bd9b-202">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd9b-203">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd9b-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd9b-204">CommonParameters</span></span>
<span data-ttu-id="6bd9b-205">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bd9b-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd9b-206">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd9b-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd9b-207">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bd9b-207">INPUTS</span></span>

### <span data-ttu-id="6bd9b-208">System. String</span><span class="sxs-lookup"><span data-stu-id="6bd9b-208">System.String</span></span>

### <span data-ttu-id="6bd9b-209">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6bd9b-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="6bd9b-210">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6bd9b-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="6bd9b-211">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayIPConfiguration, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-212">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslCertificate, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-213">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayAuthenticationCertificate, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-214">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-215">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFrontendPort, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-216">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayProbe, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-217">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-218">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendHttpSettings, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-219">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayHttpListener, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-220">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayUrlPathMap, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-221">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRequestRoutingRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-222">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd9b-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bd9b-223">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd9b-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="6bd9b-224">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6bd9b-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6bd9b-225">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bd9b-225">OUTPUTS</span></span>

### <span data-ttu-id="6bd9b-226">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bd9b-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bd9b-227">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bd9b-227">NOTES</span></span>

## <span data-ttu-id="6bd9b-228">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bd9b-228">RELATED LINKS</span></span>

[<span data-ttu-id="6bd9b-229">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6bd9b-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6bd9b-230">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6bd9b-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="6bd9b-231">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6bd9b-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6bd9b-232">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6bd9b-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6bd9b-233">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6bd9b-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6bd9b-234">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd9b-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6bd9b-235">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bd9b-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6bd9b-236">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6bd9b-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="6bd9b-237">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6bd9b-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6bd9b-238">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6bd9b-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
