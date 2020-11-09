---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 5f91f333cf7983d50ba2984fcf01845a6c555e83
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322469"
---
# <span data-ttu-id="ac6d4-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac6d4-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="ac6d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6d4-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-103">Creates an application gateway.</span></span>

## <span data-ttu-id="ac6d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac6d4-104">SYNTAX</span></span>

### <span data-ttu-id="ac6d4-105">IdentityByUserAssignedIdentityId (standard)</span><span class="sxs-lookup"><span data-stu-id="ac6d4-105">IdentityByUserAssignedIdentityId (Default)</span></span>
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
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6d4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac6d4-106">SetByResourceId</span></span>
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
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6d4-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ac6d4-107">SetByResource</span></span>
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
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6d4-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="ac6d4-108">IdentityByIdentityObject</span></span>
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
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac6d4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac6d4-109">DESCRIPTION</span></span>
<span data-ttu-id="ac6d4-110">Cmdleten **New-AzApplicationGateway** skapar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="ac6d4-111">En Programgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="ac6d4-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="ac6d4-112">En resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-112">A resource group.</span></span>
- <span data-ttu-id="ac6d4-113">Ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-113">A virtual network.</span></span>
- <span data-ttu-id="ac6d4-114">Backend-serverpoolen med IP-adresser till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="ac6d4-115">Backend-inställningar för serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-115">Back-end server pool settings.</span></span> <span data-ttu-id="ac6d4-116">Varje pool har inställningar som port, protokoll och cookie-baserad tillhörighet, som tillämpas på alla servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="ac6d4-117">Front-IP-adresser, som är de IP-adresser som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="ac6d4-118">En front-IP-adress kan vara en offentlig IP-adress eller en intern IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="ac6d4-119">Front portar, vilka är de offentliga portar som öppnas på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="ac6d4-120">Trafik som träffar dessa portar omdirigeras till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="ac6d4-121">En regel för anslutningsbegäran som binder lyssnaren och backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="ac6d4-122">Regeln definierar vilken backend-server som trafiken ska omdirigeras till när den träffar en viss lyssnare.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="ac6d4-123">En lyssnare har frontend-port, front-end IP Address, Protocol (HTTP eller HTTPS) och SSL (Secure Sockets Layer), certifikat namn (om du konfigurerar SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="ac6d4-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="ac6d4-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac6d4-124">EXAMPLES</span></span>

### <span data-ttu-id="ac6d4-125">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="ac6d4-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="ac6d4-126">I följande exempel skapas en Programgateway genom att först skapa en resurs grupp och ett virtuellt nätverk:</span><span class="sxs-lookup"><span data-stu-id="ac6d4-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="ac6d4-127">Backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="ac6d4-127">A back-end server pool</span></span>
- <span data-ttu-id="ac6d4-128">Server poolinställningarna</span><span class="sxs-lookup"><span data-stu-id="ac6d4-128">Back-end server pool settings</span></span>
- <span data-ttu-id="ac6d4-129">Front portar</span><span class="sxs-lookup"><span data-stu-id="ac6d4-129">Front-end ports</span></span>
- <span data-ttu-id="ac6d4-130">Front-IP-adresser</span><span class="sxs-lookup"><span data-stu-id="ac6d4-130">Front-end IP addresses</span></span>
- <span data-ttu-id="ac6d4-131">En regel för en anslutningsbegäran de fyra kommandona skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="ac6d4-132">Det första kommandot skapar en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="ac6d4-133">Det andra kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="ac6d4-134">Det tredje kommandot verifierar nät konfiguration och det fjärde kommandot verifierar att det virtuella nätverket har skapats.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="ac6d4-135">Med följande kommandon skapas programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="ac6d4-136">Det första kommandot skapar en IP-konfiguration med namnet GatewayIp01 för under nätet som skapades.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="ac6d4-137">Det andra kommandot skapar en backend-grupppool med namnet Pool01 med en lista över backend-IP-adresser och lagrar poolen i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="ac6d4-138">Det tredje kommandot skapar inställningarna för backend-serverpoolen och lagrar inställningarna i $PoolSetting variabeln.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="ac6d4-139">Med kommandot tillbaka skapar du en front port på port 80, namnger den FrontEndPort01 och lagrar porten i $FrontEndPort variabel.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="ac6d4-140">Det femte kommandot skapar en offentlig IP-adress genom att använda New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="ac6d4-141">Det sjätte kommandot skapar en front-IP-konfiguration med $PublicIp, namnger den FrontEndPortConfig01 och lagrar den i $FrontEndIpConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="ac6d4-142">Med det sjunde kommandot skapas en lyssnare med den tidigare skapade $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="ac6d4-143">Med kommandot åtto skapas en regel för lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="ac6d4-144">Med det nionde kommandot anges SKU.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="ac6d4-145">Det tionde kommandot skapar en gateway med de objekt som anges med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="ac6d4-146">Exempel 2: skapa en Programgateway med UserAssigned identitet</span><span class="sxs-lookup"><span data-stu-id="ac6d4-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="ac6d4-147">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac6d4-147">PARAMETERS</span></span>

