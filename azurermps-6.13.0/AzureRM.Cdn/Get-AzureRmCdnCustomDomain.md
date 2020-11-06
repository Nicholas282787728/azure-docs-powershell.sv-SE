---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585079"
---
# <span data-ttu-id="ad6ea-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ad6ea-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="ad6ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6ea-103">Hämtar en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad6ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad6ea-104">SYNTAX</span></span>

### <span data-ttu-id="ad6ea-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ad6ea-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6ea-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad6ea-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad6ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ad6ea-108">Cmdleten **Get-AzureRmCdnCustomDomain** hämtar en anpassad domän för Azure Content Delivery Network (CDN) och dess relaterade inställningar.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="ad6ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad6ea-109">EXAMPLES</span></span>

## <span data-ttu-id="ad6ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad6ea-110">PARAMETERS</span></span>

### <span data-ttu-id="ad6ea-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad6ea-111">-CdnEndpoint</span></span>
<span data-ttu-id="ad6ea-112">Anger det CDN-slutpunkt-objekt som den anpassade domänen är medlem i.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="ad6ea-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ad6ea-113">-CustomDomainName</span></span>
<span data-ttu-id="ad6ea-114">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="ad6ea-115">Namnet på den anpassade domänen skiljer sig från värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="ad6ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6ea-116">-DefaultProfile</span></span>
<span data-ttu-id="ad6ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ad6ea-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad6ea-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ad6ea-118">-EndpointName</span></span>
<span data-ttu-id="ad6ea-119">Anger namnet på den slut punkt som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ad6ea-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="ad6ea-120">-ProfileName</span></span>
<span data-ttu-id="ad6ea-121">Anger namnet på den profil som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ad6ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad6ea-123">Anger namnet på den resurs grupp som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ad6ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6ea-124">CommonParameters</span></span>
<span data-ttu-id="ad6ea-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6ea-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6ea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6ea-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad6ea-127">INPUTS</span></span>

### <span data-ttu-id="ad6ea-128">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad6ea-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="ad6ea-129">Parametrar: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad6ea-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="ad6ea-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad6ea-130">OUTPUTS</span></span>

### <span data-ttu-id="ad6ea-131">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ad6ea-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="ad6ea-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad6ea-132">NOTES</span></span>

## <span data-ttu-id="ad6ea-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad6ea-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad6ea-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ad6ea-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="ad6ea-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ad6ea-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


