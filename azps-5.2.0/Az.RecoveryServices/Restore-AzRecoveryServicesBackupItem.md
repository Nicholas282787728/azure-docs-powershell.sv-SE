---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 593603e212c2ebfd709e5f4c70797ea369877b76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411195"
---
# <span data-ttu-id="11cb1-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="11cb1-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="11cb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11cb1-102">SYNOPSIS</span></span>

<span data-ttu-id="11cb1-103">Återställer data och konfiguration för ett säkerhets kopie objekt till den angivna återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="11cb1-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="11cb1-104">Vilka parametrar som är nödvändiga beror på vilken typ av säkerhets kopia du har.</span><span class="sxs-lookup"><span data-stu-id="11cb1-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="11cb1-105">Samma kommando används för att återställa virtuella Azure-datorer, databaser som körs i virtuella Azure-datorer och även för Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="11cb1-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="11cb1-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11cb1-106">SYNTAX</span></span>

### <span data-ttu-id="11cb1-107">AzureVMParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="11cb1-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11cb1-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="11cb1-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11cb1-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="11cb1-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11cb1-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="11cb1-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11cb1-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="11cb1-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11cb1-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="11cb1-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11cb1-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11cb1-113">DESCRIPTION</span></span>

<span data-ttu-id="11cb1-114">Cmdleten **restore-AzRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="11cb1-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="11cb1-115">**För Azure VM-säkerhetskopiering**</span><span class="sxs-lookup"><span data-stu-id="11cb1-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="11cb1-116">Du kan säkerhetskopiera virtuella Azure-datorer och återställa diskar (både hanterade och ohanterade) med det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="11cb1-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="11cb1-117">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="11cb1-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="11cb1-118">Om det är en virtuell dator med hanterade diskar bör du ange en mål resurs grupp där de återställda diskarna bevaras.</span><span class="sxs-lookup"><span data-stu-id="11cb1-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="11cb1-119">Om du har angett mål resurs gruppen, om stillbilderna finns i resurs gruppen som angavs i säkerhets kopierings princip kommer återställningen att ske direkt och diskarna skapas från lokala stillbilder och sparas i mål resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="11cb1-120">Det finns också ett alternativ för att återställa dem som ohanterade diskar men detta kommer att utnyttja de data som finns i Azure Recovery Service-valvet och därmed bli mycket långsammare.</span><span class="sxs-lookup"><span data-stu-id="11cb1-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="11cb1-121">Konfigurationen av den virtuella datorn och distributions mal len som kan användas för att skapa VM på de återställda diskarna laddas ner till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="11cb1-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="11cb1-122">Om det är en ohanterad virtuell dator är stillbilderna i diskens ursprungliga lagrings konto och/eller i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="11cb1-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="11cb1-123">Om en användare tillhandahåller ett alternativ för att återställa det ursprungliga lagrings kontot kan du tillhandahålla direkt återställning.</span><span class="sxs-lookup"><span data-stu-id="11cb1-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="11cb1-124">Annars hämtas data från ett Azure Recovery Services-valv och diskar skapas i angivet lagrings konto tillsammans med konfigurationen för den virtuella datorn och distributions mal len.</span><span class="sxs-lookup"><span data-stu-id="11cb1-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11cb1-125">Som standard återställer Azure VM-säkerhetskopiering alla diskar.</span><span class="sxs-lookup"><span data-stu-id="11cb1-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="11cb1-126">Du kan selektivt säkerhetskopiera relevanta diskar med exclusionList-eller InclusionList-parametrarna under aktivera-säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="11cb1-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="11cb1-127">Alternativet för att selektivt återställa diskar är bara tillgängligt om en har säkerhetskopierat dem.</span><span class="sxs-lookup"><span data-stu-id="11cb1-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="11cb1-128">Mer information finns i olika parameter uppsättningar och parameter text.</span><span class="sxs-lookup"><span data-stu-id="11cb1-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="11cb1-129">IF-VaultId parameter används även-VaultLocation-parametern ska användas.</span><span class="sxs-lookup"><span data-stu-id="11cb1-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="11cb1-130">**För Azure File Share-säkerhetskopiering**</span><span class="sxs-lookup"><span data-stu-id="11cb1-130">**For Azure File share backup**</span></span>

<span data-ttu-id="11cb1-131">Du kan återställa en hel fil resurs eller specifika/flera filer/mappar på resursen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="11cb1-132">Du kan återställa till den ursprungliga platsen eller till en annan plats.</span><span class="sxs-lookup"><span data-stu-id="11cb1-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="11cb1-133">**För Azure-arbets belastningar**</span><span class="sxs-lookup"><span data-stu-id="11cb1-133">**For Azure Workloads**</span></span>

