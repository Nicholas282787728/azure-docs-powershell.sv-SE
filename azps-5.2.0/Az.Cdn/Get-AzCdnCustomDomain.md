---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405523"
---
# <span data-ttu-id="0058f-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0058f-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="0058f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0058f-102">SYNOPSIS</span></span>
<span data-ttu-id="0058f-103">Hämtar en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="0058f-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="0058f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0058f-104">SYNTAX</span></span>

### <span data-ttu-id="0058f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0058f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0058f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0058f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0058f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0058f-107">DESCRIPTION</span></span>
<span data-ttu-id="0058f-108">Cmdleten **Get-AzCdnCustomDomain** hämtar en anpassad domän för Azure Content Delivery Network (CDN) och dess relaterade inställningar.</span><span class="sxs-lookup"><span data-stu-id="0058f-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="0058f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0058f-109">EXAMPLES</span></span>

## <span data-ttu-id="0058f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0058f-110">PARAMETERS</span></span>

### <span data-ttu-id="0058f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0058f-111">-CdnEndpoint</span></span>
<span data-ttu-id="0058f-112">Anger det CDN-slutpunkt-objekt som den anpassade domänen är medlem i.</span><span class="sxs-lookup"><span data-stu-id="0058f-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="0058f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0058f-113">-CustomDomainName</span></span>
<span data-ttu-id="0058f-114">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="0058f-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="0058f-115">Namnet på den anpassade domänen skiljer sig från värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="0058f-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="0058f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0058f-116">-DefaultProfile</span></span>
<span data-ttu-id="0058f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0058f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0058f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0058f-118">-EndpointName</span></span>
<span data-ttu-id="0058f-119">Anger namnet på den slut punkt som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0058f-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="0058f-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="0058f-120">-ProfileName</span></span>
<span data-ttu-id="0058f-121">Anger namnet på den profil som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0058f-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="0058f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0058f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0058f-123">Anger namnet på den resurs grupp som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0058f-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="0058f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0058f-124">CommonParameters</span></span>
<span data-ttu-id="0058f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0058f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0058f-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0058f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0058f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0058f-127">INPUTS</span></span>

### <span data-ttu-id="0058f-128">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0058f-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="0058f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0058f-129">OUTPUTS</span></span>

### <span data-ttu-id="0058f-130">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0058f-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="0058f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0058f-131">NOTES</span></span>

## <span data-ttu-id="0058f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0058f-132">RELATED LINKS</span></span>

[<span data-ttu-id="0058f-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0058f-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="0058f-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0058f-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


