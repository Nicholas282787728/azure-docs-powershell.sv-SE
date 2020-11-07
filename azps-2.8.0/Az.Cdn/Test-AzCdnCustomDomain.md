---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 3c923e53fb0ab8999ec322c43609c10255af0a8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745284"
---
# <span data-ttu-id="f6226-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f6226-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="f6226-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6226-102">SYNOPSIS</span></span>
<span data-ttu-id="f6226-103">Kontrollerar om en anpassad domän kan läggas till i en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="f6226-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="f6226-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6226-104">SYNTAX</span></span>

### <span data-ttu-id="f6226-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f6226-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6226-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6226-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6226-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6226-107">DESCRIPTION</span></span>
<span data-ttu-id="f6226-108">**Testet-AzCdnCustomDomain** cmdlet kontrollerar om en anpassad domän kan läggas till i en slut punkt genom att verifiera CNAME-mappningen.</span><span class="sxs-lookup"><span data-stu-id="f6226-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="f6226-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6226-109">EXAMPLES</span></span>

## <span data-ttu-id="f6226-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6226-110">PARAMETERS</span></span>

### <span data-ttu-id="f6226-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6226-111">-CdnEndpoint</span></span>
<span data-ttu-id="f6226-112">Anger den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="f6226-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="f6226-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="f6226-113">-CustomDomainHostName</span></span>
<span data-ttu-id="f6226-114">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="f6226-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="f6226-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6226-115">-DefaultProfile</span></span>
<span data-ttu-id="f6226-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f6226-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6226-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f6226-117">-EndpointName</span></span>
<span data-ttu-id="f6226-118">Anger namnet på den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="f6226-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="f6226-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="f6226-119">-ProfileName</span></span>
<span data-ttu-id="f6226-120">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="f6226-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f6226-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6226-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6226-122">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6226-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6226-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6226-123">CommonParameters</span></span>
<span data-ttu-id="f6226-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6226-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6226-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6226-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6226-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6226-126">INPUTS</span></span>

### <span data-ttu-id="f6226-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6226-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f6226-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6226-128">OUTPUTS</span></span>

### <span data-ttu-id="f6226-129">Microsoft. Azure. commands. CDN. Models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="f6226-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="f6226-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6226-130">NOTES</span></span>

## <span data-ttu-id="f6226-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6226-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6226-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f6226-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="f6226-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f6226-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="f6226-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f6226-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


