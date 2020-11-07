---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756633"
---
# <span data-ttu-id="3f1a1-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3f1a1-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="3f1a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1a1-103">Skapar en egen domän för en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f1a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f1a1-104">SYNTAX</span></span>

### <span data-ttu-id="3f1a1-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="3f1a1-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f1a1-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="3f1a1-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f1a1-107">DESCRIPTION</span></span>
<span data-ttu-id="3f1a1-108">Cmdleten **New-AzureRmCdnCustomDomain** skapar en anpassad domän för slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="3f1a1-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3f1a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f1a1-109">EXAMPLES</span></span>

## <span data-ttu-id="3f1a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f1a1-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1a1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f1a1-111">-CdnEndpoint</span></span>
<span data-ttu-id="3f1a1-112">Anger det CDN-slutobjekt som den anpassade domänen läggs till för.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="3f1a1-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3f1a1-113">-CustomDomainName</span></span>
<span data-ttu-id="3f1a1-114">Anger resurs namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="3f1a1-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3f1a1-115">-EndpointName</span></span>
<span data-ttu-id="3f1a1-116">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="3f1a1-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="3f1a1-117">-HostName</span></span>
<span data-ttu-id="3f1a1-118">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-118">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="3f1a1-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="3f1a1-119">-ProfileName</span></span>
<span data-ttu-id="3f1a1-120">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="3f1a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="3f1a1-122">Anger namnet på den resurs grupp som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="3f1a1-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f1a1-123">-Confirm</span></span>
<span data-ttu-id="3f1a1-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1a1-125">-WhatIf</span></span>
<span data-ttu-id="3f1a1-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1a1-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1a1-128">-DefaultProfile</span></span>
<span data-ttu-id="3f1a1-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f1a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1a1-130">CommonParameters</span></span>
<span data-ttu-id="3f1a1-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f1a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1a1-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1a1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1a1-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f1a1-133">INPUTS</span></span>

### <span data-ttu-id="3f1a1-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f1a1-134">PSEndpoint</span></span>
<span data-ttu-id="3f1a1-135">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3f1a1-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3f1a1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f1a1-136">OUTPUTS</span></span>

### <span data-ttu-id="3f1a1-137">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3f1a1-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="3f1a1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f1a1-138">NOTES</span></span>

## <span data-ttu-id="3f1a1-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f1a1-139">RELATED LINKS</span></span>

[<span data-ttu-id="3f1a1-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3f1a1-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="3f1a1-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3f1a1-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="3f1a1-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3f1a1-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


