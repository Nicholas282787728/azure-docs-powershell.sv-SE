---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088836"
---
# <span data-ttu-id="25963-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="25963-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="25963-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25963-102">SYNOPSIS</span></span>
<span data-ttu-id="25963-103">Lägger till en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="25963-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="25963-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25963-104">SYNTAX</span></span>

### <span data-ttu-id="25963-105">BackendSetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="25963-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25963-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="25963-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25963-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="25963-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25963-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="25963-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25963-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25963-109">DESCRIPTION</span></span>
<span data-ttu-id="25963-110">Cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** lägger till en matris med URL-sökvägar till en adresspool Server.</span><span class="sxs-lookup"><span data-stu-id="25963-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="25963-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25963-111">EXAMPLES</span></span>

### <span data-ttu-id="25963-112">Exempel 1: lägga till en URL-sökväg till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="25963-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="25963-113">Det första kommandot får en Programgateway som heter appGwName och lagrar den i $appgw variabel.</span><span class="sxs-lookup"><span data-stu-id="25963-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="25963-114">Det andra kommandot får Server delens adresspool och lagrar det i $pool variabel.</span><span class="sxs-lookup"><span data-stu-id="25963-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="25963-115">Det tredje kommandot för in-http-inställningar och lagrar det i $poolSettings variabel.</span><span class="sxs-lookup"><span data-stu-id="25963-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="25963-116">Det fjärde kommandot Skapa en ny Sök vägs regel konfiguration med namnet rule01 och lagrar det i $pathRule variabel.</span><span class="sxs-lookup"><span data-stu-id="25963-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="25963-117">Det femte kommandot lägger till URL-sökväg för mappning med namnet url01 till Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="25963-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="25963-118">Det sjätte kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="25963-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="25963-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25963-119">PARAMETERS</span></span>

### <span data-ttu-id="25963-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25963-120">-ApplicationGateway</span></span>
<span data-ttu-id="25963-121">Anger den Programgateway till vilken denna cmdlet lägger till en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="25963-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="25963-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="25963-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="25963-123">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="25963-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="25963-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="25963-125">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="25963-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="25963-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="25963-127">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="25963-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="25963-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="25963-129">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="25963-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25963-130">-DefaultProfile</span></span>
<span data-ttu-id="25963-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25963-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25963-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="25963-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="25963-133">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="25963-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="25963-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="25963-135">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="25963-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="25963-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="25963-137">Standard regel uppsättning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="25963-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="25963-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="25963-139">ID för Application Gateway standard regel för omskrivning</span><span class="sxs-lookup"><span data-stu-id="25963-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="25963-140">-Name</span></span>
<span data-ttu-id="25963-141">Anger namnet på URL-sökvägen som denna cmdlet lägger till i Server delen.</span><span class="sxs-lookup"><span data-stu-id="25963-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="25963-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="25963-142">-PathRules</span></span>
<span data-ttu-id="25963-143">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="25963-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="25963-144">Sök vägs reglerna är ordnings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="25963-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25963-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25963-145">CommonParameters</span></span>
<span data-ttu-id="25963-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25963-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25963-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25963-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25963-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25963-148">INPUTS</span></span>

### <span data-ttu-id="25963-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25963-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25963-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25963-150">OUTPUTS</span></span>

### <span data-ttu-id="25963-151">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25963-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25963-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25963-152">NOTES</span></span>

## <span data-ttu-id="25963-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25963-153">RELATED LINKS</span></span>

[<span data-ttu-id="25963-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="25963-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="25963-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="25963-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="25963-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="25963-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="25963-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="25963-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


