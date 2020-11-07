---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 2f43cfa1e10fe115f8bf5fc94404f532f04f6573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755242"
---
# <span data-ttu-id="07d21-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="07d21-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="07d21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07d21-102">SYNOPSIS</span></span>
<span data-ttu-id="07d21-103">Skapar en schema post.</span><span class="sxs-lookup"><span data-stu-id="07d21-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07d21-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07d21-105">DESCRIPTION</span></span>
<span data-ttu-id="07d21-106">Cmdleten **New-AzureRmRedisCacheScheduleEntry** skapar ett **PSScheduleEntry** -objekt.</span><span class="sxs-lookup"><span data-stu-id="07d21-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="07d21-107">Azure Redis cache-korrigering Schemalägg cmdlets, till exempel New-AzureRmRedisCachePatchSchedule cmdlet, kräver schemaläggning av objekt.</span><span class="sxs-lookup"><span data-stu-id="07d21-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="07d21-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07d21-108">EXAMPLES</span></span>

### <span data-ttu-id="07d21-109">Exempel 1: skapa en schema post för helger</span><span class="sxs-lookup"><span data-stu-id="07d21-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="07d21-110">Det här kommandot skapar ett **PSScheduleEntry** -objekt som representerar ett helg schema med angiven start tid och det angivna fönstret.</span><span class="sxs-lookup"><span data-stu-id="07d21-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="07d21-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07d21-111">PARAMETERS</span></span>

### <span data-ttu-id="07d21-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="07d21-112">-DayOfWeek</span></span>
<span data-ttu-id="07d21-113">Anger vecko dagen för schema posten.</span><span class="sxs-lookup"><span data-stu-id="07d21-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="07d21-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="07d21-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07d21-115">Vardaglig</span><span class="sxs-lookup"><span data-stu-id="07d21-115">Everyday</span></span> 
- <span data-ttu-id="07d21-116">Migration</span><span class="sxs-lookup"><span data-stu-id="07d21-116">Weekend</span></span> 
- <span data-ttu-id="07d21-117">Dagarna</span><span class="sxs-lookup"><span data-stu-id="07d21-117">Monday</span></span> 
- <span data-ttu-id="07d21-118">Torsdag</span><span class="sxs-lookup"><span data-stu-id="07d21-118">Tuesday</span></span> 
- <span data-ttu-id="07d21-119">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="07d21-119">Wednesday</span></span> 
- <span data-ttu-id="07d21-120">Torsdag</span><span class="sxs-lookup"><span data-stu-id="07d21-120">Thursday</span></span> 
- <span data-ttu-id="07d21-121">Fredag</span><span class="sxs-lookup"><span data-stu-id="07d21-121">Friday</span></span> 
- <span data-ttu-id="07d21-122">Afton</span><span class="sxs-lookup"><span data-stu-id="07d21-122">Saturday</span></span> 
- <span data-ttu-id="07d21-123">Lördag</span><span class="sxs-lookup"><span data-stu-id="07d21-123">Sunday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d21-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d21-124">-DefaultProfile</span></span>
<span data-ttu-id="07d21-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07d21-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d21-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="07d21-126">-MaintenanceWindow</span></span>
<span data-ttu-id="07d21-127">Anger hur länge fönster tillåts för uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="07d21-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d21-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="07d21-128">-StartHourUtc</span></span>
<span data-ttu-id="07d21-129">Anger en timme på dagen då schemat startar.</span><span class="sxs-lookup"><span data-stu-id="07d21-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d21-130">CommonParameters</span></span>
<span data-ttu-id="07d21-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d21-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d21-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d21-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07d21-133">INPUTS</span></span>

### <span data-ttu-id="07d21-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="07d21-134">None</span></span>
<span data-ttu-id="07d21-135">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="07d21-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="07d21-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07d21-136">OUTPUTS</span></span>

### <span data-ttu-id="07d21-137">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="07d21-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="07d21-138">Denna cmdlet returnerar ett objekt för schemaläggning.</span><span class="sxs-lookup"><span data-stu-id="07d21-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="07d21-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07d21-139">NOTES</span></span>
* <span data-ttu-id="07d21-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="07d21-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="07d21-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07d21-141">RELATED LINKS</span></span>

[<span data-ttu-id="07d21-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07d21-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="07d21-143">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07d21-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="07d21-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="07d21-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


