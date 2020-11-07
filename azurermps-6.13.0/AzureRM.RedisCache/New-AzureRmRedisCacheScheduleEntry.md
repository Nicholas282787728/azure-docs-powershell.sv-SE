---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 8364a3a8b9d88bfd3ce34f2e70f8fcae80e9b612
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581672"
---
# <span data-ttu-id="eb33c-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="eb33c-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="eb33c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb33c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb33c-103">Skapar en schema post.</span><span class="sxs-lookup"><span data-stu-id="eb33c-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb33c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb33c-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb33c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb33c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb33c-106">Cmdleten **New-AzureRmRedisCacheScheduleEntry** skapar ett **PSScheduleEntry** -objekt.</span><span class="sxs-lookup"><span data-stu-id="eb33c-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="eb33c-107">Azure Redis cache-korrigering Schemalägg cmdlets, till exempel New-AzureRmRedisCachePatchSchedule cmdlet, kräver schemaläggning av objekt.</span><span class="sxs-lookup"><span data-stu-id="eb33c-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="eb33c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb33c-108">EXAMPLES</span></span>

### <span data-ttu-id="eb33c-109">Exempel 1: skapa en schema post för helger</span><span class="sxs-lookup"><span data-stu-id="eb33c-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="eb33c-110">Det här kommandot skapar ett **PSScheduleEntry** -objekt som representerar ett helg schema med angiven start tid och det angivna fönstret.</span><span class="sxs-lookup"><span data-stu-id="eb33c-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="eb33c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb33c-111">PARAMETERS</span></span>

### <span data-ttu-id="eb33c-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="eb33c-112">-DayOfWeek</span></span>
<span data-ttu-id="eb33c-113">Anger vecko dagen för schema posten.</span><span class="sxs-lookup"><span data-stu-id="eb33c-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="eb33c-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="eb33c-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb33c-115">Vardaglig</span><span class="sxs-lookup"><span data-stu-id="eb33c-115">Everyday</span></span> 
- <span data-ttu-id="eb33c-116">Migration</span><span class="sxs-lookup"><span data-stu-id="eb33c-116">Weekend</span></span> 
- <span data-ttu-id="eb33c-117">Dagarna</span><span class="sxs-lookup"><span data-stu-id="eb33c-117">Monday</span></span> 
- <span data-ttu-id="eb33c-118">Torsdag</span><span class="sxs-lookup"><span data-stu-id="eb33c-118">Tuesday</span></span> 
- <span data-ttu-id="eb33c-119">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="eb33c-119">Wednesday</span></span> 
- <span data-ttu-id="eb33c-120">Torsdag</span><span class="sxs-lookup"><span data-stu-id="eb33c-120">Thursday</span></span> 
- <span data-ttu-id="eb33c-121">Fredag</span><span class="sxs-lookup"><span data-stu-id="eb33c-121">Friday</span></span> 
- <span data-ttu-id="eb33c-122">Afton</span><span class="sxs-lookup"><span data-stu-id="eb33c-122">Saturday</span></span> 
- <span data-ttu-id="eb33c-123">Lördag</span><span class="sxs-lookup"><span data-stu-id="eb33c-123">Sunday</span></span>

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

### <span data-ttu-id="eb33c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb33c-124">-DefaultProfile</span></span>
<span data-ttu-id="eb33c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb33c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb33c-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="eb33c-126">-MaintenanceWindow</span></span>
<span data-ttu-id="eb33c-127">Anger hur länge fönster tillåts för uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="eb33c-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="eb33c-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="eb33c-128">-StartHourUtc</span></span>
<span data-ttu-id="eb33c-129">Anger en timme på dagen då schemat startar.</span><span class="sxs-lookup"><span data-stu-id="eb33c-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="eb33c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb33c-130">CommonParameters</span></span>
<span data-ttu-id="eb33c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb33c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb33c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb33c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb33c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb33c-133">INPUTS</span></span>

### <span data-ttu-id="eb33c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eb33c-134">System.String</span></span>

### <span data-ttu-id="eb33c-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="eb33c-135">System.Int32</span></span>

### <span data-ttu-id="eb33c-136">System. Nullable ' 1 [[system. TimeSpan, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="eb33c-136">System.Nullable\`1[[System.TimeSpan, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="eb33c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb33c-137">OUTPUTS</span></span>

### <span data-ttu-id="eb33c-138">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="eb33c-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="eb33c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb33c-139">NOTES</span></span>
* <span data-ttu-id="eb33c-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="eb33c-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="eb33c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb33c-141">RELATED LINKS</span></span>

[<span data-ttu-id="eb33c-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="eb33c-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="eb33c-143">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="eb33c-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="eb33c-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="eb33c-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)

