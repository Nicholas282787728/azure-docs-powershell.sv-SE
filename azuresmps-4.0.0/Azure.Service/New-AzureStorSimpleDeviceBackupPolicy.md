---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099438"
---
# <span data-ttu-id="1a7ff-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7ff-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="1a7ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7ff-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-103">Creates a backup policy.</span></span>

## <span data-ttu-id="1a7ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a7ff-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a7ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="1a7ff-106">Cmdleten **New-AzureStorSimpleDeviceBackupPolicy** skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="1a7ff-107">En säkerhets kopierings princip innehåller minst ett schema för säkerhets kopior som kan köras på en eller flera volymer.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="1a7ff-108">Använd cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** för att skapa ett schema för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="1a7ff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a7ff-109">EXAMPLES</span></span>

### <span data-ttu-id="1a7ff-110">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="1a7ff-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="1a7ff-111">Det första kommandot skapar ett schema för säkerhets kopierings schemaläggning med hjälp av **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet och lagrar sedan objektet i variabeln $Schedule 01.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="1a7ff-112">Det andra kommandot skapar ett annat konfigurations objekt för säkerhets kopior med hjälp av **New-AzureStorSimpleDeviceBackupScheduleAddConfig** och lagrar sedan objektet i $Schedule 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="1a7ff-113">Det tredje kommandot skapar en tom mat ris variabel, namngiven $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="1a7ff-114">Nästa två kommandon lägger till de objekt som skapats i de två första kommandona för att $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="1a7ff-115">Det sjätte kommandot får en volym behållare för enheten som heter Contoso63-AppVm med hjälp av cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** och lagrar sedan det behållar-objekt i $DeviceContainer-variabeln.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="1a7ff-116">Med det sjunde kommandot får du en volym för volymen som lagras i den första medlemmen i $DeviceContainer genom att använda cmdleten **Get-AzureStorSimpleDeviceVolume** och sedan lagra den volymen i $Volume variabeln.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="1a7ff-117">Med kommandot åtto skapas en tom mat ris variabel som heter $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="1a7ff-118">Med nästa kommando läggs ett volym-ID till $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="1a7ff-119">Det här värdet identifierar volymen, som är lagrad i $Volume, där säkerhets kopierings principen körs.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="1a7ff-120">Du kan lägga till ytterligare volym-ID: n för $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="1a7ff-121">Det sista kommandot skapar säkerhets kopierings principen med namnet GeneralPolicy07 för enheten som heter Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="1a7ff-122">Kommandot anger de schema konfigurations objekt som lagras i $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="1a7ff-123">Kommandot anger volymen eller volymerna som du vill tillämpa principen på i $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="1a7ff-124">Du kan verifiera säkerhets kopierings principen genom att använda cmdleten **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="1a7ff-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="1a7ff-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a7ff-125">PARAMETERS</span></span>

### <span data-ttu-id="1a7ff-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="1a7ff-126">-BackupPolicyName</span></span>
<span data-ttu-id="1a7ff-127">Anger namnet på säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="1a7ff-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="1a7ff-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="1a7ff-129">Anger en matris med **BackupScheduleBase** -objekt som ska läggas till i principen.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="1a7ff-130">Varje objekt representerar ett schema.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-130">Each object represents a schedule.</span></span>
<span data-ttu-id="1a7ff-131">En säkerhets kopierings princip innehåller ett eller flera scheman.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="1a7ff-132">För att få ett **BackupScheduleBase** -objekt, Använd cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="1a7ff-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7ff-133">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="1a7ff-133">-DeviceName</span></span>
<span data-ttu-id="1a7ff-134">Anger namnet på den StorSimple-enhet där säkerhets kopierings principen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="1a7ff-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a7ff-135">-Profile</span></span>
<span data-ttu-id="1a7ff-136">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="1a7ff-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="1a7ff-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="1a7ff-138">Anger en matris med ID-numren för volymer som ska läggas till i säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7ff-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1a7ff-139">-WaitForComplete</span></span>
<span data-ttu-id="1a7ff-140">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="1a7ff-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7ff-141">CommonParameters</span></span>
<span data-ttu-id="1a7ff-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7ff-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a7ff-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7ff-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a7ff-144">INPUTS</span></span>

### <span data-ttu-id="1a7ff-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="1a7ff-145">None</span></span>

## <span data-ttu-id="1a7ff-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a7ff-146">OUTPUTS</span></span>

### <span data-ttu-id="1a7ff-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7ff-147">BackupPolicy</span></span>
<span data-ttu-id="1a7ff-148">Denna cmdlet returnerar ett **BackupPolicy** -objekt som innehåller de nya scheman och volymer.</span><span class="sxs-lookup"><span data-stu-id="1a7ff-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="1a7ff-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a7ff-149">NOTES</span></span>

## <span data-ttu-id="1a7ff-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a7ff-150">RELATED LINKS</span></span>

[<span data-ttu-id="1a7ff-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7ff-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="1a7ff-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="1a7ff-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="1a7ff-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="1a7ff-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="1a7ff-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7ff-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="1a7ff-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7ff-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="1a7ff-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="1a7ff-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


