---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417248"
---
# <span data-ttu-id="40e13-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="40e13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40e13-102">SYNOPSIS</span></span>
<span data-ttu-id="40e13-103">Skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="40e13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40e13-104">SYNTAX</span></span>

### <span data-ttu-id="40e13-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="40e13-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40e13-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="40e13-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e13-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40e13-107">DESCRIPTION</span></span>
<span data-ttu-id="40e13-108">Cmdleten **New-AzApplicationGatewayPathRuleConfig** skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="40e13-109">Regler som skapas av denna cmdlet kan läggas till i en uppsättning konfigurations inställningar för URL-sökvägar och sedan tilldelas en gateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="40e13-110">Konfigurations inställningar för Sök vägs karta används för belastnings utjämning i Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="40e13-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40e13-111">EXAMPLES</span></span>

### <span data-ttu-id="40e13-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40e13-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="40e13-113">De här kommandona skapar en ny Application Gateway Sök vägs regel och använder sedan cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** för att tilldela den regeln till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="40e13-114">För att göra detta skapar det första kommandot en objekt referens till gateway-ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="40e13-115">Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="40e13-116">Nästa två kommandon skapar en adresspool och ett objekt med HTTP-inställningar för en server del. de här objekten (lagrade i variabeln $AddressPool och $HttpSettings) behövs för att skapa ett Sök vägs regel objekt.</span><span class="sxs-lookup"><span data-stu-id="40e13-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="40e13-117">Det fjärde kommandot skapar Sök vägs regel objekt och lagras i en variabel som heter $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="40e13-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="40e13-118">Med det femte kommandot används **Add-AzApplicationGatewayUrlPathMapConfig** för att lägga till konfigurations inställningarna och den nya Sök vägs regeln i dessa inställningar för ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="40e13-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="40e13-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="40e13-120">Med de här kommandona skapas en Sök vägs regel med namnet som "bas", sökvägar som "/base", BackendAddressPool som $AddressPool, BackendHttpSettings som $HttpSettings och FirewallPolicy som $firewallPolicy. ngs och den nya Sök vägs regeln i dessa inställningar till ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="40e13-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40e13-121">PARAMETERS</span></span>

### <span data-ttu-id="40e13-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40e13-122">-BackendAddressPool</span></span>
<span data-ttu-id="40e13-123">Anger en objekt referens till en samling inställningar för adresspool som ska läggas till i inställningar för gateway-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="40e13-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="40e13-124">Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendAddressPool cmdlet och syntax som liknar den här: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="40e13-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="40e13-125">Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till i adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="40e13-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="40e13-126">Observera att IP-adressen omges av citat tecken och avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="40e13-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="40e13-127">Den resulterande variabeln $AddressPool och kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="40e13-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="40e13-128">Server delens adresspool representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="40e13-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="40e13-129">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="40e13-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="40e13-130">Om du använder den här parametern kan du inte använda parametern *DefaultBackendAddressPoolId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="40e13-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="40e13-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="40e13-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="40e13-132">Anger ID för en befintlig backend-adresspool som kan läggas till i inställningar för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="40e13-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="40e13-133">Adresspool-ID: n kan returneras med Get-AzApplicationGatewayBackendAddressPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e13-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="40e13-134">När du har ID-numret kan du använda parametern *DefaultBackendAddressPoolId* i stället för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="40e13-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="40e13-135">Till exempel:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" adresspoolen representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="40e13-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="40e13-136">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="40e13-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="40e13-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="40e13-137">-BackendHttpSettings</span></span>
<span data-ttu-id="40e13-138">Anger en objekt referens till en samling av Server dels HTTP-inställningar som ska läggas till i konfigurations inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="40e13-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="40e13-139">Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendHttpSettings cmdlet och syntax som liknar den här: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-namn "ContosoHttpSettings"-port 80-Protocol "http"-CookieBasedAffinity "Disabled" variabeln $HttpSettings, kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings Server DELENS http-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="40e13-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="40e13-140">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettingsId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="40e13-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="40e13-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="40e13-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="40e13-142">Anger ID för en befintlig HTTP-konfigurationsfil i Server delen som kan läggas till i inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="40e13-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="40e13-143">HTTP inställnings-ID: n kan returneras med Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e13-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="40e13-144">När du har ID-numret kan du använda parametern *DefaultBackendHttpSettingsId* i stället för parametern *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="40e13-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="40e13-145">Till exempel:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="40e13-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="40e13-146">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettings* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="40e13-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="40e13-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="40e13-147">-FirewallPolicy</span></span>
<span data-ttu-id="40e13-148">Anger objekt referensen till en brand Väggs princip på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="40e13-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="40e13-149">Objekt referensen kan skapas med hjälp av New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e13-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="40e13-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-namn "wafPolicy1"-ResourceGroup "rgName" en brand Väggs princip som skapas med hjälp av ovanstående cmdleten kan hänvisas till en sökväg på en nivå.</span><span class="sxs-lookup"><span data-stu-id="40e13-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="40e13-151">med kommandot ovan skulle du skapa en standard princip inställning och hanterade regler.</span><span class="sxs-lookup"><span data-stu-id="40e13-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="40e13-152">I stället för standardvärden kan användarna ange PolicySettings, ManagedRules genom att använda New-AzApplicationGatewayFirewallPolicySettings och New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="40e13-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e13-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="40e13-153">-FirewallPolicyId</span></span>
<span data-ttu-id="40e13-154">Anger ID för en befintlig webb programs brand Väggs resurs på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="40e13-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="40e13-155">Brand Väggs princip-ID: n kan returneras med Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e13-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="40e13-156">När vi har det ID du kan använda parametern *FirewallPolicyId* i stället för parametern *FirewallPolicy* .</span><span class="sxs-lookup"><span data-stu-id="40e13-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="40e13-157">Till exempel:-FirewallPolicyId "/Subscriptions/<abonnemang-ID>/resourceGroups/<resurs-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="40e13-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e13-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e13-158">-DefaultProfile</span></span>
<span data-ttu-id="40e13-159">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40e13-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e13-160">-Namn</span><span class="sxs-lookup"><span data-stu-id="40e13-160">-Name</span></span>
<span data-ttu-id="40e13-161">Anger namnet på den Sök vägs regel som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="40e13-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="40e13-162">-Banor</span><span class="sxs-lookup"><span data-stu-id="40e13-162">-Paths</span></span>
<span data-ttu-id="40e13-163">Anger en eller flera Sök vägs regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="40e13-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="40e13-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="40e13-164">-RedirectConfiguration</span></span>
<span data-ttu-id="40e13-165">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="40e13-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="40e13-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="40e13-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="40e13-167">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="40e13-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="40e13-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40e13-168">-RewriteRuleSet</span></span>
<span data-ttu-id="40e13-169">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="40e13-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="40e13-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="40e13-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="40e13-171">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40e13-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="40e13-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e13-172">CommonParameters</span></span>
<span data-ttu-id="40e13-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e13-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e13-174">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e13-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e13-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40e13-175">INPUTS</span></span>

### <span data-ttu-id="40e13-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="40e13-176">None</span></span>

## <span data-ttu-id="40e13-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40e13-177">OUTPUTS</span></span>

### <span data-ttu-id="40e13-178">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="40e13-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="40e13-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40e13-179">NOTES</span></span>

## <span data-ttu-id="40e13-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40e13-180">RELATED LINKS</span></span>

[<span data-ttu-id="40e13-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40e13-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40e13-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="40e13-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40e13-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40e13-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="40e13-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="40e13-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="40e13-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="40e13-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40e13-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="40e13-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="40e13-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


