---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093474"
---
# <span data-ttu-id="03099-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="03099-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="03099-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03099-102">SYNOPSIS</span></span>
<span data-ttu-id="03099-103">Startar ett jobb som klonar en säkerhets kopia på en enhet.</span><span class="sxs-lookup"><span data-stu-id="03099-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="03099-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03099-104">SYNTAX</span></span>

### <span data-ttu-id="03099-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="03099-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="03099-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="03099-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="03099-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="03099-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03099-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03099-108">DESCRIPTION</span></span>
<span data-ttu-id="03099-109">Cmdleten **Start-AzureStorSimpleBackupCloneJob** startar ett jobb som klonar en befintlig säkerhets kopia på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="03099-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="03099-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03099-110">EXAMPLES</span></span>

### <span data-ttu-id="03099-111">Exempel 1: klona en säkerhets kopia till en annan volym med hjälp av enhets namn</span><span class="sxs-lookup"><span data-stu-id="03099-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="03099-112">Med det första kommandot hämtas den första säkerhets kopian för enheten som heter ContosoDev07 med hjälp av cmdleten **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="03099-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="03099-113">Kommandot lagrar säkerhets kopian i $Backup variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="03099-114">Det andra kommandot får åtkomst kontroll poster med cmdleten **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="03099-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="03099-115">Resultatet sparas i $Acrs variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="03099-116">Det sista kommandot startar ett jobb som klonar en angiven säkerhets kopia av en volym på en enhet till en annan volym på samma enhet.</span><span class="sxs-lookup"><span data-stu-id="03099-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="03099-117">I det här exemplet anges enheten efter namn.</span><span class="sxs-lookup"><span data-stu-id="03099-117">This example specifies the device by name.</span></span>
<span data-ttu-id="03099-118">Kommandot använder värdena som lagras i $Backup och $Acrs.</span><span class="sxs-lookup"><span data-stu-id="03099-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="03099-119">Kommandot returnerar jobbets ID.</span><span class="sxs-lookup"><span data-stu-id="03099-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="03099-120">Exempel 2: klona en säkerhets kopia till en annan volym med hjälp av enhets-ID</span><span class="sxs-lookup"><span data-stu-id="03099-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="03099-121">Med det första kommandot hämtas den första säkerhets kopian för enheten som heter ContosoDev07 med hjälp av cmdleten **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="03099-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="03099-122">Kommandot lagrar säkerhets kopian i $Backup variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="03099-123">Det andra kommandot får åtkomst kontroll poster med cmdleten **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="03099-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="03099-124">Resultatet sparas i $Acrs variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="03099-125">Det sista kommandot startar ett jobb som klonar en angiven säkerhets kopia av en volym på en enhet till en annan volym på samma enhet.</span><span class="sxs-lookup"><span data-stu-id="03099-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="03099-126">I det här exemplet anges enheten efter enhets-ID.</span><span class="sxs-lookup"><span data-stu-id="03099-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="03099-127">Kommandot använder värdena som lagras i $Backup och $Acrs.</span><span class="sxs-lookup"><span data-stu-id="03099-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="03099-128">Kommandot returnerar jobbets ID.</span><span class="sxs-lookup"><span data-stu-id="03099-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="03099-129">Exempel 3: klona en säkerhets kopia till en volym på en annan enhet med hjälp av enhets namn</span><span class="sxs-lookup"><span data-stu-id="03099-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="03099-130">Med det första kommandot hämtas den första säkerhets kopian för enheten som heter ContosoDev07 med hjälp av cmdleten **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="03099-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="03099-131">Kommandot lagrar säkerhets kopian i $Backup variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="03099-132">Det andra kommandot får åtkomst kontroll poster med cmdleten **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="03099-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="03099-133">Resultatet sparas i $Acrs variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="03099-134">Det sista kommandot startar ett jobb som klonar en angiven säkerhets kopia av en volym på en enhet till en annan enhet.</span><span class="sxs-lookup"><span data-stu-id="03099-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="03099-135">I det här exemplet anges enheterna efter namn.</span><span class="sxs-lookup"><span data-stu-id="03099-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="03099-136">Kommandot använder värdena som lagras i $Backup och $Acrs.</span><span class="sxs-lookup"><span data-stu-id="03099-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="03099-137">Kommandot returnerar jobbets ID.</span><span class="sxs-lookup"><span data-stu-id="03099-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="03099-138">Exempel 4: klona en säkerhets kopia till en annan volym med hjälp av enhets namn och operatören</span><span class="sxs-lookup"><span data-stu-id="03099-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="03099-139">Med det första kommandot hämtas den första säkerhets kopian för enheten som heter ContosoDev07 med hjälp av cmdleten **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="03099-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="03099-140">Kommandot lagrar säkerhets kopian i $Backup variabel.</span><span class="sxs-lookup"><span data-stu-id="03099-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="03099-141">Det andra kommandot får åtkomst kontroll poster med cmdleten **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="03099-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="03099-142">Kommandot skickar resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="03099-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="03099-143">Den aktuella cmdleten startar ett jobb som klonar en angiven säkerhets kopia av en volym på en enhet, till en annan volym på samma enhet.</span><span class="sxs-lookup"><span data-stu-id="03099-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="03099-144">I det här exemplet anges enheten efter namn.</span><span class="sxs-lookup"><span data-stu-id="03099-144">This example specifies the device by name.</span></span>
<span data-ttu-id="03099-145">Kommandot använder värdet som lagras i $Backup.</span><span class="sxs-lookup"><span data-stu-id="03099-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="03099-146">Kommandot tar värdet för parametern *TargetAccessControlRecords* från pipeline.</span><span class="sxs-lookup"><span data-stu-id="03099-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="03099-147">Kommandot returnerar jobbets ID.</span><span class="sxs-lookup"><span data-stu-id="03099-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="03099-148">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03099-148">PARAMETERS</span></span>