### <span data-ttu-id="ac6d4-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac6d4-148">-AsJob</span></span>
<span data-ttu-id="ac6d4-149">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ac6d4-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac6d4-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="ac6d4-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="ac6d4-151">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="ac6d4-153">Autoskalans konfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-153">Autoscale Configuration</span></span>

```yaml
Type: PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="ac6d4-154">-BackendAddressPools</span></span>
<span data-ttu-id="ac6d4-155">Anger listan över backend-adresspooler för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="ac6d4-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="ac6d4-157">Anger listan över backend-HTTP-inställningar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="ac6d4-159">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="ac6d4-159">Customer error of an application gateway</span></span>

```yaml
Type: PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6d4-160">-DefaultProfile</span></span>
<span data-ttu-id="ac6d4-161">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac6d4-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="ac6d4-162">-EnableFIPS</span></span>
<span data-ttu-id="ac6d4-163">Om FIPS är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="ac6d4-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="ac6d4-164">-EnableHttp2</span></span>
<span data-ttu-id="ac6d4-165">Om HTTP2 är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="ac6d4-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ac6d4-166">-FirewallPolicy</span></span>
<span data-ttu-id="ac6d4-167">Brand Väggs konfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-167">Firewall configuration</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ac6d4-168">-FirewallPolicyId</span></span>
<span data-ttu-id="ac6d4-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ac6d4-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="ac6d4-170">-Force</span><span class="sxs-lookup"><span data-stu-id="ac6d4-170">-Force</span></span>
<span data-ttu-id="ac6d4-171">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac6d4-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="ac6d4-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="ac6d4-173">Om Force firewallPolicy-associering är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="ac6d4-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="ac6d4-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="ac6d4-175">Anger en lista med IP-konfigurationer för front-end för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="ac6d4-176">-FrontendPorts</span></span>
<span data-ttu-id="ac6d4-177">Anger en lista över front portar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="ac6d4-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="ac6d4-179">Anger en lista med IP-konfigurationer för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="ac6d4-180">-HttpListeners</span></span>
<span data-ttu-id="ac6d4-181">Anger en lista med HTTP-lyssnare för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="ac6d4-182">-Identity</span></span>
<span data-ttu-id="ac6d4-183">Application Gateway-identitet som ska kopplas till Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-184">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac6d4-184">-Location</span></span>
<span data-ttu-id="ac6d4-185">Anger i vilken region du vill skapa programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="ac6d4-186">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac6d4-186">-Name</span></span>
<span data-ttu-id="ac6d4-187">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="ac6d4-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="ac6d4-189">Listan med privateLink-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-189">The list of privateLink Configuration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-190">-Avsöks</span><span class="sxs-lookup"><span data-stu-id="ac6d4-190">-Probes</span></span>
<span data-ttu-id="ac6d4-191">Anger Avsök för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="ac6d4-192">-RedirectConfigurations</span></span>
<span data-ttu-id="ac6d4-193">Listan med konfiguration av omdirigering</span><span class="sxs-lookup"><span data-stu-id="ac6d4-193">The list of redirect configuration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="ac6d4-194">-RequestRoutingRules</span></span>
<span data-ttu-id="ac6d4-195">Anger en lista över routningsregler för anslutningsbegäran för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6d4-196">-ResourceGroupName</span></span>
<span data-ttu-id="ac6d4-197">Anger namnet på den resurs grupp där Application Gateway ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="ac6d4-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac6d4-198">-RewriteRuleSet</span></span>
<span data-ttu-id="ac6d4-199">Listan med RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac6d4-199">The list of RewriteRuleSet</span></span>

