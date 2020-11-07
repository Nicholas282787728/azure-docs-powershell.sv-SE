---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927517"
---
# <span data-ttu-id="17983-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="17983-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="17983-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17983-102">SYNOPSIS</span></span>
<span data-ttu-id="17983-103">Skapar en schema post.</span><span class="sxs-lookup"><span data-stu-id="17983-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="17983-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17983-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17983-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17983-105">DESCRIPTION</span></span>
<span data-ttu-id="17983-106">Cmdleten **New-AzRedisCacheScheduleEntry** skapar ett **PSScheduleEntry** -objekt.</span><span class="sxs-lookup"><span data-stu-id="17983-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="17983-107">Azure Redis cache-korrigering Schemalägg cmdlets, till exempel New-AzRedisCachePatchSchedule cmdlet, kräver schemaläggning av objekt.</span><span class="sxs-lookup"><span data-stu-id="17983-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="17983-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17983-108">EXAMPLES</span></span>

### <span data-ttu-id="17983-109">Exempel 1: skapa en schema post för helger</span><span class="sxs-lookup"><span data-stu-id="17983-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="17983-110">Det här kommandot skapar ett **PSScheduleEntry** -objekt som representerar ett helg schema med angiven start tid och det angivna fönstret.</span><span class="sxs-lookup"><span data-stu-id="17983-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="17983-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17983-111">PARAMETERS</span></span>

### <span data-ttu-id="17983-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="17983-112">-DayOfWeek</span></span>
<span data-ttu-id="17983-113">Anger vecko dagen för schema posten.</span><span class="sxs-lookup"><span data-stu-id="17983-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="17983-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="17983-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17983-115">Vardaglig</span><span class="sxs-lookup"><span data-stu-id="17983-115">Everyday</span></span> 
- <span data-ttu-id="17983-116">Migration</span><span class="sxs-lookup"><span data-stu-id="17983-116">Weekend</span></span> 
- <span data-ttu-id="17983-117">Dagarna</span><span class="sxs-lookup"><span data-stu-id="17983-117">Monday</span></span> 
- <span data-ttu-id="17983-118">Torsdag</span><span class="sxs-lookup"><span data-stu-id="17983-118">Tuesday</span></span> 
- <span data-ttu-id="17983-119">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="17983-119">Wednesday</span></span> 
- <span data-ttu-id="17983-120">Torsdag</span><span class="sxs-lookup"><span data-stu-id="17983-120">Thursday</span></span> 
- <span data-ttu-id="17983-121">Fredag</span><span class="sxs-lookup"><span data-stu-id="17983-121">Friday</span></span> 
- <span data-ttu-id="17983-122">Afton</span><span class="sxs-lookup"><span data-stu-id="17983-122">Saturday</span></span> 
- <span data-ttu-id="17983-123">Lördag</span><span class="sxs-lookup"><span data-stu-id="17983-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17983-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17983-124">-DefaultProfile</span></span>
<span data-ttu-id="17983-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17983-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17983-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="17983-126">-MaintenanceWindow</span></span>
<span data-ttu-id="17983-127">Anger hur länge fönster tillåts för uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="17983-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17983-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="17983-128">-StartHourUtc</span></span>
<span data-ttu-id="17983-129">Anger en timme på dagen då schemat startar.</span><span class="sxs-lookup"><span data-stu-id="17983-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17983-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17983-130">CommonParameters</span></span>
<span data-ttu-id="17983-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17983-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17983-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17983-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17983-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17983-133">INPUTS</span></span>

### <span data-ttu-id="17983-134">System. String</span><span class="sxs-lookup"><span data-stu-id="17983-134">System.String</span></span>

### <span data-ttu-id="17983-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="17983-135">System.Int32</span></span>

### <span data-ttu-id="17983-136">System. Nullable ' 1 [[system. TimeSpan, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17983-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="17983-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17983-137">OUTPUTS</span></span>

### <span data-ttu-id="17983-138">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="17983-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="17983-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17983-139">NOTES</span></span>
* <span data-ttu-id="17983-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="17983-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="17983-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17983-141">RELATED LINKS</span></span>

[<span data-ttu-id="17983-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="17983-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="17983-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="17983-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="17983-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="17983-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


