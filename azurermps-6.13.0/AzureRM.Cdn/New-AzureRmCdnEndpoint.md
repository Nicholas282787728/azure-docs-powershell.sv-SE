---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 62a4859b5a64003956a4975411f809176f2917e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580292"
---
# <span data-ttu-id="fe065-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="fe065-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe065-102">SYNOPSIS</span></span>
<span data-ttu-id="fe065-103">Skapar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="fe065-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe065-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe065-104">SYNTAX</span></span>

### <span data-ttu-id="fe065-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fe065-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe065-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe065-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe065-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe065-107">DESCRIPTION</span></span>
<span data-ttu-id="fe065-108">Cmdleten **New-AzureRmCdnEndpoint** skapar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="fe065-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fe065-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe065-109">EXAMPLES</span></span>

## <span data-ttu-id="fe065-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe065-110">PARAMETERS</span></span>

### <span data-ttu-id="fe065-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fe065-111">-CdnProfile</span></span>
<span data-ttu-id="fe065-112">Anger det CDN-profil objekt dit slut punkten läggs till.</span><span class="sxs-lookup"><span data-stu-id="fe065-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="fe065-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="fe065-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="fe065-114">Anger en matris med innehålls typer som ska komprimeras från noden Edge till klienten.</span><span class="sxs-lookup"><span data-stu-id="fe065-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="fe065-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe065-115">-DefaultProfile</span></span>
<span data-ttu-id="fe065-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fe065-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe065-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="fe065-117">-DeliveryPolicy</span></span>
<span data-ttu-id="fe065-118">Leverans princip för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe065-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="fe065-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fe065-119">-EndpointName</span></span>
<span data-ttu-id="fe065-120">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe065-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="fe065-121">– Polyfilter</span><span class="sxs-lookup"><span data-stu-id="fe065-121">-GeoFilters</span></span>
<span data-ttu-id="fe065-122">Listan över geo filter som gäller för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe065-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="fe065-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="fe065-123">-HttpPort</span></span>
<span data-ttu-id="fe065-124">Anger HTTP-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="fe065-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="fe065-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="fe065-125">-HttpsPort</span></span>
<span data-ttu-id="fe065-126">Anger HTTPS-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="fe065-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="fe065-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="fe065-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="fe065-128">Anger om komprimering är aktiverat för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe065-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="fe065-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="fe065-129">-IsHttpAllowed</span></span>
<span data-ttu-id="fe065-130">Anger om slut punkten tillåter HTTP-trafik.</span><span class="sxs-lookup"><span data-stu-id="fe065-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="fe065-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="fe065-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="fe065-132">Anger om slut punkten aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="fe065-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="fe065-133">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe065-133">-Location</span></span>
<span data-ttu-id="fe065-134">Anger resurs platsen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe065-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="fe065-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="fe065-135">-OptimizationType</span></span>
<span data-ttu-id="fe065-136">Anger vilken optimering den här slut punkten har.</span><span class="sxs-lookup"><span data-stu-id="fe065-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="fe065-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="fe065-137">-OriginHostHeader</span></span>
<span data-ttu-id="fe065-138">Anger slut punktens ursprungs värd huvud.</span><span class="sxs-lookup"><span data-stu-id="fe065-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="fe065-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="fe065-139">-OriginHostName</span></span>
<span data-ttu-id="fe065-140">Anger värd namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="fe065-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="fe065-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="fe065-141">-OriginName</span></span>
<span data-ttu-id="fe065-142">Anger resurs namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="fe065-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="fe065-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="fe065-143">-OriginPath</span></span>
<span data-ttu-id="fe065-144">Anger sökvägen till ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="fe065-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="fe065-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="fe065-145">-ProbePath</span></span>
<span data-ttu-id="fe065-146">Anger avsöknings Sök vägen för dynamisk webbplats acceleration</span><span class="sxs-lookup"><span data-stu-id="fe065-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="fe065-147">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="fe065-147">-ProfileName</span></span>
<span data-ttu-id="fe065-148">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="fe065-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fe065-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="fe065-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="fe065-150">Anger beteendet för CDN-slutpunkten när en frågesträng finns i URL-adressen för begäran.</span><span class="sxs-lookup"><span data-stu-id="fe065-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="fe065-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe065-151">-ResourceGroupName</span></span>
<span data-ttu-id="fe065-152">Anger namnet på resurs gruppen som den här slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="fe065-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="fe065-153">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fe065-153">-Tag</span></span>
<span data-ttu-id="fe065-154">De taggar som ska kopplas till Azure CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="fe065-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="fe065-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe065-155">-Confirm</span></span>
<span data-ttu-id="fe065-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe065-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe065-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe065-157">-WhatIf</span></span>
<span data-ttu-id="fe065-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe065-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe065-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe065-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe065-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe065-160">CommonParameters</span></span>
<span data-ttu-id="fe065-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe065-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe065-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe065-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe065-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe065-163">INPUTS</span></span>

### <span data-ttu-id="fe065-164">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="fe065-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="fe065-165">Parametrar: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fe065-165">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="fe065-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe065-166">OUTPUTS</span></span>

### <span data-ttu-id="fe065-167">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-167">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="fe065-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe065-168">NOTES</span></span>

## <span data-ttu-id="fe065-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe065-169">RELATED LINKS</span></span>

[<span data-ttu-id="fe065-170">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-170">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fe065-171">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-171">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fe065-172">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-172">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fe065-173">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-173">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fe065-174">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe065-174">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


