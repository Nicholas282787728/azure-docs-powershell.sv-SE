---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 46eb4979c62a5c1f2cb8277ddc1461ee09a339c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092572"
---
# <span data-ttu-id="6e7d3-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e7d3-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="6e7d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7d3-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-103">Creates an application gateway.</span></span>

## <span data-ttu-id="6e7d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e7d3-104">SYNTAX</span></span>

### <span data-ttu-id="6e7d3-105">IdentityByUserAssignedIdentityId (standard)</span><span class="sxs-lookup"><span data-stu-id="6e7d3-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7d3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e7d3-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7d3-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6e7d3-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7d3-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="6e7d3-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e7d3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e7d3-109">DESCRIPTION</span></span>
<span data-ttu-id="6e7d3-110">Cmdleten **New-AzApplicationGateway** skapar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="6e7d3-111">En Programgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="6e7d3-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="6e7d3-112">En resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-112">A resource group.</span></span>
- <span data-ttu-id="6e7d3-113">Ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-113">A virtual network.</span></span>
- <span data-ttu-id="6e7d3-114">Backend-serverpoolen med IP-adresser till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="6e7d3-115">Backend-inställningar för serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-115">Back-end server pool settings.</span></span> <span data-ttu-id="6e7d3-116">Varje pool har inställningar som port, protokoll och cookie-baserad tillhörighet, som tillämpas på alla servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="6e7d3-117">Front-IP-adresser, som är de IP-adresser som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="6e7d3-118">En front-IP-adress kan vara en offentlig IP-adress eller en intern IP-adress.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="6e7d3-119">Front portar, vilka är de offentliga portar som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="6e7d3-120">Trafik som träffar dessa portar omdirigeras till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="6e7d3-121">En regel för anslutningsbegäran som binder lyssnaren och backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="6e7d3-122">Regeln definierar vilken backend-server som trafiken ska omdirigeras till när den träffar en viss lyssnare.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="6e7d3-123">En lyssnare har frontend-port, front-end IP Address, Protocol (HTTP eller HTTPS) och SSL (Secure Sockets Layer), certifikat namn (om du konfigurerar SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="6e7d3-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="6e7d3-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e7d3-124">EXAMPLES</span></span>

### <span data-ttu-id="6e7d3-125">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="6e7d3-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="6e7d3-126">I följande exempel skapas en Programgateway genom att först skapa en resurs grupp och ett virtuellt nätverk:</span><span class="sxs-lookup"><span data-stu-id="6e7d3-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="6e7d3-127">Backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="6e7d3-127">A back-end server pool</span></span>
- <span data-ttu-id="6e7d3-128">Server poolinställningarna</span><span class="sxs-lookup"><span data-stu-id="6e7d3-128">Back-end server pool settings</span></span>
- <span data-ttu-id="6e7d3-129">Front portar</span><span class="sxs-lookup"><span data-stu-id="6e7d3-129">Front-end ports</span></span>
- <span data-ttu-id="6e7d3-130">Front-IP-adresser</span><span class="sxs-lookup"><span data-stu-id="6e7d3-130">Front-end IP addresses</span></span>
- <span data-ttu-id="6e7d3-131">En regel för en anslutningsbegäran de fyra kommandona skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="6e7d3-132">Det första kommandot skapar en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="6e7d3-133">Det andra kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="6e7d3-134">Det tredje kommandot verifierar nät konfiguration och det fjärde kommandot verifierar att det virtuella nätverket har skapats.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="6e7d3-135">Med följande kommandon skapas programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="6e7d3-136">Det första kommandot skapar en IP-konfiguration med namnet GatewayIp01 för under nätet som skapades.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="6e7d3-137">Det andra kommandot skapar en backend-grupppool med namnet Pool01 med en lista över backend-IP-adresser och lagrar poolen i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="6e7d3-138">Det tredje kommandot skapar inställningarna för backend-serverpoolen och lagrar inställningarna i $PoolSetting variabeln.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="6e7d3-139">Med kommandot tillbaka skapar du en front port på port 80, namnger den FrontEndPort01 och lagrar porten i $FrontEndPort variabel.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="6e7d3-140">Det femte kommandot skapar en offentlig IP-adress genom att använda New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="6e7d3-141">Det sjätte kommandot skapar en front-IP-konfiguration med $PublicIp, namnger den FrontEndPortConfig01 och lagrar den i $FrontEndIpConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="6e7d3-142">Med det sjunde kommandot skapas en lyssnare med den tidigare skapade $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="6e7d3-143">Med kommandot åtto skapas en regel för lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="6e7d3-144">Med det nionde kommandot anges SKU.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="6e7d3-145">Det tionde kommandot skapar en gateway med de objekt som anges med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="6e7d3-146">Exempel 2: skapa en Programgateway med UserAssigned identitet</span><span class="sxs-lookup"><span data-stu-id="6e7d3-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="6e7d3-147">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e7d3-147">PARAMETERS</span></span>

