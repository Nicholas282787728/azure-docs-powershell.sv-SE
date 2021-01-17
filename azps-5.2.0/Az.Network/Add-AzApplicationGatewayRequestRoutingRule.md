---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412483"
---
# <span data-ttu-id="d3d2c-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3d2c-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d3d2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d2c-103">Lägger till en adresslisteregel till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="d3d2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3d2c-104">SYNTAX</span></span>

### <span data-ttu-id="d3d2c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3d2c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d3d2c-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d2c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3d2c-107">DESCRIPTION</span></span>
<span data-ttu-id="d3d2c-108">Cmdleten **Add-AzApplicationGatewayRequestRoutingRule** lägger till en regel för anslutningsbegäran till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="d3d2c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3d2c-109">EXAMPLES</span></span>

### <span data-ttu-id="d3d2c-110">Exempel 1: lägga till en operationsföljdslänkkod i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="d3d2c-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="d3d2c-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d3d2c-112">Med det andra kommandot läggs regeln för anslutningsbegäran till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="d3d2c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3d2c-113">PARAMETERS</span></span>

### <span data-ttu-id="d3d2c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3d2c-114">-ApplicationGateway</span></span>
<span data-ttu-id="d3d2c-115">Anger en Programgateway som denna cmdlet lägger till en anslutningsbegäran för.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="d3d2c-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d3d2c-116">-BackendAddressPool</span></span>
<span data-ttu-id="d3d2c-117">Anger ett objekt för en Programgateway-backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="d3d2c-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="d3d2c-119">Anger en Programgateway-adresspool-ID.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="d3d2c-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3d2c-120">-BackendHttpSettings</span></span>
<span data-ttu-id="d3d2c-121">Anger ett backend-objekt med HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="d3d2c-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="d3d2c-123">Anger ett ID för HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="d3d2c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d2c-124">-DefaultProfile</span></span>
<span data-ttu-id="d3d2c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3d2c-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d3d2c-126">-HttpListener</span></span>
<span data-ttu-id="d3d2c-127">Anger HTTP Listener-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="d3d2c-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-128">-HttpListenerId</span></span>
<span data-ttu-id="d3d2c-129">Anger HTTP-lyssnar-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="d3d2c-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3d2c-130">-Name</span></span>
<span data-ttu-id="d3d2c-131">Anger namnet på regeln för routningsregler denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="d3d2c-132">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="d3d2c-132">-Priority</span></span>
<span data-ttu-id="d3d2c-133">Regelns prioritet</span><span class="sxs-lookup"><span data-stu-id="d3d2c-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d2c-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3d2c-134">-RedirectConfiguration</span></span>
<span data-ttu-id="d3d2c-135">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d3d2c-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d3d2c-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="d3d2c-137">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3d2c-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d3d2c-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3d2c-138">-RewriteRuleSet</span></span>
<span data-ttu-id="d3d2c-139">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d3d2c-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="d3d2c-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="d3d2c-141">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3d2c-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="d3d2c-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d3d2c-142">-RuleType</span></span>
<span data-ttu-id="d3d2c-143">Anger typen för routningsregler för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="d3d2c-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d3d2c-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="d3d2c-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="d3d2c-145">-UrlPathMapId</span></span>
<span data-ttu-id="d3d2c-146">Anger URL-sökvägen för kart regeln.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="d3d2c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d2c-147">CommonParameters</span></span>
<span data-ttu-id="d3d2c-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d2c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d2c-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3d2c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d2c-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3d2c-150">INPUTS</span></span>

### <span data-ttu-id="d3d2c-151">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3d2c-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3d2c-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3d2c-152">OUTPUTS</span></span>

### <span data-ttu-id="d3d2c-153">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3d2c-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3d2c-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3d2c-154">NOTES</span></span>

## <span data-ttu-id="d3d2c-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3d2c-155">RELATED LINKS</span></span>

[<span data-ttu-id="d3d2c-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3d2c-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d3d2c-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3d2c-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d3d2c-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3d2c-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d3d2c-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3d2c-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


