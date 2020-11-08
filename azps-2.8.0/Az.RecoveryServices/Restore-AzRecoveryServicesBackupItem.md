---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919700"
---
# <span data-ttu-id="ea5ba-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ea5ba-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ea5ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea5ba-102">SYNOPSIS</span></span>

<span data-ttu-id="ea5ba-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="ea5ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea5ba-104">SYNTAX</span></span>

### <span data-ttu-id="ea5ba-105">AzureVMParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ea5ba-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5ba-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5ba-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea5ba-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5ba-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5ba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea5ba-108">DESCRIPTION</span></span>

<span data-ttu-id="ea5ba-109">Cmdleten **restore-AzRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="ea5ba-110">Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="ea5ba-111">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="ea5ba-112">Den återställer diskens data och konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="ea5ba-113">När återställningen är klar måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="ea5ba-114">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="ea5ba-115">Obs! för att köra denna cmdlet, utöver-VaultId parameter-VaultLocation, ska du också använda den.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="ea5ba-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea5ba-116">EXAMPLES</span></span>

### <span data-ttu-id="ea5ba-117">Exempel 1: Återställ ett objekt till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="ea5ba-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ea5ba-118">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="ea5ba-119">Det andra kommandot får det säkerhets kopie objekt som heter V2VM från $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ea5ba-120">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ea5ba-121">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ea5ba-122">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ea5ba-123">Det angivna datum intervallet är de senaste sju dagarna.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="ea5ba-124">Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="ea5ba-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea5ba-125">PARAMETERS</span></span>

### <span data-ttu-id="ea5ba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5ba-126">-DefaultProfile</span></span>

<span data-ttu-id="ea5ba-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea5ba-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ea5ba-128">-RecoveryPoint</span></span>

<span data-ttu-id="ea5ba-129">Anger den återställnings punkt där den virtuella datorn ska återställas.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="ea5ba-130">För att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt, Använd cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="ea5ba-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="ea5ba-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="ea5ba-131">-ResolveConflict</span></span>

<span data-ttu-id="ea5ba-132">Om det återställda objektet också finns på mål platsen kan du ange om du vill skriva över eller inte.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="ea5ba-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ea5ba-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea5ba-134">Skriva över</span><span class="sxs-lookup"><span data-stu-id="ea5ba-134">Overwrite</span></span>
- <span data-ttu-id="ea5ba-135">Vidare</span><span class="sxs-lookup"><span data-stu-id="ea5ba-135">Skip</span></span>

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

### <span data-ttu-id="ea5ba-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="ea5ba-136">-SourceFilePath</span></span>

<span data-ttu-id="ea5ba-137">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="ea5ba-138">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="ea5ba-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="ea5ba-139">-SourceFileType</span></span>

<span data-ttu-id="ea5ba-140">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="ea5ba-141">Typen av objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="ea5ba-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ea5ba-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea5ba-143">Fil</span><span class="sxs-lookup"><span data-stu-id="ea5ba-143">File</span></span>
- <span data-ttu-id="ea5ba-144">Katalogen</span><span class="sxs-lookup"><span data-stu-id="ea5ba-144">Directory</span></span>

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

### <span data-ttu-id="ea5ba-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea5ba-145">-StorageAccountName</span></span>

<span data-ttu-id="ea5ba-146">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="ea5ba-147">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="ea5ba-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5ba-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="ea5ba-149">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="ea5ba-150">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="ea5ba-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="ea5ba-151">-TargetFileShareName</span></span>

<span data-ttu-id="ea5ba-152">Fil resursen dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="ea5ba-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="ea5ba-153">-TargetFolder</span></span>

<span data-ttu-id="ea5ba-154">Den mapp där fil resursen måste återställas i TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="ea5ba-155">Om det säkerhetskopierade innehållet ska återställas till rotmappen anger du värdet för målmappen som en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="ea5ba-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5ba-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="ea5ba-157">Den resurs grupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ea5ba-158">Gäller för säkerhets kopiering av VM med hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="ea5ba-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="ea5ba-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea5ba-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="ea5ba-160">Det lagrings konto dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="ea5ba-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea5ba-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="ea5ba-162">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="ea5ba-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ea5ba-163">-VaultId</span></span>

<span data-ttu-id="ea5ba-164">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ea5ba-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="ea5ba-165">-VaultLocation</span></span>

<span data-ttu-id="ea5ba-166">Plats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ea5ba-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="ea5ba-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="ea5ba-168">Återställnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="ea5ba-168">Recovery config</span></span>

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

### <span data-ttu-id="ea5ba-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea5ba-169">-Confirm</span></span>

<span data-ttu-id="ea5ba-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5ba-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5ba-171">-WhatIf</span></span>

<span data-ttu-id="ea5ba-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea5ba-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5ba-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5ba-174">-CommonParameters</span></span>

<span data-ttu-id="ea5ba-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5ba-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5ba-176">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea5ba-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5ba-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea5ba-177">INPUTS</span></span>

### <span data-ttu-id="ea5ba-178">System. String</span><span class="sxs-lookup"><span data-stu-id="ea5ba-178">System.String</span></span>

### <span data-ttu-id="ea5ba-179">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="ea5ba-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="ea5ba-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea5ba-180">OUTPUTS</span></span>

### <span data-ttu-id="ea5ba-181">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ea5ba-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ea5ba-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea5ba-182">NOTES</span></span>

## <span data-ttu-id="ea5ba-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea5ba-183">RELATED LINKS</span></span>

[<span data-ttu-id="ea5ba-184">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ea5ba-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ea5ba-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ea5ba-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ea5ba-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ea5ba-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)