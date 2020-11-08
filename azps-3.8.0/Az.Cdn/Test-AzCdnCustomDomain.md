---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088057"
---
# <span data-ttu-id="83313-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83313-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="83313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83313-102">SYNOPSIS</span></span>
<span data-ttu-id="83313-103">Kontrollerar om en anpassad domän kan läggas till i en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="83313-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="83313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83313-104">SYNTAX</span></span>

### <span data-ttu-id="83313-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="83313-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83313-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83313-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83313-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83313-107">DESCRIPTION</span></span>
<span data-ttu-id="83313-108">**Testet-AzCdnCustomDomain** cmdlet kontrollerar om en anpassad domän kan läggas till i en slut punkt genom att verifiera CNAME-mappningen.</span><span class="sxs-lookup"><span data-stu-id="83313-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="83313-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83313-109">EXAMPLES</span></span>

## <span data-ttu-id="83313-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83313-110">PARAMETERS</span></span>

### <span data-ttu-id="83313-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="83313-111">-CdnEndpoint</span></span>
<span data-ttu-id="83313-112">Anger den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="83313-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="83313-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="83313-113">-CustomDomainHostName</span></span>
<span data-ttu-id="83313-114">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="83313-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="83313-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83313-115">-DefaultProfile</span></span>
<span data-ttu-id="83313-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="83313-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83313-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="83313-117">-EndpointName</span></span>
<span data-ttu-id="83313-118">Anger namnet på den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="83313-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="83313-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="83313-119">-ProfileName</span></span>
<span data-ttu-id="83313-120">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="83313-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="83313-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83313-121">-ResourceGroupName</span></span>
<span data-ttu-id="83313-122">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="83313-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="83313-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83313-123">CommonParameters</span></span>
<span data-ttu-id="83313-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83313-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83313-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83313-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83313-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83313-126">INPUTS</span></span>

### <span data-ttu-id="83313-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="83313-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="83313-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83313-128">OUTPUTS</span></span>

### <span data-ttu-id="83313-129">Microsoft. Azure. commands. CDN. Models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="83313-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="83313-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83313-130">NOTES</span></span>

## <span data-ttu-id="83313-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83313-131">RELATED LINKS</span></span>

[<span data-ttu-id="83313-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83313-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="83313-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83313-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="83313-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83313-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


