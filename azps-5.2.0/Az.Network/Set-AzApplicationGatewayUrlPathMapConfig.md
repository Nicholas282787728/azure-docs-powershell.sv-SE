---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417240"
---
# <span data-ttu-id="af9f1-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="af9f1-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="af9f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="af9f1-103">Anger konfiguration för en matris med URL-sökvägar till backend-server.</span><span class="sxs-lookup"><span data-stu-id="af9f1-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="af9f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af9f1-104">SYNTAX</span></span>

### <span data-ttu-id="af9f1-105">BackendSetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="af9f1-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af9f1-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af9f1-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9f1-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="af9f1-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9f1-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af9f1-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af9f1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af9f1-109">DESCRIPTION</span></span>
<span data-ttu-id="af9f1-110">Cmdleten **set-AzApplicationGatewayUrlPathMapConfig** anger konfiguration för en matris med URL-sökvägar till en Server grupp.</span><span class="sxs-lookup"><span data-stu-id="af9f1-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="af9f1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af9f1-111">EXAMPLES</span></span>

### <span data-ttu-id="af9f1-112">Exempel 1: uppdatera en URL-mappsökväg</span><span class="sxs-lookup"><span data-stu-id="af9f1-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="af9f1-113">Med det första kommandot får programgatewayen namnet appGwName och lagras resultatet i $appgw variabel.</span><span class="sxs-lookup"><span data-stu-id="af9f1-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="af9f1-114">Det andra kommandot uppdaterar URL-sökvägen med namnet map01 i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="af9f1-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="af9f1-115">Det tredje kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="af9f1-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="af9f1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af9f1-116">PARAMETERS</span></span>

### <span data-ttu-id="af9f1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af9f1-117">-ApplicationGateway</span></span>
<span data-ttu-id="af9f1-118">Anger den Programgateway till vilken denna cmdlet ställer in en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="af9f1-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="af9f1-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af9f1-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="af9f1-120">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="af9f1-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="af9f1-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="af9f1-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="af9f1-122">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="af9f1-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="af9f1-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="af9f1-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="af9f1-124">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="af9f1-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="af9f1-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="af9f1-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="af9f1-126">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="af9f1-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="af9f1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9f1-127">-DefaultProfile</span></span>
<span data-ttu-id="af9f1-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af9f1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af9f1-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="af9f1-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="af9f1-130">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="af9f1-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="af9f1-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af9f1-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="af9f1-132">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="af9f1-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="af9f1-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af9f1-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="af9f1-134">Standard regel uppsättning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="af9f1-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="af9f1-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="af9f1-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="af9f1-136">ID för Application Gateway standard regel för omskrivning</span><span class="sxs-lookup"><span data-stu-id="af9f1-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="af9f1-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="af9f1-137">-Name</span></span>
<span data-ttu-id="af9f1-138">Anger namnet på den URL-sökväg där cmdlet ställer in konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="af9f1-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="af9f1-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="af9f1-139">-PathRules</span></span>
<span data-ttu-id="af9f1-140">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="af9f1-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="af9f1-141">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="af9f1-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="af9f1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9f1-142">CommonParameters</span></span>
<span data-ttu-id="af9f1-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9f1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9f1-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9f1-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9f1-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af9f1-145">INPUTS</span></span>

### <span data-ttu-id="af9f1-146">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af9f1-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af9f1-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af9f1-147">OUTPUTS</span></span>

### <span data-ttu-id="af9f1-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af9f1-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af9f1-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af9f1-149">NOTES</span></span>

## <span data-ttu-id="af9f1-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af9f1-150">RELATED LINKS</span></span>

[<span data-ttu-id="af9f1-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="af9f1-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="af9f1-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="af9f1-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="af9f1-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="af9f1-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="af9f1-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="af9f1-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