### <span data-ttu-id="6e7d3-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e7d3-148">-AsJob</span></span>
<span data-ttu-id="6e7d3-149">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6e7d3-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e7d3-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="6e7d3-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="6e7d3-151">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="6e7d3-153">Autoskalans konfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="6e7d3-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="6e7d3-154">-BackendAddressPools</span></span>
<span data-ttu-id="6e7d3-155">Anger listan över backend-adresspooler för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="6e7d3-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="6e7d3-157">Anger listan över backend-HTTP-inställningar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="6e7d3-159">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="6e7d3-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7d3-160">-DefaultProfile</span></span>
<span data-ttu-id="6e7d3-161">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e7d3-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="6e7d3-162">-EnableFIPS</span></span>
<span data-ttu-id="6e7d3-163">Om FIPS är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="6e7d3-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="6e7d3-164">-EnableHttp2</span></span>
<span data-ttu-id="6e7d3-165">Om HTTP2 är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="6e7d3-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6e7d3-166">-FirewallPolicy</span></span>
<span data-ttu-id="6e7d3-167">Brand Väggs konfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6e7d3-168">-FirewallPolicyId</span></span>
<span data-ttu-id="6e7d3-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6e7d3-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="6e7d3-170">-Force</span><span class="sxs-lookup"><span data-stu-id="6e7d3-170">-Force</span></span>
<span data-ttu-id="6e7d3-171">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e7d3-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="6e7d3-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="6e7d3-173">Om Force firewallPolicy-associering är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="6e7d3-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="6e7d3-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="6e7d3-175">Anger en lista med IP-konfigurationer för front-end för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="6e7d3-176">-FrontendPorts</span></span>
<span data-ttu-id="6e7d3-177">Anger en lista över front portar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="6e7d3-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="6e7d3-179">Anger en lista med IP-konfigurationer för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="6e7d3-180">-HttpListeners</span></span>
<span data-ttu-id="6e7d3-181">Anger en lista med HTTP-lyssnare för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="6e7d3-182">-Identity</span></span>
<span data-ttu-id="6e7d3-183">Application Gateway-identitet som ska kopplas till Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-184">-Plats</span><span class="sxs-lookup"><span data-stu-id="6e7d3-184">-Location</span></span>
<span data-ttu-id="6e7d3-185">Anger i vilken region du vill skapa programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="6e7d3-186">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e7d3-186">-Name</span></span>
<span data-ttu-id="6e7d3-187">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="6e7d3-188">-Avsöks</span><span class="sxs-lookup"><span data-stu-id="6e7d3-188">-Probes</span></span>
<span data-ttu-id="6e7d3-189">Anger Avsök för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-189">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-190">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="6e7d3-190">-RedirectConfigurations</span></span>
<span data-ttu-id="6e7d3-191">Listan med konfiguration av omdirigering</span><span class="sxs-lookup"><span data-stu-id="6e7d3-191">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-192">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="6e7d3-192">-RequestRoutingRules</span></span>
<span data-ttu-id="6e7d3-193">Anger en lista över routningsregler för anslutningsbegäran för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-193">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-194">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e7d3-194">-ResourceGroupName</span></span>
<span data-ttu-id="6e7d3-195">Anger namnet på den resurs grupp där Application Gateway ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-195">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="6e7d3-196">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e7d3-196">-RewriteRuleSet</span></span>
<span data-ttu-id="6e7d3-197">Listan med RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e7d3-197">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-198">-SKU</span><span class="sxs-lookup"><span data-stu-id="6e7d3-198">-Sku</span></span>
<span data-ttu-id="6e7d3-199">Anger SKU (lager behållning) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-199">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="6e7d3-200">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="6e7d3-200">-SslCertificates</span></span>
<span data-ttu-id="6e7d3-201">Anger listan över SSL-certifikat (Secure Sockets Layer) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-201">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-202">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="6e7d3-202">-SslPolicy</span></span>
<span data-ttu-id="6e7d3-203">Anger en SSL-princip för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-203">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="6e7d3-204">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6e7d3-204">-Tag</span></span>
<span data-ttu-id="6e7d3-205">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-205">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6e7d3-206">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6e7d3-206">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6e7d3-207">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6e7d3-207">-TrustedRootCertificate</span></span>
<span data-ttu-id="6e7d3-208">Listan över betrodda rot certifikat</span><span class="sxs-lookup"><span data-stu-id="6e7d3-208">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-209">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="6e7d3-209">-UrlPathMaps</span></span>
<span data-ttu-id="6e7d3-210">Anger URL-sökvägar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-210">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-211">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="6e7d3-211">-UserAssignedIdentityId</span></span>
<span data-ttu-id="6e7d3-212">ResourceId för den användare tilldelade identiteten som ska kopplas till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-212">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-213">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-213">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="6e7d3-214">Anger en konfiguration för webb programs brand väggen (WAF).</span><span class="sxs-lookup"><span data-stu-id="6e7d3-214">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="6e7d3-215">Du kan använda Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet för att få en WAF.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-215">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="6e7d3-216">-Zone</span><span class="sxs-lookup"><span data-stu-id="6e7d3-216">-Zone</span></span>
<span data-ttu-id="6e7d3-217">En lista över tillgänglighets zoner som betecknar var Application Gateway måste komma från.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-217">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7d3-218">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e7d3-218">-Confirm</span></span>
<span data-ttu-id="6e7d3-219">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e7d3-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e7d3-220">-WhatIf</span></span>
<span data-ttu-id="6e7d3-221">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e7d3-222">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e7d3-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7d3-223">CommonParameters</span></span>
<span data-ttu-id="6e7d3-224">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e7d3-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7d3-225">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e7d3-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7d3-226">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e7d3-226">INPUTS</span></span>

