---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088703"
---
# <span data-ttu-id="046d6-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="046d6-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="046d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="046d6-102">SYNOPSIS</span></span>
<span data-ttu-id="046d6-103">Inaktiverar den anpassade domänen HTTPS (inaktuell).</span><span class="sxs-lookup"><span data-stu-id="046d6-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="046d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="046d6-104">SYNTAX</span></span>

### <span data-ttu-id="046d6-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="046d6-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="046d6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="046d6-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046d6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="046d6-107">DESCRIPTION</span></span>
<span data-ttu-id="046d6-108">Cmdleten **disable-AzCdnCustomDomain** inaktiverar den SÄKERSTÄLLda https-leveransen av en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="046d6-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="046d6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="046d6-109">EXAMPLES</span></span>

### <span data-ttu-id="046d6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="046d6-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="046d6-111">Inaktivera HTTPS-leverans av den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="046d6-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="046d6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="046d6-112">PARAMETERS</span></span>

### <span data-ttu-id="046d6-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="046d6-113">-CustomDomainName</span></span>
<span data-ttu-id="046d6-114">Namn på den anpassade domänen för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="046d6-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="046d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046d6-115">-DefaultProfile</span></span>
<span data-ttu-id="046d6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="046d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="046d6-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="046d6-117">-EndpointName</span></span>
<span data-ttu-id="046d6-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="046d6-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="046d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="046d6-119">-InputObject</span></span>
<span data-ttu-id="046d6-120">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="046d6-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="046d6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="046d6-121">-PassThru</span></span>
<span data-ttu-id="046d6-122">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="046d6-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046d6-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="046d6-123">-ProfileName</span></span>
<span data-ttu-id="046d6-124">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="046d6-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="046d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="046d6-126">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="046d6-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="046d6-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="046d6-127">-Confirm</span></span>
<span data-ttu-id="046d6-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="046d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046d6-129">-WhatIf</span></span>
<span data-ttu-id="046d6-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="046d6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="046d6-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="046d6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046d6-132">CommonParameters</span></span>
<span data-ttu-id="046d6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046d6-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="046d6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046d6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="046d6-135">INPUTS</span></span>

### <span data-ttu-id="046d6-136">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="046d6-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="046d6-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="046d6-137">OUTPUTS</span></span>

### <span data-ttu-id="046d6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="046d6-138">System.Boolean</span></span>

## <span data-ttu-id="046d6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="046d6-139">NOTES</span></span>

## <span data-ttu-id="046d6-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="046d6-140">RELATED LINKS</span></span>
