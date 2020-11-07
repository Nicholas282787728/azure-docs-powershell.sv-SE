---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: bc37d6c6c9be6278cc2e27782000ad242ac07a2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745319"
---
# <span data-ttu-id="7f93a-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7f93a-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="7f93a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f93a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f93a-103">Skapar en egen domän för en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="7f93a-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="7f93a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f93a-104">SYNTAX</span></span>

### <span data-ttu-id="7f93a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7f93a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f93a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f93a-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f93a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f93a-107">DESCRIPTION</span></span>
<span data-ttu-id="7f93a-108">Cmdleten **New-AzCdnCustomDomain** skapar en anpassad domän för slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="7f93a-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7f93a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f93a-109">EXAMPLES</span></span>

## <span data-ttu-id="7f93a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f93a-110">PARAMETERS</span></span>

### <span data-ttu-id="7f93a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f93a-111">-CdnEndpoint</span></span>
<span data-ttu-id="7f93a-112">Anger det CDN-slutobjekt som den anpassade domänen läggs till för.</span><span class="sxs-lookup"><span data-stu-id="7f93a-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="7f93a-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7f93a-113">-CustomDomainName</span></span>
<span data-ttu-id="7f93a-114">Anger resurs namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="7f93a-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="7f93a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f93a-115">-DefaultProfile</span></span>
<span data-ttu-id="7f93a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7f93a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f93a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f93a-117">-EndpointName</span></span>
<span data-ttu-id="7f93a-118">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="7f93a-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7f93a-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="7f93a-119">-HostName</span></span>
<span data-ttu-id="7f93a-120">Anger värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="7f93a-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="7f93a-121">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="7f93a-121">-ProfileName</span></span>
<span data-ttu-id="7f93a-122">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="7f93a-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7f93a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f93a-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f93a-124">Anger namnet på den resurs grupp som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="7f93a-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7f93a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f93a-125">-Confirm</span></span>
<span data-ttu-id="7f93a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f93a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f93a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f93a-127">-WhatIf</span></span>
<span data-ttu-id="7f93a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f93a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f93a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f93a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f93a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f93a-130">CommonParameters</span></span>
<span data-ttu-id="7f93a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f93a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f93a-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f93a-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f93a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f93a-133">INPUTS</span></span>

### <span data-ttu-id="7f93a-134">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f93a-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7f93a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f93a-135">OUTPUTS</span></span>

### <span data-ttu-id="7f93a-136">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7f93a-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="7f93a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f93a-137">NOTES</span></span>

## <span data-ttu-id="7f93a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f93a-138">RELATED LINKS</span></span>

[<span data-ttu-id="7f93a-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7f93a-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="7f93a-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7f93a-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="7f93a-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7f93a-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


