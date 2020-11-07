---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916714"
---
# <span data-ttu-id="a93ed-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="a93ed-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="a93ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a93ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a93ed-103">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="a93ed-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="a93ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a93ed-104">SYNTAX</span></span>

### <span data-ttu-id="a93ed-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="a93ed-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a93ed-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a93ed-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a93ed-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a93ed-107">DESCRIPTION</span></span>
<span data-ttu-id="a93ed-108">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="a93ed-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="a93ed-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a93ed-109">EXAMPLES</span></span>

### <span data-ttu-id="a93ed-110">Exempel 1: skapa en PSRoutingRuleObject för skapande av en lucka</span><span class="sxs-lookup"><span data-stu-id="a93ed-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="a93ed-111">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="a93ed-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="a93ed-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a93ed-112">PARAMETERS</span></span>

### <span data-ttu-id="a93ed-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="a93ed-113">-AcceptedProtocol</span></span>
<span data-ttu-id="a93ed-114">Protokoll scheman som ska matchas för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="a93ed-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="a93ed-115">Standardvärdet är {https, http}</span><span class="sxs-lookup"><span data-stu-id="a93ed-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="a93ed-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="a93ed-116">-BackendPoolName</span></span>
<span data-ttu-id="a93ed-117">Resurs-ID för den BackendPool som den här regeln dirigerar till</span><span class="sxs-lookup"><span data-stu-id="a93ed-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="a93ed-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="a93ed-118">-CustomForwardingPath</span></span>
<span data-ttu-id="a93ed-119">Den anpassade sökvägen som används för att ändra resurs Sök vägar som matchas med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="a93ed-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="a93ed-120">Lämna tomt om du vill använda inkommande sökväg.</span><span class="sxs-lookup"><span data-stu-id="a93ed-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="a93ed-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="a93ed-121">-CustomFragment</span></span>
<span data-ttu-id="a93ed-122">Fragment att lägga till i omdirigerings-URL: en.</span><span class="sxs-lookup"><span data-stu-id="a93ed-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="a93ed-123">Fragment är den del av URL-adressen som kommer efter #.</span><span class="sxs-lookup"><span data-stu-id="a93ed-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="a93ed-124">Ta inte med #.</span><span class="sxs-lookup"><span data-stu-id="a93ed-124">Do not include the #.</span></span>

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

### <span data-ttu-id="a93ed-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="a93ed-125">-CustomHost</span></span>
<span data-ttu-id="a93ed-126">Värd att omdirigera.</span><span class="sxs-lookup"><span data-stu-id="a93ed-126">Host to redirect.</span></span> <span data-ttu-id="a93ed-127">Lämna tomt om du vill använda den inkommande värden som mål värd.</span><span class="sxs-lookup"><span data-stu-id="a93ed-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="a93ed-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="a93ed-128">-CustomPath</span></span>
<span data-ttu-id="a93ed-129">Den fullständiga sökvägen till omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="a93ed-129">The full path to redirect.</span></span> <span data-ttu-id="a93ed-130">Sökvägen får inte vara tom och måste börja med/.</span><span class="sxs-lookup"><span data-stu-id="a93ed-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="a93ed-131">Lämna tomt om du vill använda den inkommande sökvägen som mål Sök väg.</span><span class="sxs-lookup"><span data-stu-id="a93ed-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="a93ed-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="a93ed-132">-CustomQueryString</span></span>
<span data-ttu-id="a93ed-133">Den uppsättning frågesträngar som ska placeras i URL-adressen för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="a93ed-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="a93ed-134">Om du anger det här värdet ersätts en befintlig frågesträng. lämna tomt om du vill behålla inkommande frågesträng.</span><span class="sxs-lookup"><span data-stu-id="a93ed-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="a93ed-135">Frågesträngen måste vara i <key>=</span><span class="sxs-lookup"><span data-stu-id="a93ed-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="a93ed-136">format.</span><span class="sxs-lookup"><span data-stu-id="a93ed-136">format.</span></span> <span data-ttu-id="a93ed-137">Den första?</span><span class="sxs-lookup"><span data-stu-id="a93ed-137">The first ?</span></span> <span data-ttu-id="a93ed-138">& läggs till automatiskt, så ta inte med dem på fram sidan, men dela upp flera frågesträngar med &.</span><span class="sxs-lookup"><span data-stu-id="a93ed-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="a93ed-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93ed-139">-DefaultProfile</span></span>
<span data-ttu-id="a93ed-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a93ed-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93ed-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="a93ed-141">-DynamicCompression</span></span>
<span data-ttu-id="a93ed-142">Om du vill aktivera dynamisk komprimering för cachelagrat innehåll när cachelagring är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="a93ed-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="a93ed-143">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="a93ed-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="a93ed-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="a93ed-144">-EnableCaching</span></span>
<span data-ttu-id="a93ed-145">Om cachelagring ska aktive ras för den här vägen.</span><span class="sxs-lookup"><span data-stu-id="a93ed-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="a93ed-146">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="a93ed-146">Default value is false</span></span>

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

