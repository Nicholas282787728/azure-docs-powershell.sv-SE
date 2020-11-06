---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572676"
---
# <span data-ttu-id="6fd7d-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6fd7d-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="6fd7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd7d-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fd7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fd7d-104">SYNTAX</span></span>

### <span data-ttu-id="6fd7d-105">AzureVMParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6fd7d-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd7d-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd7d-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd7d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fd7d-107">DESCRIPTION</span></span>
<span data-ttu-id="6fd7d-108">Cmdleten **restore-AzureRmRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="6fd7d-109">Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="6fd7d-110">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="6fd7d-111">Den återställer diskens data och konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="6fd7d-112">När återställningen är klar måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="6fd7d-113">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6fd7d-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fd7d-114">EXAMPLES</span></span>

### <span data-ttu-id="6fd7d-115">Exempel 1: Återställ ett objekt till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="6fd7d-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="6fd7d-116">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6fd7d-117">Det andra kommandot får det säkerhets kopie objekt som heter V2VM från $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="6fd7d-118">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="6fd7d-119">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="6fd7d-120">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="6fd7d-121">Det angivna datum intervallet är de senaste sju dagarna.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="6fd7d-122">Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="6fd7d-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fd7d-123">PARAMETERS</span></span>

### <span data-ttu-id="6fd7d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd7d-124">-DefaultProfile</span></span>
<span data-ttu-id="6fd7d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd7d-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6fd7d-126">-RecoveryPoint</span></span>
<span data-ttu-id="6fd7d-127">Anger den återställnings punkt där den virtuella datorn ska återställas.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="6fd7d-128">Använd Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet för att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd7d-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="6fd7d-129">-ResolveConflict</span></span>
<span data-ttu-id="6fd7d-130">Om det återställda objektet också finns på mål platsen kan du ange om du vill skriva över eller inte.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd7d-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="6fd7d-131">-SourceFilePath</span></span>
<span data-ttu-id="6fd7d-132">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="6fd7d-133">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="6fd7d-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="6fd7d-134">-SourceFileType</span></span>
<span data-ttu-id="6fd7d-135">Används för ett visst objekt återställning från en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="6fd7d-136">Sökvägen till det objekt som ska återställas inom fil resursen.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd7d-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6fd7d-137">-StorageAccountName</span></span>
<span data-ttu-id="6fd7d-138">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="6fd7d-139">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd7d-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd7d-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="6fd7d-141">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="6fd7d-142">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd7d-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="6fd7d-143">-TargetFileShareName</span></span>
<span data-ttu-id="6fd7d-144">Fil resursen dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="6fd7d-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="6fd7d-145">-TargetFolder</span></span>
<span data-ttu-id="6fd7d-146">Den mapp där fil resursen måste återställas i targetFileShareName. lämna variabeln tom om du vill återställa under rotmappen.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="6fd7d-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd7d-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="6fd7d-148">Den resurs grupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="6fd7d-149">Gäller för säkerhets kopiering av VM med hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="6fd7d-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="6fd7d-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6fd7d-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="6fd7d-151">Det lagrings konto dit fil resursen måste återställas.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="6fd7d-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fd7d-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="6fd7d-153">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="6fd7d-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6fd7d-154">-VaultId</span></span>
<span data-ttu-id="6fd7d-155">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6fd7d-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="6fd7d-156">-VaultLocation</span></span>
<span data-ttu-id="6fd7d-157">Plats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6fd7d-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6fd7d-158">-Confirm</span></span>
<span data-ttu-id="6fd7d-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd7d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd7d-160">-WhatIf</span></span>
<span data-ttu-id="6fd7d-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fd7d-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd7d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd7d-163">CommonParameters</span></span>
<span data-ttu-id="6fd7d-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd7d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd7d-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd7d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd7d-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fd7d-166">INPUTS</span></span>

### <span data-ttu-id="6fd7d-167">System. String</span><span class="sxs-lookup"><span data-stu-id="6fd7d-167">System.String</span></span>
<span data-ttu-id="6fd7d-168">Parametrar: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6fd7d-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="6fd7d-169">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="6fd7d-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="6fd7d-170">Parametrar: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6fd7d-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="6fd7d-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fd7d-171">OUTPUTS</span></span>

### <span data-ttu-id="6fd7d-172">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6fd7d-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6fd7d-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fd7d-173">NOTES</span></span>

## <span data-ttu-id="6fd7d-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fd7d-174">RELATED LINKS</span></span>

[<span data-ttu-id="6fd7d-175">Säkerhets kopiering-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6fd7d-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="6fd7d-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6fd7d-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="6fd7d-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6fd7d-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


