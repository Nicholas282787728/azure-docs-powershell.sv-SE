---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093250"
---
# <span data-ttu-id="13aa8-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="13aa8-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="13aa8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="13aa8-103">Skapar ett schema för uppdatering av säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="13aa8-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="13aa8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13aa8-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13aa8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="13aa8-106">Cmdleten **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** skapar ett **BackupScheduleUpdateRequest** -konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="13aa8-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="13aa8-107">Använd det här konfigurationsobjektet för att uppdatera en säkerhets kopierings princip med cmdleten **set-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="13aa8-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="13aa8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13aa8-108">EXAMPLES</span></span>

### <span data-ttu-id="13aa8-109">Exempel 1: skapa en begäran om schemaläggning</span><span class="sxs-lookup"><span data-stu-id="13aa8-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="13aa8-110">Det här kommandot skapar en begäran om uppdatering av säkerhets kopior för schemat med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="13aa8-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="13aa8-111">Begäran är att göra ett schema för säkerhets kopiering av moln ögonblicks bilder som återkommer varje timme.</span><span class="sxs-lookup"><span data-stu-id="13aa8-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="13aa8-112">Säkerhets kopiorna bevaras i 50 dagar.</span><span class="sxs-lookup"><span data-stu-id="13aa8-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="13aa8-113">Detta schema är aktiverat från standard tiden, vilket är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="13aa8-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="13aa8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13aa8-114">PARAMETERS</span></span>

### <span data-ttu-id="13aa8-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="13aa8-115">-BackupType</span></span>
<span data-ttu-id="13aa8-116">Anger säkerhets kopierings typen.</span><span class="sxs-lookup"><span data-stu-id="13aa8-116">Specifies the backup type.</span></span>
<span data-ttu-id="13aa8-117">Giltiga värden är: LocalSnapshot och CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="13aa8-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-118">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="13aa8-118">-Enabled</span></span>
<span data-ttu-id="13aa8-119">Anger om säkerhets kopierings schema ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="13aa8-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-120">-ID</span><span class="sxs-lookup"><span data-stu-id="13aa8-120">-Id</span></span>
<span data-ttu-id="13aa8-121">Anger instans-ID för det säkerhets kopierings schema som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="13aa8-121">Specifies the instance ID of the backup schedule to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="13aa8-122">-Profile</span></span>
<span data-ttu-id="13aa8-123">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="13aa8-123">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="13aa8-124">-RecurrenceType</span></span>
<span data-ttu-id="13aa8-125">Anger den återkommande typen för detta säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="13aa8-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="13aa8-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="13aa8-126">Valid values are:</span></span> 

- <span data-ttu-id="13aa8-127">Protokoll</span><span class="sxs-lookup"><span data-stu-id="13aa8-127">Minutes</span></span>
- <span data-ttu-id="13aa8-128">Tim</span><span class="sxs-lookup"><span data-stu-id="13aa8-128">Hourly</span></span>
- <span data-ttu-id="13aa8-129">Vardag</span><span class="sxs-lookup"><span data-stu-id="13aa8-129">Daily</span></span>
- <span data-ttu-id="13aa8-130">Vecko</span><span class="sxs-lookup"><span data-stu-id="13aa8-130">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="13aa8-131">-RecurrenceValue</span></span>
<span data-ttu-id="13aa8-132">Anger hur ofta du vill göra en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="13aa8-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="13aa8-133">Den här parametern använder enheten som anges av parametern *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="13aa8-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="13aa8-134">-RetentionCount</span></span>
<span data-ttu-id="13aa8-135">Anger antalet dagar som en säkerhets kopia ska behållas.</span><span class="sxs-lookup"><span data-stu-id="13aa8-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="13aa8-136">-StartFromDateTime</span></span>
<span data-ttu-id="13aa8-137">Anger det datum från vilket du vill börja skapa säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="13aa8-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="13aa8-138">Standardvärdet är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="13aa8-138">The default value is the current time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13aa8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13aa8-139">CommonParameters</span></span>
<span data-ttu-id="13aa8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13aa8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13aa8-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13aa8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13aa8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13aa8-142">INPUTS</span></span>

### <span data-ttu-id="13aa8-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="13aa8-143">None</span></span>

## <span data-ttu-id="13aa8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13aa8-144">OUTPUTS</span></span>

### <span data-ttu-id="13aa8-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="13aa8-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="13aa8-146">Denna cmdlet returnerar ett **BackupScheduleUpdateRequest** -objekt som innehåller information om uppdaterade säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="13aa8-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="13aa8-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13aa8-147">NOTES</span></span>

## <span data-ttu-id="13aa8-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13aa8-148">RELATED LINKS</span></span>

[<span data-ttu-id="13aa8-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="13aa8-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="13aa8-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="13aa8-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