<span data-ttu-id="11cb1-134">Du kan återställa SQL DBs i Azure VM</span><span class="sxs-lookup"><span data-stu-id="11cb1-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="11cb1-135">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11cb1-135">EXAMPLES</span></span>

### <span data-ttu-id="11cb1-136">Exempel 1: Återställ diskarna för en säkerhetshanterad virtuell dator med en säkerhets kopia från en given återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="11cb1-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="11cb1-137">Det första kommandot får Recovery Services-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="11cb1-138">Det andra kommandot får säkerhets kopian av typen AzureVM, med namnet "V2VM" och lagrar det i $BackupItem variabeln.</span><span class="sxs-lookup"><span data-stu-id="11cb1-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="11cb1-139">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="11cb1-140">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="11cb1-141">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="11cb1-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="11cb1-142">Det senaste kommandot återställer alla diskar till mål resurs gruppen Target_RG och tillhandahåller sedan den virtuella dator konfigurations informationen och distributions mal len i lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="11cb1-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="11cb1-143">Exempel 2: Återställ angivna diskar för en säkerhetshanterad virtuell dator med en säkerhets kopia från en given återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="11cb1-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="11cb1-144">Det första kommandot får Recovery Services-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="11cb1-145">Det andra kommandot får säkerhets kopian av typen AzureVM, med namnet "V2VM" och lagrar det i $BackupItem variabeln.</span><span class="sxs-lookup"><span data-stu-id="11cb1-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="11cb1-146">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="11cb1-147">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="11cb1-148">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="11cb1-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="11cb1-149">Med det sjätte kommandot lagras listan över diskar som ska återställas i variabeln restoreDiskLUN.</span><span class="sxs-lookup"><span data-stu-id="11cb1-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="11cb1-150">Med det senaste kommandot återställs de angivna diskarna, till mål resurs gruppen Target_RG, och sedan tillhandahålls konfigurations informationen för den virtuella datorn och distributions mal len i lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="11cb1-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="11cb1-151">Exempel 3: återställa diskar av en hanterad virtuell dator som ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="11cb1-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="11cb1-152">Det första kommandot får RecoveryServices-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="11cb1-153">Det andra kommandot hämtar säkerhets kopian och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="11cb1-154">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="11cb1-155">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="11cb1-156">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="11cb1-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="11cb1-157">Det sjätte kommandot återställer diskarna som ohanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="11cb1-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="11cb1-158">Exempel 4: återställa en ohanterad virtuell dator som ohanterade diskar med det ursprungliga lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="11cb1-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="11cb1-159">Det första kommandot får RecoveryServices-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="11cb1-160">Det andra kommandot hämtar säkerhets kopian och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="11cb1-161">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="11cb1-162">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="11cb1-163">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="11cb1-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="11cb1-164">Det sjätte kommandot återställer diskarna som ohanterade diskar till deras ursprungliga lagrings konton</span><span class="sxs-lookup"><span data-stu-id="11cb1-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="11cb1-165">Exempel 5: återställa flera filer för ett AzureFileShare-objekt</span><span class="sxs-lookup"><span data-stu-id="11cb1-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="11cb1-166">Det första kommandot får Recovery Services-valvet och lagrar det i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="11cb1-167">Det andra kommandot får det säkerhets kopierings objekt som heter fileshareitem och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="11cb1-168">Det tredje kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="11cb1-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="11cb1-169">Det fjärde kommandot anger vilka filer som ska återställas och lagras i $files variabel.</span><span class="sxs-lookup"><span data-stu-id="11cb1-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="11cb1-170">Det senaste kommandot återställer de angivna filerna till dess ursprungliga plats.</span><span class="sxs-lookup"><span data-stu-id="11cb1-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="11cb1-171">Exempel 6: återställa en SQL-DB i en Azure VM till en annan mål-VM för en distinkt fullständig återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="11cb1-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### <span data-ttu-id="11cb1-172">Exempel 7: återställa en SQL-DB i en Azure VM till en annan mål dator för en logg återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="11cb1-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## <span data-ttu-id="11cb1-173">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11cb1-173">PARAMETERS</span></span>

### <span data-ttu-id="11cb1-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cb1-174">-DefaultProfile</span></span>

<span data-ttu-id="11cb1-175">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11cb1-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11cb1-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="11cb1-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="11cb1-177">Används för att återställa flera filer från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="11cb1-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="11cb1-178">Sök vägarna för de objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="11cb1-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="11cb1-179">-RecoveryPoint</span></span>

<span data-ttu-id="11cb1-180">Anger den återställnings punkt där du vill återställa säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="11cb1-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="11cb1-181">För att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt, Använd cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="11cb1-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="11cb1-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="11cb1-182">-ResolveConflict</span></span>

