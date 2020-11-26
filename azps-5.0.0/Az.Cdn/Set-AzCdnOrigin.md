---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270874"
---
# <span data-ttu-id="1682b-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1682b-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="1682b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1682b-102">SYNOPSIS</span></span>
<span data-ttu-id="1682b-103">Uppdaterar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="1682b-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="1682b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1682b-104">SYNTAX</span></span>

### <span data-ttu-id="1682b-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1682b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1682b-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="1682b-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1682b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1682b-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1682b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1682b-108">DESCRIPTION</span></span>
<span data-ttu-id="1682b-109">Cmdleten **set-AzCdnOrigin** uppdaterar en Origine-Server för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="1682b-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="1682b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1682b-110">EXAMPLES</span></span>

## <span data-ttu-id="1682b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1682b-111">PARAMETERS</span></span>

### <span data-ttu-id="1682b-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1682b-112">-CdnOrigin</span></span>
<span data-ttu-id="1682b-113">Anger den ursprungs server som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="1682b-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1682b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1682b-114">-DefaultProfile</span></span>
<span data-ttu-id="1682b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1682b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1682b-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1682b-116">-EndpointName</span></span>
<span data-ttu-id="1682b-117">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="1682b-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1682b-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="1682b-118">-HostName</span></span>
<span data-ttu-id="1682b-119">Namn på en värd för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="1682b-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="1682b-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="1682b-120">-HttpPort</span></span>
<span data-ttu-id="1682b-121">Azure CDN Origin http-port.</span><span class="sxs-lookup"><span data-stu-id="1682b-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="1682b-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="1682b-122">-HttpsPort</span></span>
<span data-ttu-id="1682b-123">Azure CDN ursprunglig HTTPS-port.</span><span class="sxs-lookup"><span data-stu-id="1682b-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="1682b-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="1682b-124">-OriginHostHeader</span></span>
<span data-ttu-id="1682b-125">Käll värd rubrik för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="1682b-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="1682b-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="1682b-126">-OriginName</span></span>
<span data-ttu-id="1682b-127">Namn på Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="1682b-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="1682b-128">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="1682b-128">-Priority</span></span>
<span data-ttu-id="1682b-129">Ursprungligt original prioritet för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="1682b-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="1682b-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="1682b-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="1682b-131">Ett anpassat meddelande som ska ingå i godkännandebegäran för anslutning till den privata länken.</span><span class="sxs-lookup"><span data-stu-id="1682b-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="1682b-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="1682b-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="1682b-133">Källa för privata Länkar för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="1682b-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="1682b-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="1682b-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="1682b-135">Resurs-ID för privata Länkar för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="1682b-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="1682b-136">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="1682b-136">-ProfileName</span></span>
<span data-ttu-id="1682b-137">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="1682b-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1682b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1682b-138">-ResourceGroupName</span></span>
<span data-ttu-id="1682b-139">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="1682b-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1682b-140">-Vikt</span><span class="sxs-lookup"><span data-stu-id="1682b-140">-Weight</span></span>
<span data-ttu-id="1682b-141">Ursprunglig vikt för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="1682b-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="1682b-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1682b-142">-Confirm</span></span>
<span data-ttu-id="1682b-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1682b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1682b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1682b-144">-WhatIf</span></span>
<span data-ttu-id="1682b-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1682b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1682b-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1682b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1682b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1682b-147">CommonParameters</span></span>
<span data-ttu-id="1682b-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1682b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1682b-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1682b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1682b-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1682b-150">INPUTS</span></span>

### <span data-ttu-id="1682b-151">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="1682b-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="1682b-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1682b-152">OUTPUTS</span></span>

### <span data-ttu-id="1682b-153">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="1682b-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="1682b-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1682b-154">NOTES</span></span>

## <span data-ttu-id="1682b-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1682b-155">RELATED LINKS</span></span>

[<span data-ttu-id="1682b-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1682b-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)

