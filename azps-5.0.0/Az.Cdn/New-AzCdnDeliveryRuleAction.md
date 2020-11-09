---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322259"
---
# <span data-ttu-id="b055e-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="b055e-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="b055e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b055e-102">SYNOPSIS</span></span>
<span data-ttu-id="b055e-103">Skapar en leverans åtgärd.</span><span class="sxs-lookup"><span data-stu-id="b055e-103">Creates a delivery action.</span></span>

## <span data-ttu-id="b055e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b055e-104">SYNTAX</span></span>

### <span data-ttu-id="b055e-105">CacheExpirationActionParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b055e-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b055e-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b055e-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b055e-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b055e-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b055e-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b055e-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b055e-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b055e-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b055e-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b055e-110">DESCRIPTION</span></span>
<span data-ttu-id="b055e-111">Cmdleten **New-AzCdnDeliveryRule** skapar en leverans regel för generering av CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="b055e-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="b055e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b055e-112">EXAMPLES</span></span>

### <span data-ttu-id="b055e-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b055e-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="b055e-114">Skapa en enkel leverans regel.</span><span class="sxs-lookup"><span data-stu-id="b055e-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="b055e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b055e-115">PARAMETERS</span></span>

### <span data-ttu-id="b055e-116">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="b055e-116">-Action</span></span>
<span data-ttu-id="b055e-117">Åtgärd att utföra.</span><span class="sxs-lookup"><span data-stu-id="b055e-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="b055e-118">-CacheBehavior</span></span>
<span data-ttu-id="b055e-119">Cachelagringsalternativ för åtgärden</span><span class="sxs-lookup"><span data-stu-id="b055e-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="b055e-120">-CacheDuration</span></span>
<span data-ttu-id="b055e-121">Varaktigheten för innehållet.</span><span class="sxs-lookup"><span data-stu-id="b055e-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="b055e-122">Tillåtet format är \[ d. \] hh: mm: SS</span><span class="sxs-lookup"><span data-stu-id="b055e-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="b055e-123">-CustomFragment</span></span>
<span data-ttu-id="b055e-124">Fragment att lägga till i omdirigerings-URL: en.</span><span class="sxs-lookup"><span data-stu-id="b055e-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="b055e-125">Fragment är den del av URL-adressen som kommer efter #.</span><span class="sxs-lookup"><span data-stu-id="b055e-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="b055e-126">Ta inte med #.</span><span class="sxs-lookup"><span data-stu-id="b055e-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="b055e-127">-CustomHostname</span></span>
<span data-ttu-id="b055e-128">Värd att omdirigera.</span><span class="sxs-lookup"><span data-stu-id="b055e-128">Host to redirect.</span></span>
<span data-ttu-id="b055e-129">Lämna tomt om du vill använda den inkommande värden som mål värd.</span><span class="sxs-lookup"><span data-stu-id="b055e-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="b055e-130">-CustomPath</span></span>
<span data-ttu-id="b055e-131">Den fullständiga sökvägen till omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="b055e-131">The full path to redirect.</span></span>
<span data-ttu-id="b055e-132">Sökvägen får inte vara tom och måste börja med/.</span><span class="sxs-lookup"><span data-stu-id="b055e-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="b055e-133">Lämna tomt om du vill använda den inkommande sökvägen som mål Sök väg.</span><span class="sxs-lookup"><span data-stu-id="b055e-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="b055e-134">-CustomQueryString</span></span>
<span data-ttu-id="b055e-135">Den uppsättning frågesträngar som ska placeras i URL-adressen för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="b055e-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="b055e-136">Om du anger det här värdet ersätts en befintlig frågesträng. lämna tomt om du vill behålla inkommande frågesträng.</span><span class="sxs-lookup"><span data-stu-id="b055e-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="b055e-137">Frågesträngen måste vara i \<key\> = \<value\> formatet.</span><span class="sxs-lookup"><span data-stu-id="b055e-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="b055e-138">?</span><span class="sxs-lookup"><span data-stu-id="b055e-138">?</span></span> <span data-ttu-id="b055e-139">& läggs till automatiskt, så ta inte med dem.</span><span class="sxs-lookup"><span data-stu-id="b055e-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b055e-140">-DefaultProfile</span></span>
<span data-ttu-id="b055e-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b055e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b055e-142">-Mål</span><span class="sxs-lookup"><span data-stu-id="b055e-142">-Destination</span></span>
<span data-ttu-id="b055e-143">Definiera den relativa URL-adressen som de ovanstående begäranden kommer att återskrivas av.</span><span class="sxs-lookup"><span data-stu-id="b055e-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="b055e-144">-DestinationProtocol</span></span>
<span data-ttu-id="b055e-145">Protokoll som ska användas för omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="b055e-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="b055e-146">Standardvärdet är MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="b055e-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="b055e-147">-HeaderActionType</span></span>
<span data-ttu-id="b055e-148">Om sidhuvudet eller svars huvudet för begäran ska ändras</span><span class="sxs-lookup"><span data-stu-id="b055e-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="b055e-149">-HeaderName</span></span>
<span data-ttu-id="b055e-150">Namn på rubriken som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="b055e-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="b055e-151">-PreservePath</span></span>
<span data-ttu-id="b055e-152">Om omatchad sökväg ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="b055e-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="b055e-153">-QueryParameter</span></span>
<span data-ttu-id="b055e-154">Frågeparametrar som ska inkluderas eller exkluderas (kommaavgränsad).</span><span class="sxs-lookup"><span data-stu-id="b055e-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="b055e-155">-QueryStringBehavior</span></span>
<span data-ttu-id="b055e-156">QueryString-beteende för begär Anden</span><span class="sxs-lookup"><span data-stu-id="b055e-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b055e-157">-RedirectType</span></span>
<span data-ttu-id="b055e-158">Den omdirigerings typ som används för att omdirigera trafiken</span><span class="sxs-lookup"><span data-stu-id="b055e-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="b055e-159">-SourcePattern</span></span>
<span data-ttu-id="b055e-160">Definiera ett URI-mönster för begärande som identifierar typen av begär Anden som kan skrivas över.</span><span class="sxs-lookup"><span data-stu-id="b055e-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="b055e-161">Om värde är tomt matchas alla strängar.</span><span class="sxs-lookup"><span data-stu-id="b055e-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-162">-Värde</span><span class="sxs-lookup"><span data-stu-id="b055e-162">-Value</span></span>
<span data-ttu-id="b055e-163">Värde för den angivna åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b055e-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b055e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b055e-164">CommonParameters</span></span>
<span data-ttu-id="b055e-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b055e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b055e-166">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b055e-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b055e-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b055e-167">INPUTS</span></span>

### <span data-ttu-id="b055e-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="b055e-168">None</span></span>

## <span data-ttu-id="b055e-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b055e-169">OUTPUTS</span></span>

### <span data-ttu-id="b055e-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="b055e-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="b055e-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b055e-171">NOTES</span></span>

## <span data-ttu-id="b055e-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b055e-172">RELATED LINKS</span></span>
