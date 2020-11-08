---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100904"
---
# <span data-ttu-id="24042-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="24042-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="24042-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24042-102">SYNOPSIS</span></span>
<span data-ttu-id="24042-103">Lägger till ett uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="24042-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="24042-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24042-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24042-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24042-105">DESCRIPTION</span></span>
<span data-ttu-id="24042-106">Cmdleten **New-AzRedisCachePatchSchedule** lägger till ett uppdaterings schema i ett cache i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="24042-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="24042-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24042-107">EXAMPLES</span></span>

### <span data-ttu-id="24042-108">Exempel 1: skapa och lägga till ett uppdaterings schema i cachen</span><span class="sxs-lookup"><span data-stu-id="24042-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="24042-109">Det här kommandot lägger till ett uppdaterings schema i cachen med namnet RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="24042-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="24042-110">Parametern värden tar ett kommando som använder **nya-AzRedisCacheScheduleEntry** för att skapa ett schema.</span><span class="sxs-lookup"><span data-stu-id="24042-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="24042-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24042-111">PARAMETERS</span></span>

### <span data-ttu-id="24042-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24042-112">-DefaultProfile</span></span>
<span data-ttu-id="24042-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24042-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24042-114">-Poster</span><span class="sxs-lookup"><span data-stu-id="24042-114">-Entries</span></span>
<span data-ttu-id="24042-115">Anger en matris med scheman som denna cmdlet ställer in i cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="24042-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="24042-116">För att hämta ett **PSScheduleEntry** -objekt, Använd cmdleten New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="24042-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24042-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="24042-117">-Name</span></span>
<span data-ttu-id="24042-118">Anger namnet på cachen.</span><span class="sxs-lookup"><span data-stu-id="24042-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="24042-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24042-119">-ResourceGroupName</span></span>
<span data-ttu-id="24042-120">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="24042-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="24042-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24042-121">-Confirm</span></span>
<span data-ttu-id="24042-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24042-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24042-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24042-123">-WhatIf</span></span>
<span data-ttu-id="24042-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24042-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24042-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24042-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24042-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24042-126">CommonParameters</span></span>
<span data-ttu-id="24042-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24042-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24042-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24042-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24042-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24042-129">INPUTS</span></span>

### <span data-ttu-id="24042-130">System. String</span><span class="sxs-lookup"><span data-stu-id="24042-130">System.String</span></span>

### <span data-ttu-id="24042-131">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="24042-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="24042-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24042-132">OUTPUTS</span></span>

### <span data-ttu-id="24042-133">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="24042-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="24042-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24042-134">NOTES</span></span>
* <span data-ttu-id="24042-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="24042-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="24042-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24042-136">RELATED LINKS</span></span>

[<span data-ttu-id="24042-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="24042-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="24042-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="24042-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="24042-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="24042-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


