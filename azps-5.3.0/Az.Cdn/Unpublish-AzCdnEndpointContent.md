---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524600"
---
# <span data-ttu-id="c8e05-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="c8e05-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="c8e05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8e05-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e05-103">Rensar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="c8e05-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="c8e05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8e05-104">SYNTAX</span></span>

### <span data-ttu-id="c8e05-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c8e05-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8e05-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8e05-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8e05-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8e05-107">DESCRIPTION</span></span>
<span data-ttu-id="c8e05-108">Cmdleten **unpublishing-AzCdnEndpointContent** rensar innehållet från en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="c8e05-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c8e05-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8e05-109">EXAMPLES</span></span>

## <span data-ttu-id="c8e05-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8e05-110">PARAMETERS</span></span>

### <span data-ttu-id="c8e05-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8e05-111">-CdnEndpoint</span></span>
<span data-ttu-id="c8e05-112">Anger slut punkten som rensar den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8e05-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e05-113">-DefaultProfile</span></span>
<span data-ttu-id="c8e05-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8e05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8e05-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c8e05-115">-EndpointName</span></span>
<span data-ttu-id="c8e05-116">Anger namnet på slut punkten som den här cmdleten rensar.</span><span class="sxs-lookup"><span data-stu-id="c8e05-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="c8e05-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8e05-117">-PassThru</span></span>
<span data-ttu-id="c8e05-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c8e05-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8e05-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c8e05-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e05-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="c8e05-120">-ProfileName</span></span>
<span data-ttu-id="c8e05-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="c8e05-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c8e05-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="c8e05-122">-PurgeContent</span></span>
<span data-ttu-id="c8e05-123">Anger en matris med relativa sökvägar för innehållet på ursprungs servern som den här cmdleten rensar.</span><span class="sxs-lookup"><span data-stu-id="c8e05-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e05-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8e05-125">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="c8e05-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c8e05-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8e05-126">-Confirm</span></span>
<span data-ttu-id="c8e05-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8e05-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e05-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e05-128">-WhatIf</span></span>
<span data-ttu-id="c8e05-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8e05-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8e05-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8e05-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e05-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e05-131">CommonParameters</span></span>
<span data-ttu-id="c8e05-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e05-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e05-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8e05-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e05-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8e05-134">INPUTS</span></span>

### <span data-ttu-id="c8e05-135">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8e05-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="c8e05-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8e05-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8e05-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8e05-137">OUTPUTS</span></span>

### <span data-ttu-id="c8e05-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8e05-138">System.Boolean</span></span>

## <span data-ttu-id="c8e05-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8e05-139">NOTES</span></span>

## <span data-ttu-id="c8e05-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8e05-140">RELATED LINKS</span></span>

[<span data-ttu-id="c8e05-141">Publicera – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="c8e05-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


