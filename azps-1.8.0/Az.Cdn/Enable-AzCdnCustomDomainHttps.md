---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 87c6928b6b1a8863bdde7126b782d07d4c496207
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754654"
---
# <span data-ttu-id="4638d-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="4638d-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="4638d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4638d-102">SYNOPSIS</span></span>
<span data-ttu-id="4638d-103">Aktiverar anpassad HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4638d-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="4638d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4638d-104">SYNTAX</span></span>

### <span data-ttu-id="4638d-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4638d-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4638d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4638d-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4638d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4638d-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4638d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4638d-108">DESCRIPTION</span></span>
<span data-ttu-id="4638d-109">Cmdleten **Enable-AzCdnCustomDomainHttps** aktiverar den SÄKERSTÄLLda https-leveransen av en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="4638d-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="4638d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4638d-110">EXAMPLES</span></span>

### <span data-ttu-id="4638d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4638d-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="4638d-112">Aktivera säker leverans av den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="4638d-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="4638d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4638d-113">PARAMETERS</span></span>

### <span data-ttu-id="4638d-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4638d-114">-CustomDomainName</span></span>
<span data-ttu-id="4638d-115">Namn på den anpassade domänen för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4638d-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="4638d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4638d-116">-DefaultProfile</span></span>
<span data-ttu-id="4638d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4638d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4638d-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4638d-118">-EndpointName</span></span>
<span data-ttu-id="4638d-119">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="4638d-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4638d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4638d-120">-InputObject</span></span>
<span data-ttu-id="4638d-121">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="4638d-121">The custom domain object.</span></span>

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

### <span data-ttu-id="4638d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4638d-122">-PassThru</span></span>
<span data-ttu-id="4638d-123">Returnera objekt om det anges.</span><span class="sxs-lookup"><span data-stu-id="4638d-123">Return object if specified.</span></span>

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

### <span data-ttu-id="4638d-124">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="4638d-124">-ProfileName</span></span>
<span data-ttu-id="4638d-125">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="4638d-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4638d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4638d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4638d-127">Resurs gruppen för Azure CDN-profilen</span><span class="sxs-lookup"><span data-stu-id="4638d-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="4638d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4638d-128">-ResourceId</span></span>
<span data-ttu-id="4638d-129">ResourceId för den anpassade domänen</span><span class="sxs-lookup"><span data-stu-id="4638d-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4638d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4638d-130">-Confirm</span></span>
<span data-ttu-id="4638d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4638d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4638d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4638d-132">-WhatIf</span></span>
<span data-ttu-id="4638d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4638d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4638d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4638d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4638d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4638d-135">CommonParameters</span></span>
<span data-ttu-id="4638d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4638d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4638d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4638d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4638d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4638d-138">INPUTS</span></span>

### <span data-ttu-id="4638d-139">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4638d-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="4638d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4638d-140">System.String</span></span>

## <span data-ttu-id="4638d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4638d-141">OUTPUTS</span></span>

### <span data-ttu-id="4638d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4638d-142">System.Boolean</span></span>

## <span data-ttu-id="4638d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4638d-143">NOTES</span></span>

## <span data-ttu-id="4638d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4638d-144">RELATED LINKS</span></span>