---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: ba06dcabe874161c9f801841a5be8b0337614799
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090571"
---
# <span data-ttu-id="c8643-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="c8643-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8643-102">SYNOPSIS</span></span>
<span data-ttu-id="c8643-103">Skapar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="c8643-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="c8643-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8643-104">SYNTAX</span></span>

### <span data-ttu-id="c8643-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c8643-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8643-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8643-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8643-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8643-107">DESCRIPTION</span></span>
<span data-ttu-id="c8643-108">Cmdleten **New-AzCdnEndpoint** skapar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="c8643-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c8643-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8643-109">EXAMPLES</span></span>

## <span data-ttu-id="c8643-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8643-110">PARAMETERS</span></span>

### <span data-ttu-id="c8643-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8643-111">-CdnProfile</span></span>
<span data-ttu-id="c8643-112">Anger det CDN-profil objekt dit slut punkten läggs till.</span><span class="sxs-lookup"><span data-stu-id="c8643-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="c8643-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="c8643-114">Anger en matris med innehålls typer som ska komprimeras från noden Edge till klienten.</span><span class="sxs-lookup"><span data-stu-id="c8643-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="c8643-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8643-115">-DefaultProfile</span></span>
<span data-ttu-id="c8643-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8643-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8643-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="c8643-117">-DeliveryPolicy</span></span>
<span data-ttu-id="c8643-118">Leverans princip för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c8643-118">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c8643-119">-EndpointName</span></span>
<span data-ttu-id="c8643-120">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c8643-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="c8643-121">– Polyfilter</span><span class="sxs-lookup"><span data-stu-id="c8643-121">-GeoFilters</span></span>
<span data-ttu-id="c8643-122">Listan över geo filter som gäller för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c8643-122">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="c8643-123">-HttpPort</span></span>
<span data-ttu-id="c8643-124">Anger HTTP-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="c8643-124">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="c8643-125">-HttpsPort</span></span>
<span data-ttu-id="c8643-126">Anger HTTPS-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="c8643-126">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="c8643-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="c8643-128">Anger om komprimering är aktiverat för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c8643-128">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="c8643-129">-IsHttpAllowed</span></span>
<span data-ttu-id="c8643-130">Anger om slut punkten tillåter HTTP-trafik.</span><span class="sxs-lookup"><span data-stu-id="c8643-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="c8643-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="c8643-132">Anger om slut punkten aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="c8643-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-133">-Plats</span><span class="sxs-lookup"><span data-stu-id="c8643-133">-Location</span></span>
<span data-ttu-id="c8643-134">Anger resurs platsen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c8643-134">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="c8643-135">-OptimizationType</span></span>
<span data-ttu-id="c8643-136">Anger vilken optimering den här slut punkten har.</span><span class="sxs-lookup"><span data-stu-id="c8643-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="c8643-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="c8643-137">-OriginHostHeader</span></span>
<span data-ttu-id="c8643-138">Anger slut punktens ursprungs värd huvud.</span><span class="sxs-lookup"><span data-stu-id="c8643-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="c8643-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="c8643-139">-OriginHostName</span></span>
<span data-ttu-id="c8643-140">Anger värd namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="c8643-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="c8643-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="c8643-141">-OriginName</span></span>
<span data-ttu-id="c8643-142">Anger resurs namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="c8643-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="c8643-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="c8643-143">-OriginPath</span></span>
<span data-ttu-id="c8643-144">Anger sökvägen till ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="c8643-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="c8643-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="c8643-145">-ProbePath</span></span>
<span data-ttu-id="c8643-146">Anger avsöknings Sök vägen för dynamisk webbplats acceleration</span><span class="sxs-lookup"><span data-stu-id="c8643-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="c8643-147">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="c8643-147">-ProfileName</span></span>
<span data-ttu-id="c8643-148">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="c8643-148">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="c8643-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="c8643-150">Anger beteendet för CDN-slutpunkten när en frågesträng finns i URL-adressen för begäran.</span><span class="sxs-lookup"><span data-stu-id="c8643-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8643-151">-ResourceGroupName</span></span>
<span data-ttu-id="c8643-152">Anger namnet på resurs gruppen som den här slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="c8643-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-153">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c8643-153">-Tag</span></span>
<span data-ttu-id="c8643-154">De taggar som ska kopplas till Azure CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="c8643-154">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8643-155">-Confirm</span></span>
<span data-ttu-id="c8643-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8643-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8643-157">-WhatIf</span></span>
<span data-ttu-id="c8643-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8643-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8643-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8643-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8643-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8643-160">CommonParameters</span></span>
<span data-ttu-id="c8643-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8643-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8643-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8643-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8643-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8643-163">INPUTS</span></span>

### <span data-ttu-id="c8643-164">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c8643-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c8643-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8643-165">OUTPUTS</span></span>

### <span data-ttu-id="c8643-166">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c8643-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8643-167">NOTES</span></span>

## <span data-ttu-id="c8643-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8643-168">RELATED LINKS</span></span>

[<span data-ttu-id="c8643-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="c8643-170">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="c8643-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="c8643-172">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="c8643-173">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8643-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)