### <span data-ttu-id="03099-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="03099-149">-BackupId</span></span>
<span data-ttu-id="03099-150">Anger instans-ID för den säkerhets kopia som ska klonas.</span><span class="sxs-lookup"><span data-stu-id="03099-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="03099-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="03099-151">-CloneVolumeName</span></span>
<span data-ttu-id="03099-152">Anger namnet på den nya klonade volymen på mål enheten.</span><span class="sxs-lookup"><span data-stu-id="03099-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="03099-153">-Force</span><span class="sxs-lookup"><span data-stu-id="03099-153">-Force</span></span>
<span data-ttu-id="03099-154">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="03099-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03099-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="03099-155">-Profile</span></span>
<span data-ttu-id="03099-156">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="03099-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="03099-157">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="03099-157">-Snapshot</span></span>
<span data-ttu-id="03099-158">Anger det SnapShot-objekt som den här cmdleten klonar.</span><span class="sxs-lookup"><span data-stu-id="03099-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03099-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="03099-159">-SourceDeviceId</span></span>
<span data-ttu-id="03099-160">Anger käll enhetens instans-ID.</span><span class="sxs-lookup"><span data-stu-id="03099-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="03099-161">Denna cmdlet klonar bak sidan från käll enheten.</span><span class="sxs-lookup"><span data-stu-id="03099-161">This cmdlet clones the back from the source device.</span></span>

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

### <span data-ttu-id="03099-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="03099-162">-SourceDeviceName</span></span>
<span data-ttu-id="03099-163">Anger namnet på käll enheten.</span><span class="sxs-lookup"><span data-stu-id="03099-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="03099-164">Denna cmdlet klonar bak sidan från käll enheten.</span><span class="sxs-lookup"><span data-stu-id="03099-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03099-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="03099-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="03099-166">Anger åtkomst kontroll posterna.</span><span class="sxs-lookup"><span data-stu-id="03099-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03099-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="03099-167">-TargetDeviceId</span></span>
<span data-ttu-id="03099-168">Anger mål enhetens instans-ID.</span><span class="sxs-lookup"><span data-stu-id="03099-168">Specifies the instance ID of the target device.</span></span>

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

### <span data-ttu-id="03099-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="03099-169">-TargetDeviceName</span></span>
<span data-ttu-id="03099-170">Anger namnet på den enhet som denna cmdlet ska klona säkerhets kopian till.</span><span class="sxs-lookup"><span data-stu-id="03099-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03099-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03099-171">CommonParameters</span></span>
<span data-ttu-id="03099-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03099-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03099-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03099-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03099-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03099-174">INPUTS</span></span>

### <span data-ttu-id="03099-175">Ögonblicks bild, lista med AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="03099-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="03099-176">Du kan ta med **ögonblicks bild** objekt eller en lista med **AccessControlRecord** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03099-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="03099-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03099-177">OUTPUTS</span></span>

## <span data-ttu-id="03099-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03099-178">NOTES</span></span>

## <span data-ttu-id="03099-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03099-179">RELATED LINKS</span></span>

[<span data-ttu-id="03099-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="03099-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="03099-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="03099-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


