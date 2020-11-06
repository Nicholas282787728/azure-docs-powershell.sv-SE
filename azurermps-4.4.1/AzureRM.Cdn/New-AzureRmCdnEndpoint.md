---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581495"
---
# <span data-ttu-id="50512-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="50512-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50512-102">SYNOPSIS</span></span>
<span data-ttu-id="50512-103">Skapar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="50512-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50512-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50512-104">SYNTAX</span></span>

### <span data-ttu-id="50512-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="50512-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50512-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="50512-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50512-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50512-107">DESCRIPTION</span></span>
<span data-ttu-id="50512-108">Cmdleten **New-AzureRmCdnEndpoint** skapar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="50512-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="50512-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50512-109">EXAMPLES</span></span>

## <span data-ttu-id="50512-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50512-110">PARAMETERS</span></span>

### <span data-ttu-id="50512-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="50512-111">-CdnProfile</span></span>
<span data-ttu-id="50512-112">Anger det CDN-profil objekt dit slut punkten läggs till.</span><span class="sxs-lookup"><span data-stu-id="50512-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50512-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="50512-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="50512-114">Anger en matris med innehålls typer som ska komprimeras från noden Edge till klienten.</span><span class="sxs-lookup"><span data-stu-id="50512-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="50512-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="50512-115">-EndpointName</span></span>
<span data-ttu-id="50512-116">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="50512-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="50512-117">– Polyfilter</span><span class="sxs-lookup"><span data-stu-id="50512-117">-GeoFilters</span></span>
<span data-ttu-id="50512-118">Listan över geo filter som gäller för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="50512-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="50512-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="50512-119">-HttpPort</span></span>
<span data-ttu-id="50512-120">Anger HTTP-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="50512-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="50512-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="50512-121">-HttpsPort</span></span>
<span data-ttu-id="50512-122">Anger HTTPS-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="50512-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="50512-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="50512-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="50512-124">Anger om komprimering är aktiverat för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="50512-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="50512-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="50512-125">-IsHttpAllowed</span></span>
<span data-ttu-id="50512-126">Anger om slut punkten tillåter HTTP-trafik.</span><span class="sxs-lookup"><span data-stu-id="50512-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="50512-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="50512-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="50512-128">Anger om slut punkten aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="50512-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="50512-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="50512-129">-Location</span></span>
<span data-ttu-id="50512-130">Anger resurs platsen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="50512-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50512-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="50512-131">-OptimizationType</span></span>
<span data-ttu-id="50512-132">Anger vilken optimering den här slut punkten har.</span><span class="sxs-lookup"><span data-stu-id="50512-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="50512-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="50512-133">-OriginHostHeader</span></span>
<span data-ttu-id="50512-134">Anger slut punktens ursprungs värd huvud.</span><span class="sxs-lookup"><span data-stu-id="50512-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="50512-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="50512-135">-OriginHostName</span></span>
<span data-ttu-id="50512-136">Anger värd namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="50512-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="50512-137">-OriginName</span><span class="sxs-lookup"><span data-stu-id="50512-137">-OriginName</span></span>
<span data-ttu-id="50512-138">Anger resurs namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="50512-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="50512-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="50512-139">-OriginPath</span></span>
<span data-ttu-id="50512-140">Anger sökvägen till ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="50512-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="50512-141">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="50512-141">-ProfileName</span></span>
<span data-ttu-id="50512-142">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="50512-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50512-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="50512-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="50512-144">Anger beteendet för CDN-slutpunkten när en frågesträng finns i URL-adressen för begäran.</span><span class="sxs-lookup"><span data-stu-id="50512-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="50512-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50512-145">-ResourceGroupName</span></span>
<span data-ttu-id="50512-146">Anger namnet på resurs gruppen som den här slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="50512-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50512-147">-Taggar</span><span class="sxs-lookup"><span data-stu-id="50512-147">-Tags</span></span>
<span data-ttu-id="50512-148">Anger en hash-tabell för de taggar som är associerade med den här resursen.</span><span class="sxs-lookup"><span data-stu-id="50512-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="50512-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50512-149">-Confirm</span></span>
<span data-ttu-id="50512-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50512-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50512-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50512-151">-WhatIf</span></span>
<span data-ttu-id="50512-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50512-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50512-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50512-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50512-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50512-154">-DefaultProfile</span></span>
<span data-ttu-id="50512-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50512-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50512-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50512-156">CommonParameters</span></span>
<span data-ttu-id="50512-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50512-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50512-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50512-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50512-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50512-159">INPUTS</span></span>

### <span data-ttu-id="50512-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="50512-160">PSProfile</span></span>
<span data-ttu-id="50512-161">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="50512-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="50512-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50512-162">OUTPUTS</span></span>

### <span data-ttu-id="50512-163">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="50512-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50512-164">NOTES</span></span>

## <span data-ttu-id="50512-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50512-165">RELATED LINKS</span></span>

[<span data-ttu-id="50512-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="50512-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="50512-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="50512-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="50512-170">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50512-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


