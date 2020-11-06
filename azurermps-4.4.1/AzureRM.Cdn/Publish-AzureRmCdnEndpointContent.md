---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581487"
---
# <span data-ttu-id="a3552-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a3552-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="a3552-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3552-102">SYNOPSIS</span></span>
<span data-ttu-id="a3552-103">Läser in innehåll till en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="a3552-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3552-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3552-104">SYNTAX</span></span>

### <span data-ttu-id="a3552-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="a3552-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3552-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="a3552-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3552-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3552-107">DESCRIPTION</span></span>
<span data-ttu-id="a3552-108">Cmdleten **Publishing-AzureRmCdnEndpointContent** läser in innehåll från en ursprunglig Server för CDN-slutpunkten (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="a3552-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a3552-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3552-109">EXAMPLES</span></span>

## <span data-ttu-id="a3552-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3552-110">PARAMETERS</span></span>

### <span data-ttu-id="a3552-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3552-111">-CdnEndpoint</span></span>
<span data-ttu-id="a3552-112">Sepcifies CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="a3552-112">Sepcifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3552-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a3552-113">-EndpointName</span></span>
<span data-ttu-id="a3552-114">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="a3552-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a3552-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="a3552-115">-LoadContent</span></span>
<span data-ttu-id="a3552-116">Anger en matris med relativa sökvägar för innehållet på ursprungs servern som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="a3552-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="a3552-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3552-117">-PassThru</span></span>
<span data-ttu-id="a3552-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a3552-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a3552-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a3552-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3552-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="a3552-120">-ProfileName</span></span>
<span data-ttu-id="a3552-121">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="a3552-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a3552-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3552-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3552-123">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="a3552-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a3552-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3552-124">-DefaultProfile</span></span>
<span data-ttu-id="a3552-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3552-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3552-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3552-126">CommonParameters</span></span>
<span data-ttu-id="a3552-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3552-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3552-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3552-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3552-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3552-129">INPUTS</span></span>

### <span data-ttu-id="a3552-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3552-130">PSEndpoint</span></span>
<span data-ttu-id="a3552-131">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a3552-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a3552-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3552-132">OUTPUTS</span></span>

### <span data-ttu-id="a3552-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3552-133">System.Boolean</span></span>

## <span data-ttu-id="a3552-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3552-134">NOTES</span></span>

## <span data-ttu-id="a3552-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3552-135">RELATED LINKS</span></span>

[<span data-ttu-id="a3552-136">Avpublicering – AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a3552-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


