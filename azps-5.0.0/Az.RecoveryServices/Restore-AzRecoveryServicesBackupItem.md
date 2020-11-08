---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270442"
---
# <span data-ttu-id="4a3ed-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4a3ed-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4a3ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a3ed-102">SYNOPSIS</span></span>

<span data-ttu-id="4a3ed-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="4a3ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a3ed-104">SYNTAX</span></span>

### <span data-ttu-id="4a3ed-105">AzureVMParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4a3ed-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3ed-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a3ed-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3ed-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="4a3ed-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3ed-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a3ed-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3ed-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a3ed-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3ed-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a3ed-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3ed-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a3ed-111">DESCRIPTION</span></span>

<span data-ttu-id="4a3ed-112">Cmdleten **restore-AzRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="4a3ed-113">Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="4a3ed-114">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="4a3ed-115">De hanterade diskarna återställs till en mål resurs grupp och konfigurations information till kundens lagrings konto när återställningen är slutförd måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="4a3ed-116">Refter till olika parameter uppsättningar och parameter text för mer information.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="4a3ed-117">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="4a3ed-118">Obs! för att köra denna cmdlet, utöver-VaultId parameter-VaultLocation, ska du också använda den.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="4a3ed-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a3ed-119">EXAMPLES</span></span>

### <span data-ttu-id="4a3ed-120">Exempel 1: Återställ ett objekt till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="4a3ed-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="4a3ed-121">Det första kommandot får RecoveryServices-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="4a3ed-122">Det andra kommandot hämtar säkerhets kopiorna och lagrar dem sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4a3ed-123">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="4a3ed-124">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="4a3ed-125">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="4a3ed-126">Det sjätte kommandot anger vilka diskar som ska återställas från återställnings punkten och lagras i $restoreDiskLUNs variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="4a3ed-127">Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="4a3ed-128">Exempel 2: återställa flera filer för ett AzureFileShare-objekt</span><span class="sxs-lookup"><span data-stu-id="4a3ed-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="4a3ed-129">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4a3ed-130">Det andra kommandot får det säkerhets kopierings objekt som heter fileshareitem och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4a3ed-131">Det tredje kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="4a3ed-132">Det fjärde kommandot spceifies vilka filer som ska återställas och lagras i $files variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="4a3ed-133">Det senaste kommandot återställer de angivna filerna till dess ursprungliga plats.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="4a3ed-134">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4a3ed-134">Example 3</span></span>

<span data-ttu-id="4a3ed-135">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="4a3ed-136">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="4a3ed-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="4a3ed-137">Exempel 4: återställa en hanterad virtuell dator som hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="4a3ed-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="4a3ed-138">Det första kommandot får RecoveryServices-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="4a3ed-139">Det andra kommandot hämtar säkerhets kopian och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4a3ed-140">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="4a3ed-141">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="4a3ed-142">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="4a3ed-143">Det sjätte kommandot återställer diskarna som hanterade diskar med den angivna mål resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="4a3ed-144">Exempel 5: återställa en hanterad virtuell dator som ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="4a3ed-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="4a3ed-145">Det första kommandot får RecoveryServices-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="4a3ed-146">Det andra kommandot hämtar säkerhets kopian och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4a3ed-147">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="4a3ed-148">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="4a3ed-149">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="4a3ed-150">Det sjätte kommandot återställer diskarna som ohanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="4a3ed-151">Exempel 6: återställa en ohanterad virtuell dator som ohanterade diskar med det ursprungliga lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="4a3ed-152">Det första kommandot får RecoveryServices-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="4a3ed-153">Det andra kommandot hämtar säkerhets kopian och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4a3ed-154">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="4a3ed-155">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="4a3ed-156">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="4a3ed-157">Med det sjätte kommandot återställs diskarna som ohanterade diskar med det ursprungliga lagrings kontot för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="4a3ed-158">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a3ed-158">PARAMETERS</span></span>

### <span data-ttu-id="4a3ed-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3ed-159">-DefaultProfile</span></span>

<span data-ttu-id="4a3ed-160">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3ed-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="4a3ed-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="4a3ed-162">Används för att återställa flera filer från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="4a3ed-163">Sök vägarna för de objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="4a3ed-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4a3ed-164">-RecoveryPoint</span></span>

