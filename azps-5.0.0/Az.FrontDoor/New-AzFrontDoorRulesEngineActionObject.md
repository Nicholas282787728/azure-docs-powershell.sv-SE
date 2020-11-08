---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270642"
---
# <span data-ttu-id="65c20-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="65c20-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="65c20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65c20-102">SYNOPSIS</span></span>
<span data-ttu-id="65c20-103">Skapa ett PSRulesEngineAction-objekt för att skapa en regel för regel motor.</span><span class="sxs-lookup"><span data-stu-id="65c20-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="65c20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65c20-104">SYNTAX</span></span>

### <span data-ttu-id="65c20-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="65c20-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65c20-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65c20-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65c20-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65c20-107">DESCRIPTION</span></span>
<span data-ttu-id="65c20-108">Skapa ett PSRulesEngineAction-objekt för att skapa en regel för regel motor.</span><span class="sxs-lookup"><span data-stu-id="65c20-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="65c20-109">Använd cmdlet "New-AzFrontDoorHeaderActionObject" för att skapa PSHeaderObjects till parametrarna "-RequestHeaderActions" och "-ResponseHeaderActions".</span><span class="sxs-lookup"><span data-stu-id="65c20-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="65c20-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65c20-110">EXAMPLES</span></span>

### <span data-ttu-id="65c20-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="65c20-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="65c20-112">Skapa en regel motor åtgärd och visa hur du visar egenskaperna för regel åtgärds åtgärden skapad.</span><span class="sxs-lookup"><span data-stu-id="65c20-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="65c20-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65c20-113">PARAMETERS</span></span>

### <span data-ttu-id="65c20-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="65c20-114">-BackendPoolName</span></span>
<span data-ttu-id="65c20-115">Namnet på den BackendPool som den här regeln dirigerar till</span><span class="sxs-lookup"><span data-stu-id="65c20-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="65c20-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="65c20-116">-CustomForwardingPath</span></span>
<span data-ttu-id="65c20-117">Den anpassade sökvägen som används för att ändra resurs Sök vägar som matchas med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="65c20-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="65c20-118">Lämna tomt om du vill använda inkommande sökväg.</span><span class="sxs-lookup"><span data-stu-id="65c20-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="65c20-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="65c20-119">-CustomFragment</span></span>
<span data-ttu-id="65c20-120">Fragment att lägga till i omdirigerings-URL: en.</span><span class="sxs-lookup"><span data-stu-id="65c20-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="65c20-121">Fragment är den del av URL-adressen som kommer efter #.</span><span class="sxs-lookup"><span data-stu-id="65c20-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="65c20-122">Ta inte med #.</span><span class="sxs-lookup"><span data-stu-id="65c20-122">Do not include the #.</span></span>

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

### <span data-ttu-id="65c20-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="65c20-123">-CustomHost</span></span>
<span data-ttu-id="65c20-124">Värd att omdirigera.</span><span class="sxs-lookup"><span data-stu-id="65c20-124">Host to redirect.</span></span>
<span data-ttu-id="65c20-125">Lämna tomt om du vill använda den inkommande värden som mål värd.</span><span class="sxs-lookup"><span data-stu-id="65c20-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="65c20-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="65c20-126">-CustomPath</span></span>
<span data-ttu-id="65c20-127">Den fullständiga sökvägen till omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="65c20-127">The full path to redirect.</span></span>
<span data-ttu-id="65c20-128">Sökvägen får inte vara tom och måste börja med/.</span><span class="sxs-lookup"><span data-stu-id="65c20-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="65c20-129">Lämna tomt om du vill använda den inkommande sökvägen som mål Sök väg.</span><span class="sxs-lookup"><span data-stu-id="65c20-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="65c20-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="65c20-130">-CustomQueryString</span></span>
<span data-ttu-id="65c20-131">Den uppsättning frågesträngar som ska placeras i URL-adressen för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="65c20-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="65c20-132">Om du anger det här värdet ersätts en befintlig frågesträng. lämna tomt om du vill behålla inkommande frågesträng.</span><span class="sxs-lookup"><span data-stu-id="65c20-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="65c20-133">Frågesträngen måste vara i \<key\> = \<value\> formatet.</span><span class="sxs-lookup"><span data-stu-id="65c20-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="65c20-134">Den första?</span><span class="sxs-lookup"><span data-stu-id="65c20-134">The first ?</span></span>
<span data-ttu-id="65c20-135">& läggs till automatiskt, så ta inte med dem på fram sidan, men dela upp flera frågesträngar med &.</span><span class="sxs-lookup"><span data-stu-id="65c20-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="65c20-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c20-136">-DefaultProfile</span></span>
<span data-ttu-id="65c20-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65c20-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65c20-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="65c20-138">-DynamicCompression</span></span>
<span data-ttu-id="65c20-139">Om du vill aktivera dynamisk komprimering för cachelagrat innehåll.</span><span class="sxs-lookup"><span data-stu-id="65c20-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="65c20-140">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="65c20-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="65c20-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="65c20-141">-EnableCaching</span></span>
<span data-ttu-id="65c20-142">Om cachelagring ska aktive ras för den här vägen.</span><span class="sxs-lookup"><span data-stu-id="65c20-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="65c20-143">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="65c20-143">Default value is false</span></span>

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

