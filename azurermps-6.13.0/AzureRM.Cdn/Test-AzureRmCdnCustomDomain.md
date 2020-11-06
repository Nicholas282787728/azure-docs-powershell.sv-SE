---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e249331f70e0ef0b7e1397f514363787e9dcf0dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581763"
---
# <span data-ttu-id="424c2-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="424c2-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="424c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="424c2-102">SYNOPSIS</span></span>
<span data-ttu-id="424c2-103">Kontrollerar om en anpassad domän kan läggas till i en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="424c2-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="424c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="424c2-104">SYNTAX</span></span>

### <span data-ttu-id="424c2-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="424c2-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="424c2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="424c2-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="424c2-107">DESCRIPTION</span></span>
<span data-ttu-id="424c2-108">**Testet-AzureRmCdnCustomDomain** cmdlet kontrollerar om en anpassad domän kan läggas till i en slut punkt genom att verifiera CNAME-mappningen.</span><span class="sxs-lookup"><span data-stu-id="424c2-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="424c2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="424c2-109">EXAMPLES</span></span>

## <span data-ttu-id="424c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="424c2-110">PARAMETERS</span></span>

### <span data-ttu-id="424c2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="424c2-111">-CdnEndpoint</span></span>
<span data-ttu-id="424c2-112">Anger den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="424c2-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="424c2-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="424c2-113">-CustomDomainHostName</span></span>
<span data-ttu-id="424c2-114">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="424c2-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424c2-115">-DefaultProfile</span></span>
<span data-ttu-id="424c2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="424c2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="424c2-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="424c2-117">-EndpointName</span></span>
<span data-ttu-id="424c2-118">Anger namnet på den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="424c2-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="424c2-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="424c2-119">-ProfileName</span></span>
<span data-ttu-id="424c2-120">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="424c2-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="424c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="424c2-122">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="424c2-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="424c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424c2-123">CommonParameters</span></span>
<span data-ttu-id="424c2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424c2-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424c2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424c2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="424c2-126">INPUTS</span></span>

### <span data-ttu-id="424c2-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="424c2-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="424c2-128">Parametrar: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="424c2-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="424c2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="424c2-129">OUTPUTS</span></span>

### <span data-ttu-id="424c2-130">Microsoft. Azure. commands. CDN. Models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="424c2-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="424c2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="424c2-131">NOTES</span></span>

## <span data-ttu-id="424c2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="424c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="424c2-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="424c2-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="424c2-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="424c2-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="424c2-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="424c2-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


