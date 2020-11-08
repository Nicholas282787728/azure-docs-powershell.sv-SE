---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089920"
---
# <span data-ttu-id="d0cc5-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="d0cc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cc5-103">Hämtar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="d0cc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0cc5-104">SYNTAX</span></span>

### <span data-ttu-id="d0cc5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d0cc5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0cc5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0cc5-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0cc5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0cc5-107">DESCRIPTION</span></span>
<span data-ttu-id="d0cc5-108">Cmdleten **Get-AzCdnEndpoint** hämtar en CDN-slutpunkt (Azure Content Delivery Network) och dess tillhör ande konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="d0cc5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0cc5-109">EXAMPLES</span></span>

## <span data-ttu-id="d0cc5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0cc5-110">PARAMETERS</span></span>

### <span data-ttu-id="d0cc5-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="d0cc5-111">-CdnProfile</span></span>
<span data-ttu-id="d0cc5-112">Anger det CDN-profil objekt som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d0cc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cc5-113">-DefaultProfile</span></span>
<span data-ttu-id="d0cc5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0cc5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0cc5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d0cc5-115">-EndpointName</span></span>
<span data-ttu-id="d0cc5-116">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="d0cc5-117">Namnet på slut punkten är inte slut punktens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="d0cc5-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="d0cc5-118">-ProfileName</span></span>
<span data-ttu-id="d0cc5-119">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d0cc5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0cc5-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0cc5-121">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d0cc5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cc5-122">CommonParameters</span></span>
<span data-ttu-id="d0cc5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0cc5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cc5-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0cc5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cc5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0cc5-125">INPUTS</span></span>

### <span data-ttu-id="d0cc5-126">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d0cc5-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d0cc5-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0cc5-127">OUTPUTS</span></span>

### <span data-ttu-id="d0cc5-128">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d0cc5-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0cc5-129">NOTES</span></span>

## <span data-ttu-id="d0cc5-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0cc5-130">RELATED LINKS</span></span>

[<span data-ttu-id="d0cc5-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="d0cc5-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="d0cc5-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="d0cc5-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="d0cc5-135">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0cc5-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


