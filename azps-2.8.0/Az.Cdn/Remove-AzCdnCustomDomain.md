---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: c2259cdf42fc0f1065b37736dddea1d214b2ecb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745301"
---
# <span data-ttu-id="78118-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78118-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="78118-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78118-102">SYNOPSIS</span></span>
<span data-ttu-id="78118-103">Tar bort en egen domän.</span><span class="sxs-lookup"><span data-stu-id="78118-103">Removes a custom domain.</span></span>

## <span data-ttu-id="78118-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78118-104">SYNTAX</span></span>

### <span data-ttu-id="78118-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="78118-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78118-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78118-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78118-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78118-107">DESCRIPTION</span></span>
<span data-ttu-id="78118-108">Cmdleten **Remove-AzCdnCustomDomain** tar bort den anpassade domänen från en slut punkt för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="78118-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="78118-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78118-109">EXAMPLES</span></span>

## <span data-ttu-id="78118-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78118-110">PARAMETERS</span></span>

### <span data-ttu-id="78118-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78118-111">-CdnCustomDomain</span></span>
<span data-ttu-id="78118-112">Anger den anpassade domän som ska tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78118-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="78118-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="78118-113">-CustomDomainName</span></span>
<span data-ttu-id="78118-114">Anger resurs namnet på den anpassade domän där denna cmdlet ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="78118-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="78118-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78118-115">-DefaultProfile</span></span>
<span data-ttu-id="78118-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="78118-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78118-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="78118-117">-EndpointName</span></span>
<span data-ttu-id="78118-118">Anger namnet på den slut punkt från vilken denna cmdlet tar bort en egen domän.</span><span class="sxs-lookup"><span data-stu-id="78118-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="78118-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78118-119">-PassThru</span></span>
<span data-ttu-id="78118-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="78118-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78118-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="78118-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78118-122">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="78118-122">-ProfileName</span></span>
<span data-ttu-id="78118-123">Anger namnet på den profil som cmdleten tar bort en egen domän från.</span><span class="sxs-lookup"><span data-stu-id="78118-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="78118-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78118-124">-ResourceGroupName</span></span>
<span data-ttu-id="78118-125">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en egen domän.</span><span class="sxs-lookup"><span data-stu-id="78118-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="78118-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78118-126">-Confirm</span></span>
<span data-ttu-id="78118-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78118-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78118-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78118-128">-WhatIf</span></span>
<span data-ttu-id="78118-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78118-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78118-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78118-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78118-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78118-131">CommonParameters</span></span>
<span data-ttu-id="78118-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78118-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78118-133">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78118-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78118-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78118-134">INPUTS</span></span>

### <span data-ttu-id="78118-135">Microsoft. Azure. commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78118-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="78118-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78118-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78118-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78118-137">OUTPUTS</span></span>

### <span data-ttu-id="78118-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78118-138">System.Boolean</span></span>

## <span data-ttu-id="78118-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78118-139">NOTES</span></span>

## <span data-ttu-id="78118-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78118-140">RELATED LINKS</span></span>

[<span data-ttu-id="78118-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78118-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="78118-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78118-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="78118-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78118-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


