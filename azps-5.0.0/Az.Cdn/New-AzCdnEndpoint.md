---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269496"
---
# <span data-ttu-id="591d9-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="591d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="591d9-102">SYNOPSIS</span></span>
<span data-ttu-id="591d9-103">Skapar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="591d9-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="591d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="591d9-104">SYNTAX</span></span>

### <span data-ttu-id="591d9-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="591d9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591d9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="591d9-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="591d9-107">DESCRIPTION</span></span>
<span data-ttu-id="591d9-108">Cmdleten **New-AzCdnEndpoint** skapar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="591d9-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="591d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="591d9-109">EXAMPLES</span></span>

## <span data-ttu-id="591d9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="591d9-110">PARAMETERS</span></span>

### <span data-ttu-id="591d9-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="591d9-111">-CdnProfile</span></span>
<span data-ttu-id="591d9-112">Anger det CDN-profil objekt dit slut punkten läggs till.</span><span class="sxs-lookup"><span data-stu-id="591d9-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="591d9-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="591d9-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="591d9-114">Anger en matris med innehålls typer som ska komprimeras från noden Edge till klienten.</span><span class="sxs-lookup"><span data-stu-id="591d9-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="591d9-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="591d9-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="591d9-116">Standard start gruppen.</span><span class="sxs-lookup"><span data-stu-id="591d9-116">The default origin group.</span></span>

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

### <span data-ttu-id="591d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591d9-117">-DefaultProfile</span></span>
<span data-ttu-id="591d9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="591d9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="591d9-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="591d9-119">-DeliveryPolicy</span></span>
<span data-ttu-id="591d9-120">Leverans princip för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="591d9-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="591d9-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="591d9-121">-EndpointName</span></span>
<span data-ttu-id="591d9-122">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="591d9-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="591d9-123">– Polyfilter</span><span class="sxs-lookup"><span data-stu-id="591d9-123">-GeoFilters</span></span>
<span data-ttu-id="591d9-124">Listan över geo filter som gäller för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="591d9-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="591d9-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="591d9-125">-HttpPort</span></span>
<span data-ttu-id="591d9-126">Anger HTTP-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="591d9-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="591d9-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="591d9-127">-HttpsPort</span></span>
<span data-ttu-id="591d9-128">Anger HTTPS-portnumret på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="591d9-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="591d9-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="591d9-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="591d9-130">Anger om komprimering är aktiverat för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="591d9-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="591d9-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="591d9-131">-IsHttpAllowed</span></span>
<span data-ttu-id="591d9-132">Anger om slut punkten tillåter HTTP-trafik.</span><span class="sxs-lookup"><span data-stu-id="591d9-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="591d9-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="591d9-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="591d9-134">Anger om slut punkten aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="591d9-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="591d9-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="591d9-135">-Location</span></span>
<span data-ttu-id="591d9-136">Anger resurs platsen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="591d9-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="591d9-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="591d9-137">-OptimizationType</span></span>
<span data-ttu-id="591d9-138">Anger vilken optimering den här slut punkten har.</span><span class="sxs-lookup"><span data-stu-id="591d9-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="591d9-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="591d9-139">-OriginGroupName</span></span>
<span data-ttu-id="591d9-140">Namnet på ursprungs gruppen.</span><span class="sxs-lookup"><span data-stu-id="591d9-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="591d9-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="591d9-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="591d9-142">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="591d9-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="591d9-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="591d9-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="591d9-144">Sökvägen i förhållande till ursprunget som används för att fastställa statusen för origo.</span><span class="sxs-lookup"><span data-stu-id="591d9-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="591d9-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="591d9-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="591d9-146">Protokoll som ska användas för hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="591d9-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="591d9-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="591d9-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="591d9-148">Typ av begäran om hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="591d9-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="591d9-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="591d9-149">-OriginHostHeader</span></span>
<span data-ttu-id="591d9-150">Anger slut punktens ursprungs värd huvud.</span><span class="sxs-lookup"><span data-stu-id="591d9-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="591d9-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="591d9-151">-OriginHostName</span></span>
<span data-ttu-id="591d9-152">Anger värd namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="591d9-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="591d9-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="591d9-153">-OriginId</span></span>
<span data-ttu-id="591d9-154">Grupp-ID: n för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="591d9-154">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591d9-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="591d9-155">-OriginName</span></span>
<span data-ttu-id="591d9-156">Anger resurs namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="591d9-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="591d9-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="591d9-157">-OriginPath</span></span>
<span data-ttu-id="591d9-158">Anger sökvägen till ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="591d9-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="591d9-159">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="591d9-159">-Priority</span></span>
<span data-ttu-id="591d9-160">Ursprungligt original prioritet för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="591d9-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="591d9-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="591d9-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="591d9-162">Ett anpassat meddelande som ska ingå i godkännandebegäran för anslutning till den privata länken.</span><span class="sxs-lookup"><span data-stu-id="591d9-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="591d9-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="591d9-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="591d9-164">Källa för privata Länkar för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="591d9-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="591d9-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="591d9-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="591d9-166">Resurs-ID för privata Länkar för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="591d9-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="591d9-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="591d9-167">-ProbePath</span></span>
<span data-ttu-id="591d9-168">Anger avsöknings Sök vägen för dynamisk webbplats acceleration</span><span class="sxs-lookup"><span data-stu-id="591d9-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="591d9-169">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="591d9-169">-ProfileName</span></span>
<span data-ttu-id="591d9-170">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="591d9-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="591d9-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="591d9-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="591d9-172">Anger beteendet för CDN-slutpunkten när en frågesträng finns i URL-adressen för begäran.</span><span class="sxs-lookup"><span data-stu-id="591d9-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="591d9-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591d9-173">-ResourceGroupName</span></span>
<span data-ttu-id="591d9-174">Anger namnet på resurs gruppen som den här slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="591d9-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="591d9-175">-Tagg</span><span class="sxs-lookup"><span data-stu-id="591d9-175">-Tag</span></span>
<span data-ttu-id="591d9-176">De taggar som ska kopplas till Azure CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="591d9-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="591d9-177">-Vikt</span><span class="sxs-lookup"><span data-stu-id="591d9-177">-Weight</span></span>
<span data-ttu-id="591d9-178">Ursprunglig vikt för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="591d9-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="591d9-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="591d9-179">-Confirm</span></span>
<span data-ttu-id="591d9-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="591d9-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591d9-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591d9-181">-WhatIf</span></span>
<span data-ttu-id="591d9-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="591d9-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591d9-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="591d9-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591d9-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591d9-184">CommonParameters</span></span>
<span data-ttu-id="591d9-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591d9-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591d9-186">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="591d9-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591d9-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="591d9-187">INPUTS</span></span>

### <span data-ttu-id="591d9-188">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="591d9-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="591d9-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="591d9-189">OUTPUTS</span></span>

### <span data-ttu-id="591d9-190">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="591d9-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="591d9-191">NOTES</span></span>

## <span data-ttu-id="591d9-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="591d9-192">RELATED LINKS</span></span>

[<span data-ttu-id="591d9-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="591d9-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="591d9-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="591d9-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="591d9-197">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="591d9-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)