### <span data-ttu-id="6e7d3-227">System. String</span><span class="sxs-lookup"><span data-stu-id="6e7d3-227">System.String</span></span>

### <span data-ttu-id="6e7d3-228">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6e7d3-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="6e7d3-229">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6e7d3-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="6e7d3-230">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="6e7d3-231">Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="6e7d3-232">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="6e7d3-233">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="6e7d3-234">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="6e7d3-235">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="6e7d3-236">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="6e7d3-237">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="6e7d3-238">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="6e7d3-239">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="6e7d3-240">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="6e7d3-241">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="6e7d3-242">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="6e7d3-243">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6e7d3-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="6e7d3-244">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="6e7d3-245">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="6e7d3-246">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6e7d3-246">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6e7d3-247">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6e7d3-247">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="6e7d3-248">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e7d3-248">OUTPUTS</span></span>

### <span data-ttu-id="6e7d3-249">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e7d3-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e7d3-250">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e7d3-250">NOTES</span></span>

## <span data-ttu-id="6e7d3-251">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e7d3-251">RELATED LINKS</span></span>

[<span data-ttu-id="6e7d3-252">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6e7d3-252">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6e7d3-253">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6e7d3-253">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="6e7d3-254">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6e7d3-254">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6e7d3-255">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e7d3-255">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6e7d3-256">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e7d3-256">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6e7d3-257">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e7d3-257">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6e7d3-258">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e7d3-258">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e7d3-259">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6e7d3-259">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="6e7d3-260">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6e7d3-260">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="6e7d3-261">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6e7d3-261">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
