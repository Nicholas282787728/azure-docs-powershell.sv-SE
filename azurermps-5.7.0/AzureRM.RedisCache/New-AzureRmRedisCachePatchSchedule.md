---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573323"
---
# <span data-ttu-id="746a8-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="746a8-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="746a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="746a8-102">SYNOPSIS</span></span>
<span data-ttu-id="746a8-103">Lägger till ett uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="746a8-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="746a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="746a8-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="746a8-105">DESCRIPTION</span></span>
<span data-ttu-id="746a8-106">Cmdleten **New-AzureRmRedisCachePatchSchedule** lägger till ett uppdaterings schema i ett cache i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="746a8-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="746a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="746a8-107">EXAMPLES</span></span>

### <span data-ttu-id="746a8-108">Exempel 1: skapa och lägga till ett uppdaterings schema i cachen</span><span class="sxs-lookup"><span data-stu-id="746a8-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="746a8-109">Det här kommandot lägger till ett uppdaterings schema i cachen med namnet RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="746a8-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="746a8-110">Parametern värden tar ett kommando som använder **nya-AzureRmRedisCacheScheduleEntry** för att skapa ett schema.</span><span class="sxs-lookup"><span data-stu-id="746a8-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="746a8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="746a8-111">PARAMETERS</span></span>

### <span data-ttu-id="746a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746a8-112">-DefaultProfile</span></span>
<span data-ttu-id="746a8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="746a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746a8-114">-Poster</span><span class="sxs-lookup"><span data-stu-id="746a8-114">-Entries</span></span>
<span data-ttu-id="746a8-115">Anger en matris med scheman som denna cmdlet ställer in i cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="746a8-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="746a8-116">För att hämta ett **PSScheduleEntry** -objekt, Använd cmdleten New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="746a8-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746a8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="746a8-117">-Name</span></span>
<span data-ttu-id="746a8-118">Anger namnet på cachen.</span><span class="sxs-lookup"><span data-stu-id="746a8-118">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="746a8-120">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="746a8-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746a8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="746a8-121">-Confirm</span></span>
<span data-ttu-id="746a8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="746a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746a8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746a8-123">-WhatIf</span></span>
<span data-ttu-id="746a8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="746a8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="746a8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="746a8-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746a8-126">CommonParameters</span></span>
<span data-ttu-id="746a8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746a8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="746a8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746a8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="746a8-129">INPUTS</span></span>

### <span data-ttu-id="746a8-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="746a8-130">None</span></span>
<span data-ttu-id="746a8-131">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="746a8-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="746a8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="746a8-132">OUTPUTS</span></span>

### <span data-ttu-id="746a8-133">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="746a8-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="746a8-134">Den här cmdleten returnerar de ändrings schema poster som är inställda i cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="746a8-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="746a8-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="746a8-135">NOTES</span></span>
* <span data-ttu-id="746a8-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="746a8-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="746a8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="746a8-137">RELATED LINKS</span></span>

[<span data-ttu-id="746a8-138">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="746a8-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="746a8-139">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="746a8-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="746a8-140">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="746a8-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


