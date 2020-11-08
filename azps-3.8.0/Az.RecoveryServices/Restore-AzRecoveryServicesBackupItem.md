---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 69b115fab623d1a951fa2f77632a33fb437a3555
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091259"
---
# <span data-ttu-id="c226a-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c226a-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="c226a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c226a-102">SYNOPSIS</span></span>

<span data-ttu-id="c226a-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="c226a-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="c226a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c226a-104">SYNTAX</span></span>

### <span data-ttu-id="c226a-105">AzureVMParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c226a-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c226a-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c226a-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c226a-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="c226a-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c226a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c226a-108">DESCRIPTION</span></span>

<span data-ttu-id="c226a-109">Cmdleten **restore-AzRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="c226a-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="c226a-110">Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c226a-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="c226a-111">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c226a-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="c226a-112">De hanterade diskarna återställs till en mål resurs grupp och konfigurations information till kundens lagrings konto när återställningen är slutförd måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="c226a-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="c226a-113">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="c226a-113">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="c226a-114">Obs! för att köra denna cmdlet, utöver-VaultId parameter-VaultLocation, ska du också använda den.</span><span class="sxs-lookup"><span data-stu-id="c226a-114">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="c226a-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c226a-115">EXAMPLES</span></span>

### <span data-ttu-id="c226a-116">Exempel 1: Återställ ett objekt till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="c226a-116">Example 1: Restore an item to a recovery point</span></span>

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

<span data-ttu-id="c226a-117">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c226a-118">Det andra kommandot får det säkerhets kopie objekt som heter V2VM från $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c226a-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="c226a-119">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="c226a-120">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="c226a-121">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="c226a-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="c226a-122">Det angivna datum intervallet är de senaste sju dagarna.</span><span class="sxs-lookup"><span data-stu-id="c226a-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="c226a-123">Det sjunde kommandot anger vilka diskar som ska återställas från återställnings punkten och lagrar dem i $restoreDiskLUNs variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-123">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="c226a-124">Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="c226a-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="c226a-125">Exempel 2: återställa flera filer för ett AzureFileShare-objekt</span><span class="sxs-lookup"><span data-stu-id="c226a-125">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="c226a-126">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-126">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c226a-127">Det andra kommandot får det säkerhets kopierings objekt som heter fileshareitem och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-127">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="c226a-128">Det tredje kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="c226a-128">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="c226a-129">Det fjärde kommandot spceifies vilka filer som ska återställas och lagras i $files variabel.</span><span class="sxs-lookup"><span data-stu-id="c226a-129">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="c226a-130">Det senaste kommandot återställer de angivna filerna till dess ursprungliga plats.</span><span class="sxs-lookup"><span data-stu-id="c226a-130">The last command restores the specified files to its original location.</span></span>

## <span data-ttu-id="c226a-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c226a-131">PARAMETERS</span></span>

### <span data-ttu-id="c226a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c226a-132">-DefaultProfile</span></span>

<span data-ttu-id="c226a-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c226a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c226a-134">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="c226a-134">-MultipleSourceFilePath</span></span>
<span data-ttu-id="c226a-135">Används för att återställa flera filer från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="c226a-135">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="c226a-136">Sök vägarna för de objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="c226a-136">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="c226a-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c226a-137">-RecoveryPoint</span></span>

<span data-ttu-id="c226a-138">Anger den återställnings punkt där den virtuella datorn ska återställas.</span><span class="sxs-lookup"><span data-stu-id="c226a-138">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="c226a-139">För att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt, Använd cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="c226a-139">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="c226a-140">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="c226a-140">-ResolveConflict</span></span>

<span data-ttu-id="c226a-141">Om det återställda objektet också finns på mål platsen kan du ange om du vill skriva över eller inte.</span><span class="sxs-lookup"><span data-stu-id="c226a-141">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="c226a-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c226a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c226a-143">Skriva över</span><span class="sxs-lookup"><span data-stu-id="c226a-143">Overwrite</span></span>
- <span data-ttu-id="c226a-144">Vidare</span><span class="sxs-lookup"><span data-stu-id="c226a-144">Skip</span></span>

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

