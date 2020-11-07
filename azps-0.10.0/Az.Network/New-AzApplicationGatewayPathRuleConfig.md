---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922163"
---
# <span data-ttu-id="f1fbf-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="f1fbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fbf-103">Skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="f1fbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1fbf-104">SYNTAX</span></span>

### <span data-ttu-id="f1fbf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1fbf-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fbf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f1fbf-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1fbf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1fbf-107">DESCRIPTION</span></span>
<span data-ttu-id="f1fbf-108">Cmdleten **New-AzApplicationGatewayPathRuleConfig** skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="f1fbf-109">Regler som skapas av denna cmdlet kan läggas till i en uppsättning konfigurations inställningar för URL-sökvägar och sedan tilldelas en gateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="f1fbf-110">Konfigurations inställningar för Sök vägs karta används för belastnings utjämning i Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="f1fbf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1fbf-111">EXAMPLES</span></span>

### <span data-ttu-id="f1fbf-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f1fbf-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="f1fbf-113">De här kommandona skapar en ny Application Gateway Sök vägs regel och använder sedan cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** för att tilldela den regeln till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="f1fbf-114">För att göra detta skapar det första kommandot en objekt referens till gateway-ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="f1fbf-115">Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="f1fbf-116">Nästa två kommandon skapar en adresspool och ett objekt med HTTP-inställningar för en server del. de här objekten (lagrade i variabeln $AddressPool och $HttpSettings) behövs för att skapa ett Sök vägs regel objekt.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="f1fbf-117">Det fjärde kommandot skapar Sök vägs regel objekt och lagras i en variabel som heter $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="f1fbf-118">Med det femte kommandot används **Add-AzApplicationGatewayUrlPathMapConfig** för att lägga till konfigurations inställningarna och den nya Sök vägs regeln i dessa inställningar för ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="f1fbf-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1fbf-119">PARAMETERS</span></span>

### <span data-ttu-id="f1fbf-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f1fbf-120">-BackendAddressPool</span></span>
<span data-ttu-id="f1fbf-121">Anger en objekt referens till en samling inställningar för adresspool som ska läggas till i inställningar för gateway-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="f1fbf-122">Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendAddressPool cmdlet och syntax som liknar den här:</span><span class="sxs-lookup"><span data-stu-id="f1fbf-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="f1fbf-123">Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till i adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="f1fbf-124">Observera att IP-adressen omges av citat tecken och avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="f1fbf-125">Den resulterande variabeln $AddressPool och kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="f1fbf-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="f1fbf-126">Server delens adresspool representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="f1fbf-127">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="f1fbf-128">Om du använder den här parametern kan du inte använda parametern *DefaultBackendAddressPoolId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fbf-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f1fbf-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="f1fbf-130">Anger ID för en befintlig backend-adresspool som kan läggas till i inställningar för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="f1fbf-131">Adresspool-ID: n kan returneras med Get-AzApplicationGatewayBackendAddressPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="f1fbf-132">När du har ID-numret kan du använda parametern *DefaultBackendAddressPoolId* i stället för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="f1fbf-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="f1fbf-133">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="f1fbf-133">For instance:</span></span>

<span data-ttu-id="f1fbf-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="f1fbf-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="f1fbf-135">Server delens adresspool representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="f1fbf-136">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="f1fbf-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1fbf-137">-BackendHttpSettings</span></span>
<span data-ttu-id="f1fbf-138">Anger en objekt referens till en samling av Server dels HTTP-inställningar som ska läggas till i konfigurations inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="f1fbf-139">Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendHttpSetting cmdlet och syntax som liknar den här:</span><span class="sxs-lookup"><span data-stu-id="f1fbf-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="f1fbf-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-namn "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="f1fbf-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="f1fbf-141">Den resulterande variabeln, $HttpSettings, kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="f1fbf-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="f1fbf-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1fbf-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="f1fbf-143">Server delens HTTP-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="f1fbf-144">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettingsId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fbf-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f1fbf-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f1fbf-146">Anger ID för en befintlig HTTP-konfigurationsfil i Server delen som kan läggas till i inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="f1fbf-147">HTTP inställnings-ID: n kan returneras med Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="f1fbf-148">När du har ID-numret kan du använda parametern *DefaultBackendHttpSettingsId* i stället för parametern *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="f1fbf-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="f1fbf-149">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="f1fbf-149">For instance:</span></span>

<span data-ttu-id="f1fbf-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="f1fbf-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="f1fbf-151">Server delens HTTP-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="f1fbf-152">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettings* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="f1fbf-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fbf-153">-DefaultProfile</span></span>
<span data-ttu-id="f1fbf-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1fbf-155">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1fbf-155">-Name</span></span>
<span data-ttu-id="f1fbf-156">Anger namnet på den Sök vägs regel som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fbf-157">-Banor</span><span class="sxs-lookup"><span data-stu-id="f1fbf-157">-Paths</span></span>
<span data-ttu-id="f1fbf-158">Anger en eller flera Sök vägs regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-158">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fbf-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1fbf-159">-RedirectConfiguration</span></span>
<span data-ttu-id="f1fbf-160">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f1fbf-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fbf-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f1fbf-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="f1fbf-162">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1fbf-162">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f1fbf-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fbf-163">CommonParameters</span></span>
<span data-ttu-id="f1fbf-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fbf-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1fbf-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fbf-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1fbf-166">INPUTS</span></span>

###  
<span data-ttu-id="f1fbf-167">**New-AzApplicationGatewayPathRuleConfig** accepterar inte förloppet.</span><span class="sxs-lookup"><span data-stu-id="f1fbf-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="f1fbf-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1fbf-168">OUTPUTS</span></span>

###  
<span data-ttu-id="f1fbf-169">**New-AzApplicationGatewayPathRuleConfig** skapar nya instanser av **Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="f1fbf-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="f1fbf-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1fbf-170">NOTES</span></span>

## <span data-ttu-id="f1fbf-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1fbf-171">RELATED LINKS</span></span>

[<span data-ttu-id="f1fbf-172">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f1fbf-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1fbf-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f1fbf-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f1fbf-175">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f1fbf-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f1fbf-176">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f1fbf-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f1fbf-177">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="f1fbf-178">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f1fbf-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f1fbf-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1fbf-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