<span data-ttu-id="11cb1-183">Om det återställda objektet också finns på mål platsen kan du ange om du vill skriva över eller inte.</span><span class="sxs-lookup"><span data-stu-id="11cb1-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="11cb1-184">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="11cb1-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11cb1-185">Skriva över</span><span class="sxs-lookup"><span data-stu-id="11cb1-185">Overwrite</span></span>
- <span data-ttu-id="11cb1-186">Vidare</span><span class="sxs-lookup"><span data-stu-id="11cb1-186">Skip</span></span>

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

### <span data-ttu-id="11cb1-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="11cb1-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="11cb1-188">Använd den här växeln för att ange återställning som ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="11cb1-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="11cb1-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="11cb1-189">-RestoreDiskList</span></span>
<span data-ttu-id="11cb1-190">Ange vilka diskar som ska återställas till den säkerhetskopierade virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="11cb1-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="11cb1-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="11cb1-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="11cb1-192">Använd den här växeln för att återställa endast OS-diskar för en säkerhets kopie rad virtuell dator</span><span class="sxs-lookup"><span data-stu-id="11cb1-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="11cb1-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="11cb1-193">-SourceFilePath</span></span>

<span data-ttu-id="11cb1-194">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="11cb1-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="11cb1-195">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="11cb1-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="11cb1-196">-SourceFileType</span></span>

<span data-ttu-id="11cb1-197">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="11cb1-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="11cb1-198">Typen av objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="11cb1-199">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="11cb1-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11cb1-200">Fil</span><span class="sxs-lookup"><span data-stu-id="11cb1-200">File</span></span>
- <span data-ttu-id="11cb1-201">Katalogen</span><span class="sxs-lookup"><span data-stu-id="11cb1-201">Directory</span></span>

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

### <span data-ttu-id="11cb1-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="11cb1-202">-StorageAccountName</span></span>

<span data-ttu-id="11cb1-203">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="11cb1-204">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="11cb1-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="11cb1-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cb1-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="11cb1-206">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cb1-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="11cb1-207">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="11cb1-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="11cb1-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="11cb1-208">-TargetFileShareName</span></span>

<span data-ttu-id="11cb1-209">Fil resursen dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="11cb1-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="11cb1-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="11cb1-210">-TargetFolder</span></span>

<span data-ttu-id="11cb1-211">Den mapp där fil resursen måste återställas i TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="11cb1-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="11cb1-212">Om det säkerhetskopierade innehållet ska återställas till rotmappen anger du värdet för målmappen som en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="11cb1-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="11cb1-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cb1-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="11cb1-214">Den resurs grupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="11cb1-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="11cb1-215">Gäller för säkerhets kopiering av VM med hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="11cb1-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="11cb1-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="11cb1-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="11cb1-217">Det lagrings konto dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="11cb1-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="11cb1-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11cb1-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="11cb1-219">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="11cb1-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="11cb1-220">-VaultId</span><span class="sxs-lookup"><span data-stu-id="11cb1-220">-VaultId</span></span>

<span data-ttu-id="11cb1-221">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="11cb1-221">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="11cb1-222">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="11cb1-222">-VaultLocation</span></span>

<span data-ttu-id="11cb1-223">Plats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="11cb1-223">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="11cb1-224">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="11cb1-224">-WLRecoveryConfig</span></span>

<span data-ttu-id="11cb1-225">Återställnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="11cb1-225">Recovery config</span></span>

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

### <span data-ttu-id="11cb1-226">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11cb1-226">-Confirm</span></span>

<span data-ttu-id="11cb1-227">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11cb1-227">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11cb1-228">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11cb1-228">-WhatIf</span></span>

<span data-ttu-id="11cb1-229">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11cb1-229">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="11cb1-230">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cb1-230">CommonParameters</span></span>
<span data-ttu-id="11cb1-231">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cb1-231">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cb1-232">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11cb1-232">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cb1-233">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11cb1-233">INPUTS</span></span>

### <span data-ttu-id="11cb1-234">System. String</span><span class="sxs-lookup"><span data-stu-id="11cb1-234">System.String</span></span>

### <span data-ttu-id="11cb1-235">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="11cb1-235">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="11cb1-236">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11cb1-236">OUTPUTS</span></span>

### <span data-ttu-id="11cb1-237">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="11cb1-237">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="11cb1-238">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11cb1-238">NOTES</span></span>

## <span data-ttu-id="11cb1-239">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11cb1-239">RELATED LINKS</span></span>

[<span data-ttu-id="11cb1-240">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="11cb1-240">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="11cb1-241">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="11cb1-241">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="11cb1-242">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="11cb1-242">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
