---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: c3970b61d53b6afdd214aca5c4ca89c735377713
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917585"
---
# <span data-ttu-id="c7201-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c7201-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="c7201-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7201-102">SYNOPSIS</span></span>
<span data-ttu-id="c7201-103">Inaktiverar den anpassade domänen HTTPS (inaktuell).</span><span class="sxs-lookup"><span data-stu-id="c7201-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="c7201-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7201-104">SYNTAX</span></span>

### <span data-ttu-id="c7201-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c7201-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7201-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7201-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7201-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7201-107">DESCRIPTION</span></span>
<span data-ttu-id="c7201-108">Cmdleten **disable-AzCdnCustomDomain** inaktiverar den SÄKERSTÄLLda https-leveransen av en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="c7201-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="c7201-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7201-109">EXAMPLES</span></span>

### <span data-ttu-id="c7201-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7201-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="c7201-111">Inaktivera HTTPS-leverans av den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="c7201-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="c7201-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7201-112">PARAMETERS</span></span>

### <span data-ttu-id="c7201-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c7201-113">-CustomDomainName</span></span>
<span data-ttu-id="c7201-114">Namn på den anpassade domänen för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c7201-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="c7201-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7201-115">-DefaultProfile</span></span>
<span data-ttu-id="c7201-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7201-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7201-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c7201-117">-EndpointName</span></span>
<span data-ttu-id="c7201-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="c7201-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c7201-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7201-119">-InputObject</span></span>
<span data-ttu-id="c7201-120">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="c7201-120">The custom domain object.</span></span>

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

### <span data-ttu-id="c7201-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7201-121">-PassThru</span></span>
<span data-ttu-id="c7201-122">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="c7201-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="c7201-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="c7201-123">-ProfileName</span></span>
<span data-ttu-id="c7201-124">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="c7201-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c7201-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7201-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7201-126">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="c7201-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c7201-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7201-127">-Confirm</span></span>
<span data-ttu-id="c7201-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7201-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7201-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7201-129">-WhatIf</span></span>
<span data-ttu-id="c7201-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7201-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7201-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7201-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7201-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7201-132">CommonParameters</span></span>
<span data-ttu-id="c7201-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7201-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7201-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7201-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7201-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7201-135">INPUTS</span></span>

### <span data-ttu-id="c7201-136">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c7201-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="c7201-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7201-137">OUTPUTS</span></span>

### <span data-ttu-id="c7201-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7201-138">System.Boolean</span></span>

## <span data-ttu-id="c7201-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7201-139">NOTES</span></span>

## <span data-ttu-id="c7201-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7201-140">RELATED LINKS</span></span>
