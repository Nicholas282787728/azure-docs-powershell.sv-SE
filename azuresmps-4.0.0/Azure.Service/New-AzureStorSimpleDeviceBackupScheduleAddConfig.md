---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093254"
---
# <span data-ttu-id="72022-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="72022-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="72022-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72022-102">SYNOPSIS</span></span>
<span data-ttu-id="72022-103">Skapar ett konfigurations objekt för säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="72022-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="72022-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72022-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="72022-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72022-105">DESCRIPTION</span></span>
<span data-ttu-id="72022-106">Cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** skapar ett **BackupScheduleBase** -konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="72022-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="72022-107">Använd det här konfigurationsobjektet för att skapa en ny säkerhets kopierings princip genom att använda cmdlet **New-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="72022-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="72022-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72022-108">EXAMPLES</span></span>

### <span data-ttu-id="72022-109">Exempel 1: skapa ett konfigurations objekt för säkerhets kopior</span><span class="sxs-lookup"><span data-stu-id="72022-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="72022-110">Det här kommandot skapar ett bas objekt för säkerhets kopierings schema för säkerhets kopiering av moln ögonblick.</span><span class="sxs-lookup"><span data-stu-id="72022-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="72022-111">Säkerhets kopian sker varje dag och säkerhets kopiorna behålls i 100 dagar.</span><span class="sxs-lookup"><span data-stu-id="72022-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="72022-112">Detta schema är aktiverat från standard tiden, vilket är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="72022-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="72022-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72022-113">PARAMETERS</span></span>

### <span data-ttu-id="72022-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="72022-114">-BackupType</span></span>
<span data-ttu-id="72022-115">Anger säkerhets kopierings typen.</span><span class="sxs-lookup"><span data-stu-id="72022-115">Specifies the backup type.</span></span>
<span data-ttu-id="72022-116">Giltiga värden är: LocalSnapshot och CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="72022-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="72022-117">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="72022-117">-Enabled</span></span>
<span data-ttu-id="72022-118">Anger om säkerhets kopierings schema ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="72022-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72022-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="72022-119">-Profile</span></span>
<span data-ttu-id="72022-120">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="72022-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="72022-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="72022-121">-RecurrenceType</span></span>
<span data-ttu-id="72022-122">Anger den återkommande typen för detta säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="72022-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="72022-123">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="72022-123">Valid values are:</span></span> 

- <span data-ttu-id="72022-124">Protokoll</span><span class="sxs-lookup"><span data-stu-id="72022-124">Minutes</span></span>
- <span data-ttu-id="72022-125">Tim</span><span class="sxs-lookup"><span data-stu-id="72022-125">Hourly</span></span>
- <span data-ttu-id="72022-126">Vardag</span><span class="sxs-lookup"><span data-stu-id="72022-126">Daily</span></span>
- <span data-ttu-id="72022-127">Vecko</span><span class="sxs-lookup"><span data-stu-id="72022-127">Weekly</span></span>

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

### <span data-ttu-id="72022-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="72022-128">-RecurrenceValue</span></span>
<span data-ttu-id="72022-129">Anger hur ofta du vill göra en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="72022-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="72022-130">Den här parametern använder enheten som anges av parametern *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="72022-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="72022-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="72022-131">-RetentionCount</span></span>
<span data-ttu-id="72022-132">Anger antalet dagar som en säkerhets kopia ska behållas.</span><span class="sxs-lookup"><span data-stu-id="72022-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="72022-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="72022-133">-StartFromDateTime</span></span>
<span data-ttu-id="72022-134">Anger det datum från vilket du vill börja skapa säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="72022-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="72022-135">Standardvärdet är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="72022-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="72022-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72022-136">CommonParameters</span></span>
<span data-ttu-id="72022-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72022-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72022-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72022-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72022-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72022-139">INPUTS</span></span>

### <span data-ttu-id="72022-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="72022-140">None</span></span>

## <span data-ttu-id="72022-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72022-141">OUTPUTS</span></span>

### <span data-ttu-id="72022-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="72022-142">BackupScheduleBase</span></span>
<span data-ttu-id="72022-143">Denna cmdlet returnerar ett **BackupScheduleBase** -objekt.</span><span class="sxs-lookup"><span data-stu-id="72022-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="72022-144">Använd en **BackupScheduleBase** för att skapa en ny säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="72022-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="72022-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72022-145">NOTES</span></span>

## <span data-ttu-id="72022-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72022-146">RELATED LINKS</span></span>

[<span data-ttu-id="72022-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="72022-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="72022-148">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="72022-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


