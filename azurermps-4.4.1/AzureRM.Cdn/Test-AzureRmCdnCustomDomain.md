---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578431"
---
# <span data-ttu-id="664c4-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="664c4-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="664c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="664c4-102">SYNOPSIS</span></span>
<span data-ttu-id="664c4-103">Kontrollerar om en anpassad domän kan läggas till i en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="664c4-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="664c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="664c4-104">SYNTAX</span></span>

### <span data-ttu-id="664c4-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="664c4-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="664c4-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="664c4-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="664c4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="664c4-107">DESCRIPTION</span></span>
<span data-ttu-id="664c4-108">**Testet-AzureRmCdnCustomDomain** cmdlet kontrollerar om en anpassad domän kan läggas till i en slut punkt genom att verifiera CNAME-mappningen.</span><span class="sxs-lookup"><span data-stu-id="664c4-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="664c4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="664c4-109">EXAMPLES</span></span>

## <span data-ttu-id="664c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="664c4-110">PARAMETERS</span></span>

### <span data-ttu-id="664c4-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="664c4-111">-CdnEndpoint</span></span>
<span data-ttu-id="664c4-112">Anger den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="664c4-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="664c4-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="664c4-113">-CustomDomainHostName</span></span>
<span data-ttu-id="664c4-114">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="664c4-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="664c4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="664c4-115">-EndpointName</span></span>
<span data-ttu-id="664c4-116">Anger namnet på den slut punkt som du vill lägga till den anpassade domänen för.</span><span class="sxs-lookup"><span data-stu-id="664c4-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="664c4-117">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="664c4-117">-ProfileName</span></span>
<span data-ttu-id="664c4-118">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="664c4-118">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="664c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="664c4-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="664c4-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="664c4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664c4-121">-DefaultProfile</span></span>
<span data-ttu-id="664c4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="664c4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="664c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664c4-123">CommonParameters</span></span>
<span data-ttu-id="664c4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="664c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664c4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664c4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664c4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="664c4-126">INPUTS</span></span>

### <span data-ttu-id="664c4-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="664c4-127">PSEndpoint</span></span>
<span data-ttu-id="664c4-128">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="664c4-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="664c4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="664c4-129">OUTPUTS</span></span>

### <span data-ttu-id="664c4-130">Microsoft. Azure. commands. CDN. Models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="664c4-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="664c4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="664c4-131">NOTES</span></span>

## <span data-ttu-id="664c4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="664c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="664c4-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="664c4-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="664c4-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="664c4-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="664c4-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="664c4-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