### <span data-ttu-id="a93ed-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="a93ed-147">-EnabledState</span></span>
<span data-ttu-id="a93ed-148">Om användning av den här regeln ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="a93ed-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="a93ed-149">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="a93ed-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="a93ed-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="a93ed-150">-ForwardingProtocol</span></span>
<span data-ttu-id="a93ed-151">Protokollet som används för att vidarebefordra trafik till standardvärdet för MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="a93ed-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ed-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a93ed-152">-FrontDoorName</span></span>
<span data-ttu-id="a93ed-153">Namnet på den främre dörren som den här regeln tillhör.</span><span class="sxs-lookup"><span data-stu-id="a93ed-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="a93ed-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="a93ed-154">-FrontendEndpointName</span></span>
<span data-ttu-id="a93ed-155">Namnen på slut punkter för klient delen som är associerade med den här regeln</span><span class="sxs-lookup"><span data-stu-id="a93ed-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="a93ed-156">-Namn</span><span class="sxs-lookup"><span data-stu-id="a93ed-156">-Name</span></span>
<span data-ttu-id="a93ed-157">RoutingRule namn.</span><span class="sxs-lookup"><span data-stu-id="a93ed-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="a93ed-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="a93ed-158">-PatternToMatch</span></span>
<span data-ttu-id="a93ed-159">Linjens flödes mönster får inte ha några \* förutom den sista/efter slutet av sökvägen.</span><span class="sxs-lookup"><span data-stu-id="a93ed-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="a93ed-160">Standardvärdet är/\*</span><span class="sxs-lookup"><span data-stu-id="a93ed-160">Default value is /\*</span></span>

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

### <span data-ttu-id="a93ed-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="a93ed-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="a93ed-162">Behandlingen av URL-frågor när du skapar cache-tangenten.</span><span class="sxs-lookup"><span data-stu-id="a93ed-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="a93ed-163">Standardvärdet är StripAll</span><span class="sxs-lookup"><span data-stu-id="a93ed-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ed-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="a93ed-164">-RedirectProtocol</span></span>
<span data-ttu-id="a93ed-165">Protokollet för mål platsen där trafiken omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="a93ed-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="a93ed-166">Standardvärdet är MatchRequest</span><span class="sxs-lookup"><span data-stu-id="a93ed-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ed-167">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="a93ed-167">-RedirectType</span></span>
<span data-ttu-id="a93ed-168">Omdirigerings typ regeln används vid omdirigering av trafik.</span><span class="sxs-lookup"><span data-stu-id="a93ed-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="a93ed-169">Standardvärdet flyttas</span><span class="sxs-lookup"><span data-stu-id="a93ed-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ed-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93ed-170">-ResourceGroupName</span></span>
<span data-ttu-id="a93ed-171">Namnet på resurs gruppen som RoutingRule skapas i.</span><span class="sxs-lookup"><span data-stu-id="a93ed-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="a93ed-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93ed-172">CommonParameters</span></span>
<span data-ttu-id="a93ed-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93ed-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93ed-174">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a93ed-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93ed-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a93ed-175">INPUTS</span></span>

### <span data-ttu-id="a93ed-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="a93ed-176">None</span></span>

## <span data-ttu-id="a93ed-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a93ed-177">OUTPUTS</span></span>

### <span data-ttu-id="a93ed-178">Microsoft. Azure. commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a93ed-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="a93ed-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a93ed-179">NOTES</span></span>

## <span data-ttu-id="a93ed-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a93ed-180">RELATED LINKS</span></span>

<span data-ttu-id="a93ed-181">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a93ed-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
