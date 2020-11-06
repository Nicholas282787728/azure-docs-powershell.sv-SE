---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578968"
---
# <span data-ttu-id="a4998-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a4998-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="a4998-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4998-102">SYNOPSIS</span></span>
<span data-ttu-id="a4998-103">Inaktiverar anpassad HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a4998-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4998-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4998-104">SYNTAX</span></span>

### <span data-ttu-id="a4998-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a4998-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4998-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4998-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4998-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4998-107">DESCRIPTION</span></span>
<span data-ttu-id="a4998-108">Cmdleten **disable-AzureRmCdnCustomDomain** inaktiverar den SÄKERSTÄLLda https-leveransen av en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="a4998-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="a4998-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4998-109">EXAMPLES</span></span>

### <span data-ttu-id="a4998-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4998-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="a4998-111">Inaktivera HTTPS-leverans av den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="a4998-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="a4998-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4998-112">PARAMETERS</span></span>

### <span data-ttu-id="a4998-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a4998-113">-CustomDomainName</span></span>
<span data-ttu-id="a4998-114">Namn på den anpassade domänen för Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a4998-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="a4998-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4998-115">-DefaultProfile</span></span>
<span data-ttu-id="a4998-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4998-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4998-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a4998-117">-EndpointName</span></span>
<span data-ttu-id="a4998-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="a4998-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a4998-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4998-119">-InputObject</span></span>
<span data-ttu-id="a4998-120">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="a4998-120">The custom domain object.</span></span>

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

### <span data-ttu-id="a4998-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4998-121">-PassThru</span></span>
<span data-ttu-id="a4998-122">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="a4998-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="a4998-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="a4998-123">-ProfileName</span></span>
<span data-ttu-id="a4998-124">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="a4998-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a4998-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4998-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4998-126">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="a4998-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a4998-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4998-127">-Confirm</span></span>
<span data-ttu-id="a4998-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4998-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4998-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4998-129">-WhatIf</span></span>
<span data-ttu-id="a4998-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4998-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4998-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4998-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4998-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4998-132">CommonParameters</span></span>
<span data-ttu-id="a4998-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4998-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4998-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4998-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4998-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4998-135">INPUTS</span></span>

### <span data-ttu-id="a4998-136">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a4998-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="a4998-137">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4998-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a4998-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4998-138">OUTPUTS</span></span>

### <span data-ttu-id="a4998-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4998-139">System.Boolean</span></span>

## <span data-ttu-id="a4998-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4998-140">NOTES</span></span>

## <span data-ttu-id="a4998-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4998-141">RELATED LINKS</span></span>