<span data-ttu-id="4a3ed-165">Anger den återställnings punkt där du vill återställa säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="4a3ed-166">För att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt, Använd cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="4a3ed-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="4a3ed-167">-ResolveConflict</span></span>

<span data-ttu-id="4a3ed-168">Om det återställda objektet också finns på mål platsen kan du ange om du vill skriva över eller inte.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="4a3ed-169">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4a3ed-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a3ed-170">Skriva över</span><span class="sxs-lookup"><span data-stu-id="4a3ed-170">Overwrite</span></span>
- <span data-ttu-id="4a3ed-171">Vidare</span><span class="sxs-lookup"><span data-stu-id="4a3ed-171">Skip</span></span>

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

### <span data-ttu-id="4a3ed-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="4a3ed-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="4a3ed-173">Använd den här växeln för att ange återställning som ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="4a3ed-173">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="4a3ed-174">-RestoreDiskList</span></span>
<span data-ttu-id="4a3ed-175">Ange vilka diskar som ska återställas till den säkerhetskopierade virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="4a3ed-175">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="4a3ed-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="4a3ed-177">Använd den här växeln för att återställa endast OS-diskar för en säkerhets kopie rad virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4a3ed-177">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="4a3ed-178">-SourceFilePath</span></span>

<span data-ttu-id="4a3ed-179">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="4a3ed-180">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="4a3ed-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="4a3ed-181">-SourceFileType</span></span>

<span data-ttu-id="4a3ed-182">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="4a3ed-183">Typen av objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="4a3ed-184">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4a3ed-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a3ed-185">Fil</span><span class="sxs-lookup"><span data-stu-id="4a3ed-185">File</span></span>
- <span data-ttu-id="4a3ed-186">Katalogen</span><span class="sxs-lookup"><span data-stu-id="4a3ed-186">Directory</span></span>

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

### <span data-ttu-id="4a3ed-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a3ed-187">-StorageAccountName</span></span>

<span data-ttu-id="4a3ed-188">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="4a3ed-189">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a3ed-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="4a3ed-191">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="4a3ed-192">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="4a3ed-193">-TargetFileShareName</span></span>

<span data-ttu-id="4a3ed-194">Fil resursen dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="4a3ed-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="4a3ed-195">-TargetFolder</span></span>

<span data-ttu-id="4a3ed-196">Den mapp där fil resursen måste återställas i TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="4a3ed-197">Om det säkerhetskopierade innehållet ska återställas till rotmappen anger du värdet för målmappen som en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="4a3ed-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a3ed-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="4a3ed-199">Den resurs grupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="4a3ed-200">Gäller för säkerhets kopiering av VM med hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="4a3ed-200">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a3ed-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="4a3ed-202">Det lagrings konto dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="4a3ed-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a3ed-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="4a3ed-204">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3ed-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4a3ed-205">-VaultId</span></span>

<span data-ttu-id="4a3ed-206">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4a3ed-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="4a3ed-207">-VaultLocation</span></span>

<span data-ttu-id="4a3ed-208">Plats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4a3ed-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="4a3ed-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="4a3ed-210">Återställnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3ed-210">Recovery config</span></span>

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

### <span data-ttu-id="4a3ed-211">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a3ed-211">-Confirm</span></span>

<span data-ttu-id="4a3ed-212">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3ed-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3ed-213">-WhatIf</span></span>

<span data-ttu-id="4a3ed-214">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="4a3ed-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3ed-215">CommonParameters</span></span>
<span data-ttu-id="4a3ed-216">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3ed-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3ed-217">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a3ed-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3ed-218">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a3ed-218">INPUTS</span></span>

### <span data-ttu-id="4a3ed-219">System. String</span><span class="sxs-lookup"><span data-stu-id="4a3ed-219">System.String</span></span>

### <span data-ttu-id="4a3ed-220">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4a3ed-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="4a3ed-221">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a3ed-221">OUTPUTS</span></span>

### <span data-ttu-id="4a3ed-222">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4a3ed-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4a3ed-223">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a3ed-223">NOTES</span></span>

## <span data-ttu-id="4a3ed-224">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a3ed-224">RELATED LINKS</span></span>

[<span data-ttu-id="4a3ed-225">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4a3ed-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4a3ed-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4a3ed-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4a3ed-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4a3ed-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
