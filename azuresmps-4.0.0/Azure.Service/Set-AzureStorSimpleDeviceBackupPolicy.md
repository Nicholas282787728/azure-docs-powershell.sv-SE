---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099082"
---
# <span data-ttu-id="35486-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="35486-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="35486-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35486-102">SYNOPSIS</span></span>
<span data-ttu-id="35486-103">Uppdaterar en befintlig säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="35486-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="35486-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35486-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="35486-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35486-105">DESCRIPTION</span></span>
<span data-ttu-id="35486-106">Cmdleten **set-AzureStorSimpleDeviceBackupPolicy** uppdaterar en befintlig säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="35486-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="35486-107">Du kan byta namn på principen, lägga till, uppdatera eller ta bort scheman och uppdatera de volymer som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="35486-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="35486-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35486-108">EXAMPLES</span></span>

### <span data-ttu-id="35486-109">Exempel 1: ändra namnet på en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="35486-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="35486-110">Det här kommandot ändrar namnet på säkerhets kopian som har angivet ID till UpdatedGeneralPolicy07.</span><span class="sxs-lookup"><span data-stu-id="35486-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="35486-111">Det här kommandot anger parametern *WaitForComplete* så att kommandot slutför uppgiften och returnerar sedan ett **TaskStatusInfo** -objekt för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="35486-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="35486-112">Exempel 2: uppdatera schemat för en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="35486-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="35486-113">Det första kommandot skapar ett Update-konfigurationsobjekt med hjälp av **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet och lagrar det sedan i $UpdateConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="35486-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="35486-114">Det andra kommandot skapar en ny mat ris variabel, namngiven $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="35486-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="35486-115">Med nästa kommando läggs uppdateringen som är lagrad i $UpdateConfig till i matrisen.</span><span class="sxs-lookup"><span data-stu-id="35486-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="35486-116">Du kan lägga till fler än en uppdatering av matrisen.</span><span class="sxs-lookup"><span data-stu-id="35486-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="35486-117">Det sista kommandot uppdaterar säkerhets kopierings principen som har angivet ID på enheten Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="35486-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="35486-118">Principen har nu det uppdaterade schemat i $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="35486-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="35486-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35486-119">PARAMETERS</span></span>

### <span data-ttu-id="35486-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="35486-120">-BackupPolicyId</span></span>
<span data-ttu-id="35486-121">Anger instans-ID för det **BackupPolicy** -objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="35486-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="35486-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="35486-122">-BackupPolicyName</span></span>
<span data-ttu-id="35486-123">Anger ett nytt namn för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="35486-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="35486-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="35486-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="35486-125">Anger en matris med instans-ID: n för **BackupSchedule** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="35486-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35486-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="35486-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="35486-127">Anger en matris med **BackupScheduleBase** -objekt som ska läggas till i principen.</span><span class="sxs-lookup"><span data-stu-id="35486-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="35486-128">För att få ett **BackupScheduleBase** -objekt, Använd cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="35486-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35486-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="35486-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="35486-130">Anger en matris med **BackupScheduleUpdateRequest** -objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="35486-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="35486-131">För att få ett **BackupScheduleUpdateRequest** -objekt, Använd cmdleten **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** .</span><span class="sxs-lookup"><span data-stu-id="35486-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35486-132">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="35486-132">-DeviceName</span></span>
<span data-ttu-id="35486-133">Anger namnet på den StorSimple-enhet som du vill uppdatera säkerhets kopierings principen för.</span><span class="sxs-lookup"><span data-stu-id="35486-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="35486-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="35486-134">-NewName</span></span>
<span data-ttu-id="35486-135">Anger ett namn för enheten.</span><span class="sxs-lookup"><span data-stu-id="35486-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="35486-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="35486-136">-Profile</span></span>
<span data-ttu-id="35486-137">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="35486-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="35486-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="35486-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="35486-139">Anger en matris med ID-nummer för volymer som du kan uppdatera säkerhets kopierings principer för.</span><span class="sxs-lookup"><span data-stu-id="35486-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35486-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="35486-140">-WaitForComplete</span></span>
<span data-ttu-id="35486-141">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="35486-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="35486-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35486-142">CommonParameters</span></span>
<span data-ttu-id="35486-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35486-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35486-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35486-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35486-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35486-145">INPUTS</span></span>

### <span data-ttu-id="35486-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="35486-146">None</span></span>

## <span data-ttu-id="35486-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35486-147">OUTPUTS</span></span>

### <span data-ttu-id="35486-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="35486-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="35486-149">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="35486-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="35486-150">Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="35486-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="35486-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35486-151">NOTES</span></span>

## <span data-ttu-id="35486-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35486-152">RELATED LINKS</span></span>

[<span data-ttu-id="35486-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="35486-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="35486-154">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="35486-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="35486-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="35486-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="35486-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="35486-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


