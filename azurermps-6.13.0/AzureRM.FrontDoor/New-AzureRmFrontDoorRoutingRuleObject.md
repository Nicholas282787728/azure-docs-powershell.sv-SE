---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580079"
---
# <span data-ttu-id="f6b11-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="f6b11-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="f6b11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6b11-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b11-103">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="f6b11-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6b11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6b11-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6b11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6b11-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b11-106">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="f6b11-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="f6b11-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6b11-107">EXAMPLES</span></span>

### <span data-ttu-id="f6b11-108">Exempel 1: skapa en PSRoutingRuleObject för skapande av en lucka</span><span class="sxs-lookup"><span data-stu-id="f6b11-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

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

<span data-ttu-id="f6b11-109">Skapa en PSRoutingRuleObject för skapande av front dörrar</span><span class="sxs-lookup"><span data-stu-id="f6b11-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="f6b11-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6b11-110">PARAMETERS</span></span>

### <span data-ttu-id="f6b11-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="f6b11-111">-AcceptedProtocol</span></span>
<span data-ttu-id="f6b11-112">Protokoll scheman som ska matchas för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="f6b11-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="f6b11-113">Standardvärdet är {https, http}</span><span class="sxs-lookup"><span data-stu-id="f6b11-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="f6b11-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="f6b11-114">-BackendPoolName</span></span>
<span data-ttu-id="f6b11-115">Resurs-ID för den BackendPool som den här regeln dirigerar till</span><span class="sxs-lookup"><span data-stu-id="f6b11-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="f6b11-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="f6b11-116">-CustomForwardingPath</span></span>
<span data-ttu-id="f6b11-117">Den anpassade sökvägen som används för att ändra resurs Sök vägar som matchas med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="f6b11-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="f6b11-118">Lämna tomt om du vill använda inkommande sökväg.</span><span class="sxs-lookup"><span data-stu-id="f6b11-118">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b11-119">-DefaultProfile</span></span>
<span data-ttu-id="f6b11-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6b11-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="f6b11-121">-DynamicCompression</span></span>
<span data-ttu-id="f6b11-122">Om du vill aktivera dynamisk komprimering för cachelagrat innehåll när cachelagring är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="f6b11-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="f6b11-123">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="f6b11-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="f6b11-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="f6b11-124">-EnableCaching</span></span>
<span data-ttu-id="f6b11-125">Om cachelagring ska aktive ras för den här vägen.</span><span class="sxs-lookup"><span data-stu-id="f6b11-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="f6b11-126">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="f6b11-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b11-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f6b11-127">-EnabledState</span></span>
<span data-ttu-id="f6b11-128">Om användning av den här regeln ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="f6b11-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="f6b11-129">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="f6b11-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="f6b11-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="f6b11-130">-ForwardingProtocol</span></span>
<span data-ttu-id="f6b11-131">Protokollet som används för att vidarebefordra trafik till standardvärdet för MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="f6b11-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b11-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="f6b11-132">-FrontDoorName</span></span>
<span data-ttu-id="f6b11-133">Namnet på den främre dörren som den här regeln tillhör.</span><span class="sxs-lookup"><span data-stu-id="f6b11-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="f6b11-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="f6b11-134">-FrontendEndpointName</span></span>
<span data-ttu-id="f6b11-135">Namnen på slut punkter för klient delen som är associerade med den här regeln</span><span class="sxs-lookup"><span data-stu-id="f6b11-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="f6b11-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6b11-136">-Name</span></span>
<span data-ttu-id="f6b11-137">RoutingRule namn.</span><span class="sxs-lookup"><span data-stu-id="f6b11-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="f6b11-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="f6b11-138">-PatternToMatch</span></span>
<span data-ttu-id="f6b11-139">Linjens flödes mönster får inte ha några \* förutom den sista/efter slutet av sökvägen.</span><span class="sxs-lookup"><span data-stu-id="f6b11-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="f6b11-140">Standardvärdet är/\*</span><span class="sxs-lookup"><span data-stu-id="f6b11-140">Default value is /\*</span></span>

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

### <span data-ttu-id="f6b11-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="f6b11-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="f6b11-142">Behandlingen av URL-frågor när du skapar cache-tangenten.</span><span class="sxs-lookup"><span data-stu-id="f6b11-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="f6b11-143">Standardvärdet är StripAll</span><span class="sxs-lookup"><span data-stu-id="f6b11-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b11-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b11-144">-ResourceGroupName</span></span>
<span data-ttu-id="f6b11-145">Namnet på resurs gruppen som RoutingRule skapas i.</span><span class="sxs-lookup"><span data-stu-id="f6b11-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="f6b11-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b11-146">CommonParameters</span></span>
<span data-ttu-id="f6b11-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b11-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b11-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b11-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b11-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6b11-149">INPUTS</span></span>

### <span data-ttu-id="f6b11-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6b11-150">None</span></span>

## <span data-ttu-id="f6b11-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6b11-151">OUTPUTS</span></span>

### <span data-ttu-id="f6b11-152">Microsoft. Azure. commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f6b11-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="f6b11-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6b11-153">NOTES</span></span>

## <span data-ttu-id="f6b11-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6b11-154">RELATED LINKS</span></span>

<span data-ttu-id="f6b11-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f6b11-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
