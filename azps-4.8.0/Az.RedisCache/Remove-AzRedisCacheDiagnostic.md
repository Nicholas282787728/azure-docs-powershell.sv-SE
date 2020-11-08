---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260423"
---
# <span data-ttu-id="1c147-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c147-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="1c147-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c147-102">SYNOPSIS</span></span>
<span data-ttu-id="1c147-103">Inaktiverar diagnostik på en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="1c147-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="1c147-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c147-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c147-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c147-105">DESCRIPTION</span></span>
<span data-ttu-id="1c147-106">Cmdleten **Remove-AzRedisCacheDiagnostic** inaktiverar diagnostik på en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="1c147-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="1c147-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c147-107">EXAMPLES</span></span>

### <span data-ttu-id="1c147-108">Exempel 1: inaktivera diagnostik</span><span class="sxs-lookup"><span data-stu-id="1c147-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="1c147-109">Det här kommandot inaktiverar diagnostik i angivet Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="1c147-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="1c147-110">Detta inaktiverar diagnostik för alla Azure Redis-cacheminnen i samma region för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1c147-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="1c147-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c147-111">PARAMETERS</span></span>

### <span data-ttu-id="1c147-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c147-112">-DefaultProfile</span></span>
<span data-ttu-id="1c147-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c147-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c147-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c147-114">-Name</span></span>
<span data-ttu-id="1c147-115">Anger namnet på cachen.</span><span class="sxs-lookup"><span data-stu-id="1c147-115">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c147-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c147-116">-ResourceGroupName</span></span>
<span data-ttu-id="1c147-117">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="1c147-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c147-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c147-118">-Confirm</span></span>
<span data-ttu-id="1c147-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c147-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c147-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c147-120">-WhatIf</span></span>
<span data-ttu-id="1c147-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c147-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c147-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c147-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c147-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c147-123">CommonParameters</span></span>
<span data-ttu-id="1c147-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c147-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c147-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c147-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c147-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c147-126">INPUTS</span></span>

### <span data-ttu-id="1c147-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1c147-127">System.String</span></span>

## <span data-ttu-id="1c147-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c147-128">OUTPUTS</span></span>

### <span data-ttu-id="1c147-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="1c147-129">System.Void</span></span>

## <span data-ttu-id="1c147-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c147-130">NOTES</span></span>
* <span data-ttu-id="1c147-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="1c147-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1c147-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c147-132">RELATED LINKS</span></span>

[<span data-ttu-id="1c147-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c147-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


