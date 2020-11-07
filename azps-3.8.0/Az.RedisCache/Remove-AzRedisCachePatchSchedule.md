---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927505"
---
# <span data-ttu-id="37710-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="37710-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="37710-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37710-102">SYNOPSIS</span></span>
<span data-ttu-id="37710-103">Tar bort uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="37710-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="37710-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37710-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37710-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37710-105">DESCRIPTION</span></span>
<span data-ttu-id="37710-106">Cmdleten **Remove-AzRedisCachePatchSchedule** tar bort uppdaterings schema från cachen i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="37710-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="37710-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37710-107">EXAMPLES</span></span>

### <span data-ttu-id="37710-108">Exempel 1: ta bort uppdaterings schema</span><span class="sxs-lookup"><span data-stu-id="37710-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="37710-109">Det här kommandot tar bort uppdaterings schema från cachen som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="37710-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="37710-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37710-110">PARAMETERS</span></span>

### <span data-ttu-id="37710-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37710-111">-DefaultProfile</span></span>
<span data-ttu-id="37710-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37710-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37710-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="37710-113">-Name</span></span>
<span data-ttu-id="37710-114">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="37710-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="37710-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37710-115">-PassThru</span></span>
<span data-ttu-id="37710-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="37710-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="37710-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37710-117">-ResourceGroupName</span></span>
<span data-ttu-id="37710-118">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="37710-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="37710-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37710-119">-Confirm</span></span>
<span data-ttu-id="37710-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37710-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37710-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37710-121">-WhatIf</span></span>
<span data-ttu-id="37710-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37710-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37710-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37710-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37710-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37710-124">CommonParameters</span></span>
<span data-ttu-id="37710-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37710-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37710-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37710-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37710-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37710-127">INPUTS</span></span>

### <span data-ttu-id="37710-128">System. String</span><span class="sxs-lookup"><span data-stu-id="37710-128">System.String</span></span>

## <span data-ttu-id="37710-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37710-129">OUTPUTS</span></span>

### <span data-ttu-id="37710-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37710-130">System.Boolean</span></span>

## <span data-ttu-id="37710-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37710-131">NOTES</span></span>
* <span data-ttu-id="37710-132">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="37710-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="37710-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37710-133">RELATED LINKS</span></span>

[<span data-ttu-id="37710-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="37710-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="37710-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="37710-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="37710-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="37710-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


