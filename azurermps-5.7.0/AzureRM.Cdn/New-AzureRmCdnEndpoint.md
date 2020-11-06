---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574386"
---
# <span data-ttu-id="e3dd8-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e3dd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e3dd8-103">Skapar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3dd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3dd8-104">SYNTAX</span></span>

### <span data-ttu-id="e3dd8-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e3dd8-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3dd8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3dd8-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3dd8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3dd8-107">DESCRIPTION</span></span>
<span data-ttu-id="e3dd8-108">Cmdleten **New-AzureRmCdnEndpoint** skapar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="e3dd8-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e3dd8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3dd8-109">EXAMPLES</span></span>

## <span data-ttu-id="e3dd8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3dd8-110">PARAMETERS</span></span>

### <span data-ttu-id="e3dd8-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e3dd8-111">-CdnProfile</span></span>
<span data-ttu-id="e3dd8-112">Anger det CDN-profil objekt dit slut punkten läggs till.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="e3dd8-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="e3dd8-114">Anger en matris med innehålls typer som ska komprimeras från noden Edge till klienten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3dd8-115">-DefaultProfile</span></span>
<span data-ttu-id="e3dd8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e3dd8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e3dd8-117">-EndpointName</span></span>
<span data-ttu-id="e3dd8-118">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-119">– Polyfilter</span><span class="sxs-lookup"><span data-stu-id="e3dd8-119">-GeoFilters</span></span>
<span data-ttu-id="e3dd8-120">Listan över geo filter som gäller för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e3dd8-121">-HttpPort</span></span>
<span data-ttu-id="e3dd8-122">Anger HTTP-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e3dd8-123">-HttpsPort</span></span>
<span data-ttu-id="e3dd8-124">Anger HTTPS-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="e3dd8-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="e3dd8-126">Anger om komprimering är aktiverat för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="e3dd8-127">-IsHttpAllowed</span></span>
<span data-ttu-id="e3dd8-128">Anger om slut punkten tillåter HTTP-trafik.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="e3dd8-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="e3dd8-130">Anger om slut punkten aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="e3dd8-131">-Location</span></span>
<span data-ttu-id="e3dd8-132">Anger resurs platsen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="e3dd8-133">-OptimizationType</span></span>
<span data-ttu-id="e3dd8-134">Anger vilken optimering den här slut punkten har.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="e3dd8-135">-OriginHostHeader</span></span>
<span data-ttu-id="e3dd8-136">Anger slut punktens ursprungs värd huvud.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="e3dd8-137">-OriginHostName</span></span>
<span data-ttu-id="e3dd8-138">Anger värd namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-139">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e3dd8-139">-OriginName</span></span>
<span data-ttu-id="e3dd8-140">Anger resurs namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="e3dd8-141">-OriginPath</span></span>
<span data-ttu-id="e3dd8-142">Anger sökvägen till ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-143">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="e3dd8-143">-ProfileName</span></span>
<span data-ttu-id="e3dd8-144">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="e3dd8-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="e3dd8-146">Anger beteendet för CDN-slutpunkten när en frågesträng finns i URL-adressen för begäran.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3dd8-147">-ResourceGroupName</span></span>
<span data-ttu-id="e3dd8-148">Anger namnet på resurs gruppen som den här slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e3dd8-149">-Tag</span></span>
<span data-ttu-id="e3dd8-150">De taggar som ska kopplas till Azure CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3dd8-151">-Confirm</span></span>
<span data-ttu-id="e3dd8-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3dd8-153">-WhatIf</span></span>
<span data-ttu-id="e3dd8-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3dd8-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3dd8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3dd8-156">CommonParameters</span></span>
<span data-ttu-id="e3dd8-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3dd8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3dd8-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3dd8-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3dd8-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3dd8-159">INPUTS</span></span>

### <span data-ttu-id="e3dd8-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="e3dd8-160">PSProfile</span></span>
<span data-ttu-id="e3dd8-161">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e3dd8-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="e3dd8-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3dd8-162">OUTPUTS</span></span>

### <span data-ttu-id="e3dd8-163">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e3dd8-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3dd8-164">NOTES</span></span>

## <span data-ttu-id="e3dd8-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3dd8-165">RELATED LINKS</span></span>

[<span data-ttu-id="e3dd8-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e3dd8-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e3dd8-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e3dd8-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e3dd8-170">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3dd8-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


