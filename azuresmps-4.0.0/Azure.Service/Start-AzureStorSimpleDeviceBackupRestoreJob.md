---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093473"
---
# <span data-ttu-id="622b7-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="622b7-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="622b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="622b7-102">SYNOPSIS</span></span>
<span data-ttu-id="622b7-103">Startar ett jobb som återställer en säkerhets kopia på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="622b7-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="622b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="622b7-104">SYNTAX</span></span>

### <span data-ttu-id="622b7-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="622b7-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="622b7-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="622b7-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="622b7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="622b7-107">DESCRIPTION</span></span>
<span data-ttu-id="622b7-108">Cmdleten **Start-AzureStorSimpleDeviceBackupRestoreJob** startar ett jobb som återställer en säkerhets kopia på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="622b7-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="622b7-109">Ange ett säkerhets kopie-ID och valfritt ögonblicks bild-ID.</span><span class="sxs-lookup"><span data-stu-id="622b7-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="622b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="622b7-110">EXAMPLES</span></span>

### <span data-ttu-id="622b7-111">Exempel 1: starta ett jobb för att återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="622b7-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="622b7-112">Det här kommandot startar ett jobb som återställer det säkerhetskopierade objekt som har det angivna ID: t och dess tillhör ande stillbilder på den enhet som heter Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="622b7-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="622b7-113">Kommandot anger parametern *WaitForComplete* , så jobbet slutar innan cmdleten returnerar kontrollen till konsolen.</span><span class="sxs-lookup"><span data-stu-id="622b7-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="622b7-114">Exempel 2: starta ett jobb för att återställa en viss ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="622b7-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="622b7-115">Det här kommandot startar ett jobb som återställer ögonblicks bilden med det angivna ID: t.</span><span class="sxs-lookup"><span data-stu-id="622b7-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="622b7-116">Kommandot anger säkerhetskopierat objekt efter ID på enheten med namnet Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="622b7-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="622b7-117">Kommandot anger parametern *Force* , så start jobbet startas utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="622b7-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="622b7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="622b7-118">PARAMETERS</span></span>

### <span data-ttu-id="622b7-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="622b7-119">-BackupId</span></span>
<span data-ttu-id="622b7-120">Anger instans-ID för säkerhets kopian som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="622b7-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="622b7-121">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="622b7-121">-DeviceName</span></span>
<span data-ttu-id="622b7-122">Anger namnet på den StorSimple-enhet där säkerhets kopian finns.</span><span class="sxs-lookup"><span data-stu-id="622b7-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="622b7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="622b7-123">-Force</span></span>
<span data-ttu-id="622b7-124">Anger att du inte behöver bekräfta med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="622b7-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b7-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="622b7-125">-Profile</span></span>
<span data-ttu-id="622b7-126">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="622b7-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="622b7-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="622b7-127">-SnapshotId</span></span>
<span data-ttu-id="622b7-128">Anger instans-ID för den ögonblicks bild som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="622b7-128">Specifies the instance ID of the snapshot to restore.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b7-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="622b7-129">-WaitForComplete</span></span>
<span data-ttu-id="622b7-130">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="622b7-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622b7-131">CommonParameters</span></span>
<span data-ttu-id="622b7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622b7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622b7-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622b7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622b7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="622b7-134">INPUTS</span></span>

### <span data-ttu-id="622b7-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="622b7-135">None</span></span>

## <span data-ttu-id="622b7-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="622b7-136">OUTPUTS</span></span>

### <span data-ttu-id="622b7-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="622b7-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="622b7-138">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="622b7-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="622b7-139">Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="622b7-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="622b7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="622b7-140">NOTES</span></span>

## <span data-ttu-id="622b7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="622b7-141">RELATED LINKS</span></span>

[<span data-ttu-id="622b7-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="622b7-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="622b7-143">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="622b7-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


