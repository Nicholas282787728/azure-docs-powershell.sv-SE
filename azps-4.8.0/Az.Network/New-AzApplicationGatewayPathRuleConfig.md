---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262603"
---
# <span data-ttu-id="c2ca3-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="c2ca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ca3-103">Skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="c2ca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2ca3-104">SYNTAX</span></span>

### <span data-ttu-id="c2ca3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ca3-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2ca3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c2ca3-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2ca3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2ca3-107">DESCRIPTION</span></span>
<span data-ttu-id="c2ca3-108">Cmdleten **New-AzApplicationGatewayPathRuleConfig** skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="c2ca3-109">Regler som skapas av denna cmdlet kan läggas till i en uppsättning konfigurations inställningar för URL-sökvägar och sedan tilldelas en gateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="c2ca3-110">Konfigurations inställningar för Sök vägs karta används för belastnings utjämning i Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="c2ca3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2ca3-111">EXAMPLES</span></span>

### <span data-ttu-id="c2ca3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2ca3-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="c2ca3-113">De här kommandona skapar en ny Application Gateway Sök vägs regel och använder sedan cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** för att tilldela den regeln till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="c2ca3-114">För att göra detta skapar det första kommandot en objekt referens till gateway-ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="c2ca3-115">Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="c2ca3-116">Nästa två kommandon skapar en adresspool och ett objekt med HTTP-inställningar för en server del. de här objekten (lagrade i variabeln $AddressPool och $HttpSettings) behövs för att skapa ett Sök vägs regel objekt.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="c2ca3-117">Det fjärde kommandot skapar Sök vägs regel objekt och lagras i en variabel som heter $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="c2ca3-118">Med det femte kommandot används **Add-AzApplicationGatewayUrlPathMapConfig** för att lägga till konfigurations inställningarna och den nya Sök vägs regeln i dessa inställningar för ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="c2ca3-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c2ca3-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="c2ca3-120">Med de här kommandona skapas en Sök vägs regel med namnet som "bas", sökvägar som "/base", BackendAddressPool som $AddressPool, BackendHttpSettings som $HttpSettings och FirewallPolicy som $firewallPolicy. ngs och den nya Sök vägs regeln i dessa inställningar till ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="c2ca3-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2ca3-121">PARAMETERS</span></span>

### <span data-ttu-id="c2ca3-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2ca3-122">-BackendAddressPool</span></span>
<span data-ttu-id="c2ca3-123">Anger en objekt referens till en samling inställningar för adresspool som ska läggas till i inställningar för gateway-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="c2ca3-124">Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendAddressPool cmdlet och syntax som liknar den här: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="c2ca3-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="c2ca3-125">Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till i adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="c2ca3-126">Observera att IP-adressen omges av citat tecken och avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="c2ca3-127">Den resulterande variabeln $AddressPool och kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="c2ca3-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="c2ca3-128">Server delens adresspool representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="c2ca3-129">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="c2ca3-130">Om du använder den här parametern kan du inte använda parametern *DefaultBackendAddressPoolId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c2ca3-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="c2ca3-132">Anger ID för en befintlig backend-adresspool som kan läggas till i inställningar för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c2ca3-133">Adresspool-ID: n kan returneras med Get-AzApplicationGatewayBackendAddressPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="c2ca3-134">När du har ID-numret kan du använda parametern *DefaultBackendAddressPoolId* i stället för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="c2ca3-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="c2ca3-135">Till exempel:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" adresspoolen representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="c2ca3-136">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="c2ca3-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2ca3-137">-BackendHttpSettings</span></span>
<span data-ttu-id="c2ca3-138">Anger en objekt referens till en samling av Server dels HTTP-inställningar som ska läggas till i konfigurations inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c2ca3-139">Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendHttpSettings cmdlet och syntax som liknar den här: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-namn "ContosoHttpSettings"-port 80-Protocol "http"-CookieBasedAffinity "Disabled" variabeln $HttpSettings, kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings Server DELENS http-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="c2ca3-140">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettingsId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c2ca3-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c2ca3-142">Anger ID för en befintlig HTTP-konfigurationsfil i Server delen som kan läggas till i inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c2ca3-143">HTTP inställnings-ID: n kan returneras med Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="c2ca3-144">När du har ID-numret kan du använda parametern *DefaultBackendHttpSettingsId* i stället för parametern *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="c2ca3-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="c2ca3-145">Till exempel:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="c2ca3-146">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettings* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="c2ca3-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c2ca3-147">-FirewallPolicy</span></span>
<span data-ttu-id="c2ca3-148">Anger objekt referensen till en brand Väggs princip på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="c2ca3-149">Objekt referensen kan skapas med hjälp av New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="c2ca3-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-namn "wafPolicy1"-ResourceGroup "rgName" en brand Väggs princip som skapas med hjälp av ovanstående cmdleten kan hänvisas till en sökväg på en nivå.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="c2ca3-151">med kommandot ovan skulle du skapa en standard princip inställning och hanterade regler.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="c2ca3-152">I stället för standardvärden kan användarna ange PolicySettings, ManagedRules genom att använda New-AzApplicationGatewayFirewallPolicySettings och New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c2ca3-153">-FirewallPolicyId</span></span>
<span data-ttu-id="c2ca3-154">Anger ID för en befintlig webb programs brand Väggs resurs på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="c2ca3-155">Brand Väggs princip-ID: n kan returneras med Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="c2ca3-156">När vi har det ID du kan använda parametern *FirewallPolicyId* i stället för parametern *FirewallPolicy* .</span><span class="sxs-lookup"><span data-stu-id="c2ca3-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="c2ca3-157">Till exempel:-FirewallPolicyId "/Subscriptions/<abonnemang-ID>/resourceGroups/<resurs-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="c2ca3-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ca3-158">-DefaultProfile</span></span>
<span data-ttu-id="c2ca3-159">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2ca3-160">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2ca3-160">-Name</span></span>
<span data-ttu-id="c2ca3-161">Anger namnet på den Sök vägs regel som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c2ca3-162">-Banor</span><span class="sxs-lookup"><span data-stu-id="c2ca3-162">-Paths</span></span>
<span data-ttu-id="c2ca3-163">Anger en eller flera Sök vägs regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-163">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ca3-164">-RedirectConfiguration</span></span>
<span data-ttu-id="c2ca3-165">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c2ca3-165">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c2ca3-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="c2ca3-167">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ca3-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c2ca3-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2ca3-168">-RewriteRuleSet</span></span>
<span data-ttu-id="c2ca3-169">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c2ca3-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ca3-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c2ca3-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="c2ca3-171">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2ca3-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c2ca3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ca3-172">CommonParameters</span></span>
<span data-ttu-id="c2ca3-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ca3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ca3-174">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ca3-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ca3-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2ca3-175">INPUTS</span></span>

### <span data-ttu-id="c2ca3-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="c2ca3-176">None</span></span>

## <span data-ttu-id="c2ca3-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2ca3-177">OUTPUTS</span></span>

### <span data-ttu-id="c2ca3-178">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="c2ca3-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="c2ca3-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2ca3-179">NOTES</span></span>

## <span data-ttu-id="c2ca3-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2ca3-180">RELATED LINKS</span></span>

[<span data-ttu-id="c2ca3-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2ca3-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2ca3-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c2ca3-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2ca3-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2ca3-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c2ca3-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c2ca3-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c2ca3-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="c2ca3-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2ca3-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2ca3-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2ca3-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


