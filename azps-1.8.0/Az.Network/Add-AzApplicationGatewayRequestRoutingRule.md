---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ffd65085cba383556f4c749c8b7e2b915bb0071c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753964"
---
# <span data-ttu-id="9d5f2-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d5f2-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="9d5f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5f2-103">Lägger till en adresslisteregel till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="9d5f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d5f2-104">SYNTAX</span></span>

### <span data-ttu-id="9d5f2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d5f2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d5f2-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d5f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d5f2-107">DESCRIPTION</span></span>
<span data-ttu-id="9d5f2-108">Cmdleten **Add-AzApplicationGatewayRequestRoutingRule** lägger till en regel för anslutningsbegäran till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="9d5f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d5f2-109">EXAMPLES</span></span>

### <span data-ttu-id="9d5f2-110">Exempel 1: lägga till en operationsföljdslänkkod i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="9d5f2-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="9d5f2-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9d5f2-112">Med det andra kommandot läggs regeln för anslutningsbegäran till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="9d5f2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d5f2-113">PARAMETERS</span></span>

### <span data-ttu-id="9d5f2-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d5f2-114">-ApplicationGateway</span></span>
<span data-ttu-id="9d5f2-115">Anger en Programgateway som denna cmdlet lägger till en anslutningsbegäran för.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="9d5f2-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9d5f2-116">-BackendAddressPool</span></span>
<span data-ttu-id="9d5f2-117">Anger ett objekt för en Programgateway-backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="9d5f2-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="9d5f2-119">Anger en Programgateway-adresspool-ID.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="9d5f2-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9d5f2-120">-BackendHttpSettings</span></span>
<span data-ttu-id="9d5f2-121">Anger ett backend-objekt med HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="9d5f2-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="9d5f2-123">Anger ett ID för HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="9d5f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5f2-124">-DefaultProfile</span></span>
<span data-ttu-id="9d5f2-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d5f2-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9d5f2-126">-HttpListener</span></span>
<span data-ttu-id="9d5f2-127">Anger HTTP Listener-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="9d5f2-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-128">-HttpListenerId</span></span>
<span data-ttu-id="9d5f2-129">Anger HTTP-lyssnar-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="9d5f2-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d5f2-130">-Name</span></span>
<span data-ttu-id="9d5f2-131">Anger namnet på regeln för routningsregler denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="9d5f2-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d5f2-132">-RedirectConfiguration</span></span>
<span data-ttu-id="9d5f2-133">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9d5f2-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9d5f2-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="9d5f2-135">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d5f2-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9d5f2-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d5f2-136">-RewriteRuleSet</span></span>
<span data-ttu-id="9d5f2-137">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9d5f2-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9d5f2-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="9d5f2-139">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d5f2-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9d5f2-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="9d5f2-140">-RuleType</span></span>
<span data-ttu-id="9d5f2-141">Anger typen för routningsregler för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="9d5f2-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="9d5f2-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="9d5f2-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="9d5f2-143">-UrlPathMapId</span></span>
<span data-ttu-id="9d5f2-144">Anger URL-sökvägen för kart regeln.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-144">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="9d5f2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5f2-145">CommonParameters</span></span>
<span data-ttu-id="9d5f2-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5f2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5f2-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5f2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5f2-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d5f2-148">INPUTS</span></span>

### <span data-ttu-id="9d5f2-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d5f2-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d5f2-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d5f2-150">OUTPUTS</span></span>

### <span data-ttu-id="9d5f2-151">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d5f2-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d5f2-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d5f2-152">NOTES</span></span>

## <span data-ttu-id="9d5f2-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d5f2-153">RELATED LINKS</span></span>

[<span data-ttu-id="9d5f2-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d5f2-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9d5f2-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d5f2-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9d5f2-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d5f2-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9d5f2-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d5f2-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