```yaml
Type: PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="ac6d4-200">-Sku</span></span>
<span data-ttu-id="ac6d4-201">Anger SKU (lager behållning) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="ac6d4-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="ac6d4-202">-SslCertificates</span></span>
<span data-ttu-id="ac6d4-203">Anger listan över SSL-certifikat (Secure Sockets Layer) för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="ac6d4-204">-SslPolicy</span></span>
<span data-ttu-id="ac6d4-205">Anger en SSL-princip för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-205">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="ac6d4-206">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ac6d4-206">-Tag</span></span>
<span data-ttu-id="ac6d4-207">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-207">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ac6d4-208">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ac6d4-208">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ac6d4-209">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ac6d4-209">-TrustedRootCertificate</span></span>
<span data-ttu-id="ac6d4-210">Listan över betrodda rot certifikat</span><span class="sxs-lookup"><span data-stu-id="ac6d4-210">The list of trusted root certificates</span></span>

```yaml
Type: PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-211">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="ac6d4-211">-UrlPathMaps</span></span>
<span data-ttu-id="ac6d4-212">Anger URL-sökvägar för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-212">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-213">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="ac6d4-213">-UserAssignedIdentityId</span></span>
<span data-ttu-id="ac6d4-214">ResourceId för den användare tilldelade identiteten som ska kopplas till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-214">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-215">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-215">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="ac6d4-216">Anger en konfiguration för webb programs brand väggen (WAF).</span><span class="sxs-lookup"><span data-stu-id="ac6d4-216">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="ac6d4-217">Du kan använda Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet för att få en WAF.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-217">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="ac6d4-218">-Zone</span><span class="sxs-lookup"><span data-stu-id="ac6d4-218">-Zone</span></span>
<span data-ttu-id="ac6d4-219">En lista över tillgänglighets zoner som betecknar var Application Gateway måste komma från.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-219">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6d4-220">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac6d4-220">-Confirm</span></span>
<span data-ttu-id="ac6d4-221">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-221">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac6d4-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac6d4-222">-WhatIf</span></span>
<span data-ttu-id="ac6d4-223">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac6d4-224">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-224">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac6d4-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6d4-225">CommonParameters</span></span>
<span data-ttu-id="ac6d4-226">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6d4-227">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac6d4-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6d4-228">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac6d4-228">INPUTS</span></span>

### <span data-ttu-id="ac6d4-229">System. String</span><span class="sxs-lookup"><span data-stu-id="ac6d4-229">System.String</span></span>

### <span data-ttu-id="ac6d4-230">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac6d4-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="ac6d4-231">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ac6d4-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="ac6d4-232">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="ac6d4-233">Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="ac6d4-234">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="ac6d4-235">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="ac6d4-236">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="ac6d4-237">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="ac6d4-238">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="ac6d4-239">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="ac6d4-240">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="ac6d4-241">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="ac6d4-242">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="ac6d4-243">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="ac6d4-244">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="ac6d4-245">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ac6d4-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="ac6d4-246">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="ac6d4-247">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="ac6d4-248">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ac6d4-248">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ac6d4-249">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ac6d4-249">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="ac6d4-250">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac6d4-250">OUTPUTS</span></span>

### <span data-ttu-id="ac6d4-251">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac6d4-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac6d4-252">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac6d4-252">NOTES</span></span>

## <span data-ttu-id="ac6d4-253">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac6d4-253">RELATED LINKS</span></span>

[<span data-ttu-id="ac6d4-254">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ac6d4-254">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ac6d4-255">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ac6d4-255">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ac6d4-256">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ac6d4-256">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ac6d4-257">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac6d4-257">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ac6d4-258">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac6d4-258">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac6d4-259">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac6d4-259">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ac6d4-260">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ac6d4-260">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ac6d4-261">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac6d4-261">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="ac6d4-262">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ac6d4-262">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="ac6d4-263">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ac6d4-263">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
