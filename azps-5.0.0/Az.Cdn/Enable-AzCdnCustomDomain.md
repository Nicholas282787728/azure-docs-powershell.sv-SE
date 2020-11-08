---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272441"
---
# <span data-ttu-id="e0a97-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e0a97-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="e0a97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0a97-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a97-103">Aktiverar anpassad HTTPS-domän (inaktuell).</span><span class="sxs-lookup"><span data-stu-id="e0a97-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="e0a97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0a97-104">SYNTAX</span></span>

### <span data-ttu-id="e0a97-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e0a97-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0a97-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0a97-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0a97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0a97-107">DESCRIPTION</span></span>
<span data-ttu-id="e0a97-108">Cmdleten **Enable-AzCdnCustomDomain** aktiverar den SÄKERSTÄLLda https-leveransen av en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="e0a97-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="e0a97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0a97-109">EXAMPLES</span></span>

### <span data-ttu-id="e0a97-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0a97-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="e0a97-111">Aktivera HTTPS-leverans av den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="e0a97-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="e0a97-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0a97-112">PARAMETERS</span></span>

### <span data-ttu-id="e0a97-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e0a97-113">-CustomDomainName</span></span>
<span data-ttu-id="e0a97-114">Namn på den anpassade domänen för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e0a97-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="e0a97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a97-115">-DefaultProfile</span></span>
<span data-ttu-id="e0a97-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0a97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0a97-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e0a97-117">-EndpointName</span></span>
<span data-ttu-id="e0a97-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="e0a97-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e0a97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0a97-119">-InputObject</span></span>
<span data-ttu-id="e0a97-120">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="e0a97-120">The custom domain object.</span></span>

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

### <span data-ttu-id="e0a97-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0a97-121">-PassThru</span></span>
<span data-ttu-id="e0a97-122">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="e0a97-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="e0a97-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="e0a97-123">-ProfileName</span></span>
<span data-ttu-id="e0a97-124">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="e0a97-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e0a97-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a97-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0a97-126">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="e0a97-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="e0a97-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0a97-127">-Confirm</span></span>
<span data-ttu-id="e0a97-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0a97-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0a97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a97-129">-WhatIf</span></span>
<span data-ttu-id="e0a97-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0a97-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0a97-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0a97-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0a97-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a97-132">CommonParameters</span></span>
<span data-ttu-id="e0a97-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0a97-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a97-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0a97-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a97-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0a97-135">INPUTS</span></span>

### <span data-ttu-id="e0a97-136">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e0a97-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="e0a97-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0a97-137">OUTPUTS</span></span>

### <span data-ttu-id="e0a97-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0a97-138">System.Boolean</span></span>

## <span data-ttu-id="e0a97-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0a97-139">NOTES</span></span>

## <span data-ttu-id="e0a97-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0a97-140">RELATED LINKS</span></span>
