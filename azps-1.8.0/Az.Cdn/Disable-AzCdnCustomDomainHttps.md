---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 58ad23747583162643ee3a1ee7b0547311adcadf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754656"
---
# <span data-ttu-id="b6771-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="b6771-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="b6771-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6771-102">SYNOPSIS</span></span>
<span data-ttu-id="b6771-103">Inaktiverar anpassad domän HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b6771-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="b6771-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6771-104">SYNTAX</span></span>

### <span data-ttu-id="b6771-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b6771-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6771-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6771-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6771-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6771-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6771-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6771-108">DESCRIPTION</span></span>
<span data-ttu-id="b6771-109">Cmdleten **disable-AzCdnCustomDomainHttps** inaktiverar den SÄKERSTÄLLda https-leveransen av en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="b6771-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="b6771-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6771-110">EXAMPLES</span></span>

### <span data-ttu-id="b6771-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6771-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="b6771-112">Inaktivera säker leverans av den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="b6771-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="b6771-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6771-113">PARAMETERS</span></span>

### <span data-ttu-id="b6771-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b6771-114">-CustomDomainName</span></span>
<span data-ttu-id="b6771-115">Namn på den anpassade domänen för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="b6771-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="b6771-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6771-116">-DefaultProfile</span></span>
<span data-ttu-id="b6771-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6771-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6771-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b6771-118">-EndpointName</span></span>
<span data-ttu-id="b6771-119">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="b6771-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="b6771-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6771-120">-InputObject</span></span>
<span data-ttu-id="b6771-121">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="b6771-121">The custom domain object.</span></span>

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

### <span data-ttu-id="b6771-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6771-122">-PassThru</span></span>
<span data-ttu-id="b6771-123">Returnera objekt om det anges.</span><span class="sxs-lookup"><span data-stu-id="b6771-123">Return object if specified.</span></span>

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

### <span data-ttu-id="b6771-124">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="b6771-124">-ProfileName</span></span>
<span data-ttu-id="b6771-125">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="b6771-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="b6771-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6771-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6771-127">Resurs gruppen för Azure CDN-profilen</span><span class="sxs-lookup"><span data-stu-id="b6771-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="b6771-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6771-128">-ResourceId</span></span>
<span data-ttu-id="b6771-129">ResourceId för den anpassade domänen</span><span class="sxs-lookup"><span data-stu-id="b6771-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="b6771-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6771-130">-Confirm</span></span>
<span data-ttu-id="b6771-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6771-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6771-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6771-132">-WhatIf</span></span>
<span data-ttu-id="b6771-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6771-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6771-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6771-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6771-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6771-135">CommonParameters</span></span>
<span data-ttu-id="b6771-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6771-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6771-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6771-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6771-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6771-138">INPUTS</span></span>

### <span data-ttu-id="b6771-139">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b6771-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="b6771-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b6771-140">System.String</span></span>

## <span data-ttu-id="b6771-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6771-141">OUTPUTS</span></span>

### <span data-ttu-id="b6771-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6771-142">System.Boolean</span></span>

## <span data-ttu-id="b6771-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6771-143">NOTES</span></span>

## <span data-ttu-id="b6771-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6771-144">RELATED LINKS</span></span>
