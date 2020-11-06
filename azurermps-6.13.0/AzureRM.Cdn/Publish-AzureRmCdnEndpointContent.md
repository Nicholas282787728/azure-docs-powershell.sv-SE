---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a4a2479c6dc7c116ff7da9151fcd5dea5ec26660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578964"
---
# <span data-ttu-id="ae3ab-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="ae3ab-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="ae3ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3ab-103">Läser in innehåll till en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae3ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae3ab-104">SYNTAX</span></span>

### <span data-ttu-id="ae3ab-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ae3ab-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae3ab-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae3ab-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae3ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae3ab-107">DESCRIPTION</span></span>
<span data-ttu-id="ae3ab-108">Cmdleten **Publishing-AzureRmCdnEndpointContent** läser in innehåll från en ursprunglig Server för CDN-slutpunkten (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="ae3ab-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ae3ab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae3ab-109">EXAMPLES</span></span>

## <span data-ttu-id="ae3ab-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae3ab-110">PARAMETERS</span></span>

### <span data-ttu-id="ae3ab-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae3ab-111">-CdnEndpoint</span></span>
<span data-ttu-id="ae3ab-112">Sepcifies CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="ae3ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3ab-113">-DefaultProfile</span></span>
<span data-ttu-id="ae3ab-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ae3ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae3ab-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ae3ab-115">-EndpointName</span></span>
<span data-ttu-id="ae3ab-116">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="ae3ab-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="ae3ab-117">-LoadContent</span></span>
<span data-ttu-id="ae3ab-118">Anger en matris med relativa sökvägar för innehållet på ursprungs servern som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="ae3ab-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae3ab-119">-PassThru</span></span>
<span data-ttu-id="ae3ab-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae3ab-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae3ab-122">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="ae3ab-122">-ProfileName</span></span>
<span data-ttu-id="ae3ab-123">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ae3ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae3ab-125">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ae3ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3ab-126">CommonParameters</span></span>
<span data-ttu-id="ae3ab-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3ab-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3ab-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae3ab-129">INPUTS</span></span>

### <span data-ttu-id="ae3ab-130">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae3ab-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="ae3ab-131">Parametrar: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae3ab-131">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="ae3ab-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae3ab-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae3ab-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae3ab-133">OUTPUTS</span></span>

### <span data-ttu-id="ae3ab-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae3ab-134">System.Boolean</span></span>

## <span data-ttu-id="ae3ab-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae3ab-135">NOTES</span></span>

## <span data-ttu-id="ae3ab-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae3ab-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae3ab-137">Avpublicering – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="ae3ab-137">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


