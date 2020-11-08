---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092635"
---
# <span data-ttu-id="07f89-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f89-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="07f89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07f89-102">SYNOPSIS</span></span>
<span data-ttu-id="07f89-103">Skapar en egen domän för en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="07f89-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="07f89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07f89-104">SYNTAX</span></span>

### <span data-ttu-id="07f89-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="07f89-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f89-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f89-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f89-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07f89-107">DESCRIPTION</span></span>
<span data-ttu-id="07f89-108">Cmdleten **New-AzCdnCustomDomain** skapar en anpassad domän för slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="07f89-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="07f89-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07f89-109">EXAMPLES</span></span>

## <span data-ttu-id="07f89-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07f89-110">PARAMETERS</span></span>

### <span data-ttu-id="07f89-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f89-111">-CdnEndpoint</span></span>
<span data-ttu-id="07f89-112">Anger det CDN-slutobjekt som den anpassade domänen läggs till för.</span><span class="sxs-lookup"><span data-stu-id="07f89-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="07f89-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="07f89-113">-CustomDomainName</span></span>
<span data-ttu-id="07f89-114">Anger resurs namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="07f89-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="07f89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f89-115">-DefaultProfile</span></span>
<span data-ttu-id="07f89-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="07f89-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07f89-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="07f89-117">-EndpointName</span></span>
<span data-ttu-id="07f89-118">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="07f89-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="07f89-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="07f89-119">-HostName</span></span>
<span data-ttu-id="07f89-120">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="07f89-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="07f89-121">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="07f89-121">-ProfileName</span></span>
<span data-ttu-id="07f89-122">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="07f89-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="07f89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f89-123">-ResourceGroupName</span></span>
<span data-ttu-id="07f89-124">Anger namnet på den resurs grupp som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="07f89-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="07f89-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07f89-125">-Confirm</span></span>
<span data-ttu-id="07f89-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07f89-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f89-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f89-127">-WhatIf</span></span>
<span data-ttu-id="07f89-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07f89-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f89-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07f89-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f89-130">CommonParameters</span></span>
<span data-ttu-id="07f89-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f89-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f89-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f89-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07f89-133">INPUTS</span></span>

### <span data-ttu-id="07f89-134">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f89-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="07f89-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07f89-135">OUTPUTS</span></span>

### <span data-ttu-id="07f89-136">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f89-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="07f89-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07f89-137">NOTES</span></span>

## <span data-ttu-id="07f89-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07f89-138">RELATED LINKS</span></span>

[<span data-ttu-id="07f89-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f89-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="07f89-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f89-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="07f89-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f89-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


