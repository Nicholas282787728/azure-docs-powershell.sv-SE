---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090568"
---
# <span data-ttu-id="57b87-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="57b87-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="57b87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57b87-102">SYNOPSIS</span></span>
<span data-ttu-id="57b87-103">Läser in innehåll till en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="57b87-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="57b87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57b87-104">SYNTAX</span></span>

### <span data-ttu-id="57b87-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="57b87-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57b87-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57b87-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b87-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57b87-107">DESCRIPTION</span></span>
<span data-ttu-id="57b87-108">Cmdleten **Publishing-AzCdnEndpointContent** läser in innehåll från en ursprunglig Server för CDN-slutpunkten (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="57b87-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="57b87-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57b87-109">EXAMPLES</span></span>

## <span data-ttu-id="57b87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57b87-110">PARAMETERS</span></span>

### <span data-ttu-id="57b87-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57b87-111">-CdnEndpoint</span></span>
<span data-ttu-id="57b87-112">Anger CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="57b87-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="57b87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b87-113">-DefaultProfile</span></span>
<span data-ttu-id="57b87-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57b87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57b87-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="57b87-115">-EndpointName</span></span>
<span data-ttu-id="57b87-116">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="57b87-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="57b87-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="57b87-117">-LoadContent</span></span>
<span data-ttu-id="57b87-118">Anger en matris med relativa sökvägar för innehållet på ursprungs servern som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="57b87-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="57b87-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57b87-119">-PassThru</span></span>
<span data-ttu-id="57b87-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="57b87-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57b87-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="57b87-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57b87-122">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="57b87-122">-ProfileName</span></span>
<span data-ttu-id="57b87-123">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="57b87-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="57b87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b87-124">-ResourceGroupName</span></span>
<span data-ttu-id="57b87-125">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="57b87-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="57b87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b87-126">CommonParameters</span></span>
<span data-ttu-id="57b87-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b87-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57b87-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b87-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57b87-129">INPUTS</span></span>

### <span data-ttu-id="57b87-130">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="57b87-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="57b87-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="57b87-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57b87-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57b87-132">OUTPUTS</span></span>

### <span data-ttu-id="57b87-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57b87-133">System.Boolean</span></span>

## <span data-ttu-id="57b87-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57b87-134">NOTES</span></span>

## <span data-ttu-id="57b87-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57b87-135">RELATED LINKS</span></span>

[<span data-ttu-id="57b87-136">Avpublicering – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="57b87-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


