---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 82ce25cec07855232d627f3ae912b00d4714f104
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091565"
---
# <span data-ttu-id="c14e6-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="c14e6-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="c14e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c14e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c14e6-103">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="c14e6-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c14e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c14e6-104">SYNTAX</span></span>

### <span data-ttu-id="c14e6-105">ByFieldsWithForwardingParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c14e6-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14e6-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14e6-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c14e6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c14e6-107">DESCRIPTION</span></span>
<span data-ttu-id="c14e6-108">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="c14e6-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c14e6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c14e6-109">EXAMPLES</span></span>

### <span data-ttu-id="c14e6-110">Exempel 1: skapa en PSRoutingRuleObject för skapande av en lucka med en vidarebefordrings regel</span><span class="sxs-lookup"><span data-stu-id="c14e6-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="c14e6-111">Exempel 2: skapa en PSRoutingRuleObject för skapande av en lucka med en regler för omdirigering</span><span class="sxs-lookup"><span data-stu-id="c14e6-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="c14e6-112">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="c14e6-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c14e6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c14e6-113">PARAMETERS</span></span>

### <span data-ttu-id="c14e6-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="c14e6-114">-AcceptedProtocol</span></span>
<span data-ttu-id="c14e6-115">Protokoll scheman som ska matchas för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="c14e6-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="c14e6-116">Standardvärdet är {https, http}</span><span class="sxs-lookup"><span data-stu-id="c14e6-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="c14e6-117">-BackendPoolName</span></span>
<span data-ttu-id="c14e6-118">Resurs-ID för den BackendPool som den här regeln dirigerar till</span><span class="sxs-lookup"><span data-stu-id="c14e6-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="c14e6-119">-CustomForwardingPath</span></span>
<span data-ttu-id="c14e6-120">Den anpassade sökvägen som används för att ändra resurs Sök vägar som matchas med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="c14e6-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="c14e6-121">Lämna tomt om du vill använda inkommande sökväg.</span><span class="sxs-lookup"><span data-stu-id="c14e6-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="c14e6-122">-CustomFragment</span></span>
<span data-ttu-id="c14e6-123">Fragment att lägga till i omdirigerings-URL: en.</span><span class="sxs-lookup"><span data-stu-id="c14e6-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="c14e6-124">Fragment är den del av URL-adressen som kommer efter #.</span><span class="sxs-lookup"><span data-stu-id="c14e6-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="c14e6-125">Ta inte med #.</span><span class="sxs-lookup"><span data-stu-id="c14e6-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="c14e6-126">-CustomHost</span></span>
<span data-ttu-id="c14e6-127">Värd att omdirigera.</span><span class="sxs-lookup"><span data-stu-id="c14e6-127">Host to redirect.</span></span> <span data-ttu-id="c14e6-128">Lämna tomt om du vill använda den inkommande värden som mål värd.</span><span class="sxs-lookup"><span data-stu-id="c14e6-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="c14e6-129">-CustomPath</span></span>
<span data-ttu-id="c14e6-130">Den fullständiga sökvägen till omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="c14e6-130">The full path to redirect.</span></span> <span data-ttu-id="c14e6-131">Sökvägen får inte vara tom och måste börja med/.</span><span class="sxs-lookup"><span data-stu-id="c14e6-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="c14e6-132">Lämna tomt om du vill använda den inkommande sökvägen som mål Sök väg.</span><span class="sxs-lookup"><span data-stu-id="c14e6-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="c14e6-133">-CustomQueryString</span></span>
<span data-ttu-id="c14e6-134">Den uppsättning frågesträngar som ska placeras i URL-adressen för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="c14e6-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="c14e6-135">Om du anger det här värdet ersätts en befintlig frågesträng. lämna tomt om du vill behålla inkommande frågesträng.</span><span class="sxs-lookup"><span data-stu-id="c14e6-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="c14e6-136">Frågesträngen måste vara i <key>=</span><span class="sxs-lookup"><span data-stu-id="c14e6-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="c14e6-137">format.</span><span class="sxs-lookup"><span data-stu-id="c14e6-137">format.</span></span> <span data-ttu-id="c14e6-138">Den första?</span><span class="sxs-lookup"><span data-stu-id="c14e6-138">The first ?</span></span> <span data-ttu-id="c14e6-139">& läggs till automatiskt, så ta inte med dem på fram sidan, men dela upp flera frågesträngar med &.</span><span class="sxs-lookup"><span data-stu-id="c14e6-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14e6-140">-DefaultProfile</span></span>
<span data-ttu-id="c14e6-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c14e6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14e6-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="c14e6-142">-DynamicCompression</span></span>
<span data-ttu-id="c14e6-143">Om du vill aktivera dynamisk komprimering för cachelagrat innehåll när cachelagring är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="c14e6-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="c14e6-144">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="c14e6-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="c14e6-145">-EnableCaching</span></span>
<span data-ttu-id="c14e6-146">Om cachelagring ska aktive ras för den här vägen.</span><span class="sxs-lookup"><span data-stu-id="c14e6-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="c14e6-147">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="c14e6-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c14e6-148">-EnabledState</span></span>
<span data-ttu-id="c14e6-149">Om användning av den här regeln ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="c14e6-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="c14e6-150">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="c14e6-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="c14e6-151">-ForwardingProtocol</span></span>
<span data-ttu-id="c14e6-152">Protokollet som används för att vidarebefordra trafik till standardvärdet för MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="c14e6-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c14e6-153">-FrontDoorName</span></span>
<span data-ttu-id="c14e6-154">Namnet på den främre dörren som den här regeln tillhör.</span><span class="sxs-lookup"><span data-stu-id="c14e6-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="c14e6-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="c14e6-155">-FrontendEndpointName</span></span>
<span data-ttu-id="c14e6-156">Namnen på slut punkter för klient delen som är associerade med den här regeln</span><span class="sxs-lookup"><span data-stu-id="c14e6-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="c14e6-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="c14e6-157">-Name</span></span>
<span data-ttu-id="c14e6-158">RoutingRule namn.</span><span class="sxs-lookup"><span data-stu-id="c14e6-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="c14e6-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="c14e6-159">-PatternToMatch</span></span>
<span data-ttu-id="c14e6-160">Linjens flödes mönster får inte ha några \* förutom den sista/efter slutet av sökvägen.</span><span class="sxs-lookup"><span data-stu-id="c14e6-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="c14e6-161">Standardvärdet är/\*</span><span class="sxs-lookup"><span data-stu-id="c14e6-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="c14e6-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="c14e6-163">Behandlingen av URL-frågor när du skapar cache-tangenten.</span><span class="sxs-lookup"><span data-stu-id="c14e6-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="c14e6-164">Standardvärdet är StripAll</span><span class="sxs-lookup"><span data-stu-id="c14e6-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="c14e6-165">-RedirectProtocol</span></span>
<span data-ttu-id="c14e6-166">Protokollet för mål platsen där trafiken omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="c14e6-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="c14e6-167">Standardvärdet är MatchRequest</span><span class="sxs-lookup"><span data-stu-id="c14e6-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="c14e6-168">-RedirectType</span></span>
<span data-ttu-id="c14e6-169">Omdirigerings typ regeln används vid omdirigering av trafik.</span><span class="sxs-lookup"><span data-stu-id="c14e6-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="c14e6-170">Standardvärdet flyttas</span><span class="sxs-lookup"><span data-stu-id="c14e6-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e6-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14e6-171">-ResourceGroupName</span></span>
<span data-ttu-id="c14e6-172">Namnet på resurs gruppen som RoutingRule skapas i.</span><span class="sxs-lookup"><span data-stu-id="c14e6-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="c14e6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14e6-173">CommonParameters</span></span>
<span data-ttu-id="c14e6-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14e6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14e6-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c14e6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14e6-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c14e6-176">INPUTS</span></span>

### <span data-ttu-id="c14e6-177">Ingen</span><span class="sxs-lookup"><span data-stu-id="c14e6-177">None</span></span>

## <span data-ttu-id="c14e6-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c14e6-178">OUTPUTS</span></span>

### <span data-ttu-id="c14e6-179">Microsoft. Azure. commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c14e6-179">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="c14e6-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c14e6-180">NOTES</span></span>

## <span data-ttu-id="c14e6-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c14e6-181">RELATED LINKS</span></span>

<span data-ttu-id="c14e6-182">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="c14e6-182">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
