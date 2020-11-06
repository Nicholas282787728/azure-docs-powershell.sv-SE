---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f72fb4eb80475b421ca4a893a598d8686dde64c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582347"
---
# <span data-ttu-id="539cd-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="539cd-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="539cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="539cd-102">SYNOPSIS</span></span>
<span data-ttu-id="539cd-103">Lägger till en adresslisteregel till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="539cd-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="539cd-104">SYNTAX</span></span>

### <span data-ttu-id="539cd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="539cd-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="539cd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="539cd-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539cd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="539cd-107">DESCRIPTION</span></span>
<span data-ttu-id="539cd-108">Cmdleten **Add-AzureRmApplicationGatewayRequestRoutingRule** lägger till en regel för anslutningsbegäran till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="539cd-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="539cd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="539cd-109">EXAMPLES</span></span>

### <span data-ttu-id="539cd-110">Exempel 1: lägga till en operationsföljdslänkkod i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="539cd-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="539cd-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="539cd-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="539cd-112">Med det andra kommandot läggs regeln för anslutningsbegäran till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="539cd-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="539cd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="539cd-113">PARAMETERS</span></span>

### <span data-ttu-id="539cd-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539cd-114">-ApplicationGateway</span></span>
<span data-ttu-id="539cd-115">Anger en Programgateway som denna cmdlet lägger till en anslutningsbegäran för.</span><span class="sxs-lookup"><span data-stu-id="539cd-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="539cd-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="539cd-116">-BackendAddressPool</span></span>
<span data-ttu-id="539cd-117">Anger ett objekt för en Programgateway-backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="539cd-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="539cd-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="539cd-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="539cd-119">Anger en Programgateway-adresspool-ID.</span><span class="sxs-lookup"><span data-stu-id="539cd-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="539cd-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="539cd-120">-BackendHttpSettings</span></span>
<span data-ttu-id="539cd-121">Anger ett backend-objekt med HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="539cd-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="539cd-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="539cd-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="539cd-123">Anger ett ID för HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="539cd-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="539cd-124">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="539cd-124">-HttpListener</span></span>
<span data-ttu-id="539cd-125">Anger HTTP Listener-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="539cd-125">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cd-126">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="539cd-126">-HttpListenerId</span></span>
<span data-ttu-id="539cd-127">Anger HTTP-lyssnar-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="539cd-127">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="539cd-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="539cd-128">-Name</span></span>
<span data-ttu-id="539cd-129">Anger namnet på regeln för routningsregler denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="539cd-129">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="539cd-130">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="539cd-130">-RedirectConfiguration</span></span>
<span data-ttu-id="539cd-131">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="539cd-131">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="539cd-132">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="539cd-132">-RedirectConfigurationId</span></span>
<span data-ttu-id="539cd-133">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="539cd-133">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="539cd-134">-RuleType</span><span class="sxs-lookup"><span data-stu-id="539cd-134">-RuleType</span></span>
<span data-ttu-id="539cd-135">Anger typen för routningsregler för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="539cd-135">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cd-136">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="539cd-136">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cd-137">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="539cd-137">-UrlPathMapId</span></span>
<span data-ttu-id="539cd-138">Anger URL-sökvägen för kart regeln.</span><span class="sxs-lookup"><span data-stu-id="539cd-138">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="539cd-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539cd-139">-DefaultProfile</span></span>
<span data-ttu-id="539cd-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="539cd-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="539cd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539cd-141">CommonParameters</span></span>
<span data-ttu-id="539cd-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539cd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539cd-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539cd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539cd-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="539cd-144">INPUTS</span></span>

### <span data-ttu-id="539cd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="539cd-145">System.String</span></span>

## <span data-ttu-id="539cd-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="539cd-146">OUTPUTS</span></span>

### <span data-ttu-id="539cd-147">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539cd-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="539cd-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="539cd-148">NOTES</span></span>

## <span data-ttu-id="539cd-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="539cd-149">RELATED LINKS</span></span>

[<span data-ttu-id="539cd-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="539cd-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="539cd-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="539cd-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="539cd-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="539cd-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="539cd-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="539cd-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


