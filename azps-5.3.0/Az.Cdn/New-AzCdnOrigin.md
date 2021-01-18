---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524623"
---
# <span data-ttu-id="89327-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="89327-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="89327-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89327-102">SYNOPSIS</span></span>
<span data-ttu-id="89327-103">Skapar ett nytt CDN-ursprung</span><span class="sxs-lookup"><span data-stu-id="89327-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="89327-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89327-104">SYNTAX</span></span>

### <span data-ttu-id="89327-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="89327-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89327-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="89327-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89327-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89327-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89327-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89327-108">DESCRIPTION</span></span>
<span data-ttu-id="89327-109">New-AzCdnOrigin skapar ett nytt CDN-ursprung inom den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="89327-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="89327-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89327-110">EXAMPLES</span></span>

### <span data-ttu-id="89327-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89327-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="89327-112">Denna cmdlet kommer att skapa ett nytt CDN-ursprung för den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="89327-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="89327-113">Det här värd namnet används som ursprung.</span><span class="sxs-lookup"><span data-stu-id="89327-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="89327-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89327-114">PARAMETERS</span></span>

### <span data-ttu-id="89327-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="89327-115">-CdnOrigin</span></span>
<span data-ttu-id="89327-116">Originalvärdet Origin-objekt.</span><span class="sxs-lookup"><span data-stu-id="89327-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89327-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89327-117">-DefaultProfile</span></span>
<span data-ttu-id="89327-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89327-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89327-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="89327-119">-EndpointName</span></span>
<span data-ttu-id="89327-120">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="89327-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="89327-121">-HostName</span></span>
<span data-ttu-id="89327-122">Namn på en värd för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="89327-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="89327-123">-HttpPort</span></span>
<span data-ttu-id="89327-124">Azure CDN Origin http-port.</span><span class="sxs-lookup"><span data-stu-id="89327-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="89327-125">-HttpsPort</span></span>
<span data-ttu-id="89327-126">Azure CDN ursprunglig HTTPS-port.</span><span class="sxs-lookup"><span data-stu-id="89327-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="89327-127">-OriginHostHeader</span></span>
<span data-ttu-id="89327-128">Käll värd rubrik för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="89327-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="89327-129">-OriginName</span></span>
<span data-ttu-id="89327-130">Namn på Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="89327-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-131">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="89327-131">-Priority</span></span>
<span data-ttu-id="89327-132">Ursprungligt original prioritet för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="89327-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="89327-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="89327-134">Ett anpassat meddelande som ska ingå i godkännandebegäran för anslutning till den privata länken.</span><span class="sxs-lookup"><span data-stu-id="89327-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="89327-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="89327-136">Källa för privata Länkar för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="89327-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="89327-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="89327-138">Resurs-ID för privata Länkar för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="89327-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-139">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="89327-139">-ProfileName</span></span>
<span data-ttu-id="89327-140">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="89327-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89327-141">-ResourceGroupName</span></span>
<span data-ttu-id="89327-142">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="89327-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-143">-Vikt</span><span class="sxs-lookup"><span data-stu-id="89327-143">-Weight</span></span>
<span data-ttu-id="89327-144">Ursprunglig vikt för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="89327-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89327-145">-Confirm</span></span>
<span data-ttu-id="89327-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89327-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89327-147">-WhatIf</span></span>
<span data-ttu-id="89327-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89327-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89327-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89327-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89327-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89327-150">CommonParameters</span></span>
<span data-ttu-id="89327-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89327-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89327-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89327-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89327-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89327-153">INPUTS</span></span>

### <span data-ttu-id="89327-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="89327-154">None</span></span>

## <span data-ttu-id="89327-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89327-155">OUTPUTS</span></span>

### <span data-ttu-id="89327-156">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="89327-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="89327-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89327-157">NOTES</span></span>

## <span data-ttu-id="89327-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89327-158">RELATED LINKS</span></span>
