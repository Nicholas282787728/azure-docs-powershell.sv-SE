---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 9eb2d3a0dfa960ecd3b3b66ce44a01de64d7f5bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755431"
---
# <span data-ttu-id="e5890-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e5890-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="e5890-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5890-102">SYNOPSIS</span></span>
<span data-ttu-id="e5890-103">Inaktiverar diagnostik på en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="e5890-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5890-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5890-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5890-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5890-105">DESCRIPTION</span></span>
<span data-ttu-id="e5890-106">Cmdleten **Remove-AzureRmRedisCacheDiagnostics** inaktiverar diagnostik på en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="e5890-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e5890-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5890-107">EXAMPLES</span></span>

### <span data-ttu-id="e5890-108">Exempel 1: inaktivera diagnostik</span><span class="sxs-lookup"><span data-stu-id="e5890-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="e5890-109">Det här kommandot inaktiverar diagnostik i angivet Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="e5890-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="e5890-110">Detta inaktiverar diagnostik för alla Azure Redis-cacheminnen i samma region för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e5890-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="e5890-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5890-111">PARAMETERS</span></span>

### <span data-ttu-id="e5890-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5890-112">-Name</span></span>
<span data-ttu-id="e5890-113">Anger namnet på cachen.</span><span class="sxs-lookup"><span data-stu-id="e5890-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="e5890-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5890-114">-ResourceGroupName</span></span>
<span data-ttu-id="e5890-115">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="e5890-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e5890-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5890-116">-Confirm</span></span>
<span data-ttu-id="e5890-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5890-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5890-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5890-118">-WhatIf</span></span>
<span data-ttu-id="e5890-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5890-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5890-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5890-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5890-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5890-121">-DefaultProfile</span></span>
<span data-ttu-id="e5890-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5890-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5890-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5890-123">CommonParameters</span></span>
<span data-ttu-id="e5890-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5890-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5890-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5890-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5890-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5890-126">INPUTS</span></span>

### <span data-ttu-id="e5890-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="e5890-127">None</span></span>

## <span data-ttu-id="e5890-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5890-128">OUTPUTS</span></span>

### <span data-ttu-id="e5890-129">Tom</span><span class="sxs-lookup"><span data-stu-id="e5890-129">Void</span></span>

## <span data-ttu-id="e5890-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5890-130">NOTES</span></span>
* <span data-ttu-id="e5890-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="e5890-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e5890-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5890-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5890-133">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e5890-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


