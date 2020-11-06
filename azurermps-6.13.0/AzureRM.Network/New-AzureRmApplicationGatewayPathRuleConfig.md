---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f8d9a4266474f18a2dd20fd4ddc0746320359f59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580784"
---
# <span data-ttu-id="ec43a-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="ec43a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec43a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec43a-103">Skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec43a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec43a-104">SYNTAX</span></span>

### <span data-ttu-id="ec43a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec43a-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec43a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ec43a-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec43a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec43a-107">DESCRIPTION</span></span>
<span data-ttu-id="ec43a-108">Cmdleten **New-AzureRmApplicationGatewayPathRuleConfig** skapar en Sök vägs regel för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="ec43a-109">Regler som skapas av denna cmdlet kan läggas till i en uppsättning konfigurations inställningar för URL-sökvägar och sedan tilldelas en gateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="ec43a-110">Konfigurations inställningar för Sök vägs karta används för belastnings utjämning i Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="ec43a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec43a-111">EXAMPLES</span></span>

### <span data-ttu-id="ec43a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec43a-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="ec43a-113">De här kommandona skapar en ny Application Gateway Sök vägs regel och använder sedan cmdleten **Add-AzureRmApplicationGatewayUrlPathMapConfig** för att tilldela den regeln till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="ec43a-114">För att göra detta skapar det första kommandot en objekt referens till gateway-ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="ec43a-115">Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ec43a-116">Nästa två kommandon skapar en adresspool och ett objekt med HTTP-inställningar för en server del. de här objekten (lagrade i variabeln $AddressPool och $HttpSettings) behövs för att skapa ett Sök vägs regel objekt.</span><span class="sxs-lookup"><span data-stu-id="ec43a-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="ec43a-117">Det fjärde kommandot skapar Sök vägs regel objekt och lagras i en variabel som heter $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="ec43a-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="ec43a-118">Med det femte kommandot används **Add-AzureRmApplicationGatewayUrlPathMapConfig** för att lägga till konfigurations inställningarna och den nya Sök vägs regeln i dessa inställningar för ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="ec43a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec43a-119">PARAMETERS</span></span>

### <span data-ttu-id="ec43a-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ec43a-120">-BackendAddressPool</span></span>
<span data-ttu-id="ec43a-121">Anger en objekt referens till en samling inställningar för adresspool som ska läggas till i inställningar för gateway-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="ec43a-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="ec43a-122">Du kan skapa denna objekt referens genom att använda New-AzureRmApplicationGatewayBackendAddressPool cmdlet och syntax som liknar den här: `$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="ec43a-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="ec43a-123">Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till i adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="ec43a-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="ec43a-124">Observera att IP-adressen omges av citat tecken och avgränsas med kommatecken.</span><span class="sxs-lookup"><span data-stu-id="ec43a-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="ec43a-125">Den resulterande variabeln $AddressPool och kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="ec43a-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="ec43a-126">Server delens adresspool representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="ec43a-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="ec43a-127">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="ec43a-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="ec43a-128">Om du använder den här parametern kan du inte använda parametern *DefaultBackendAddressPoolId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ec43a-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="ec43a-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ec43a-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="ec43a-130">Anger ID för en befintlig backend-adresspool som kan läggas till i inställningar för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="ec43a-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="ec43a-131">Adresspool-ID: n kan returneras med Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec43a-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="ec43a-132">När du har ID-numret kan du använda parametern *DefaultBackendAddressPoolId* i stället för parametern *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="ec43a-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="ec43a-133">Till exempel:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" adresspoolen representerar IP-adresserna på backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="ec43a-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="ec43a-134">Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="ec43a-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="ec43a-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec43a-135">-BackendHttpSettings</span></span>
<span data-ttu-id="ec43a-136">Anger en objekt referens till en samling av Server dels HTTP-inställningar som ska läggas till i konfigurations inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="ec43a-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="ec43a-137">Du kan skapa denna objekt referens genom att använda New-AzureRmApplicationGatewayBackendHttpSettings cmdlet och syntax som liknar den här: $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-namn "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "Disabled" variabeln $HttpSettings, kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings Server DELENS http-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="ec43a-137">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="ec43a-138">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettingsId* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ec43a-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="ec43a-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ec43a-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="ec43a-140">Anger ID för en befintlig HTTP-konfigurationsfil i Server delen som kan läggas till i inställningarna för gateway-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="ec43a-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="ec43a-141">HTTP inställnings-ID: n kan returneras med Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec43a-141">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="ec43a-142">När du har ID-numret kan du använda parametern *DefaultBackendHttpSettingsId* i stället för parametern *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="ec43a-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="ec43a-143">Till exempel:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.</span><span class="sxs-lookup"><span data-stu-id="ec43a-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="ec43a-144">Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettings* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ec43a-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="ec43a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec43a-145">-DefaultProfile</span></span>
<span data-ttu-id="ec43a-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec43a-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec43a-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec43a-147">-Name</span></span>
<span data-ttu-id="ec43a-148">Anger namnet på den Sök vägs regel som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="ec43a-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ec43a-149">-Banor</span><span class="sxs-lookup"><span data-stu-id="ec43a-149">-Paths</span></span>
<span data-ttu-id="ec43a-150">Anger en eller flera Sök vägs regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ec43a-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="ec43a-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec43a-151">-RedirectConfiguration</span></span>
<span data-ttu-id="ec43a-152">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ec43a-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="ec43a-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ec43a-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="ec43a-154">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec43a-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="ec43a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec43a-155">CommonParameters</span></span>
<span data-ttu-id="ec43a-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec43a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec43a-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec43a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec43a-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec43a-158">INPUTS</span></span>

### <span data-ttu-id="ec43a-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="ec43a-159">None</span></span>

## <span data-ttu-id="ec43a-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec43a-160">OUTPUTS</span></span>

### <span data-ttu-id="ec43a-161">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="ec43a-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="ec43a-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec43a-162">NOTES</span></span>

## <span data-ttu-id="ec43a-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec43a-163">RELATED LINKS</span></span>

[<span data-ttu-id="ec43a-164">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-164">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ec43a-165">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec43a-165">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ec43a-166">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-166">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ec43a-167">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ec43a-167">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ec43a-168">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec43a-168">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="ec43a-169">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-169">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="ec43a-170">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-170">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ec43a-171">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-171">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ec43a-172">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ec43a-172">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


