---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745313"
---
# <span data-ttu-id="19b7f-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="19b7f-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="19b7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="19b7f-103">Skapar en leverans åtgärd.</span><span class="sxs-lookup"><span data-stu-id="19b7f-103">Creates a delivery action.</span></span>

## <span data-ttu-id="19b7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19b7f-104">SYNTAX</span></span>

### <span data-ttu-id="19b7f-105">CacheExpirationActionParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="19b7f-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b7f-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b7f-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b7f-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b7f-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19b7f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19b7f-108">DESCRIPTION</span></span>
<span data-ttu-id="19b7f-109">Cmdleten **New-AzCdnDeliveryRule** skapar en leverans regel för generering av CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="19b7f-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="19b7f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19b7f-110">EXAMPLES</span></span>

### <span data-ttu-id="19b7f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19b7f-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="19b7f-112">Skapa en enkel leverans regel.</span><span class="sxs-lookup"><span data-stu-id="19b7f-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="19b7f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19b7f-113">PARAMETERS</span></span>

### <span data-ttu-id="19b7f-114">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="19b7f-114">-Action</span></span>
<span data-ttu-id="19b7f-115">Åtgärd att utföra.</span><span class="sxs-lookup"><span data-stu-id="19b7f-115">Action to perform.</span></span>

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

### <span data-ttu-id="19b7f-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="19b7f-116">-CacheBehavior</span></span>
<span data-ttu-id="19b7f-117">Cachelagringsalternativ för åtgärden</span><span class="sxs-lookup"><span data-stu-id="19b7f-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="19b7f-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="19b7f-118">-CacheDuration</span></span>
<span data-ttu-id="19b7f-119">Varaktigheten för innehållet.</span><span class="sxs-lookup"><span data-stu-id="19b7f-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="19b7f-120">Tillåtet format är \[ d. \] hh: mm: SS</span><span class="sxs-lookup"><span data-stu-id="19b7f-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="19b7f-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="19b7f-121">-CustomFragment</span></span>
<span data-ttu-id="19b7f-122">Fragment att lägga till i omdirigerings-URL: en.</span><span class="sxs-lookup"><span data-stu-id="19b7f-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="19b7f-123">Fragment är den del av URL-adressen som kommer efter #.</span><span class="sxs-lookup"><span data-stu-id="19b7f-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="19b7f-124">Ta inte med #.</span><span class="sxs-lookup"><span data-stu-id="19b7f-124">Do not include the #.</span></span>

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

### <span data-ttu-id="19b7f-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="19b7f-125">-CustomHostname</span></span>
<span data-ttu-id="19b7f-126">Värd att omdirigera.</span><span class="sxs-lookup"><span data-stu-id="19b7f-126">Host to redirect.</span></span>
<span data-ttu-id="19b7f-127">Lämna tomt om du vill använda den inkommande värden som mål värd.</span><span class="sxs-lookup"><span data-stu-id="19b7f-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="19b7f-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="19b7f-128">-CustomPath</span></span>
<span data-ttu-id="19b7f-129">Den fullständiga sökvägen till omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="19b7f-129">The full path to redirect.</span></span>
<span data-ttu-id="19b7f-130">Sökvägen får inte vara tom och måste börja med/.</span><span class="sxs-lookup"><span data-stu-id="19b7f-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="19b7f-131">Lämna tomt om du vill använda den inkommande sökvägen som mål Sök väg.</span><span class="sxs-lookup"><span data-stu-id="19b7f-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="19b7f-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="19b7f-132">-CustomQueryString</span></span>
<span data-ttu-id="19b7f-133">Den uppsättning frågesträngar som ska placeras i URL-adressen för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="19b7f-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="19b7f-134">Om du anger det här värdet ersätts en befintlig frågesträng. lämna tomt om du vill behålla inkommande frågesträng.</span><span class="sxs-lookup"><span data-stu-id="19b7f-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="19b7f-135">Frågesträngen måste vara i \< ett \> = \< värde \> format.</span><span class="sxs-lookup"><span data-stu-id="19b7f-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="19b7f-136">?</span><span class="sxs-lookup"><span data-stu-id="19b7f-136">?</span></span> <span data-ttu-id="19b7f-137">& läggs till automatiskt, så ta inte med dem.</span><span class="sxs-lookup"><span data-stu-id="19b7f-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="19b7f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b7f-138">-DefaultProfile</span></span>
<span data-ttu-id="19b7f-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19b7f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b7f-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="19b7f-140">-DestinationProtocol</span></span>
<span data-ttu-id="19b7f-141">Protokoll som ska användas för omdirigeringen.</span><span class="sxs-lookup"><span data-stu-id="19b7f-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="19b7f-142">Standardvärdet är MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="19b7f-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="19b7f-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="19b7f-143">-HeaderActionType</span></span>
<span data-ttu-id="19b7f-144">Om sidhuvudet eller svars huvudet för begäran ska ändras</span><span class="sxs-lookup"><span data-stu-id="19b7f-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="19b7f-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="19b7f-145">-HeaderName</span></span>
<span data-ttu-id="19b7f-146">Namn på rubriken som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="19b7f-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="19b7f-147">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="19b7f-147">-RedirectType</span></span>
<span data-ttu-id="19b7f-148">Den omdirigerings typ som används för att omdirigera trafiken</span><span class="sxs-lookup"><span data-stu-id="19b7f-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="19b7f-149">-Värde</span><span class="sxs-lookup"><span data-stu-id="19b7f-149">-Value</span></span>
<span data-ttu-id="19b7f-150">Värde för den angivna åtgärden.</span><span class="sxs-lookup"><span data-stu-id="19b7f-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="19b7f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b7f-151">CommonParameters</span></span>
<span data-ttu-id="19b7f-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b7f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b7f-153">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19b7f-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b7f-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19b7f-154">INPUTS</span></span>

### <span data-ttu-id="19b7f-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="19b7f-155">None</span></span>

## <span data-ttu-id="19b7f-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19b7f-156">OUTPUTS</span></span>

### <span data-ttu-id="19b7f-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="19b7f-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="19b7f-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19b7f-158">NOTES</span></span>

## <span data-ttu-id="19b7f-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19b7f-159">RELATED LINKS</span></span>