### <span data-ttu-id="65c20-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="65c20-144">-ForwardingProtocol</span></span>
<span data-ttu-id="65c20-145">Protokollet som den här regeln ska använda när trafik vidarebefordras till bakände.</span><span class="sxs-lookup"><span data-stu-id="65c20-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="65c20-146">Standardvärdet är MatchRequest</span><span class="sxs-lookup"><span data-stu-id="65c20-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="65c20-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="65c20-147">-FrontDoorName</span></span>
<span data-ttu-id="65c20-148">Namnet på den främre dörren som den här regeln tillhör.</span><span class="sxs-lookup"><span data-stu-id="65c20-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="65c20-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="65c20-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="65c20-150">Behandlingen av URL-frågor när du skapar cache-tangenten.</span><span class="sxs-lookup"><span data-stu-id="65c20-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="65c20-151">Standardvärdet är StripAll</span><span class="sxs-lookup"><span data-stu-id="65c20-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="65c20-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="65c20-152">-RedirectProtocol</span></span>
<span data-ttu-id="65c20-153">Protokollet för mål platsen där trafiken omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="65c20-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="65c20-154">Standardvärdet är MatchRequest</span><span class="sxs-lookup"><span data-stu-id="65c20-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="65c20-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="65c20-155">-RedirectType</span></span>
<span data-ttu-id="65c20-156">Omdirigerings typ regeln används vid omdirigering av trafik.</span><span class="sxs-lookup"><span data-stu-id="65c20-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="65c20-157">Standardvärdet flyttas</span><span class="sxs-lookup"><span data-stu-id="65c20-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="65c20-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="65c20-158">-RequestHeaderAction</span></span>
<span data-ttu-id="65c20-159">En lista med rubrik åtgärder som ska utföras från AFD till ursprunget.</span><span class="sxs-lookup"><span data-stu-id="65c20-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c20-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c20-160">-ResourceGroupName</span></span>
<span data-ttu-id="65c20-161">Namnet på resurs gruppen som RoutingRule skapas i.</span><span class="sxs-lookup"><span data-stu-id="65c20-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="65c20-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="65c20-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="65c20-163">En lista med rubrik åtgärder som ska gälla från svaret från AFD till klienten.</span><span class="sxs-lookup"><span data-stu-id="65c20-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c20-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c20-164">CommonParameters</span></span>
<span data-ttu-id="65c20-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c20-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c20-166">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65c20-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c20-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65c20-167">INPUTS</span></span>

### <span data-ttu-id="65c20-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="65c20-168">None</span></span>

## <span data-ttu-id="65c20-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65c20-169">OUTPUTS</span></span>

### <span data-ttu-id="65c20-170">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="65c20-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="65c20-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65c20-171">NOTES</span></span>

## <span data-ttu-id="65c20-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65c20-172">RELATED LINKS</span></span>
