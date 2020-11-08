---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102602"
---
# <span data-ttu-id="a57a3-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a57a3-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a57a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a57a3-102">SYNOPSIS</span></span>

<span data-ttu-id="a57a3-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="a57a3-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="a57a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a57a3-104">SYNTAX</span></span>

### <span data-ttu-id="a57a3-105">AzureVMParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a57a3-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57a3-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57a3-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57a3-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57a3-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57a3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a57a3-108">DESCRIPTION</span></span>

<span data-ttu-id="a57a3-109">Cmdleten **restore-AzRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="a57a3-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="a57a3-110">Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a57a3-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="a57a3-111">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a57a3-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="a57a3-112">De hanterade diskarna återställs till en mål resurs grupp och konfigurations information till kundens lagrings konto när återställningen är slutförd måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="a57a3-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="a57a3-113">Refter till olika parameter uppsättningar och parameter text för mer information.</span><span class="sxs-lookup"><span data-stu-id="a57a3-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="a57a3-114">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="a57a3-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="a57a3-115">Obs! för att köra denna cmdlet, utöver-VaultId parameter-VaultLocation, ska du också använda den.</span><span class="sxs-lookup"><span data-stu-id="a57a3-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="a57a3-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a57a3-116">EXAMPLES</span></span>

### <span data-ttu-id="a57a3-117">Exempel 1: Återställ ett objekt till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="a57a3-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="a57a3-118">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a57a3-119">Det andra kommandot får det säkerhets kopie objekt som heter V2VM från $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a57a3-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a57a3-120">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a57a3-121">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a57a3-122">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a57a3-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="a57a3-123">Det angivna datum intervallet är de senaste sju dagarna.</span><span class="sxs-lookup"><span data-stu-id="a57a3-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="a57a3-124">Det sjunde kommandot anger vilka diskar som ska återställas från återställnings punkten och lagrar dem i $restoreDiskLUNs variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="a57a3-125">Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="a57a3-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="a57a3-126">Exempel 2: återställa flera filer för ett AzureFileShare-objekt</span><span class="sxs-lookup"><span data-stu-id="a57a3-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="a57a3-127">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a57a3-128">Det andra kommandot får det säkerhets kopierings objekt som heter fileshareitem och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a57a3-129">Det tredje kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="a57a3-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="a57a3-130">Det fjärde kommandot spceifies vilka filer som ska återställas och lagras i $files variabel.</span><span class="sxs-lookup"><span data-stu-id="a57a3-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="a57a3-131">Det senaste kommandot återställer de angivna filerna till dess ursprungliga plats.</span><span class="sxs-lookup"><span data-stu-id="a57a3-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="a57a3-132">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a57a3-132">Example 3</span></span>

<span data-ttu-id="a57a3-133">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="a57a3-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="a57a3-134">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="a57a3-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="a57a3-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a57a3-135">PARAMETERS</span></span>

### <span data-ttu-id="a57a3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57a3-136">-DefaultProfile</span></span>

<span data-ttu-id="a57a3-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a57a3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a57a3-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="a57a3-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="a57a3-139">Används för att återställa flera filer från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="a57a3-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="a57a3-140">Sök vägarna för de objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="a57a3-140">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a57a3-141">-RecoveryPoint</span></span>

<span data-ttu-id="a57a3-142">Anger den återställnings punkt där du vill återställa säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="a57a3-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="a57a3-143">För att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt, Använd cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="a57a3-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="a57a3-144">-ResolveConflict</span></span>

<span data-ttu-id="a57a3-145">Om det återställda objektet också finns på mål platsen kan du ange om du vill skriva över eller inte.</span><span class="sxs-lookup"><span data-stu-id="a57a3-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="a57a3-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a57a3-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a57a3-147">Skriva över</span><span class="sxs-lookup"><span data-stu-id="a57a3-147">Overwrite</span></span>
- <span data-ttu-id="a57a3-148">Vidare</span><span class="sxs-lookup"><span data-stu-id="a57a3-148">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="a57a3-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="a57a3-150">Använd den här växeln för att ange återställning som ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="a57a3-150">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="a57a3-151">-RestoreDiskList</span></span>
<span data-ttu-id="a57a3-152">Ange vilka diskar som ska återställas till den säkerhetskopierade virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="a57a3-152">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="a57a3-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="a57a3-154">Använd den här växeln för att återställa endast OS-diskar för en säkerhets kopie rad virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a57a3-154">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="a57a3-155">-SourceFilePath</span></span>

<span data-ttu-id="a57a3-156">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="a57a3-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a57a3-157">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="a57a3-157">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="a57a3-158">-SourceFileType</span></span>

<span data-ttu-id="a57a3-159">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="a57a3-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a57a3-160">Typen av objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="a57a3-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="a57a3-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a57a3-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a57a3-162">Fil</span><span class="sxs-lookup"><span data-stu-id="a57a3-162">File</span></span>
- <span data-ttu-id="a57a3-163">Katalogen</span><span class="sxs-lookup"><span data-stu-id="a57a3-163">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a57a3-164">-StorageAccountName</span></span>

<span data-ttu-id="a57a3-165">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a57a3-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="a57a3-166">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a57a3-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57a3-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="a57a3-168">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a57a3-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="a57a3-169">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a57a3-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="a57a3-170">-TargetFileShareName</span></span>

<span data-ttu-id="a57a3-171">Fil resursen dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="a57a3-171">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="a57a3-172">-TargetFolder</span></span>

<span data-ttu-id="a57a3-173">Den mapp där fil resursen måste återställas i TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="a57a3-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="a57a3-174">Om det säkerhetskopierade innehållet ska återställas till rotmappen anger du värdet för målmappen som en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="a57a3-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57a3-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="a57a3-176">Den resurs grupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="a57a3-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a57a3-177">Gäller för säkerhets kopiering av VM med hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="a57a3-177">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a57a3-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="a57a3-179">Det lagrings konto dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="a57a3-179">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a57a3-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="a57a3-181">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="a57a3-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a57a3-182">-VaultId</span></span>

<span data-ttu-id="a57a3-183">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a57a3-183">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="a57a3-184">-VaultLocation</span></span>

<span data-ttu-id="a57a3-185">Plats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a57a3-185">Location of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="a57a3-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="a57a3-187">Återställnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="a57a3-187">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-188">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a57a3-188">-Confirm</span></span>

<span data-ttu-id="a57a3-189">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a57a3-189">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57a3-190">-WhatIf</span></span>

<span data-ttu-id="a57a3-191">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a57a3-191">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57a3-192">CommonParameters</span></span>
<span data-ttu-id="a57a3-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57a3-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57a3-194">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a57a3-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57a3-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a57a3-195">INPUTS</span></span>

### <span data-ttu-id="a57a3-196">System. String</span><span class="sxs-lookup"><span data-stu-id="a57a3-196">System.String</span></span>

### <span data-ttu-id="a57a3-197">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a57a3-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a57a3-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a57a3-198">OUTPUTS</span></span>

### <span data-ttu-id="a57a3-199">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a57a3-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a57a3-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a57a3-200">NOTES</span></span>

## <span data-ttu-id="a57a3-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a57a3-201">RELATED LINKS</span></span>

[<span data-ttu-id="a57a3-202">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a57a3-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a57a3-203">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a57a3-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a57a3-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a57a3-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
