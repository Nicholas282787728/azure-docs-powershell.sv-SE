---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: bb55b858e4c2464cced362357ffbc91a3969b1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578339"
---
# <span data-ttu-id="418cf-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="418cf-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="418cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="418cf-102">SYNOPSIS</span></span>
<span data-ttu-id="418cf-103">Rensar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="418cf-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="418cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="418cf-104">SYNTAX</span></span>

### <span data-ttu-id="418cf-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="418cf-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="418cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="418cf-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418cf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="418cf-107">DESCRIPTION</span></span>
<span data-ttu-id="418cf-108">Cmdleten **unpublishing-AzureRmCdnEndpointContent** rensar innehållet från en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="418cf-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="418cf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="418cf-109">EXAMPLES</span></span>

## <span data-ttu-id="418cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="418cf-110">PARAMETERS</span></span>

### <span data-ttu-id="418cf-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="418cf-111">-CdnEndpoint</span></span>
<span data-ttu-id="418cf-112">Anger slut punkten som rensar den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="418cf-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="418cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418cf-113">-DefaultProfile</span></span>
<span data-ttu-id="418cf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="418cf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="418cf-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="418cf-115">-EndpointName</span></span>
<span data-ttu-id="418cf-116">Anger namnet på slut punkten som den här cmdleten rensar.</span><span class="sxs-lookup"><span data-stu-id="418cf-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="418cf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="418cf-117">-PassThru</span></span>
<span data-ttu-id="418cf-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="418cf-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="418cf-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="418cf-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418cf-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="418cf-120">-ProfileName</span></span>
<span data-ttu-id="418cf-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="418cf-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="418cf-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="418cf-122">-PurgeContent</span></span>
<span data-ttu-id="418cf-123">Anger en matris med relativa sökvägar för innehållet på ursprungs servern som den här cmdleten rensar.</span><span class="sxs-lookup"><span data-stu-id="418cf-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="418cf-125">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="418cf-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="418cf-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="418cf-126">-Confirm</span></span>
<span data-ttu-id="418cf-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="418cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418cf-128">-WhatIf</span></span>
<span data-ttu-id="418cf-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="418cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="418cf-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="418cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418cf-131">CommonParameters</span></span>
<span data-ttu-id="418cf-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418cf-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418cf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418cf-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="418cf-134">INPUTS</span></span>

### <span data-ttu-id="418cf-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="418cf-135">PSEndpoint</span></span>
<span data-ttu-id="418cf-136">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="418cf-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="418cf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="418cf-137">OUTPUTS</span></span>

### <span data-ttu-id="418cf-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="418cf-138">System.Boolean</span></span>

## <span data-ttu-id="418cf-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="418cf-139">NOTES</span></span>

## <span data-ttu-id="418cf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="418cf-140">RELATED LINKS</span></span>

[<span data-ttu-id="418cf-141">Publicera – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="418cf-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