### <span data-ttu-id="c226a-145">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="c226a-145">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="c226a-146">Använd den här växeln för att ange återställning som ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="c226a-146">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="c226a-147">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="c226a-147">-RestoreDiskList</span></span>
<span data-ttu-id="c226a-148">Ange vilka diskar som ska återställas till den säkerhetskopierade virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="c226a-148">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="c226a-149">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="c226a-149">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="c226a-150">Använd den här växeln för att återställa endast OS-diskar för en säkerhets kopie rad virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c226a-150">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="c226a-151">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="c226a-151">-SourceFilePath</span></span>

<span data-ttu-id="c226a-152">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="c226a-152">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="c226a-153">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="c226a-153">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="c226a-154">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="c226a-154">-SourceFileType</span></span>

<span data-ttu-id="c226a-155">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="c226a-155">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="c226a-156">Typen av objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="c226a-156">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="c226a-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c226a-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c226a-158">Fil</span><span class="sxs-lookup"><span data-stu-id="c226a-158">File</span></span>
- <span data-ttu-id="c226a-159">Katalogen</span><span class="sxs-lookup"><span data-stu-id="c226a-159">Directory</span></span>

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

### <span data-ttu-id="c226a-160">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c226a-160">-StorageAccountName</span></span>

<span data-ttu-id="c226a-161">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c226a-161">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="c226a-162">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c226a-162">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="c226a-163">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c226a-163">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="c226a-164">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c226a-164">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="c226a-165">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c226a-165">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="c226a-166">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="c226a-166">-TargetFileShareName</span></span>

<span data-ttu-id="c226a-167">Fil resursen dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="c226a-167">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="c226a-168">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="c226a-168">-TargetFolder</span></span>

<span data-ttu-id="c226a-169">Den mapp där fil resursen måste återställas i TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="c226a-169">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="c226a-170">Om det säkerhetskopierade innehållet ska återställas till rotmappen anger du värdet för målmappen som en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="c226a-170">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="c226a-171">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c226a-171">-TargetResourceGroupName</span></span>

<span data-ttu-id="c226a-172">Den resurs grupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="c226a-172">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c226a-173">Gäller för säkerhets kopiering av VM med hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="c226a-173">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="c226a-174">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c226a-174">-TargetStorageAccountName</span></span>

<span data-ttu-id="c226a-175">Det lagrings konto dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="c226a-175">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="c226a-176">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c226a-176">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="c226a-177">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="c226a-177">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="c226a-178">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c226a-178">-VaultId</span></span>

<span data-ttu-id="c226a-179">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c226a-179">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c226a-180">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="c226a-180">-VaultLocation</span></span>

<span data-ttu-id="c226a-181">Plats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c226a-181">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c226a-182">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="c226a-182">-WLRecoveryConfig</span></span>

<span data-ttu-id="c226a-183">Återställnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="c226a-183">Recovery config</span></span>

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

### <span data-ttu-id="c226a-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c226a-184">-Confirm</span></span>

<span data-ttu-id="c226a-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c226a-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c226a-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c226a-186">-WhatIf</span></span>

<span data-ttu-id="c226a-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c226a-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c226a-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c226a-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c226a-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c226a-189">CommonParameters</span></span>
<span data-ttu-id="c226a-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c226a-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c226a-191">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c226a-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c226a-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c226a-192">INPUTS</span></span>

### <span data-ttu-id="c226a-193">System. String</span><span class="sxs-lookup"><span data-stu-id="c226a-193">System.String</span></span>

### <span data-ttu-id="c226a-194">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="c226a-194">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="c226a-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c226a-195">OUTPUTS</span></span>

### <span data-ttu-id="c226a-196">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c226a-196">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c226a-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c226a-197">NOTES</span></span>

## <span data-ttu-id="c226a-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c226a-198">RELATED LINKS</span></span>

[<span data-ttu-id="c226a-199">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c226a-199">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="c226a-200">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c226a-200">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="c226a-201">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c226a-201">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
