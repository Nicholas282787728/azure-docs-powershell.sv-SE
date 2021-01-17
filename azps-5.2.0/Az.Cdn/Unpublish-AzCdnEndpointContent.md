---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399395"
---
# <span data-ttu-id="fb325-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="fb325-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="fb325-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb325-102">SYNOPSIS</span></span>
<span data-ttu-id="fb325-103">Rensar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="fb325-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="fb325-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb325-104">SYNTAX</span></span>

### <span data-ttu-id="fb325-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fb325-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb325-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb325-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb325-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb325-107">DESCRIPTION</span></span>
<span data-ttu-id="fb325-108">Cmdleten **unpublishing-AzCdnEndpointContent** rensar innehållet från en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="fb325-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fb325-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb325-109">EXAMPLES</span></span>

## <span data-ttu-id="fb325-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb325-110">PARAMETERS</span></span>

### <span data-ttu-id="fb325-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb325-111">-CdnEndpoint</span></span>
<span data-ttu-id="fb325-112">Anger slut punkten som rensar den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb325-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="fb325-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb325-113">-DefaultProfile</span></span>
<span data-ttu-id="fb325-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb325-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb325-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fb325-115">-EndpointName</span></span>
<span data-ttu-id="fb325-116">Anger namnet på slut punkten som den här cmdleten rensar.</span><span class="sxs-lookup"><span data-stu-id="fb325-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="fb325-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb325-117">-PassThru</span></span>
<span data-ttu-id="fb325-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fb325-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb325-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fb325-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb325-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="fb325-120">-ProfileName</span></span>
<span data-ttu-id="fb325-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="fb325-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="fb325-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="fb325-122">-PurgeContent</span></span>
<span data-ttu-id="fb325-123">Anger en matris med relativa sökvägar för innehållet på ursprungs servern som den här cmdleten rensar.</span><span class="sxs-lookup"><span data-stu-id="fb325-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="fb325-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb325-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb325-125">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="fb325-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="fb325-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb325-126">-Confirm</span></span>
<span data-ttu-id="fb325-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb325-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb325-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb325-128">-WhatIf</span></span>
<span data-ttu-id="fb325-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb325-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb325-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb325-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb325-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb325-131">CommonParameters</span></span>
<span data-ttu-id="fb325-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb325-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb325-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb325-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb325-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb325-134">INPUTS</span></span>

### <span data-ttu-id="fb325-135">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb325-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="fb325-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb325-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb325-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb325-137">OUTPUTS</span></span>

### <span data-ttu-id="fb325-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb325-138">System.Boolean</span></span>

## <span data-ttu-id="fb325-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb325-139">NOTES</span></span>

## <span data-ttu-id="fb325-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb325-140">RELATED LINKS</span></span>

[<span data-ttu-id="fb325-141">Publicera – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="fb325-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


